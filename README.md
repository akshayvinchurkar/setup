# Front End Web Developer Setup

I'm Tania, a self-taught web developer who has been working professionally in the field since June, 2015. I also have a [blog of web development tutorials and articles](https://www.taniarascia.com/) I work on in my spare time. I'm going to write about the setup, programs, and plugins I use on a daily basis with some brief descriptions and alternate options. This is not meant to be an extensive list. This is my list.

## Contents

* [Operating System](#operating-system)
* [Browser](#browser)
* [Text Editor / IDE](#text-editor--ide)
* [Stack](#stack)
* [Hosting / Cloud Computing](#hosting--cloud-computing)
* [Version Control](#version-control)
* [Content Management System (CMS)](#content-management-system-cms)
* [JS Task Runner](#js-task-runner)
* [CSS Preprocessor](#css-preprocessor)
* [CSS Framework](#css-framework)
* [Content Delivery Network (CDN)](#content-delivery-network-cdn)
* [Miscellaneous](#miscellaneous)

## Operating System

The software a computer runs on.

### [macOS (Apple)](http://www.apple.com/macos/sierra/)

I used Windows exclusively from 1994 to 2015. Now I work on a Mac, currently running the Sierra macOS.

### Configuration

* Hide desktop icons: `defaults write com.apple.finder CreateDesktop false`
* Show hidden files: `defaults write com.apple.finder AppleShowAllFiles YES`
* Show path bar in finder: `defaults write com.apple.finder ShowPathbar -bool true`

#### Install XCode

1. Download [XCode](Xcode)

#### Install Command Line Tools

1. `xcode-select --install`

#### Install Homebrew

1. `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
1. `brew update`

#### Install Node.js

1. `brew install node`

#### Install Git

1. `brew install git`
1. `git config --global user.name "Firstname Lastname"`
1. `git config --global user.email username@email.com`

#### Install Gulp

1. `npm install --global gulp-cli`

#### Additional Programs

1. [Spectacle](https://www.spectacleapp.com/)
1. [Sip](http://sipapp.io/)

> **Other Options:** [Windows](https://www.microsoft.com/en-us/windows), [Linux](https://en.wikipedia.org/wiki/Linux)

## Browser

The program used for navigating the internet.

### [Google Chrome](https://www.google.com/chrome/)

> **Other Options:**  [Firefox](https://www.mozilla.org/en-US/firefox/products/), [Opera](http://www.opera.com/), [Safari](http://www.apple.com/safari/) (Mac only), [Edge](https://www.microsoft.com/en-us/windows/microsoft-edge/microsoft-edge) (Windows only)

## Hosting / Cloud Computing

The service that allows a website to be viewed on the internet.

### [NearlyFreeSpeech](https://www.nearlyfreespeech.net/)

> **Other Options:** [Amazon Web Services (AWS)](https://aws.amazon.com/), [Digital Ocean](https://www.digitalocean.com/), [MediaTemple](https://www.mediatemple.net/), [Rackspace](https://www.rackspace.com/)

## Stack

The platform used for web development.

### [Linux Apache MySQL PHP (LAMP)](https://en.wikipedia.org/wiki/LAMP_(software_bundle))

## Text Editor / IDE

The program used to write code and edit text files.

### [Brackets](http://brackets.io/)

#### Install Extensions

All extensions are installed by going to `File > Extension Manager`.

1. [New Moon Color Theme](https://github.com/taniarascia/new-moon)
1. [Emmet](https://github.com/emmetio/brackets-emmet)
1. [Beautify](https://github.com/brackets-beautify/brackets-beautify)
1. [Custom Working Tabs](https://github.com/DH3ALEJANDRO/custom-work-for-brackets)
1. [Indent Guides](https://github.com/lkcampbell/brackets-indent-guides)
1. [Color Highlighter](https://github.com/Taraflex/Brackets-Color-Highlighter)

> **Other Options:** [Sublime Text](https://www.sublimetext.com/), [Atom](https://atom.io/), [Visual Studio Code](http://code.visualstudio.com/)

## Version Control

The Git repository hosting service used for keeping track of revisions and collaboration.

### [GitHub](https://github.com/)

> **Other Options:** [BitBucket](https://bitbucket.org), [GitLab](https://about.gitlab.com/), [AWS CodeCommit](https://aws.amazon.com/codecommit/)

## Content Management System (CMS)

The software used to create and manage a website through an admin dashboard.

### [WordPress](https://wordpress.org/)

> **Other Options:** [Jekyll](https://jekyllrb.com)

## JS Task Runner

Automation for common repetitive tasks.

### [Gulp](http://gulpjs.com/)

> **Other Options:** [Grunt](http://gruntjs.com/), [Brunch](http://brunch.io/)

## CSS Preprocessor

Extend the features of CSS and compile it back into CSS.

### [Sass](http://sass-lang.com/)

> **Other Options:** [LESS](http://lesscss.org/), [Stylus](http://stylus-lang.com/)

## CSS Framework

A base stylesheet used as a starting point for designing a website.

### [Primitive](https://taniarascia.github.io/primitive/)

> **Other Options:** [Bootstrap](http://getbootstrap.com/), [Foundation](http://foundation.zurb.com/)

## Encryption (TLS/SSL)

Increase the security of data transmitted through the internet.

### [ComodoSSL](https://comodosslstore.com/)

> **Other Options:** [Let's Encrypt](https://letsencrypt.org/)

## Content Delivery Network (CDN)

Geographically dispersed servers that cache website content.

### [Cloudflare](https://www.cloudflare.com/)

> **Other Options:** [MaxCDN](https://www.maxcdn.com/), [AWS CloudFront](https://aws.amazon.com/cloudfront/)

## Analytics

Track and report website traffic.

### [Google Analytics](https://analytics.google.com/)

## Miscellaneous

* [Evernote](https://evernote.com/)
* [Slack](https://slack.com/)


