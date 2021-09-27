# Getting started

To get started you will first need to get a copy of this repository. Follow the steps below to get your own personal copy. This only needs to be done once.

1. Get the GitHub classroom invitation link from Toledo
1. Accept the assignment
1. Wait for your own personal copy to be created (can take up to several minutes)
1. Open the GitHub page of your repository
1. Copy the ssh clone-url (green button) that looks like `git@github.com:vives-web-essentials-2020/web-essentials_practical-<username>.git`
1. Traverse to a local directory on your system where you wish to clone the repo using Windows Explorer. Open `PowerShell` in that location by typing powershell in the location bar as shown in the screenshot below.

_Please don't choose a destination directory that is nested very deeply. The structure of this repo introduces quite a lot of subdirectories and might give problems towards maximum path length in Windows._

![Opening PowerShell in directory](./img/powershell.png)

Issue the git clone command followed by the url you copied.

```shell
git clone <place-ssh-url-here>
```

You should get the following output:

```shell
Cloning into 'web-essentials-practical-sillevl'...
Warning: Permanently added the RSA host key for IP address '192.30.253.113' to the list of known hosts.
remote: Enumerating objects: 185, done.
remote: Compressing objects: 100% (109/109), done.
Receiving objects: 100% (185/185), 128.22 KiB | 625.00 KiB/s, done.
Resolving deltas: 100% (57/57), done.
```

Now you should have your local copy of the repository.

All git commands in other sections should always be executed inside of the project dir called `web-essentials-practical-<username>`.

## Install dependencies

In order to get some extra tools working you need to install them. Just run the following command inside the project directory:

```shell
npm install
```

This will install some 'linter' tools. These tools will check if your documents are structured correctly. The following linter are available:

* Markdown: `npm run lint-markdown`
* HTML: `npm run lint-html`
* CSS: `npm run lint-css`
* JavaScript: `npm run lint-js`

These linters will be ran every time you upload code to GitHub as well. This will give you feedback if any problems should be detected in your documents. Please make sure to keep your documents will structured and formatted. If errors or warnings occur in documents, a descriptive message will be displayed giving more details about the error. Most of the time you get enough information to solve the problems. If you are unable to solve the problems, just contact the teacher.
