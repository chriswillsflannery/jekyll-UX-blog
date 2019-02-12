---
layout: post
title:  "Up and running with Gatsby + React"
date:   2019-02-12 11:45:23 -0500
categories: React
---

So today I'm building a new static site using Gatsby, which is basically a javascript package for React which does the "setup" steps for you
when you're building a new React site. You can basically think of it as Bootstrap for React. Normally if you were building a new React site
you would do something like `npm create-react-app new` in your javascript environment and it would create a folder with some basics, just to get
you up and running locally. Gatsby does this, but also builds out a basic template for your homepage including a brand/navbar-type block on top,
some content, and a footer. When you create your first Gatsby folder and `run develop` you'll see something like this:

![Gatsby template](https://imgur.com/GU5ylmY "Gatsby template")

The implications of this are pretty sick - React is already fast AF and with Gatsby you can make new static sites in like 2 seconds. I could see
this being particularly useful for blogs, portfolio sites, simple brochure type info, etc...

If you're new to React, it's important to understand that the way React works is basically like a vanilla JS + HTML + CSS site but instead of having
all your content in your `index.html` file your content is broken up into components, or bits of code, which pass information up a hierarchical path.
For example, if you want to make a navbar, you could create the navbar component in one file, then call it in the parent file, thereby passing it upward.
To give you an idea, here's a way oversimplified visual representation:

![React basics](https://imgur.com/qrIfSrV "React basics")

There's a ton of good stuff included in the Gatsby folder you just created. Components like Header, Images, Layout, and SEO are created automatically and just sitting there waiting for you to populate with whatever you want. An `index.js` file pulls information from a `layout.js` file, using components. All the
info in each component file feeds into its respective parent file. There's a ton of options, and once you get the hang of it, the entire process is super slick and easy to understand.

Gatsby's dev website has a ton of plugin like google analytics and sass which you can add to your projects.
Basically whatever functionality you need to find is right there in their database. And once you push your new
Gatsby site to Github, from there, it's easy to deploy the site to Netlify or another host.
I created a super simple site and deployed to Netlify for free, which you can see here:


[https://pedantic-feynman-35e198.netlify.com/](https://pedantic-feynman-35e198.netlify.com/)

While I was creating my first Gatsby site I was kinda bummed to find out that Atom (the text editor I'm using) supports Emmet (a plugin which makes it waaaaaay faster to write HTML) in HTML but not in JSX (JSX is basically HTML, but inside of some javascript). That's too bad, because when you're working with React files you'll be writing a lot of JSX, and it would have been super convenient to be able to do shortcuts with Emmet, like I have done in the past when writing regular HTML. I did find out, though, thatVisual Code and some other text editors do support Emmet in JSX. Poor me. Too late to switch, I've already sold my soul to Atom.

ALL HAIL THE GITHUB OVERLORDS but forreal Github pls make emmet compatible with JSX in Atom soon thx @github #help #me #im #needy
