## drat Package for R package management

This is a test repo to learn the functionality of drat for managing packages.

### Setting up a repo

To set up a drat repo you need to first make a local git repo in a folder called `drat` with this folder structure `src/contrib`.

drat repos work by using github pages therefore you need to estabilish a git hub page for this repo by creating a branch called `gh-pages` and pushing to your git hub. This will then create the domain `https://<your-git-username>.github.io/drat`.

In R you need to add this drat repo using the following syntax:
`library(drat)`
`drat::addRepo("mynewdratrepo","https://<your-git-username>.github.io/drat" )`

To add packages into this repo you first need to insert the tar file into the `drat/src/contrib` folder using the following:
`drat::insertRepo("my_package_0.1.tar.gz", "<path-to-my-local-drat>/drat")`

Once this is pushed to your gh-pages you are ready to use the package repo. Packages can be installed from this repo in R like this:
`install.packages("mypacakge",repos="https://<your-git-username>.github.io/drat")`

