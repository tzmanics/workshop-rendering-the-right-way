# Pre-rendering with Angular Universal

This is a very small section because we just need one command to pre-render our angular application.

`npm run prerender`

This will guess your static routes using guess-parser, build by [Minko Gechev](https://twitter.com/mgechev) and pre-render them into static files. Instead of just guessing you can also add known routes to be pre-rendered by linking a list of routes in `angular.json` and passing it to the `prerender` script.

[Sam Vloeberghs](https://samvloeberghs.be/) has a script in [his blog post on the v9 Universal release](https://samvloeberghs.be/posts/angular-v9-universal-ssr-and-prerendering-out-of-the-box/) that shows you how to do just that:

> ```js
> const fs = require("fs");
> const axios = require("axios");
> const endOfLine = require("os").EOL;
> const newsDataPath = "http://localhost:4200/assets/news.json";
> const routesFile = "./routes.txt";
> axios
>   .get(newsDataPath)
>   .then((res) => {
>     const routes = [];
>     res.data.forEach((newsitem) => {
>       routes.push("news/" + newsitem.id);
>     });
>     fs.writeFileSync(routesFile, routes.join(endOfLine), "utf8");
>   })
>   .catch((e) => console.log(e));
> ```
>
> The scripts in our package.json now look like this:
>
> ```json
>   "scripts": {
>     "..", "..",
>     "list-routes": "node ./scripts/list-routes.js",
>     "prerender": "npm run list-routes && ng run ng-v9-universal:prerender --routesFile routes.txt"
>   },
> ```

For us today, let's just run `npm run prerender` and see what shows up in `dist/browser`.
