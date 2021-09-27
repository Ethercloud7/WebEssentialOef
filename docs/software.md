# Required Software

In this course we need some software to get everything up and running.

* Text / Code editor for programming and coding our source files and projects.
* Webserver, better known as an `HTTP Server` to make our projects available and browsable.
* Browser to view the results of our code and projects.
* Version control system for managing our code and progress.

## Visual Studio Code

To write code any text editor could be of use. Notepad is ok, but does not provide any additional tools that could make it more easy to program. On the other hand an IDE or Integrated Development Environment is to big and bulky for our simple projects. For this reason we will make use of an lightweight code editor that provides all the bells and whistles to make programming fun and easy.

There are many code editors available. In this course, we will make use of `Visual Studio Code`. This is an lightweight and free editor from Microsoft that is based on the Visual Studio IDE.

Just surf to [code.visualstudio.com](https://code.visualstudio.com/) and download and install the latest version.

## Node.js

Node.js is a JavaScript runtime that enable you to execute JavaScript code outside of the browser. Node.js provides a whole ecosystem of tools, libraries and frameworks to build software, be also to support or automated development tasks.

Just surf to [nodejs.org](https://nodejs.org) and download and install the latest version.

## HTTP Server

To be able to view the results in the browser in a correct manner. We need a HTTP server. There exist many dedicated HTTP servers for production and development environments. In this case we will mainly focus on development of webpages. Therefore we don't need a full blown HTTP server like [Apache](https://httpd.apache.org/) or [Nginx](https://www.nginx.com/). Instead we will use a lightweight and easy to use HTTP server called [Serve](https://github.com/vercel/serve). Serve is a HTTP server written in JavaScript and can easily be installed using the [NPM](https://npmjs.org) package manager.

Just make sure to have Node.js already installed on your machine. Open your terminal and use the following command:

```shell
npm install -g serve
```

This command will install serve globally (`-g`), and will provide a `serve` command.

## Browser

Once the webserver (= http server) is up and running, the results of the programming can be viewed with the use of a web browser. There are many options available, but our method of choice is the Google Chrome browser. It provides many options for developers, and will make things more easy to work with.

* Firefox: [www.mozilla.org/nl/firefox/](https://www.mozilla.org/nl/firefox/)
* Chrome: [www.google.com/intl/nl/chrome/](https://www.google.com/intl/nl/chrome/)

Download and install both web browsers.

## Git source code management

When writing software and code, you will be confronted with many challenges. One of these challenges is managing code changes and different versions of your project. Git is a tool that will allow us to manage these challenges. It enables to capture changes and keep a history of the project. It also allows to cooperate with different developers and provides means to easily share code.

To work with a remote repository like Github, we need to make sure we are working securely and as easy as possible. Therefor it is important to configure your SSH keys correctly and configure git.

For more detailed instructions, please take a look at the Git installation guide: [https://vives.gitbook.io/software-installation-guide/git](https://vives.gitbook.io/software-installation-guide/git)

Make sure you setup and configure the following things:

* Install git and configure your name and email
* Create an GitHub Account
* Create an SSH key and add your public key to GitHub
* Install posh-git

[Installation instructions](./software/git-github.md)

## Netlify webhosting

Once your webpage is build and tested locally on your machine, it is time to host it somewhere on a real public server. For this we can make use of the free tier of [Netlify](https://www.netlify.com/). Netlify will host your webpage just like any other webpage on the internet.

If you have a GitHub account, you are ready to use Netlify. Just surf to [app.netlify.com/](https://app.netlify.com/) and login with your GitHub account.
