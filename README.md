# Foster Commerce Pull Request Templates

Starter pull request templates we use for internal projects. Feel free to fork and adapt.

## Why?

Merging changes through pull requests helps us with accountability, documentation, and code reviews. But it's hard to remember everything that goes into a PR, and to remember the steps to take when deploying to staging or production. 

See
- GitHub: [Creating a pull request template for your repository](https://help.github.com/en/github/building-a-strong-community/creating-a-pull-request-template-for-your-repository)
- Paige Niedringhaus/Medium: [Github Templates: The Smarter Way to Formalize Pull Requests Among Development Teams](https://medium.com/better-programming/github-templates-the-smarter-way-to-formalize-pull-requests-among-development-teams-89f8d6a204f)

## How to use

We currently use two templates:

1. The base PR template will always show up. It includes a link to the deploy template, a place to document what the PR does, a place for extra notes, and a checklist for merging into staging.
2. The deploy PR template is accessed through a custom link (see below). It includes a place to note all the previous PRs it includes, as well as a checklist for deploying to production.

### Add to your project

[Per GitHub](https://help.github.com/en/github/building-a-strong-community/creating-a-pull-request-template-for-your-repository#adding-a-pull-request-template), you can put your templates in a hidden `.github` directory, or in a `docs` directory. You could just download and copy over the `.github` directory from this repo.

### Customize deploy link for your repo

The base PR template

The deploy repository link automatically:

- creates a pull request to merge your staging branch into your production branch
- Titles it `DEPLOY YYYY-MM-DD` (you still have to replace the date)
- Labels it `DEPLOY`


Replace the variables in this URL (it's using JS syntax, so get rid of the concatenation symbols too) and then add it to your base PR template.

```js
'https://github.com/' + UserName + '/' + repoName + '/compare/' + prodBranch + '...' + stagingBranch + '?title=DEPLOY+YYYY-MM-DD&labels=DEPLOY&template=deploy.md'
```

### Customize the rest

You may also want to change some of the checklist steps, or ask for different information. Go to town!

### ACTIVATE 🤖

Commit and merge the files into your default branch, whatever it is. Try making a PR and see what happens!
