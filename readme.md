### Cloud-barista multi-cloud project

is under construction.

### Under the Hood

This site is made with [Jekyll](http://jekyllrb.com), an open source static site generator. This means the Jekyll program takes the content we want to be on the site and turns them into HTML files ready to be hosted somewhere. Awesomely, GitHub provides free web hosting for repositories, called [GitHub Pages](http://pages.github.com/), and that's how this site is hosted. The content for the site is on a branch named [gh-pages](https://github.com/github/government.github.com/tree/gh-pages).

## Contributing

#### Fix/Edit Content

If you see an error or a place where content should be updated or improved, just fork this repository to your account, make the change you'd like and then submit a pull request. If you're not able to make the change, file an [issue](https://github.com/github/government.github.com/issues/new).

#### Add Organization

If you know of an [GitHub organization](https://help.github.com/articles/about-organizations/) that should be added to the organization list that generates the matrix of avatars on the [Community](https://government.github.com/community/) page: fork this repository, open the [_data/civic_hackers.yml](_data/civic_hackers.yml), [_data/governments.yml](_data/governments.yml), or[_data/research.yml](_data/research.yml) file and add it to the appropriate section of the list in the format being used. Commit your change and submit a pull request to us!

---

## To Set up Locally

You can take all the files of this site and run them just on your computer as if it were live online, only it's just on your machine.

#### Requirements

* [Jekyll](http://jekyllrb.com/)
* [Ruby](https://www.ruby-lang.org/en/)
* [Git](http://git-scm.com/)

_If you have installed [GitHub Desktop](https://desktop.github.com), Git was also installed automatically._

To copy the repository's files from here onto your computer and to view and serve those files locally, at your computer's command line type:

```bash
git clone https://github.com/github/government.github.com.git
cd government.github.com
script/bootstrap
script/server
```
Open `http://localhost:4000` in your browser

## Deploying

github.government.com now utilizes a two-repo approach to managing staging and production deployments:

- **Production:** [github/government.github.com](https://github.com/github/government.github.com/) (this repository)
- **Staging:** [government/staging](https://ghe.io/government/staging)

For small changes, you can deploy right to production by merging a pull request. For larger changes, push your branch to the staging repo from Terminal. Here's how to setup staging and deploy to it:

```
$ script/stage staging
```


This script will generate the government site (without starting the local server) and prep it for staging. It does this by creating a temporary Git repo within the compiled `_site` directory and force pushing that to a separate remote repo (in this case, https://ghe.io/government/staging).

Pushing to the staging repo requires authenticating with GitHub via Terminal. You'll be asked for a username and password when running `script/stage`. Use your GHE.io username and, since we enforce 2FA, use a [personal access token](https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/) as your password.

_Having trouble deploying to a staging server? Delete the entire `_site` directory and try again. Sometimes the temporary Git repository we make in the script can go awry._

When you're done with staging and your pull request has been approved, you can merge your branch. Your changes will be automatically deployed to the production site in a few minutes.

----

#### Triage Issues [![Open Source Helpers](https://www.codetriage.com/github/government.github.com/badges/users.svg)](https://www.codetriage.com/github/government.github.com)

In addition to contributing changes, you can help to triage issues. This can include asking for vital information or requesting formatting changes. If you would like to start triaging issues, one easy way to get started is to [subscribe to government.github.com on CodeTriage](https://www.codetriage.com/github/government.github.com).

----

Don't see what you're looking for? Create an [issue](https://github.com/github/government.github.com/issues/new), we'll do our best to help you out.
