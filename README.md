Travis-CI Documentation Scripts
===============================

This repository contains common files and scripts for verification and deployment of OSG documentation using GitHub Pages. This repository is intended to be used as a submodule of your documentation repository.

Getting started
---------------

1. From the directory containing your documentation repository

        $ git submodule add https://github.com/opensciencegrid/doc-ci-scripts ci

1. Check the newly created `ci` directory for contents. If it's empty, run the following to pull down the latest commit from this repository:

        $ git submodule update --init --recursive

1. From the root directory of your documentation repository, copy the template to your travis configuration:

        cp ci/travis.template.yml .travis.yml

    Merging in any local customizations from your existing `.travis.yml` file.

1. Fill in the template as appropriate for your repository.

For an example `.travis.yml`, see the [docs repository](https://github.com/opensciencegrid/docs/blob/master/.travis.yml).

Updating your submodule
-----------------------

You must explicitly update this submodule in your documentation repository if there are updates to this repository, i.e. `git pull` doesn't automatically pull in updates for this repository. To perform an update, run the following command:

```
git submodule update --init --recursive
```

