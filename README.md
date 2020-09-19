This is the website for the Buddhist Study Association of Indiana University Bloomington. 

If you are the administrator of BSA, and want to be able to update the website, read the following instructions. I am assuming you are using a Mac. 

Table of Contents
=================
* [Create an account on GitHub](#create-an-account-on-github)
* [Configure git](#configure-git)
* [Download Hugo](#download-hugo)
* [Clone the project](#clone-the-project)
* [Install nvm, npm, Node.js](#install-nvm-npm-nodejs)
* [Install postcss-cli, and autoprefixer](#install-postcss-cli-and-autoprefixer)
* [Make changes to the website content](#make-changes-to-the-website-content)
    * [Add new posts in updates](#add-new-posts-in-updates)
    * [Download Sublime Text](#download-sublime-text)
    * [Add a new album](#add-a-new-album)
    * [Add a new posts section](#add-a-new-posts-section)
    * [Add a new single page](#add-a-new-single-page)
* [Publish](#publish)
* [Terminal](#terminal)


## Create an account on GitHub
First of all, create an account on Github (https://github.com/join). After this is done, send me an email and let me know your GitHub username. My email address can be found on [my homepage](https://hongtaoh.com/).

## Configure git
`git` should come pre-installed on Mac. 

Now open your Terminal. If you don't know how to open Terminal: On the right-top corner, you can see a search icon, i.e., Spotlight Search. Click it and input "Terminal" and then press the `Enter` key. 

Don't close your Terminal throughout the instruction. 

In your Terminal, type `git --version` and press the `Enter` key. You should be able to see your git version. If not, you need to download git [here](https://git-scm.com/downloads) first. 

After making sure that git is installed, you need to set up git with your user name and email. 

In your Terminal, copy and paste the following two lines of code and then press the enter key:

```bash
git config --global user.name "Your username here" 
git config --global user.email "your_email@example.com"
```
The username and email does not have to be the same as your GitHub ones, although it will be simpler if you use the same. 

## Download Hugo

You can find instructions [here](https://hongtaoh.com/en/2020/01/29/how-to-install-and-upgrade-hugo-on-mac/).

After you have moved `hugo` to `usr/local/bin`, type `hugo version` in your Terminal (and press the Enter key) to verify that you have successfully downloaded Hugo.

If you see:

```bash
Hugo Static Site Generator v0.70.0-7F47B99E darwin/amd64 BuildDate: 2020-05-06T11:16:48Z
```
in your Terminal, that means your installation is successful. 

Every time you input things in Terminal, you need to press the `Enter` key after the **last** line of code. If you copy and past multiple lines of code, it's better if you press the `Enter` key after the first few lines have been execuated. If you don't want to wait, you can press it as soon as you have pasted the codes. 

I won't remind you of pressing the Enter key later. 

AFTER you have emailed me and successfully installed Hugo, you can do the following. 

## Clone the project

Go back to your Terminal, and input the following:

```bash
cd Desktop 
git clone https://github.com/hongtaoh/bsa
cd BSA
```

Now, you should see a folder named `bsa` on your Desktop. 

## Install nvm, npm, Node.js

All the codes you see should be copied and pasted into your Terminal. I won't repeat remind of inputing things in your Terminal later. 

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.2/install.sh | bash
nvm install stable
```

## Install `postcss-cli`, and `autoprefixer`

```bash
sudo npm i -g postcss-cli
```

You might be asked to input your passwords. When you do, the passwords you are inputing will be insivible. Don't worry and just go ahead. After your input is done, press the `Enter` key. 

Then:

```bash
sudo npm i -g autoprefixer 
```

You will be asked to input your passwords again. Repeat the process. 

## Make changes to the website content

Now, close your Terminal, and open it anew.

Every time you want add changes to the website, you first need to tell Terminal where the website folder is located. We have just downloaded the folder into your Desktop, so you need to do this:

```bash
cd Desktop/bsa
```

Don't close your Terminal from now. 

### Add new posts in `updates`

I recommend you to include the dates in the name of the new post. For example, if you want to add a post named `2020-10-02-a-new-activity.md`, you can add it this way:

```bash
hugo new updates/2020-10-02-a-new-activity.md
```

Now, go to `bsa - content - updates`, you'll be able to see the new post:

```md
---
title: "2020 10 02 a New Activity"
date: 2020-09-19T07:15:00-04:00
showDate: true
draft: false
---
```

You can edit the `title` as needed. That title will be the title shown on the website. 

The post content will be written in `[markdown](https://en.wikipedia.org/wiki/Markdown)`. You can add [headers](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#headers), [images](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#images), [hyperlinks](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#links), [quotes](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#blockquotes), *italics*, **bold font**, [ordered or unordered lists](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#links), [codes](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#code), [tables](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#tables) and [horizontal rules](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#hr) within the markdown file. 

Refer to this [markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

You can also embed YouTube videos:

```md
{{< youtube id="w7Ft2ymGmfc" autoplay="true" >}}
```

(The above line of code is not for Terminal)

Every YouTube Video ends with `watch?v=....`. Just copy what's after `v=` and paste them into the `id=`.  

or Vimeo videos:

```md
{{< vimeo 146022717 >}}
```

(The above line of code is not for Termainl)

You can view the results [here](https://hugo-tutorial.hongtaoh.com/2020/06/05/what-you-can-do-with-hugo-and-markdown/).

### Download Sublime Text

When you open `.md` files, Mac will open them with TextEdit by default. However, if will be much easier to edit markdown files with professional text editor. I recommend downloading Sublime Text [here](https://www.sublimetext.com/). It's free. 

### Add a new album
If you want to add a new album named YourAlbumNmae (You are free to use whatevery name you want):

```bash
hugo new YourAlbumName/_index.md
```

Within `bsa - content`, you'll find a new folder named `YourAlbumNmae` and a file named `_index.md`. Open `_index.md`, delete all the content, copey and past the following:

```md
---
title: "YourAlbumName"
type: "gallery"
url: "/YourAlbumName"
maxWidth: "600x"
clickablePhotos: true
---
```

(The above lines of code are not for Termainl)

Please notice that for `url`, if you have multiple words, like `Your Album Name`, you need to either put them together: `YourAlbumName` or put hyphens in between: `Your-Album-Name`. 

You can see examples of this in `yoga` and `retreat` album. 

Then, within the `bsa` folder, open `config.toml`. At the end of these

```toml
[[params.mainMenu]]
    link = "about"
    text = "About BSA"

[[params.mainMenu]]
    link = "retreat"
    text = "Retreat Gallery"

[[params.mainMenu]]
    link = "yoga"
    text = "Yoga Gallery"

[[params.mainMenu]]
    link = "updates"
    text = "Updates"
```

(The above lines of code is not for Termainl)

Add a new entry:

```toml
[[params.mainMenu]]
    link = "YourAlbumName" 
    text = "YourAlbumName"
```

(The above lines of code are not for Termainl)

### Add a new posts section

If you want to add a new posts section just like `updates` where you can post more than one articles, do the following. 

```bash
hugo new YourPostSectionName/_index.md
```

Within `bsa - content`, you'll find a new folder named `YourPostSectionName` and a file named `_index.md`. Open `_index.md`, delete all the content, copey and past the following:

```md
---
title: "YourPostSectionName"
---

If you want to say something before the list of posts, you can see it here. 
```
(The above lines of code are not for Termainl)

Then, within the `bsa` folder, open `config.toml`, add a new entry:

```toml
[[params.mainMenu]]
    link = "YourPostSectionName" # Use the lower case
    text = "YourPostSectionName"
```
(The above lines of code are not for Termainl)

### Add a new single page

If you want to add a single page like [About BSA](https://iubsa.netlify.app/about/), you can do the following. 

```bash
hugo new YourSinglePageName.md
```

Then, edit the title as needed and put your content below the `---`. Look at the `bas- content - about.md` for reference. 

Then, within the `bsa` folder, open `config.toml`, add a new entry:

```toml
[[params.mainMenu]]
    link = "YourSinglePageName" # Use the lower case
    text = "YourSinglePageName"
```
(The above lines of code are not for Termainl)

Don't close your Terminal. 

## Publish 
Every time you finish making changes to the website, do the following:

```bash
bash deploy.sh
```

The website will update itself. 

## Terminal
Everytime when you are making changes to the `bsa` folder, you must make sure that you don't close your Terminal. If you happen to have closed it by accident, don't worry. Open it anew and type

```bash
cd Desktop/bsa
```