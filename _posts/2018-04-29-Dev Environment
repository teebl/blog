---
layout: post
title: Setting up my Development Environment
---

Today I'll be talking about setting up a development environment using node package manager, webpack, and a slew of other tools. I've been using Facebook's create-react-app tool a lot, and I didn't like the 'black box' nature of it. Did I mention I learned React?

Some backstory: I did some long needed maintenance on my PC, and was left with a fresh new install to break in, so I figured, hey, why don't I take the time to set things up right? So I did some searching, and found a few articles that had just the sort of information I was looking for.

To start it off, I  installed my current preferred text editor: [Sublime Text 3](https://www.sublimetext.com/3). When I first started making websites, I used brackets. Brackets is a good first text editor, but I now like Sublime, it's got a lot of good tools, and the program is very lean. My laptop is no powerhouse, and it needs to spare all of the CPU and memory it can.

With Sublime came the packages. Emmet, Babel, SCSS, SublimeLinter-esLint, and a couple autocomplete packages. These are all quality of life add-ons, making syntax highlight the way I want it to, and checking for errors in my code before compile. Emmet in particular is excellent, making a shorthand syntax for making otherwise time-consuming html elements:

    //This is the Emmett syntax:
    .header>h1{Title}+h2>a{smaller Title}
    
    //and here is its output:
    <div class="header">
		<h1>Title</h1>
		<h2><a href="">smaller Title</a></h2>
	</div>
	

   That's pretty amazing. I can't even imagine how much time I could have saved if I had just learned it sooner!

Now, onto the production. Like most people, I typically used [create-react-app](https://github.com/facebook/create-react-app) for my websites. This is fine, and probably the most common avenue for React developers, but I was dissatisfied with the 'black box' I was working with.  Although I understood the basics of npm and webpack,  what was going on under the hood was very much a mystery to me. So what better way to learn them than to start with  the lego *un*assembled this time?

To accomplish my own React environment, I started in where every developer does: Google. Quite quickly (because the web development community is amazing) I came across a tutorial that satisfied my needs. [Setting up a React project from scratch](https://codeburst.io/setting-up-a-react-project-from-scratch-d62f38ab6d97) by Manoj Singh Negi went through every step of assembling the tools for a React website, right up to a hotloading locally hosted test site.

This an excellent guide, step by step and very readable, but parsed enough that I could take the time to assess what the purpose of each action, installation dependency was. So I got to work, and carefully walked myself through the process. I'll make a summary of my additions, all of them were incorporated using npm.

 1. npm init, git init, git remote add

> Old hat for me. Get the git linked to a github repo, and prepare node and npm for the coming packages.

 2. npm install --save react react-dom
 >I found out during this the purpose of --save, It's to save a step of adding the dependency to package.json
 3. npm install --save webpack webpack-dev-server
 >webpack builds the code I make into something optimized for the web. Webpack-dev-server is how I'll host the website while I'm working on it.
 4. npm install --save-dev *a whole whack of babel packages*
>Babel takes modern JS and JSX and turns it into readable JS for the browsers.
5.  Set up the webpack config and the package.json.
>These are the commands and specifications webpack and npm will utilize to build the site, as well as keep track of dependencies and CLI commands, among other things. 

I did deviate from the instructions a bit here. The instructions have you install a less-loader, instead I installed and incorporated a sass loader, as that's my CSS precompiler of choice. After that, I needed to build out some standard files, index.js, index.html, app.js, the usual.

From here, I was ready for `npm run dev`! It was crazy to think how simple it would be to bui- oh, it broke. "Unexpected token" at the '<' in `<App />`. After looking things over, it wasn't a problem with my semantics, I had to figure out what I was missing.

I could tell it was not reading the JSX part of the JS, so I starting by reinstalling the packages for Babel. No luck. Then, I read the comments of the article for people with similar issues. Nada.  Now to searching. After a combination of 'unexpected token', 'webpack', and 'jsx', I found some leads that indicated the problem. the package of babel-preset-es2015 had been deprecated, and the new kid in town was babel-preset-env. Babel had a [page](https://babeljs.io/env/) explaining the replacement, and what to swap in package.json to solve the issue.

And on round 2: Success! A mostly white page with the words "Hello, world!" in the upper left corner. I'm surprised how satisifying that sight can be. I threw up an .scss file with a blue background to ensure sass was playing nice, and I was all set. I took a quick detour after this with `npm install pretty-quick husky `. This utilizes [Prettier](https://prettier.io/) and [Husky](https://github.com/typicode/husky), and will incorporate formatting with every git commit, cleaning up my code, and encouraging me to commit more when things get untidy.

Now, onto building a website! I'm pleased with today's work. I'll still be using create-react-app in the future, but It's good to know I have an alternative, as well as an improved understanding of the process! No doubt I'll be more inclined to streamline my work with automation and tweaks. As for now, I'm eager to get familiar with Emmett, 'til next time!
