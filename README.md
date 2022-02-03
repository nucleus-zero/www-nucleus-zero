
# nucleus-zero website

This blog is built on [Hugo](https://gohugo.io/), a static site generator written in Go and using NPM for many operations. You can run it locally on your MacBook and deploy it to [Google firebase](https://firebase.google.com/).

## pre-requistites

You need golang, NPM, firebase tools and hugo installed locally to develop and deploy. The easiest way is to use [homebrew](https://brew.sh/) on your Mac to install and manage it all.

Install homebrew

    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

brew install npm
brew install hugo

clone this repo
hugo serve

hugo -D regenerates output HTML

## deploy

npm install -g firebase-tools

login to your firebase account

firebase login

"hugo && firebase deploy" to deploy


## Customizing theme

touch to build
