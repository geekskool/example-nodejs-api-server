# Example NodeJS API Server

### Make Project Directory and initialize Git

    $ mkdir apiserver
    $ cd apiserver
    $ git init
    
    Initialized empty Git repository in /Users/workspace/apiserver/.git/file

Add `.gitignore` file to the directory
    npm_modules

### Create Node Project - package.json

    $ npm init
    This utility will walk you through creating a package.json file.
    It only covers the most common items, and tries to guess sensible defaults.
    
    See `npm help json` for definitive documentation on these fields
    and exactly what they do.
    
    Use `npm install <pkg> --save` afterwards to install a package and
    save it as a dependency in the package.json file.
    
    Press ^C at any time to quit.
    name: (apiserver)
    version: (1.0.0)
    description: Example JSON API Server
    entry point: (index.js)
    test command:
    git repository:
    keywords:
    author: Santosh Rajan
    license: (ISC) MIT
    About to write to /Users/santosh/workspace/apiserver/package.json:
    
    {
      "name": "apiserver",
      "version": "1.0.0",
      "description": "Example JSON API Server",
      "main": "index.js",
      "directories": {
        "doc": "docs"
      },
      "scripts": {
        "test": "echo \"Error: no test specified\" && exit 1"
      },
      "author": "Santosh Rajan",
      "license": "MIT"
    }
    
    Is this ok? (yes) yes

Add the following line to the scripts tag in `package.json`
    "start": "node ./bin/www",

Create a `bin` folder and a file called www with the following line
    console.log("Hello! From my own Node Server")

Now run your server.

    $ npm run start
    
    > apiserver@1.0.0 start /Users/workspace/apiserver
    > node ./bin/www
    
    Hello! From my own Node Server

Lets now create a lib folder where all the server code will reside. Create a file `server.js`
in the `lib` folder. We will use the Express framework for the server.

    console.log
    var express = require('express')
    
    console.log("Hello! From my own Node Server")
