
# Hello World application

Ok. Lets create our very first HTML document and get everything up and running.

## minimal Hello World document

First we need to create an `index.html` document inside this projects directory (`hello-world`). You can do this by right-clicking the directory in the explorer window and open click on `Open with Code`.

Visual Studio Code will now open up and set the `hello-world` directory as the projects context. This means that all commands and actions are applied in function of this directory. Create and save a new file called `index.html`

In this document we need to place the following code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>

</body>
</html>
```

Before you start typing or copy-pasting let me teach you a trick. Programmers and developers are lazy people. They will try to get the work done with the least amount of effort. The result is still the most important part. So no corners will be cut, only faster results.

Visual Studio Code supports many languages. Support for all these language is not built-in, but can be added by means of `Extensions`. So before we begin lets install the `HTML Snippets` extension. Snippets are peaces of code that can be placed in the document by using *tab completion*.

Once the `HTML Snippets` extension is installed. Visual Studio Code will now know how to type and complete HTML code for us.

In your - still empty - document, you can type `html:5` and then press the `tab` key. Visual Studio Code will type out some HTML code for you. Easy right?

## Add something interesting

The code above is the minimal code needed to create a valid HTML document. It will show nothing more than an white empty page.

Lets add something more interesting. Lets add some text to the document.

All content that needs to be visible for the visitor of the page must be placed between the `<body>` and `</body>` tags. So lets place the text `Hello World!` between those body tags. The result will look like this:

```html
...
<body>
    Hello World!
</body>
...
```

### HINT: Tabs and HTML

> Notice that the `Hello World!` text is indented with an tab. The sole purpose for this is to *improve* readability for the programmer. It makes it obvious that the text is IN the body of the document.
>
> Please make use of this indentation it will prevent a lot of frustration when searching for errors and bugs. It is a good practice to follow.

Don't forget to save you documents ! `control + s` should be in your fingers.

## View it in the browser

Ok, Now that we have our first document, let's view it in the browser.

Open up chrome and type in [http://localhost](http://localhost).

You should see something like this:

![localhost no connection](img/localhost-noconnection.png)

Did we expect to see this? What went wrong?

So we told the browser to make a **request** to localhost. Instead we got an error with the message that the connection was refused. This means that nobody or nothing was listening for the request. There is no HTTP server that could answer that request.

### HINT: connection refused

> Just remember that whenever you see this error that you don't have an HTTP server up and running.

## Starting the HTTP server

Earlier we installed the Serve HTTP server. Let's start it up so that it can respond to our HTTP requests and serve up the requested documents.

In Visual Studio Code, press the `control + ??` key. It will open up a console or terminal for us. It will load up an embedded version of Powershell where we can execute commands.

Lets type the following:

```powershell
serve
```

This command will start a *server*  in the current directory that listens to localhost on port `5000`. Don't panic if you don't understand all of this. This will get clear following this course. For now just remember to type this command to start a server.

Any other port can be used (1024 and up). For example, when developing port `3000` or port `8080` can be used as well. This can be done by supplying the `-l` option. `serve -l 3000` will start a HTTP server that _listens_ on port `3000` instead of `5000`.

### HINT: Localhost

> Whenever you surf the internet, you type in the domain name like `vives.be`. In our case we have no domain name. We have a server that runs on our computer. So how can we tell the browser to send the request to that server and not some random server somewhere on the planet? Exactly `localhost`
>
> `localhost` is known by every computer as a synonym for `itself`. So when browsing to `localhost` it will always use your own HTTP server to handle the request.
>
> `localhost` consists out of two words... `local` and `host`. Now get it?

### HINT: What about 127.0.0.1

> Another way of telling your browser to use the local machine is by using the ip address `127.0.0.1`. `127.0.0.1` and `localhost` are synonyms so you can choose what ever you are happy with. The result is exactly the same.

Ok, now that our HTTP server is up and running lets reload the webpage in Chrome or FireFox by pressing the `F5` key.

## 404 object not found

Ok, this is still not our webpage.

![object not found](img/404-not-found.png)

What went wrong this time?

Well we asked our browser to get the HTML document inside the root directory of `web-essentials-practical-name`. This is where we executed the `serve` command.

There are no HTML files inside that directory to show.

Ok, lets take it to the `01-hello-world/hello-world` directory then. This directory - if you saved your file correctly - should contain and file called `index.html`.

So lets got back to our browser and ask for the following page: [http://localhost](http://localhost)

### HINT: index.html is the default

> If a file is called `index.html` then it will be the default document that is responded by the HTTP server. [http://localhost](http://localhost) and [http://localhost/index.html](http://localhost/index.html) are essentially the same. In essence, if you forget to provide a document name (.html file), then the HTTP server will check if there is an file called `index.html` available. If there is, then it will respond with that document. This means that you never need to add the `index.html` part at the end of the URL.

What do we get now?

![Hello browser](img/hello-browser.png)

Congratulations! You just made your very first HTML document.

## Submitting your exercise (to GitHub)

### Making changes

Lets make a change in our `index.html` file and add our name in the body element. Make sure to save your file (`control + S` remember)

![git committing](img/git-committing.png)

This tab tells us that - compared to the last time a commit was done -  one change has been made to the documents. In our case that one change is in the `index.html` file where we added our name.

#### Reviewing our change

If you click on the file in the `changes` list. Visual Studio Code will show you what changes you have made. This is handy to review you changes before you commit them.

![reviewing changes](img/reviewing-changes.png)

We can see that the line we added was marked in green. If a line was deleted it will be marked in red. If a change is made it will show a red line and a green line to mark the change.

#### Undoing changes

If we made a mistake or we want to return to an older state of the project, you can reject the changes for that file. This is like an `undo` button, but for software developers. It gives us more power and functionality than an `undo` button. In git this is called *reverting* and can be done with the back arrow button next to the filename.

![reverting](img/reverting.png)

#### Committing a change

If you are pleased with the change and you want to save it, you need to `commit` the change so that we can send it to gitlab.
First we need to mark the file to be committed. This is done by pressing on the `+` sign next to the filename. This is called `staging a change`. Next we need to provide a commit message and finally pres the `???` mark on the top.

The commit message should be a short but meaningful message describing the changes we made. In this case we could type in something like:

```text
add our name to index.html
```

![commit message](img/git-commit-message.png)

Now click on the `???` checkmark to apply the commit.

Ok, the commit is stored locally on your computer now. We still need to `push` it to the server.

Note that Visual Studio Code tells us that there are no changes to the project.

Click on the `...` button and choose `push`. Visual Studio Code will now push the committed changes to gitlab.

![git push](img/git-push.png)

When everything is done and uploaded we can review everything on the GitHub repository webpage.

We can see our latest commit message on top. And if we browse to the `index.html` file we can see its content.
