# Front End Web Developer Setup

*11/10/2016*

I'm Tania, a self-taught web developer who has been working professionally in the field since June, 2015. I also have a [blog of web development tutorials and articles](https://www.taniarascia.com/) I work on in my spare time. I'm going to write about the setup, programs, and plugins I use on a daily basis with some brief descriptions and alternate options. 

### Disclaimer

It doesn't matter what you use: Mac or Windows. Vim or Emacs. Tabs or spaces. PHP or Python. If all the options didn't have merit, there wouldn't be an argument. This list is not meant to be an endorsement for or against anything, just one person's web development workflow. Learn. Be open minded. Try new things. Research. Discover what works best for you. This is not an extensive list; this is my list.

## Contents

- [Operating System](#operating-system)
- [Browser](#browser)
- [Text Editor / IDE](#text-editor--ide)
- [Stack](#stack)
- [Hosting / Cloud Computing](#hosting--cloud-computing)
- [Version Control Hosting](#version-control-hosting)
- [Content Management System (CMS)](#content-management-system-cms)
- [JS Task Runner](#js-task-runner)
- [CSS Preprocessor](#css-preprocessor)
- [CSS Framework](#css-framework)
- [Content Delivery Network (CDN)](#content-delivery-network-cdn)
- [Analytics](#analytics)
- [Performance and Search Engine Optimization (SEO)](#performance-and-search-engine-optimization-seo)
- [Miscellaneous](#miscellaneous)

## Operating System

> The software a computer runs on.

### **I use:** [macOS (Apple)](http://www.apple.com/macos/sierra/)
**Other Options:** [Windows](https://www.microsoft.com/en-us/windows), [Linux](https://en.wikipedia.org/wiki/Linux)

I used Windows exclusively from 1994 to 2015. Now I work on a Mac, currently running Sierra. One of the biggest game changers for my web development journey was learning how to use the command line, which is done through the Terminal application in macOS. 

### Configuration

- Allow app installation: `Security and Privacy -> General -> Allow apps from identified developers`
- Hide desktop icons

```shell
defaults write com.apple.finder CreateDesktop false
```

- Show hidden files

```shell
defaults write com.apple.finder AppleShowAllFiles YES
```

- Show path bar in finder

```shell
defaults write com.apple.finder ShowPathbar -bool true
```

### Installations

#### Install XCode

XCode is a suite of development tools and libraries from Apple. 

1. Download [XCode](https://developer.apple.com/xcode/)

#### Install Command Line Tools

An additional package that other programs will depend on.

```shell
xcode-select --install
```

#### Install Homebrew

[Homebrew](http://brew.sh/) is a package manager for macOS that makes it easy to install software.

```shell
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew update
```

#### Install Git

[Git](https://git-scm.com/) is a version control system for software development and collaboration.

```shell
brew install git
git config --global user.name "Tania Rascia"
git config --global user.email taniarascia@gmail.com
```

#### Install Node.js

[Node.js](https://nodejs.org/en/) is used to run server-side JavaScript.

```shell
brew install node
```

#### Install Gulp

[Gulp](http://gulpjs.com/) is a JavaScript task runner.

```shell
npm install --global gulp-cli
```

#### Install Vim

[Vim](http://www.vim.org/) is a text editor that runs in the terminal.

```shell
git clone https://github.com/vim/vim.git
cd vim/src
make
```

### Dotfiles

Extra configuration files.

#### SSH

Location: `~/.ssh/config`

```shell
Host example
    HostName example.com
    User example-user
    IdentityFile key.pem
```

Command: `ssh example` will output `ssh -i key.pem example-user@example.com`.

#### Git

Location: `~/.gitconfig`

```shell
[alias]
	c = commit -am
	s = status
	a = add
	pom = push origin master
	pog = push origin gh-pages
	cob = checkout -b
 ```
 
 Command: `git pom` will output `git push origin master`.
 
### Additional Programs

- [Spectacle](https://www.spectacleapp.com/) - simplified window resizing.
- [Sip](http://sipapp.io/) - collect the code for any color on your screen.
- [GistBox](http://www.gistboxapp.com/) - organize code snippets.

## Browser

> The program used for navigating the internet.

### **I use:** [Google Chrome](https://www.google.com/chrome/)
**Other Options:**  [Firefox](https://www.mozilla.org/en-US/firefox/products/), [Opera](http://www.opera.com/), [Safari](http://www.apple.com/safari/) (Mac only), [Edge](https://www.microsoft.com/en-us/windows/microsoft-edge/microsoft-edge) (Windows only)

As a front end web developer, you should have all the browsers downloaded for testing. If you're in an Apple environment, you can download virtual machines or generate screenshots of Edge at the [Microsoft Developer Tools](https://developer.microsoft.com/en-us/microsoft-edge/tools/) website.

### Extensions

- [AdBlock Plus](https://chrome.google.com/webstore/detail/adblock-plus/cfhdojbkjhnklbpkdaibdccddilifddb?hl=en-US) - block ads.
- [JSON View](https://chrome.google.com/webstore/detail/jsonview/chklaanhfefbnpoihckbnefhakgolnmc) - format JSON files.
- [Sight](https://chrome.google.com/webstore/detail/sight/epmaefhielclhlnmjofcdapbeepkmggh) - add syntax highlighting to files.
- [Stylish](https://chrome.google.com/webstore/detail/stylish/fjnbnpbmkenffdnngjfgmeleoegfcffe?hl=en) - add stylesheets to websites.
- [Awesome Screenshot Capture](https://chrome.google.com/webstore/detail/awesome-screenshot-screen/nlipoenfbbikpbjkfpfillcgkoblgpmj) - take screenshots of websites.
- [Empty New Tab Page](https://chrome.google.com/webstore/detail/empty-new-tab-page-black/fllomkdgoahjlgcblpldnpjcilipjelp) - clean new tab page.

## Hosting / Cloud Computing

> A service that allows a website to be viewed on the internet.

### **I use:** [NearlyFreeSpeech](https://www.nearlyfreespeech.net/)
**Other Options:** [Amazon Web Services (AWS)](https://aws.amazon.com/), [Digital Ocean](https://www.digitalocean.com/), [MediaTemple](https://www.mediatemple.net/), [Rackspace](https://www.rackspace.com/)

You have a choice between managed hosting, or setting up your own Virtual Private Server (VPS) in the cloud through services like Digital Ocean and AWS. The tradeoff is security and simplicity with managed hosting vs. having complete control and being able to keep prices down with a VPS. 

I have some experience with both, and NearlyFreeSpeech has been a great middle ground for me. It's inexpensive, allows me more control than traditional shared hosting, and I don't have to worry about server security and upkeep. I might change my mind in the future, but for now, it works for me.

## Stack

> The software bundle used for web development.

### **I use:**  [Linux Apache MySQL PHP (LAMP)](https://en.wikipedia.org/wiki/LAMP_(software_bundle))
**Other Options:** [MEAN](http://mean.io/)

A stack describes the platform used for web development. The server my website runs on and the professional websites I've made have been on the LAMP stack, which has been a stable and popular choice for many years. The LAMP stack is a generalized name, as you can easily change out Linux for Windows, Apache for NGINX, MySQL for MariaDB, PHP for Python, and so on. Every layer in LAMP is free and open source.

For local development, I use [MAMP](https://www.mamp.info/en/) instead of installing everything manually. MAMP is easy to set up and leaves my default system settings alone, creating sandbox environment. This is preferable for me, but might not be for others. 

- **Operating System:** Linux (many distributions available)
- **Web Server:** [Apache](https://www.apache.org/)
- **Database:** [MySQL](https://www.mysql.com/)
- **Language:** [PHP](http://php.net/)

## Text Editor / IDE

> The program used to write code and edit text files.

### **I use:** [Brackets](http://brackets.io/)
**Other Options:** [Sublime Text](https://www.sublimetext.com/), [Atom](https://atom.io/), [Visual Studio Code](http://code.visualstudio.com/)

Brackets is not the most popular choice for text editors, but after downloading and playing around with a few different ones, it remains my favorite. VSC and Atom have a delay with syntax highlighting that bothers me too much. I like to refrain from relying on a text editor for doing things like minification, prefixing, and compiling Sass, so I feel comfortable switching it up. I don't currently use an Integrated Development Environment (IDE). 

### Extensions

All extensions are installed by going to `File > Extension Manager`.

- [New Moon Color Theme](https://github.com/taniarascia/new-moon) - my color theme.
- [Emmet](https://github.com/emmetio/brackets-emmet) - simplify writing HTML.
- [Beautify](https://github.com/brackets-beautify/brackets-beautify) - formatting and indentation for files.
- [Custom Working Tabs](https://github.com/DH3ALEJANDRO/custom-work-for-brackets) - add tabs.
- [Indent Guides](https://github.com/lkcampbell/brackets-indent-guides) - add indent guides.
- [Color Highlighter](https://github.com/Taraflex/Brackets-Color-Highlighter) - show colors.

### Configuration

```js
{
    "styleActiveLine": true,
    "themes.theme": "new-moon",
    "brackets-indent-guides.enabled": true,
    "useTabChar": true,
    "spaceUnits": 2,
    "tabSize": 2,
    "closeTags": {
        "whenOpening": false,
        "whenClosing": true,
        "indentTags": []
    },
    "fonts.fontSize": "14.5px",
    "fonts.fontFamily": "'Menlo', monospace"
 }
 ```

## Version Control Hosting

> The Git repository hosting service used for keeping track of revisions and collaboration.

### **I use:** [GitHub](https://github.com/)
**Other Options:** [BitBucket](https://bitbucket.org), [GitLab](https://about.gitlab.com/), [AWS CodeCommit](https://aws.amazon.com/codecommit/)

GitHub is easily the most well-known place to host public and private Git repositories. Depending on what you want to do with private repositories, other options might be better or cheaper. GitHub doubles as a web development portfolio and resume and industry-specific social media.

## Content Management System (CMS)

> The software used to create and manage a website through an admin dashboard.

### **I use:** [WordPress](https://wordpress.org/)
**Other Options:** [Jekyll](https://jekyllrb.com)

Currently, I use the WordPress CMS both for professional projects and my personal website. The alternative option is using a Static Site Generator like Jekyll and countless others, which have many advantages like speed and increased security. WordPress is extremely popular and extendable, and it works for me at the moment. I also like to play around with and learn other systems, so I might update or change my personal site in the future.

### Plugins

- [Akismet](https://akismet.com/) - protect against comment spam.
- [Intuitive Custom Post Order](https://wordpress.org/plugins/intuitive-custom-post-order/) - easily drag and drop to reposition post and pages.
- [Move Login](https://wordpress.org/plugins/sf-move-login/) - disable the `/wp-admin` and `wp-login.php` URLs and replace them with your own, custom URL.
- [WP Performance Score Booster](https://wordpress.org/plugins/wp-performance-score-booster/) - most simple and effective speed and caching plugin I've used.
- [Google XML Sitemaps](https://wordpress.org/plugins/google-sitemap-generator/) - generate a sitemap.
- [WP Smush](https://wordpress.org/plugins/wp-smushit/) - image compression.

## JS Task Runner

> Command line automation for common repetitive tasks.

### **I use:** [Gulp](http://gulpjs.com/)
**Other Options:** [Grunt](http://gruntjs.com/), [Brunch](http://brunch.io/)

Task runners like Gulp are useful for watching changes to files and performing tasks like compiling, minifying, autoprefixing, linting, and more. I use Gulp to automatically watch for changes in my `/src` Sass directory, and output the minified, prefixed, compiled CSS, along with Sourcemaps. I don't currently use Gulp for automatically refreshing the browser with the new content, or JavaScript, as I don't work with very advanced JavaScript at the moment.

### Plugins

- [Sass](https://www.npmjs.com/package/gulp-sass)
- [Sourcemaps](https://www.npmjs.com/package/gulp-sourcemaps)
- [CSS Nano](https://www.npmjs.com/package/gulp-cssnano)
- [Autoprefixer](https://github.com/postcss/autoprefixer)

## Bower 
> Package Manager for Web.

### [bower](https://bower.io/)
**Other Options:** [npm](https://www.npmjs.com/)

Bower is simple easy to use package Manager for Web Its almost same as npm but its simple. if you clone any repository from github and it has bower.json file in it then
you have to install those dependencies. installing bower is simple task open up your terminal and type.

```js
npm install -g bower
```

and ex. if you want to install bootstrap for your project then type

```js
bower install bootstrap
```

this will install boostrap and jquery into bower_components folder in your project.

## Scaffolding Tool

> Start Your New Project with ease

### [Yeoman](http://yeoman.io/)

Yeoman is Scaffolding tool what is this mean? ok if you starting a new project if you follow the latest trends then you have to configure all those tools in this setup right? yeoman make your life simple it has premade project templates that generate your plain basic template just like if you want to develope your wordpress theme you used userscore theme. basically it pakage your whole app and give you simple starting point install it like this

```
npm install -g yeoman

```

## CSS Preprocessor

> Extend the features of CSS and compile it back into CSS.

### **I use:** [Sass](http://sass-lang.com/)
**Other Options:** [LESS](http://lesscss.org/), [Stylus](http://stylus-lang.com/)

A preprocessor is a program that takes a bit of code and compiles it into a different bit of code. In the case of CSS preprocessors, we’re compiling the Sass language into regular old CSS that the browser can interpret. I like having the ability to define variables, nest, create loops, and organize my project into multiple files, all of which and more I can do with Sass, specifically the `.scss` extension. I started with LESS, but as Sass grew in popularity, I switched over and now prefer it.

## CSS Framework

> A base stylesheet used as a starting point for designing a website.

### **I use:** [Primitive](https://taniarascia.github.io/primitive/)
**Other Options:** [Bootstrap](http://getbootstrap.com/), [Foundation](http://foundation.zurb.com/)

The first responsive designs I made were with Bootstrap, because I didn't yet understand the underlying concepts of grids, media queries, viewports, and so on. When I realized I didn't feel comfortable making a website without a framework, I sought to teach myself how to make a grid, navigation, and other UI elements from scratch. I started building all my websites that way, but when I realized I was re-writing a lot of the same code, I compiled it all into my own framework. Now I understand how my entire system works, only use exactly what I need, and I save a lot of time, with the added bonus of working on my documentation skills by making a page for it. 

This has been my choice because I have the freedom to do so, but I also feel comfortable jumping into any framework if necessary.

## Encryption (TLS/SSL)

> Protocal that increases the security of data transmitted through the internet.

### **I use:** [ComodoSSL](https://comodosslstore.com/)
**Other Options:** [Let's Encrypt](https://letsencrypt.org/)

Encrypted websites are becoming the standard, and there's no reason not to encrypt your site's traffic with a TLS certificate. I got a $10/year certificate through ComodoSSL, which was before I learned about Let's Encrypt, a free option. Either way, transmitted content through my website is more secure, and my site is more trustworthy.

- Generate Certificate Request

```shell
openssl req -new -newkey rsa:2048 -nodes -keyout example.com.key -out example.com.csr
```

- Extra WordPress Configuration

```php
$_SERVER['HTTPS'] = 'on';
define('FORCE_SSL_ADMIN', true);
```

```apacheconf
RewriteEngine On
RewriteCond %{HTTP:X-Forwarded-Proto} !https
RewriteRule ^ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]
```

### Testing

- [SSL Server Test](https://www.ssllabs.com/ssltest/)

## Content Delivery Network (CDN)

> Deliver cached website content to geographically dispersed servers.

### **I use:** [Cloudflare](https://www.cloudflare.com/)
**Other Options:** [MaxCDN](https://www.maxcdn.com/), [AWS CloudFront](https://aws.amazon.com/cloudfront/)

I pay for hosting based on bandwidth usage. Utilizing a CDN was as easy as pointing my name servers to Cloudflare's, and my bandwidth usage immediately dropped by at least 60%. My site got a speed and performance boost, I pay less for bandwidth, and it was fast and free to implement.

## Performance and Search Engine Optimization (SEO)

> Improve speed, performance, and search rankings.

I regularly run my site through multiple speed and performance tests to see how good I'm doing and what I can improve. Much of what I've listed above contributes to my positive scores and high search rankings.

- Use a [CDN](https://www.cloudflare.com/) to improve speed and performance.
- Use [SSL/TLS](https://letsencrypt.org/) to improve security.
- [Performance Score Booster](https://wordpress.org/plugins/wp-performance-score-booster/) for WordPress enables GZIP compression, browser caching, and file minification.
- Use [structured data](https://developers.google.com/search/docs/guides/intro-structured-data) to help Google understand your content.
- Add a [sitemap](https://wordpress.org/plugins/google-sitemap-generator/).
- [Compress images](https://wordpress.org/plugins/wp-smushit/)

### Steps to Improve Google Search Ranking

1. Make good content. 

### Testing

- [Google PageSpeed](https://developers.google.com/speed/pagespeed/insights/) - 91/100
- [GT Metrix](https://gtmetrix.com/)
- [SEO Site Checkup](http://seositecheckup.com/) - 89/100
- [Pingdom Website Speed Test](https://tools.pingdom.com/)
- [YSlow](http://yslow.org/)
- [Webpage Test](http://www.webpagetest.org/) - A/A/A/A/A Yes

### Analytics

Track and report website traffic.

- [Google Analytics](https://analytics.google.com/)
- [Google Search Console](https://www.google.com/webmasters)

## Miscellaneous

A few other programs I use on a regular basis.

- [Evernote](https://evernote.com/) - for note taking, synced accross multiple devices (well, 2).
- [Slack](https://slack.com/) - for communication between teams.
- [Adobe](http://www.adobe.com/) - I use Photoshop and Illustrator for design.

### Things I Don't Know About Yet

- Vagrant
- VirtualBox (Virtualbox is Hypervisor in simple words you can run any operating system in Virtualbox)
- Docker
- Composer (composer is a dependencie manager it manage yor php project dependencies)
- JavaScript frameworks (React, Angular, Vue)
- Programming languages besides PHP
- A lot of other stuff
