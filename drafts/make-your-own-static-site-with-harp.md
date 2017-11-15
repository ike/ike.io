The web has become [really complicated](http://eev.ee/blog/2015/09/17/the-sad-state-of-web-app-deployment/). It takes so much time, so much frustration, and so much specialized knowledge to set up a new site, blog, forum, or chatroom that many internet citizens no longer build independent experiences. It's become so simple to join an existing silo ([tumblr](http://tumblr.com), [wordpress](https://wordpress.com/), [disqus](https://disqus.com/), [discourse](http://www.discourse.org/)) that we're not as likely to consider the idea of building something that's simple, clear, and completely ours.

I've been involved in indieweb stuff for a while now. The Indieweb is the idea that you can (and should) own your own internet persona – the data that you create online should live, primarily, on your own internet "homestead". The problem is that for a long time, the internet hasn't had tools that made that easy. Traditional personal-data skills like running your own Unix server with a web service and your own email and photo gallery are almost completely foreign to most internet citizens today. While those skills are super valuable, and I encourage anyone to learn them, we're not going to continue to create a freer internet if we relegate any personal-data skills to the land of roll-up-your-sleeves Unix Ops.

_Enter, Static-web Generators._

_[Collective Groan]_

Static web generators have really sucked. I have used tons of them, even helped build one from scratch, and I've been disappointed miserably every time. Jekyll, Hexo, Octopress, GH Pages – all very well-intentioned tools that still kept the knowledge-barrier high enough to be frustrating. Le sigh.

Until I discovered Harp, that is.

Harp is "The static web server with built-in preprocessing." It _just works_. Write your site in almost anything (Jade, Markdown, EJS, CoffeeScript, Sass, LESS and Stylus), and Harp will create a clean, fast site in HTML, CSS, and JS. Presto, exactly what we're looking for.

Let's dig in:

(If you haven't got Node.js on your computer, you can use [this guide](/blog/installing-node-using-nvm.html) to help you get it set up.)

* * * 

**Installing Harp.js**

Harp includes several components – a project builder (installation wizard to walk you through creating a static site), a compiler (compiles your templates and content into a `www` directory of HTML, CSS, and JS), and a server (to locally serve your uncompiled content, updating as you edit files). All of these components are installed with one npm module. With [Node.js installed](/blog/installing-node-using-nvm.html), copy and paste the following command into your Terminal application:

```sh
sudo npm install -g harp
```

After you type your computer's password, a progress bar will appear as all the components of Harp are downloaded and installed. Once that's finished, you can start your first static website.

First, [navigate to the directory]http://stackoverflow.com/questions/9547730/how-to-navigate-to-to-different-directories-in-the-terminal-mac you'd like to keep your static website. Then, initialize a Harp project by typing the following in your Terminal:

```sh
harp init myproject
```

Replace `myproject` with the name of your static website.

Check it out! It dumped some stuff into this directory! When you use the `harp init` command, it downloads some boilerplate from the Harp website, and create the following files:

```
404.jade
_layout.jade
index.jade
main.less
```

Now we can spin up a local server to see our new static site. Type `harp server` into your Terminal. 

[Note: this is why I love Node.js. Instead of having to install php and mysql and apache, you just install Node - an entire browser’s worth of JavaScript – and we're running a local server in minutes, instead of days]

It will tell you exactly where it is running! 

```sh
------------
Harp v0.19.0 – Chloi Inc. 2012–2015
Your server is listening at http://localhost:9000/
Press Ctl+C to stop the server
------------
```

You should be able to navigate to [http://localhost:9000/](http://localhost:9000/) and see your brand-new boilerplate static website.
 
Now you can just open up that directory in your computer's Finder and leave the local server running while you edit your site. The server will just monitor the folder and automatically update what you change on the site. Just refresh your browser when you make an edit.

Now you can edit your static site. The boilerplate is all written in [Jade](http://jade-lang.com/) and [Less](http://lesscss.org/), but you can write in almost any templating language you want, including [Markdown](http://daringfireball.net/projects/markdown/), [EJS](http://www.embeddedjs.com/), [CoffeeScript](http://coffeescript.org/), [Sass](http://sass-lang.com/), and [Stylus](https://learnboost.github.io/stylus/). Try creating some new documents and viewing the output HTML in your browser. Pretty magical, right?

Harp has fantastic [documentation on their website](http://harpjs.com/docs/) for [structuring your site](http://harpjs.com/docs/development/rules), [creating layouts](http://harpjs.com/docs/development/layout), [using preprocessors like Markdown](http://harpjs.com/docs/development/markdown), and [deploying to hosts like Github Pages](http://harpjs.com/docs/deployment/github-pages).

Personally, I like hosting on [Neocities.org](https://neocities.org/), which is fantastically easy.

First, we have to compile our static site into HTML, CSS, and JS. To do this, type the following in your Terminal:

```sh
harp compile
```

This will compile your static site into HTML, CSS, and JS in the `www` directory within your project directory.

Now, to deploy my site to Neocities, I just open that `www` directory in my finder, and:



