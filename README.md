# 🏔 Alaska | Static-site Boilerplate

[![Open Source](https://badgen.net/badge/icon/Open%20Source?icon=github&label&color=black)](https://github.com/pixelsbyeryc/alaska)
[![License: CC0-1.0](https://badgen.net/badge/License%20/CC0/black?icon=false)](http://creativecommons.org/publicdomain/zero/1.0/)
[![Buy me coffee](https://badgen.net/badge/icon/Tip%20me%20in%20ETH?icon=buymeacoffee&label&color=yellow)](https://etherscan.io/address/0x750889c704857f766420b14723Ecb8320EB8E9ab)

:zap: **Fastest way to build HTML and CSS static sites.**

You don't have to learn complicated tools to build simple websites in a modular way.

Alaska uses efficient technology that's similar to what you're used to.

| Technology | Description |
| :--- | :--- |
| [**PugJS**](https://pugjs.org/) | Templating tool for building HTML in a beautiful and modular way. <br> It's basically HTML, but modular, programmable, and without closing tags. |
| [**Sass**](https://sass-lang.com/) | CSS processor that extends the capabilities of current CSS. |
| [**GulpJS**](https://gulpjs.com/) | File processor to watch your files as you edit, reload the page on save, and build minified files. |

## Contents

1. [Running Alaska](#running-alaska)
    1. [Requirements](#requirements)
    2. [Installing](#installing)
    3. [Commands](#commands)
2. [Build in Alaska](#build-in-alaska)
    1. [Structure](#structure)
    2. [Gulpfile](#gulpfile)
3. [License](#license) _(Read carefully)_

## Running Alaska

Running Alaska is quite simple. You just install all the `npm` dependencies and you're good to go. 

But if you need some in-depth guidance, I'll hand it off to Poh, a friendly Polar Bear that will guide you on your journey to building in Alaska.

> 🐻‍❄️ <br>**LET'S GO!!!**

Chill, Poh. They want instructions, not hype.

> 🐻‍❄️ <br>Shut up. YOU! Let's go...

### Requirements

> 🐻‍❄️ <br>If you want to do any running in Alaska, you have to prepare. 
> <br>And I'm not talking about warm clothes and water. 
> <br>I'm taking about N-P-M ᵐᵒᵗʰᵉʳᶠᵘᶜᵏᵉʳ`
>
> **Here's what you need to have installed on your machine:**

* [NodeJS](https://nodejs.org/en/download/) - Click to install.
* [NPM Cli](https://github.com/npm/cli) - Click to learn how to install if Node didn't already install it.
* [Yarn](https://classic.yarnpkg.com/en/docs/install) _(Optional)_ - Run: `npm i -g yarn` to install.
* [Gulp Cli](https://gulpjs.com/docs/en/getting-started/quick-start) - Run `npm i -g gulp-cli` to install.

> 🐻‍❄️ <br>Now we need to pull all the files from Github.
> <br>Go to your Projects folder `cd ~/projects/` or whatever you use.
> <br>Then clone the project like this:

```
git clone git@github.com:pixelsbyeryc/alaska.git
```
_If you have SSH_

```
git clone https://github.com/pixelsbyeryc/alaska.git
```
_In case you're cloning from HTTPS_

### Installing

> 🐻‍❄️ <br>Now what you have the code on your computer, 
> <br>we're going to install the dependencies.
> <br>It's as simple as:

```
yarn
```
_If you like using yarn instead of npm, or..._

```
npm i
```
_If you prefer the bland outputs of npm. Your choice._

### Commands

> 🐻‍❄️ <br>There are two commands you can run:

```
yarn dev
```
_Will watch the files for any changes and hotreload your browser._

```
yarn build
```
_Will build your project under the folder_ `/public`

> 🐻‍❄️ <br>Want to stop the terminal from running?
> <br>Press Control+C on your terminal. It'll stop the execution.

## Build in Alaska

> 🐻‍❄️ <br>To build in Alaska, you need to understand how the structure works.
> <br>We like to break our ~~food~~, I mean, code in small portions, you feel me?
> 
> Lemme give you the ins-and-outs of this place...

### Structure

> 🐻‍❄️ <br>Here's your folder/file structure:

```
alaska
|   .gitignore
|   gulpfile
|   LICENSE    
│   package.json
│   README.md
|   yarn.lock
│
└───src
│   └───js
│   |   │   magic.js
│   |   └   ...
|   |   
│   └───sass
│   │   |   sassy.sass
│   │   └   ...
|   |   
│   └───views
|       └───_data
│       |   |   data.pug
│       |   └   ...
│       |   
|       └───_includes
│       |   |   head.pug
│       |   └   ...
│       |   
|       └───components
│       |   |   header.pug
│       |   |   footer.pug
│       |   └   ...
│       |   
|       └───layouts
│       |   |   base.pug
│       |   └   ...
│       |   
|       └───pages
│           |   index.pug
│           └   ...
│   
└───public
    └   ...
```

#### Source Files `src`

> 🐻‍❄️ <br>Source files are the ones you'll be editing.
> 
> Once will you run `yarn dev` or `yarn build`, Gulp will automatically process your files and spill them into the `public` folder.

#### Public Files `public`

> 🐻‍❄️ <br>Public files are ready for deployment.
>
> They will have pretty and minified options for your JS and CSS files.
> <br>You can also set up in your [Gulpfile.js](#gulpfile) to minify your HTMLs for a slimmer code.

#### Views `src/views`

> 🐻‍❄️ <br>Views folder will encompass all your Pug files — your HTML.
>
> Let's go over them:

* **Pages** `src/views/pages`: This is where your single pages will live (eg: Home Page). You can add as many pages as you want. All of the `.pug` files here will be sent to the `public` folder.
* **Layouts** `src/views/layouts`: Layouts are used to set up the basic structure of a page. You can re-use layouts on as many pages as you want.
* **Components** `src/views/components`: Components help you to split up your code and make it more maintainable. You can also create components as [Pug Mixins](https://pugjs.org/language/mixins.html) and pass data to them.
* **Includes** `src/views/_includes`: Includes are chucks of code, much like components: they help you split up your HTML and make it more maintainable. I usually use them for things like `<head> ... </head>`.
* **Data** `src/views/_data`: You can write JSON-like files with Pug and use them to iterate components so you don't have to write the same structure over and over and over again.

#### Styles `src/sass`
> 🐻‍❄️ <br>Sass folder will encompass all your Sass files — your CSS.
>
> For now, we only have our `sassy.sass` — which is the main file.
> <br>But we encourage you to create more files and organize them as you wish.
>
> **Note:** Currently, Gulp only moves `sassy.sass` as `sassy.css` to the `public` folder. If you want to add another file to `public`, modify your [Gulpfile](#gulpfile).

#### Scripts `src/js`
> 🐻‍❄️ <br>Scripts folder will encompass all your JS.
>
> For now, we only have one file called `magic.js`.
> <br>You can create as many files as you want.
>
> **Note:** Currently, Gulp only moves `magic.js` to the `public` folder. If you want to add another js file to `public`, modify your [Gulpfile](#gulpfile).

### Gulpfile

## License

:stuck_out_tongue_closed_eyes: License to do whatever ~ᵗʰᵉ ᶠᵘᶜᵏ~ you want. **Go nuts.**

[![forthebadge cc-0](http://ForTheBadge.com/images/badges/cc-0.svg)](http://ForTheBadge.com)
