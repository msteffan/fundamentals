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

Install Gitbook plugins

```
$ gitbook install
```

Run a local copy at http://localhost:4000 with:

```
$ gitbook serve
```

> If any plugins error, you can install directly from github. For example if quizzes won't still, try the following:

```
npm install git+ssh://git@github.com:GitbookIO/plugin-quizzes.git
```

The project is similar to a Jykell blog. Chapters are written in markdown files and compiled down to HTML inside `_book`

To build the static website use:

```
$ gitbook build
```

> Warning! Inline code blocks ie single back ticks are not properly escaping HTML entities.
> To work around this use `<code>`

```
<code>"This works"</code>
`"This doesn't"`
```

# Making Changes

This project is currently hosted on GitHub and GitLab.
To make changes to the content, fork the GitLab repo and file a pull/merge request.

~~Quizzes are hosted through TypeForm. To make changes to quizzes contact JD?~~

Quizzes and Exercises are written with Gitbook's Quizzes and Exercises Plugins

### Quiz Format

Quizzes are designated with three dashes before and after the quiz.

Use Github flavored checkboxes for possible answers.

Mark the correct answer with an 'x'

Use '>' for solution text.

```
---

This is a question
- [ ] These appear
- [ ] As check boxes
- [x] This will be the correct answer

> This is the solution text

---
```

### Exercise Format

Exercises use special nunchuck tags:

```
{% exercise %}
Question
{% initial %}
// Code appears in repl.
var studentCode;
{% solution %}
// this code will appear in the repl if a student cliks on 'solution'
{% validation %}
assert(studentCode == answer, "Wrong Answer Message");
{% context %}
var answer;
var codeAvailableInContext;
{% endexercise %}
```

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
