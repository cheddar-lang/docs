# Developing

Developing for Cheddar development was designed to be as easy and quick to make as possible. Unfortunately, the workings can be confusing to someone not familiar with how cheddar works. This chapter will cover how Cheddar works, and how to develop for it. If you have _any_ questions at all, please do not hesitate to ask on [Slack](http://cheddarlang.slack.com), [Stack Exchange Chat](http://chat.stackexchange.com/rooms/37686/cheddar), or [Gitter](https://gitter.im/cheddar-lang/Cheddar).

## Downloading
**Note:** if you are on *Windows* you can install `make` from [here](http://gnuwin32.sourceforge.net/packages/make.htm) if you haven't already. Make sure `make` is in your PATH, if it isn't **that's okay**, but you'll have to manually build using `<location of make> build`


To download the source **make sure you have `node`, `npm`, and `make` installed**. Once you've done that clone the `develop` branch from Github:

```bash
$ git clone -b develop http://github.com/cheddar-lang/Cheddar.git
```
now in that directory, you're going to see a `src/` folder. That is where the source code is. 

Before developing, make sure you run:

```
$ npm install
```

to install the required dependencies

## Running
To run it, first run `make build`:

```bash
$ make build
```

this will compile the code. If it doesn't error, you can run it:

```bash
$ node ./dist/cli/cheddar.js
```