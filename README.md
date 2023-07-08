# node_installation_with_nvm
When we are consulting the [documentation of npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) to install it in our environments we do not find that this package manager strongly recommends us to use a node version manager.

[Node version managers](https://github.com/nvm-sh/nvm) allow you to install and switch between multiple versions of Node.js and npm on your system so you can test your applications on multiple versions of npm to ensure they work for users on different versions.

## Steps
-  The first thing to do is to check if we have any version of node installed in the environment we are going to work with.
```sh
node -v
```
The answer we expect is: ' *"node" is not recognized as an internal or external command, program or executable batch file'*. If not, we must uninstall node from our environment

- In this guide we are going to use [nvm-windows](https://github.com/coreybutler/nvm-windows). But npm has another option [nodist](https://github.com/nullivex/nodist)
  - When we are in the nvm-windows repository, what we must do is to click on [download now!](https://github.com/coreybutler/nvm-windows/releases) that will take us to the repo releases. 
  - There we will look for the **nvm-setup.zip** and when we click on it, it will start downloading.
  - When you have it downloaded, unzip it and execute the file (like any other executable file, I make it so simple to avoid problems when I want to update with the update executable that is in the same repo).
  - Now, restart the command line in which we are working and run nvm  
```sh
nvm
```
```sh
Running version 1.1.10.

Usage:

  nvm arch                     : Show if node is running in 32 or 64 bit mode.
  nvm current                  : Display active version.
  nvm install <version> [arch] : The version can be a specific version, "latest" for the latest current version, or "lts" for the
                                 most recent LTS version. Optionally specify whether to install the 32 or 64 bit version (defaults
                                 to system arch). Set [arch] to "all" to install 32 AND 64 bit versions.
                                 Add --insecure to the end of this command to bypass SSL validation of the remote download server.
  nvm list [available]         : List the node.js installations. Type "available" at the end to see what can be installed. Aliased as ls.
  nvm on                       : Enable node.js version management.
  nvm off                      : Disable node.js version management.
  nvm proxy [url]              : Set a proxy to use for downloads. Leave [url] blank to see the current proxy.
                                 Set [url] to "none" to remove the proxy.
  nvm node_mirror [url]        : Set the node mirror. Defaults to https://nodejs.org/dist/. Leave [url] blank to use default url.
  nvm npm_mirror [url]         : Set the npm mirror. Defaults to https://github.com/npm/cli/archive/. Leave [url] blank to default url.
  nvm uninstall <version>      : The version must be a specific version.
  nvm use [version] [arch]     : Switch to use the specified version. Optionally use "latest", "lts", or "newest".
                                 "newest" is the latest installed version. Optionally specify 32/64bit architecture.
                                 nvm use <arch> will continue using the selected version, but switch to 32/64 bit mode.
  nvm root [path]              : Set the directory where nvm should store different versions of node.js.
                                 If <path> is not set, the current root will be displayed.
  nvm [--]version              : Displays the current running version of nvm for Windows. Aliased as v.
```

- Now we can install node and as we can see we have several options to install node
```sh
nvm install lts -> to install the latest lts version
nvm install lates ->to install the latest version
nvm install specific version (example: 18.14.2)
```

- Now we can see the versions of node that we have installed in our environment with 
```sh
nvm list
```

- To finish configuring the node version that we want to use in our environment we run the command in a terminal with administrator permissions 
```sh
nvm use node-version (example: nvm use 18.14.2)
```

- To check the node version we are using we run the command
```sh
nvm current
```

- After installing node restart the command line and check the version we installed previously
```sh
node -v
```

- We can also uninstall node versions that we have in the environment.
```sh
nvm uninstall node-version (example: nvm uninstall 18.14.2)
```

Finishing this tutorial we have installed node through a node version manager that as it is recommended 

⭐ From: [The Coder Cave esp](https://www.youtube.com/watch?v=Z-Ofqd2yBCc&t=399s)
