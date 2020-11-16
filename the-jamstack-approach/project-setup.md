# The Jamstack Approach - Project Setup

## Make the demo yours!

The project we'll be using for this workshop lives at [https://github.com/tzmanics/workshop-rendering-the-right-way](https://github.com/tzmanics/workshop-rendering-the-right-way). There are a few ways to grab this project, here are two:

1. Push the 'Use this template' ԅ(´ڡ\`ԅ) button at the top of the repo page. Then clone it locally with `git clone`.

![screenshot of the button](https://res.cloudinary.com/dzkoxrsdj/image/upload/v1605530823/Screen_Shot_2020-11-16_at_7.45.01_AM_ew2fhe.jpg)

2. Locally run `git clone https://github.com/tzmanics/rtrw-demo`, then create a new repo in your git account and push it on up there.

You'll also want to change the remote origin to your new repo with these two commands:

- `git remote rm origin`
- `git remote add origin <your repo address>`

Once you have the project in its new home. Run these two commands from theh base directory to get it up and running locally:

- `npm install`
- `ng serve`

This base project is a bit of an empty skeleton that we will fill with each new stop of the workshop.
