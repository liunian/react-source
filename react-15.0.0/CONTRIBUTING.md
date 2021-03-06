# Contributing to React

React is one of Facebook's first open source projects that is both under very active development and is also being used to ship code to everybody on [facebook.com](https://www.facebook.com). We're still working out the kinks to make contributing to this project as easy and transparent as possible, but we're not quite there yet. Hopefully this document makes the process for contributing clear and answers some questions that you may have.

## [Code of Conduct](https://code.facebook.com/codeofconduct)

Facebook has adopted a Code of Conduct that we expect project participants to adhere to. Please read [the full text](https://code.facebook.com/codeofconduct) so that you can understand what actions will and will not be tolerated.

## Our Development Process

Some of the core team will be working directly on GitHub. These changes will be public from the beginning. Other changesets will come via a bridge with Facebook's internal source control. This is a necessity as it allows engineers at Facebook outside of the core team to move fast and contribute from an environment they are comfortable in.

### `master` is unsafe

We will do our best to keep `master` in good shape, with tests passing at all times. But in order to move fast, we will make API changes that your application might not be compatible with. We will do our best to communicate these changes and always version appropriately so you can lock into a specific version if need be.

### Test Suite

Use `grunt test` to run the full test suite with PhantomJS.

This command is just a facade to [Jest](https://facebook.github.io/jest/). You may optionally run `npm install -g jest-cli` and use Jest commands directly to have more control over how tests are executed.

For example, `jest --watch` lets you automatically run the test suite on every file change.

You can also run a subset of tests by passing a prefix to `jest`. For instance, `jest ReactDOMSVG` will only run tests in the files that start with `ReactDOMSVG`, such as `ReactDOMSVG-test.js`.

When you know which tests you want to run, you can achieve a fast feedback loop by using these two features together. For example, `jest ReactDOMSVG --watch` will re-run only the matching tests on every change.

Just make sure to run the whole test suite before submitting a pull request!

### Pull Requests

**Working on your first Pull Request?** You can learn how from this *free* series [How to Contribute to an Open Source Project on GitHub](https://egghead.io/series/how-to-contribute-to-an-open-source-project-on-github)

The core team will be monitoring for pull requests. When we get one, we'll run some Facebook-specific integration tests on it first. From here, we'll need to get another person to sign off on the changes and then merge the pull request. For API changes we may need to fix internal uses, which could cause some delay. We'll do our best to provide updates and feedback throughout the process.

*Before* submitting a pull request, please make sure the following is done???

1. Fork the repo and create your branch from `master`.
2. If you've added code that should be tested, add tests!
3. If you've changed APIs, update the documentation.
4. Ensure the test suite passes (`grunt test`).
5. Make sure your code lints (`grunt lint`) - we've done our best to make sure these rules match our internal linting guidelines.
6. If you haven't already, complete the CLA.

### Contributor License Agreement (CLA)

In order to accept your pull request, we need you to submit a CLA. You only need to do this once, so if you've done this for another Facebook open source project, you're good to go. If you are submitting a pull request for the first time, just let us know that you have completed the CLA and we can cross-check with your GitHub username.

[Complete your CLA here.](https://code.facebook.com/cla)

## Bugs

### Where to Find Known Issues

We will be using GitHub Issues for our public bugs. We will keep a close eye on this and try to make it clear when we have an internal fix in progress. Before filing a new task, try to make sure your problem doesn't already exist.

### Reporting New Issues

The best way to get your bug fixed is to provide a reduced test case. jsFiddle, jsBin, and other sites provide a way to give live examples. Those are especially helpful though may not work for `JSX`-based code.

### Security Bugs

Facebook has a [bounty program](https://www.facebook.com/whitehat/) for the safe disclosure of security bugs. With that in mind, please do not file public issues; go through the process outlined on that page.

## How to Get in Touch

* IRC - [#reactjs on freenode](https://webchat.freenode.net/?channels=reactjs)
* Discussion forum - [discuss.reactjs.org](https://discuss.reactjs.org/)

## Meeting Notes

React team meets once a week to discuss the development of React, future plans, and priorities.  
You can find the meeting notes in a [dedicated repository](https://github.com/reactjs/core-notes/).

## Style Guide

Our linter will catch most styling issues that may exist in your code.
You can check the status of your code styling by simply running: `grunt lint`

However, there are still some styles that the linter cannot pick up. If you are unsure about something, looking at [Airbnb's Style Guide](https://github.com/airbnb/javascript) will guide you in the right direction.

### Code Conventions

* Use semicolons `;`
* Commas last `,`
* 2 spaces for indentation (no tabs)
* Prefer `'` over `"`
* `'use strict';`
* 80 character line length
* Write "attractive" code
* Do not use the optional parameters of `setTimeout` and `setInterval`

### Documentation

* Do not wrap lines at 80 characters

## License

By contributing to React, you agree that your contributions will be licensed under its BSD license.
