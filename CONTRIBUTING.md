Hello! Thank you for choosing to help contribute to the nodejs-http-client project. There are many ways you can contribute and help is always welcome.

We use [Milestones](https://github.com/sendgrid/nodejs-http-client/milestones) to help define current roadmaps, please feel free to grab an issue from the current milestone. Please indicate that you have begun work on it to avoid collisions. Once a PR is made, community review, comments, suggestions and additional PRs are welcomed and encouraged.

* [Feature Request](#feature_request)
* [Submit a Bug Report](#submit_a_bug_report)
* [Improvements to the Codebase](#improvements_to_the_codebase)
* [Understanding the Code Base](#understanding_the_codebase)
* [Testing](#testing)
* [Style Guidelines & Naming Conventions](#style_guidelines_and_naming_conventions)
* [Creating a Pull Request](#creating_a_pull_request)

There are a few ways to contribute, which we'll enumerate below:

<a name="feature_request"></a>
## Feature Request

If you'd like to make a feature request, please read this section.

The GitHub issue tracker is the preferred channel for library feature requests, but please respect the following restrictions:

- Please **search for existing issues** in order to ensure we don't have duplicate bugs/feature requests.
- Please be respectful and considerate of others when commenting on issues

<a name="submit_a_bug_report"></a>
## Submit a Bug Report

Note: DO NOT include your credentials in ANY code examples, descriptions, or media you make public.

A software bug is a demonstrable issue in the code base. In order for us to diagnose the issue and respond as quickly as possible, please add as much detail as possible into your bug report.

Before you decide to create a new issue, please try the following:

1. Check the Github issues tab if the identified issue has already been reported, if so, please add a +1 to the existing post.
2. Update to the latest version of this code and check if issue has already been fixed
3. Copy and fill in the Bug Report Template we have provided below

### Please use our Bug Report Template

In order to make the process easier, we've included a sample bug report template (borrowed from [Ghost](https://github.com/TryGhost/Ghost/)). The template uses [GitHub flavored markdown](https://help.github.com/articles/github-flavored-markdown/) for formatting.

```
Short and descriptive example bug report title

#### Issue Summary

A summary of the issue and the environment in which it occurs. If suitable, include the steps required to reproduce the bug. Please feel free to include screenshots, screencasts, code examples.


#### Steps to Reproduce

1. This is the first step
2. This is the second step
3. Further steps, etc.

Any other information you want to share that is relevant to the issue being reported. Especially, why do you consider this to be a bug? What do you expect to happen instead?

#### Technical details:

* node-http-client Version: master (latest commit: [commit number])
* Node.js Version: 4.1.2
```

<a name="improvements_to_the_codebase"></a>
## Improvements to the Codebase

We welcome direct contributions to the rest code base. Thank you!

### Development Environment ###

#### Install and run locally ####

##### Prerequisites #####

* Node.js 0.8 and up
* Please see [package.json](https://github.com/sendgrid/nodejs-http-client/blob/master/package.json)

##### Initial setup: #####

```
git clone https://github.com/sendgrid/nodejs-http-client.git
cd nodejs-http-client
```

##### Execute: #####

See the [examples folder](https://github.com/sendgrid/nodejs-http-client/tree/master/examples) to get started quickly.

You will need to setup the following environment to use the SendGrid example:

```
echo "export SENDGRID_API_KEY='YOUR_API_KEY'" > sendgrid.env
echo "sendgrid.env" >> .gitignore
source ./sendgrid.env
node examples/example.js
```

<a name="understanding_the_codebase"></a>
## Understanding the Code Base

**/examples**

Working examples that demonstrate usage.

**client.go**

There is a object to hold both the request and response to the API server. 

The main function that does the heavy lifting (and external entry point) is `API`.

<a name="testing"></a>
## Testing

All PRs require passing tests before the PR will be reviewed.

All test files are in `[test/test.js](https://github.com/sendgrid/nodejs-http-client/blob/master/test/test.js)`.

For the purposes of contributing to this repo, please update the [`test.js`](https://github.com/sendgrid/nodejs-http-client/blob/master/test/test.js) file with unit tests as you modify the code.

Run the test:

`mocha`

<a name="style_guidelines_and_naming_conventions"></a>
## Style Guidelines & Naming Conventions

Generally, we follow the style guidelines as suggested by the official language. However, we ask that you conform to the styles that already exist in the library. If you wish to deviate, please explain your reasoning.

* [Unofficial Style Guide](https://github.com/felixge/node-style-guide)

Please run your code through [ESLint](http://eslint.org/) Standard style guide.

### Directory Structure

* `examples` for example calls
* `lib` for the main source code
* `test` for the unit tests

## Creating a Pull Request<a name="creating_a_pull_request"></a>

1. [Fork](https://help.github.com/fork-a-repo/) the project, clone your fork,
   and configure the remotes:

   ```bash
   # Clone your fork of the repo into the current directory
   git clone https://github.com/sendgrid/nodejs-http-client
   # Navigate to the newly cloned directory
   cd nodejs-http-client
   # Assign the original repo to a remote called "upstream"
   git remote add upstream https://github.com/sendgrid/nodejs-http-client
   ```

2. If you cloned a while ago, get the latest changes from upstream:

   ```bash
   git checkout <dev-branch>
   git pull upstream <dev-branch>
   ```

3. Create a new topic branch (off the main project development branch) to
   contain your feature, change, or fix:

   ```bash
   git checkout -b <topic-branch-name>
   ```

4. Commit your changes in logical chunks. Please adhere to these [git commit
   message guidelines](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
   or your code is unlikely be merged into the main project. Use Git's
   [interactive rebase](https://help.github.com/articles/interactive-rebase)
   feature to tidy up your commits before making them public.

4a. Create tests.

4b. Create or update the example code that demonstrates the functionality of this change to the code.

5. Locally merge (or rebase) the upstream development branch into your topic branch:

   ```bash
   git pull [--rebase] upstream master
   ```

6. Push your topic branch up to your fork:

   ```bash
   git push origin <topic-branch-name>
   ```

7. [Open a Pull Request](https://help.github.com/articles/using-pull-requests/)
    with a clear title and description against the `master` branch. All tests must be passing before we will review the PR.

If you have any additional questions, please feel free to [email](mailto:dx@sendgrid.com) us or create an issue in this repo.