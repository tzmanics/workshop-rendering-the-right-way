# Setup Hosting

We're going to host the universally rendered version of our Angular app on Firebase using functions.

## Installing Firebase Tools

We can work from the command line using Firebase tools by first installing them.

`npm install firebase-tools -g`

You may also need to login by running

`firebase login`

## Creating a Project & Setup Functions

### Firebase & Google Cloud Setup

To make a new project we'll run

`firebase init`

It will first have us choose what we want to setup. For this project, we want Hosting and Functiions.

![firebase setup menu](https://res.cloudinary.com/dzkoxrsdj/image/upload/v1605535470/Screen_Shot_2020-11-16_at_8.28.04_AM_rzbigj.jpg)

Then to set up the project we will choose to create a new project and name it (you will need a Google Cloud Platform since we're using functions). Once everything is made we'll get our project information and link to the Firebase project console.

![firebase project setup output](https://res.cloudinary.com/dzkoxrsdj/image/upload/v1605535633/Screen_Shot_2020-11-16_at_8.55.00_AM_becs8v.jpg)

> 🚨 If you see this error `FirebaseError: Callers must accept Terms of Service`, as I did, you just need to head to your [Google Cloud dashboard](https://console.cloud.google.com/home/) and hit 'Create project' in order to accept the Terms of Service.

Next, we'll setup our Cloud Functions. I chose to write mine in JS but feel free to choose TypeScript (I choose this to have as many similarites between rendering options just for this workshop). Then we can say 'No' for now to enforce ESLint and we will want to install dependencies now.

![firebase functions setup](https://res.cloudinary.com/dzkoxrsdj/image/upload/v1605537030/Screen_Shot_2020-11-16_at_8.55.15_AM_swj2na.jpg)

Finally, they will ask about the hosting setup. We want will

- choose the defualt `public` directory
- say no to the single-page app rewrite
- say yes to automatic builds and deploys (this is optional. i, personally, like things done for me 😛)

![firebase hosting setup](https://res.cloudinary.com/dzkoxrsdj/image/upload/v1605537103/Screen_Shot_2020-11-16_at_8.55.34_AM_yyx2lx.jpg)
