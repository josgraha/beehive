beehive
=======

beehive is a flexible event system, which allows you to create your own action-
chains and filters. It is modular and easy to extend - for anyone. It can be
your IRC bot, it can activate your heating system or make you a cup of coffee.
Yes, finally!

## Installation

Make sure you have a working Go environment. See the [install instructions](http://golang.org/doc/install.html).

First we need to get the required dependencies. beehive itself is part of that
list so the main executable can depend on our sub-packages:

    go get github.com/fluffle/goirc/client
    go get github.com/mattn/go-xmpp
    go get github.com/jteeuwen/go-pkg-rss
    go get github.com/hoisie/web
    go get github.com/muesli/beehive

Now we can build beehive:

    git clone git://github.com/muesli/beehive.git
    cd beehive
    go build

To run the application you will (currently) need to specify at least a few options,
e.g. for using the IRC-bee module:

    ./beehive -irchost="some.server:6667" -ircchannel="#beehive"

Run beehive -help to see a full list of options!

## Configuring your chains

To be written by someone! :-)

Until then you can find a [few chain recipes here](https://github.com/muesli/beehive/tree/master/recipes).
Pick one, edit it to your needs and store it as 'beehive.conf'. beehive looks for this
configuration file in its current working directory.

## Development

API docs can be found [here](http://godoc.org/github.com/muesli/beehive).

Continuous integration: [![Build Status](https://secure.travis-ci.org/muesli/beehive.png)](http://travis-ci.org/muesli/beehive)
