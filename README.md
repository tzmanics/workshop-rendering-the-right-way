# Workshop: Render the Right Way

In order to figure out which way to render works best for the project, we need to know the different approaches. In this workshop we'll walk through multiple ways of rendering content.  

# Workshop Setup

Now that we know what we're doing here. Let's get setup. 

> 🍎 If you can get your setup ready before the workshop it will allow us to really utilize our workshop time for learning time!

## Coding Set Up

You are free to use whatever code editor you prefer. Using [VS Code](https://code.visualstudio.com/download) will allow us to code together if needed, but, again, use the editor that's most comfortable.

- [Link for VS Code Install](https://code.visualstudio.com/download)

### Angular Requirements

A few things to create our example will work best with the Angular v9 CLI. If you don't have the Angular CLI installed already when you do install it will give you the latest version. If not, you can check your version by running the `ng --version` command in your command line to see if you need to update.

- To install the Angular CLI run

```bash
npm install -g @angular/cli
```

- [Link on updating to v9.](https://update.angular.io/)

Once you have the Angular CLI installed and up to date, you may want to run the project generation command `ng new` to make sure everything works ok.

### Version Control

I know _you never_ make mistakes BUT just in case, it's always good to commit and commit often. If you don't already have a git account somewhere, may I recommend signing up for GitHub.

- [Link to make a GitHub account.](https://github.com/join)


Either [fork](https://docs.github.com/en/github/getting-started-with-github/fork-a-repo) this repo or clone it to a local directory:

```bash
git clone https://github.com/tzmanics/workshop-rendering-the-right-way
```

### Hosting

For this workshop we'll be using [Netlify](https://www.netlify.com/?utm_source=github-repo&utm_medium=angular-workshop_tzm&utm_campaign=devex) to throw our site online. If you don't already have an account you can sign up for a free one. It will then hook up to your git account and allow us to make quick work of our [CI/CD](https://www.netlify.com/products/build/?utm_source=github-repo&utm_medium=angular-workshop_tzm&utm_campaign=devex) setup.

- [Link to setup Netlify account.](https://app.netlify.com/signup?utm_source=github-repo&utm_medium=angular-workshop_tzm&utm_campaign=devex)

> Heads up, I work for Netlify. Even before I did, I always recommended using them because I LOVE their developer experience. Which, in turn, is why I happily work on their developer experience team. Just wanted to be transparent 👍.

## Checklist

Here's a little tldr; of what to have before coming to the workshop. Again, this helps us to really get the most out of the workshop.

- [ ] A code editor like VS Code, Sublime, sick vim setup, etc.
- [ ] Angular CLI v9
- [ ] A git account
- [ ] A Netlify account
- [ ] A good knock-knock joke (just in case)

## Pre-Workshop Resources

So excited and want to jump in immediately? Here are some resources you can checkout to learn more about SSR and the Jamstack architecture.

- [Is SSR Compatible with the Jamstack](https://dev.to/shortdiv/is-ssr-compatible-with-the-jamstack-5959)