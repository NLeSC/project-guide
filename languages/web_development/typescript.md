# TypeScript

http://www.typescriptlang.org

Typescript is a typed superset of JavaScript which compiles to plain JavaScript.

## Getting Started

To learn about TypeScript the following resources are available:

* [youtube](http://www.youtube.com/playlist?list=PLyJiOytEPs4d9QUQHHSuY3n3nBmkBuqro): tutorials playlist about TypeScript
* [tutorial](http://www.typescriptlang.org/Tutorial) from Microsoft's TypeScript website  
* [blog post](http://www.aaron-powell.com/posts/2012-10-03-typescript-source-maps.html) about how TypeScript can be used with the Google Chrome/Chromium debuggers (and [presumably](http://blog.oio.de/2014/04/04/internet-explorer-11-source-map-based-debugging/) Firefox, and Internet Explorer) through the use of so-called 'source maps'. (Follow [this](http://www.codeproject.com/Articles/649271/How-to-Enable-Source-Maps-in-Firefox) link to set up source mapping for Firefox, also useful for debugging minified JavaScript code).
* [blog post](http://www.sitepen.com/blog/2013/12/31/definitive-guide-to-typescript/) that supposedly is the definitive guide to TypeScript
* TypeScript Language Specification [pdf](http://www.typescriptlang.org/Content/TypeScript%20Language%20Specification.pdf)

## Basic Workflow

### Quickstart

To install most common TypeScript dependencies run:

```shell
# system packages (Ubuntu/Debian)
sudo apt-get install npm
#
sudo apt-get install nodejs
#
sudo apt-get install nodejs-legacy
#
sudo apt-get install ruby
#
sudo apt-get install ruby-dev

# Ruby package
sudo gem install compass

# Node packages
npm install -g typescript
#
npm install -g typings
#
npm install -g bower
#
npm install -g nodemon
#
npm install -g http-server
```

### Starting a project

Similar to JavaScript a new project could be created using [Yeoman](http://yeoman.io/). 
For instance [Fountainjs](http://fountainjs.io/) is a generator that can create a project that uses TypeScript.

```shell
#
npm install -g yo
#
npm install -g generator-fountain-webapp
#
npm install -g bower
```

```shell
#
yo fountain-webapp
```

However, most of these generators use either ``gulp`` or ``grunt`` as a build system, while for most cases ``npm`` works just fine by defining a number of npm scripts in the package.json.
See [this blog post](http://substack.net/task_automation_with_npm_run) for more information.

### Dealing with Types

In TypeScript, variables are typed and these types are checked.
This implies that when using frameworks, the types of these frameworks need to be installed.
The easiest way to make sure you have the correct types for your framework is by using the [typings tool](https://github.com/typings/typings), which can be installed using ``npm``.

```shell
npm install -g typings
```

This tool works similar to bower and npm in that you can search for typings and install them.
For example say we want to use the ``angular-ui-bootstrap`` package which we installed using ``bower``:
```shell
bower install angular-bootstrap --save
```

To be able to use its functionality in TypeScript we need to install the typings. 
We can search for the correct package:

```shell
> typings search angular-ui-bootstrap
Viewing 1 of 1

NAME                 SOURCE HOMEPAGE                                DESCRIPTION VERSIONS UPDATED                 
angular-ui-bootstrap dt     https://github.com/angular-ui/bootstrap             1        2016-07-05T22:14:53.000Z
```

And install it with:

```shell
typings install angular-ui-bootstrap --global --save
```

The ``--global`` flag is needed as it is a framework package.
The ``--save`` flag saves this installation to the typings.json file.
The typings.json file can be used to quickly install all typings when cloning the repository. 


### Development Environment

These are some good TypeScript editors:

* JetBeans [WebStorm](https://www.jetbrains.com/webstorm/)
* Github [Atom](http://atom.io) with the ``atom-typescript`` Atom package.
* Microsoft [Visual Studio Code](https://code.visualstudio.com)
* Adobe [Brackets](http://brackets.io/?lang=en)

The best JavaScript editors are currently WebStorm and Visual Studio Code. Atom can have some performance problems.



* JetBeans [WebStorm](https://www.jetbrains.com/webstorm/)
* Github [Atom](http://atom.io) with the ``atom-typescript`` Atom package when using TypeScript
* Microsoft [Visual Studio Code](https://code.visualstudio.com)
* Adobe [Brackets](http://brackets.io/?lang=en), [screenshot](https://raw.githubusercontent.com/wiki/NLeSC/kb/attachments/screenshot-brackets.png)


### Debugging


In web development, debugging is typically done in the browser. 

* The best debugging tool suite is currently the debugger built into the Google Chrome webbrowser, and its open-source counterpart, Chromium. It can watch variables, step through the code, lets you monitor network traffic, and much more. Activate the debugger through the F12 key.
* On Firefox, use either the built-in debugging functionality (again accessible through the F12 button) or install the [Firebug](https://addons.mozilla.org/en-US/firefox/addon/firebug/) Addon for some more advanced debugging functionality.
* Microsoft has a debugging toolset called 'F12' for their Internet Explorer and Edge browsers. It offers similar capability as that of Google Chrome, Chromium, and Firefox. 
* In Safari on OS X, press ⌘⌥U.

Sometimes the JavaScript code in the browser is not an exact copy of the code you see in your development environment, for example because the original source code is minified/uglified or transpiled before it's loaded in the browser. 
All major browsers can now deal with this through so-called _source maps_, which instruct the browser which symbol/line in a javascript file corresponds to which line in the human-readable source code. 
Look for the 'create sourcemaps' option when using minification/uglification/transpiling tools.

See [this blog post](http://www.aaron-powell.com/posts/2012-10-03-typescript-source-maps.html) for more information.

### Documentation

It seems that [TypeDoc](http://typedoc.io/) is a good tool to use.
Alternative could be [TSdoc](https://www.npmjs.com/package/tsdoc)

### Style Guides

[TSLint](https://github.com/palantir/tslint) is a good tool to check your codestyle.

For the [sim-city-cs project](https://github.com/indodutch/sim-city-cs/) we use the following tslint.json file:

```code
{
  "rules": {
    "class-name": true,
    "curly": true,
    "eofline": true,
    "forin": false,
    "indent": [true, "spaces"],
    "interface-name": "never-prefix",
    "jsdoc-format": true,
    "label-position": true,
    "label-undefined": true,
    "max-line-length": [true, 200],
    "no-arg": true,
    "no-bitwise": true,
    "no-console": [true,
      "debug",
      "info",
      "time",
      "timeEnd",
      "trace"
    ],
    "no-construct": true,
    "no-debugger": true,
    "no-duplicate-key": true,
    "no-duplicate-variable": true,
    "no-empty": true,
    "no-eval": true,
    "no-string-literal": false,
    "trailing-comma": true,
    "no-trailing-whitespace": true,
    "no-unused-variable": [true, {"ignore-pattern": "^_"}],
    "no-unreachable": true,
    "no-use-before-declare": true,
    "one-line": [true,
      "check-open-brace",
      "check-catch",
      "check-else",
      "check-whitespace"
    ],
    "quotemark": [true, "single"],
    "radix": true,
    "semicolon": true,
    "triple-equals": [true, "allow-null-check"],
    "variable-name": [true, "allow-leading-underscore"],
    "whitespace": [true,
      "check-branch",
      "check-decl",
      "check-operator",
      "check-separator"
    ]
  }
}
```
