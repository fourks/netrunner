[![Build status](https://circleci.com/gh/mtgred/netrunner/tree/master.svg?style=shield)](https://circleci.com/gh/mtgred/netrunner)

Play Android: Netrunner in the browser.

## Live server

http://www.jinteki.net

[Gameplay videos](https://www.youtube.com/results?search_query=jinteki.net)

![screenshot](https://dl.dropboxusercontent.com/u/5601199/screenshot.jpg)


## Development status

The deck builder implements all the deck building constraints. It is optimised for fast deck editing. It is possible for instance to copy & paste a decklist from a forum and it will be parsed.

The implementation of the game rules is in progress. About 95% of the cards are currently automated. For the cards that aren't, it is possible to resolve them manually most of the time.

[Card rules implementation status](https://docs.google.com/spreadsheets/d/1ICv19cNjSaW9C-DoEEGH3iFt09PBTob4CAutGex0gnE/pubhtml)


## Dependencies

* Node.js, Node Package Manager
* Leiningen (version 2+)
* MongoDB
* Zero MQ


## Installation

Install frontend dependencies:

```
$ npm install
```

Launch MongoDB and fetch card data:

```
$ mongod
$ npm run fetch
```

Compile and watch client side Clojurescript files:

```
$ lein figwheel
```

Compile server side Clojure files:

```
$ lein uberjar
```

Launch game server:

```
$ java -jar target/netrunner-0.1.0-SNAPSHOT-standalone.jar
```

Launch the Node server:

```
$ npm start
```

## Tests

To run all tests:

```
$ lein test test.all
```

To run a single test file:
```
$ lein test test.cards.agendas
```


For more information refer to the [development guide](https://github.com/mtgred/netrunner/wiki/Getting-Started-with-Development).

## License

Jinteki.net is released under the [MIT License](http://www.opensource.org/licenses/MIT).
