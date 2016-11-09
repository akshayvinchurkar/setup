# Front End Web Developer Setup

*11/9/2016*

I'm Tania, a self-taught web developer who has been working professionally in the field since June, 2015. I also have a [blog of web development tutorials and articles](https://www.taniarascia.com/) I work on in my spare time. I'm going to write about the setup, programs, and plugins I use on a daily basis with some brief descriptions and alternate options. This is not meant to be an extensive list; this is my list.

## Contents

- [Operating System](#operating-system)
- [Browser](#browser)
- [Text Editor / IDE](#text-editor--ide)
- [Stack](#stack)
- [Hosting / Cloud Computing](#hosting--cloud-computing)
- [Version Control](#version-control)
- [Content Management System (CMS)](#content-management-system-cms)
- [JS Task Runner](#js-task-runner)
- [CSS Preprocessor](#css-preprocessor)
- [CSS Framework](#css-framework)
- [Content Delivery Network (CDN)](#content-delivery-network-cdn)
- [Miscellaneous](#miscellaneous)

## Operating System

> The software a computer runs on.

### **I use:** [macOS (Apple)](http://www.apple.com/macos/sierra/)
**Other Options:** [Windows](https://www.microsoft.com/en-us/windows), [Linux](https://en.wikipedia.org/wiki/Linux)

I used Windows exclusively from 1994 to 2015. Now I work on a Mac, currently running Sierra. One of the biggest game changers for my web development journey was learning how to use the command line, which is done through the Terminal application in macOS. 

### Configuration

- Allow app installation: `Security and Privacy -> General -> Allow apps from identified developers`
- Hide desktop icons: `defaults write com.apple.finder CreateDesktop false`
- Show hidden files: `defaults write com.apple.finder AppleShowAllFiles YES`
- Show path bar in finder: `defaults write com.apple.finder ShowPathbar -bool true`

### Installations

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

#### Install Vim

1. `git clone https://github.com/vim/vim.git`
1. `cd vim/src`
1. `make`

### Dotfiles

#### SSH

`~/.ssh/config`

```
Host example
 HostName example.com
 User example-user
 IdentityFile key.pem
```

#### Git

`~/.gitconfig`

```
[alias]
	c = commit -am
	s = status
	a = add
	pom = push origin master
	pog = push origin gh-pages
	cob = checkout -b
 ```
 
### Additional Programs

- [Spectacle](https://www.spectacleapp.com/) - simplified window resizing.
- [Sip](http://sipapp.io/) - collect the code for any color on your screen.
- [GistBox](http://www.gistboxapp.com/) - organize code snippets.

## Browser

> The program used for navigating the internet.

### **I use:** [Google Chrome](https://www.google.com/chrome/)
**Other Options:**  [Firefox](https://www.mozilla.org/en-US/firefox/products/), [Opera](http://www.opera.com/), [Safari](http://www.apple.com/safari/) (Mac only), [Edge](https://www.microsoft.com/en-us/windows/microsoft-edge/microsoft-edge) (Windows only)

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

## Stack

> The software bundle used for web development.

### **I use:**  [Linux Apache MySQL PHP (LAMP)](https://en.wikipedia.org/wiki/LAMP_(software_bundle))
**Other Options:** [Mean](http://mean.io/), 

## Text Editor / IDE

> The program used to write code and edit text files.

### **I use:** [Brackets](http://brackets.io/)
**Other Options:** [Sublime Text](https://www.sublimetext.com/), [Atom](https://atom.io/), [Visual Studio Code](http://code.visualstudio.com/)

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

## Version Control

> The Git repository hosting service used for keeping track of revisions and collaboration.

### **I use:** [GitHub](https://github.com/)
**Other Options:** [BitBucket](https://bitbucket.org), [GitLab](https://about.gitlab.com/), [AWS CodeCommit](https://aws.amazon.com/codecommit/)

## Content Management System (CMS)

> The software used to create and manage a website through an admin dashboard.

### **I use:** [WordPress](https://wordpress.org/)
**Other Options:** [Jekyll](https://jekyllrb.com)

## JS Task Runner

> Command line automation for common repetitive tasks.

### **I use:** [Gulp](http://gulpjs.com/)
**Other Options:** [Grunt](http://gruntjs.com/), [Brunch](http://brunch.io/)

## CSS Preprocessor

> Extend the features of CSS and compile it back into CSS.

### **I use:** [Sass](http://sass-lang.com/)
**Other Options:** [LESS](http://lesscss.org/), [Stylus](http://stylus-lang.com/)

## CSS Framework

> A base stylesheet used as a starting point for designing a website.

### **I use:** [Primitive](https://taniarascia.github.io/primitive/)
**Other Options:** [Bootstrap](http://getbootstrap.com/), [Foundation](http://foundation.zurb.com/)

## Encryption (TLS/SSL)

> Protocal that increases the security of data transmitted through the internet.

### **I use:** [ComodoSSL](https://comodosslstore.com/)
**Other Options:** [Let's Encrypt](https://letsencrypt.org/)

## Content Delivery Network (CDN)

> Deliver cached website content to geographically dispersed servers.

### **I use:** [Cloudflare](https://www.cloudflare.com/)
**Other Options:** [MaxCDN](https://www.maxcdn.com/), [AWS CloudFront](https://aws.amazon.com/cloudfront/)

## Analytics

> Track and report website traffic.

### **I use:** [Google Analytics](https://analytics.google.com/)

## Miscellaneous

- [Evernote](https://evernote.com/)
- [Slack](https://slack.com/)

### Things I Don't Know About Yet

- Vagrant
- VirtualBox
- Docker
- Composer
- JavaScript frameworks (React, Angular, Vue)
- Programming languages besides PHP and JS
- A lot of other stuff
