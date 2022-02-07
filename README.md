
## nucleus-zero.com website


The blog is built on a static site generator called [Hugo](https://gohugo.io/) which is written in GoLang. It also uses NPM for various build tasks and so you need Hugo and NPM and installed.

**Step 1 - Setup**
=======
## Clone and Run

`brew install npm hugo`

	git clone https://github.com/nucleus-zero/blog.git
	
	cd blog

	brew install npm

	brew install hugo

	npm install

	npm install -g firebase-tools

At this point you should have everything you need to run and deploy the blog.
=======
`hugo serve`

`hugo -D` regenerates output HTML

## Deploy

`npm install -g firebase-tools`

**Step 2 - Run and Dev Locally**

Hugo runs locally from the CLI and hot loads so you can easily make changes.

	hugo serve
=======
`firebase login`

`hugo && firebase deploy` to deploy

You will now have a fully functioning local version running at http://localhost:1313/

## Customizing theme
Hugo has theme plugins. I built the Nucleus Zero theme by cloning and then customizing the [Mediumish](https://github.com/lgaida/mediumish-gohugo-theme) theme but rather than add it as a git submodule and use the override HTML, I have cloned it and made it part of the project to avoid upstream issues.

The theme files are all in the /themes/nucleus-zero folder. The main folders to be aware of are /layouts which contains all the partials and /assets which contains the CSS. You can add CSS to either medium.css or additional.css (at some point I will merge them).

Some parts of the site are pulled from the main config file config.toml in the projects root directory. There are many options that can be added to this file.

This page on templates covers layout https://gohugo.io/templates/

This page has special instructions about the homepage layout https://gohugo.io/templates/homepage/

## PR to GitHub
Create a branch in Github and submit a PR back to main tagging @curphey in the PR for review.

## deploy
To generate fresh HTML use

	hugo -D

The current setup outputs HTML in the /public folder which is used by Google Firebase for hosting. You do not need to regenerate html when developing locally but should when deploying to production.

To deploy login to your firebase account from the command line.

	firebase login

You can optionally test the deploy locally to ensure any firebase config won't conflict with your hosting setup.

	firebase emulators:start

To deploy

	"hugo && firebase deploy"
