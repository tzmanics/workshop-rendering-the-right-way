# Workshop: Render the Right Way

In order to figure out which way to render works best for the project, we need to know the different approaches. In this workshop we'll walk through multiple ways of rendering content, focusing on two approaches: Server Side Rendering (SSR) or Hybrid with Angular Universal and the Jamstack architecture approach with pre-rendering and serverless functions.

We'll also be shining light on the other surrounding concerns like set up, costs, developer experience, and more. The point of this workshop is not to tell you which approach is the best, but to give you the information to make that decision on your own.

## The Agenda

:00 - :30

- intros
- render refresher: what even is rendering?

:30 - :55

- hybrid rendering benefits & pitfalls
- Angular Universal setup

:55 - 1:00

break time ヽ(´∇´)ノ　(∇´ ノ)　ヽ(　　　)ノ　(ヽ ´∇) ヽ(´∇`)ﾉ

1:00 - 1:30

- building with Angular Universal: developing, pre-rendering, ssr

1:30 - 1:55

- the jamstack approach benefits & pitfalls

1:55 - 2:00

break time ヽ(´∇´)ノ　(∇´ ノ)　ヽ(　　　)ノ　(ヽ ´∇) ヽ(´∇`)ﾉ

2:00 - 2:45

- pre-rendering with a static site generator, [Scully](http://scullyio.com/)
- adding hydration with serverless functions

2:45 - 3:00

- wrap up
- q & a

# Workshop Setup

Now that we know what we're doing here. Let's get setup.

> 🍎 If you can get your setup ready before the workshop it will allow us to really utilize our workshop time for learning time!

## Coding Set Up

You are free to use whatever code editor you prefer. Using [VS Code](https://code.visualstudio.com/download) will allow us to code together if needed, but, again, use the editor that's most comfortable.

- [Link for VS Code Install](https://code.visualstudio.com/download)

### Angular Requirements

It's always best to yse the latest version of Angular (at the writing of this that is v11). If you don't have the Angular CLI installed already when you do install it will give you the latest version. If not, you can check your version by running the `ng --version` command in your command line to see if you need to update.

- To install the Angular CLI run

```bash
npm install -g @angular/cli @angular/core
```

- [Link on updating to v11.](https://t.co/4aX9kL8lnE?amp=1)
- [Link to Mark Techson's post on updating to v11](https://blog.angular.io/version-11-of-angular-now-available-74721b7952f7)

Once you have the Angular CLI installed and up to date, you may want to run the project generation command `ng new` to make sure everything works ok.

### Version Control

I know _you never_ make mistakes BUT just in case, it's always good to commit and commit often. If you don't already have a git account somewhere, may I recommend signing up for GitHub.

- [Link to make a GitHub account.](https://github.com/join)

Once you have a GitHub account you can make your own version of this repo to work on all the examples.

Either [fork](https://docs.github.com/en/github/getting-started-with-github/fork-a-repo) this repo or clone it to a local directory:

```bash
git clone https://github.com/tzmanics/workshop-rendering-the-right-way
```

### Hosting

For this workshop we'll be using [Netlify](https://www.netlify.com/?utm_source=github-repo&utm_medium=angular-workshop_tzm&utm_campaign=devex) to throw our site online. If you don't already have an account you can sign up for a free one. It will then hook up to your git account and allow us to make quick work of our [CI/CD](https://www.netlify.com/products/build/?utm_source=github-repo&utm_medium=angular-workshop_tzm&utm_campaign=devex) setup.

- [Link to setup Netlify account.](https://app.netlify.com/signup?utm_source=github-repo&utm_medium=angular-workshop_tzm&utm_campaign=devex)

> Heads up, I work for Netlify. Even before I did, I always recommended using them because I LOVE their developer experience. Which, in turn, is why I happily work on their developer experience team. Just wanted to be transparent 👍.

We'll also be using [Firebase](https://firebase.google.com/?gclid=Cj0KCQiA48j9BRC-ARIsAMQu3WTH_JCbfErgfs9lixpwLRsQZBtMSuCx_SY680Slhcsck6694CLU1GYaAiTTEALw_wcB). You can click the 'Get started` or 'Sign in' button to create your account.

## Checklist

Here's a little tldr; of what to have before coming to the workshop. Again, this helps us to really get the most out of the workshop.

- [ ] A code editor like VS Code, Sublime, sick vim setup, etc.
- [ ] Latest version of the Angular CLI
- [ ] A git account
- [ ] A Netlify account
- [ ] A Firebase account
- [ ] A good knock-knock joke (just in case)

## Pre-Workshop Resources

So excited and want to jump in immediately? Here are some resources you can checkout to learn more about SSR and the Jamstack architecture.

- [Is SSR Compatible with the Jamstack](https://dev.to/shortdiv/is-ssr-compatible-with-the-jamstack-5959)
- [Angular Universal SSR](https://angular.io/guide/universal)
- [Jamstack.org](https://jamstack.org/)
- [Angular Universal v9: What's New](https://trilon.io/blog/angular-universal-v9-whats-new)
- [Scully](http://scullyio.com/) the Angular Static Site Generator
