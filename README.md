# WinnipegAWS.ca

This repo is/was a repo cloned from the Academic Kickstart theme below. In this repo, we use a `git worktree` directory on the `public/` directory which has the `gh-pages` branch checked out. Changes are generated and published to the `public/` directory and then committed in that branch, and finally the generated html/css/js is pushed up to github. See the `commit-gh-pages-files.sh` for details.

Installation:

```
brew install hugo
git submodule update --init --recursive
git worktree add -B gh-pages public upstream/gh-pages

# Check it out locally
hugo server

# Generate files into public/ directory
hugo

# commit files in public/ directory and publish on winnipegaws.ca
./commit-gh-pages-files.sh
./push-gh-pages-files.sh
```
