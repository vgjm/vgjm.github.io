---
title: "How to Setup GitHub Pages with HUGO"
date: 2022-04-23T15:11:47+08:00
---

I setup this website with GitHub Pages today. Just want to share my fresh experience with the friends on the internet.

Requirement:
- Create a [Github](https://github.com/) account
- Install [Git](https://git-scm.com/)

## What is GitHub Pages?

---

[GitHub Pages](https://pages.github.com/) is a free service provided by GitHub. You can use it to deploy a simple *static* website. *Static* basically means it can not be super sophisticated. Since what I need is just a place to record my thoughts and share with other people, it's useful enough.

To use GitHub Pages, simply create a repository named *username*.github.io, where username is your username on GitHub. Then put some contents in that repository. GitHub will deploy it automatically.

I assume you have a little bit knowledge about git, which is a version control system. But in case you don't have any idea about how to use git, just read this [Git Tutorial](https://www.w3schools.com/git/git_intro.asp?remote=github). It's really worth it.

## HUGO framework

---

After you have created the repository for GitHub Pages. The next task is writing some contents for it. Traditionally, this requires knowledges about [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) and [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS). HTML helps us to organize your contents and CSS defines the layout and style of your webpages. You have to spend a lot of time if you want to learn these two languages. Fortunately, there is a tool that simplifies this task greatly. That is [HUGO](https://gohugo.io/).

HUGO allows you to use some pre-defined templates. What you should do is to choose a [theme](https://themes.gohugo.io/) and toggle the configuration. So you can just focus on the text content. With the help of HUGO, you just write your blog post in a language named [Markdown](https://en.wikipedia.org/wiki/Markdown). HUGO will translate it into HTML. Markdown is very easy to learn. I believe every one can learn the basics of Markdown in several hours.

## Install HUGO

---

To install HUGO, you need choose the best way according to the operating system and architecture of your computer.

You can use `uname -sm` to check your machine's OS an architecture.

```shell
$ uname -sm
Linux x86_64
```

### Homebrew (macOS)

If you are on macOS and using Homebrew, you can install Hugo with the following one-liner:

```
brew install hugo
```

### Homebrew (Linux)

If you are using Homebrew on Linux, you can install Hugo with the following one-liner:

```
brew install hugo
```

### Binary (Cross-platform)

If your machine's OS is Linux but you don't use homebrew (Please do not install it through apt. The version is usually outdated.) or you are using Windows:

Download the appropriate version for your platform from Hugo [Releases](https://github.com/gohugoio/hugo/releases). Once downloaded, the binary can be run from anywhere. You don’t need to install it into a global location. This works well for shared hosts and other systems where you don’t have a privileged account.

Ideally, you should install it somewhere in your PATH for easy use. /usr/local/bin is the most probable location.

## HUGO Quick Start

---

HUGO has a official [Quick Start](https://gohugo.io/getting-started/quick-start/), which is very helpful. You can learn the usage of it by reading that. I have some supplements on it.

### Don't use submodule

The Quick Start use git submodule to add a theme in [Add a theme](https://gohugo.io/getting-started/quick-start/#step-3-add-a-theme) section. But git submodule is a little tricky to use, especially for beginners. I recommend download the release of the theme you want to use. 

For example, I use [PaperMod](https://github.com/adityatelange/hugo-PaperMod) as my blog's theme. So I can download it from it's [Release Page](https://github.com/adityatelange/hugo-PaperMod/releases). Then just extract it into the themes/PaperMod sub-directory of your HUGO website project, which is created with this command:

```
hugo new site quickstart
```

### How to insert pictures?

Firstly, create a directory with the name `static`:

```
cd quickstart
mkdir static
```

All of the static resources of your website should be in this directory. I will create another directory for all image type resources:

```
mkdir static/img
```

Then just paste your images into this directory, and you can use it in your blog post, the syntax is:

```
![alt](/img/pic.jpg)
```

Where *alt* is the text to display when the picture itself is failed to be load.

Try to play with it!
