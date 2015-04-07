# How to contribute

Fork this project.  See "Getting Started" for the GitBook build process.

https://docs.google.com/a/generalassemb.ly/spreadsheets/d/184bho-gmTAQVfg5Zv3ERXcmjDjaNWW8V2iHIwusnYIo/edit#gid=1118564563

# Getting Started

Fundamentals is a GitBook.

How to use Gitbook:

GitBook can be installed from NPM using:

```
$ npm install gitbook-cli -g
```

Create the directories and files for a book from its SUMMARY.md file (if existing) using

```
$ gitbook init
```

You can serve a repository as a book using:

```
$ gitbook serve
```

Or simply build the static website using:

```
$ gitbook build
```

Install necessary plugins for development

```
$ gitbook install
```

# Making Changes

This project is currently hosted on GitHub and GitLab.
To make changes to the content, fork the GitLab repo and file a pull request.

Quizzes are hosted through TypeForm. To make changes to quizzes contact JD?

# Deployment

The subtree `_book` is deployed to Github on the `gh-pages` branch.
Currently any changes or issues should be filed as pull requests against GitLab/Development.

Deployment scheme compiled from these sources
- https://gist.github.com/cobyism/4730490
- http://stevenclontz.com/blog/2014/05/08/git-subtree-push-for-deployment/

```
# replace build_folder as appropriate
git subtree push --prefix _book origin gh-pages
```

One caveat here. Since git subtree push doesn’t have a --force option, you will have trouble on the first push if you have an existing gh-pages branch. You can actually chain git commands together to fix this, thankfully.

```
git push origin `git subtree split --prefix _book master`:gh-pages --force
```


# Roadmap

- [ ] a gap analysis on projects and exercises

- [ ] clarify homework instructions

- [ ] reevaluate scaffolded assignments

- [ ] what changes do we need to make to exercises to connect competencies to those homework assignments?

- [ ] clarify and simplify the Git steps in each homework

- [ ] connect exercises to competencies in homework assignments

- [ ] add solutions to the exercises

# Additional Resources

- [Gitbook](https://github.com/GitbookIO/gitbook)
- [AirBnB Style Guide](https://github.com/airbnb/javascript)
