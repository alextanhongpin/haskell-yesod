# haskell-api

## Installation

To install/upgrade `stack`:

```bash
$ curl -sSL https://get.haskellstack.org/ | sh -s - -f
```

## Scaffold

```bash
# View available templates
$ stack templates

# Start a new template with mysql
$ stack new my-project yesod-mysql && cd my-project
```

## Yesod CLI

```bash
$ stack install yesod-bin --install-ghc
```

## Build

```bash
$ stack build
```

## Run

```bash
$ stack exec -- yesod devel
```

## Pull

```bash
$ stack docker pull
```

## View

```bash
$ docker images | grep fpco/stack-build
fpco/stack-build                                lts-11.6            91e60896cf30        6 weeks ago         7.15GB
```

## Database Setup

After installing MySQL, run:

```
mysql --user=root
```

Then enter:

```
CREATE DATABASE haskell-api;
CREATE DATABASE haskell-api_test;
CREATE USER 'haskell-api'@'localhost' IDENTIFIED BY 'haskell-api';
GRANT ALL PRIVILEGES ON *.* to 'haskell-api'@'localhost';
```
<!-- 
## Haskell Setup

1. If you haven't already, [install Stack](https://haskell-lang.org/get-started)
	* On POSIX systems, this is usually `curl -sSL https://get.haskellstack.org/ | sh`
2. Install the `yesod` command line tool: `stack install yesod-bin --install-ghc`
3. Build libraries: `stack build`

If you have trouble, refer to the [Yesod Quickstart guide](https://www.yesodweb.com/page/quickstart) for additional detail.

## Development

Start a development server with:

```
stack exec -- yesod devel
```

As your code changes, your site will be automatically recompiled and redeployed to localhost.

## Tests

```
stack test --flag haskell-api:library-only --flag haskell-api:dev
```

(Because `yesod devel` passes the `library-only` and `dev` flags, matching those flags means you don't need to recompile between tests and development, and it disables optimization to speed up your test compile times).

## Documentation

* Read the [Yesod Book](https://www.yesodweb.com/book) online for free
* Check [Stackage](http://stackage.org/) for documentation on the packages in your LTS Haskell version, or [search it using Hoogle](https://www.stackage.org/lts/hoogle?q=). Tip: Your LTS version is in your `stack.yaml` file.
* For local documentation, use:
	* `stack haddock --open` to generate Haddock documentation for your dependencies, and open that documentation in a browser
	* `stack hoogle <function, module or type signature>` to generate a Hoogle database and search for your query
* The [Yesod cookbook](https://github.com/yesodweb/yesod-cookbook) has sample code for various needs

## Getting Help

* Ask questions on [Stack Overflow, using the Yesod or Haskell tags](https://stackoverflow.com/questions/tagged/yesod+haskell)
* Ask the [Yesod Google Group](https://groups.google.com/forum/#!forum/yesodweb)
* There are several chatrooms you can ask for help:
	* For IRC, try Freenode#yesod and Freenode#haskell
	* [Functional Programming Slack](https://fpchat-invite.herokuapp.com/), in the #haskell, #haskell-beginners, or #yesod channels. -->
