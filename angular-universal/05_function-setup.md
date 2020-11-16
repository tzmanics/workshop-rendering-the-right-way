# Function Setup

To get our SSR app running we'll need to setup some functions.

Now that we have firebase set up we'll want to update `firbase.json`

```json
{
  "hosting": {
    "public": "dist/<your-project-name>/browser",
    // ...
    "rewrites": [
      {
        "source": "**",
        "function": "ssr"
      }
    ]
  }
}
```

Next, we want to copy our the built app into the functions environment. First, we'll install `fs-extra` in the functions directory.

```bash
cd functions
npm install fs-extra
```

Once we have that, we can create a file in the functions directory to make that copy. Let's call it `functions/cp-angular.js`.

```js
const fs = require("fs-extra");

(async () => {
  const src = "../dist";
  const copy = "./dist";

  await fs.remove(copy);
  await fs.copy(src, copy);
})();
```

With this, we'll want to update the functions build script in `functions/package.json`

```json
  "scripts": {
    "build": "node cp-angular"
  }
```

Then we need to copy the project into the functions environment because the function just needs that universal app in the working directory. In `functions/index.js` (or `.ts` if you chose to write in TypeScript).

```js
const functions = require("firebase-functions");
const universal = require(`${process.cwd()}/dist/rtrw-demo/server/main`).app();

exports.ssr = functions.https.onRequest(universal);
```

Finally, we'll make some new build commands in `src/package.json`

```json
"build:functions": "npm run --prefix functions build"
"build:all": "npm run build:ssr && npm run build:functions"
```

Now we can run our build scripts then deploy to firebase.

```bash
npm run build:all
firebase deploy
```

> Big thanks to [Pritam Banerjee's aritcle on deployment!](https://bapittu.medium.com/angular-9-universal-ssr-with-firebase-and-deployment-in-cloud-function-54867020a656)!!
