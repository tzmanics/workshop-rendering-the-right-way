# Angular Universal Setup

The next step we'll take is to incorporate [Angular Universal](https://angular.io/guide/universal) into our project.

## Adding Angular Universal

First we'll use the `ng add` command to bring in the server-side app module.

`ng add @nguniversal/express-engine`

Here is what's changes (this is from the Angular documentation):

![the new file structure](https://res.cloudinary.com/dzkoxrsdj/image/upload/v1605531076/Screen_Shot_2020-11-16_at_7.51.03_AM_qq7bxx.jpg)

Once we have that all added, we can run

`npm run dev:ssr`

and head to [http://localhost:4200/](http://localhost:4200/) to see itup and running locally.

Eventhough it's running on a local server, we'll find everything should look and act the same as when we ran `ng serve`. This is because `routerLink` events are supported since they use native anchor tags (`<a>`). Eventually, we'll add other user events that will have to wait for the full client app to work.

The Angular docs also give a few handy tips for trying out how your app will acutally render in the real world:

> 1. Open the Chrome Dev Tools and go to the Network tab.
> 2. Find the Network Throttling dropdown on the far right of the menu bar.
> 3. Try one of the "3G" speeds.
