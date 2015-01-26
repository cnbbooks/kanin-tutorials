# Kanin / RabbitMQ Tutorials


## Overview

The Kanin Tutorials are several things:

1. In-depth documentation for Kanin, the LFE RabbitMQ client library;
1. An LFE port of the [Erlang RabbitMQ Tutorial code](https://github.com/rabbitmq/rabbitmq-tutorials/tree/master/erlang); and, to a certain extent,
1. An LFE conversion of the [Python RabbitMQ tutorials](http://www.rabbitmq.com/tutorials/tutorial-one-python.html)


## About RabbitMQ

RabbitMQ is a message broker. The principal idea is pretty simple: it accepts
and forwards messages. You can think about it as a post office: when you send
mail to the post box you're pretty sure that Mr. Postman will eventually deliver
the mail to your recipient. Using this metaphor RabbitMQ is a post box, a post
office and a postman.

The major difference between RabbitMQ and the post office is the fact that it
doesn't deal with paper, instead it accepts, stores and forwards binary blobs of
data ‒ messages.

RabbitMQ, and messaging in general, uses some jargon.

* **Producer** - Producing means nothing more than sending. A program   that
  sends messages is a producer.

* **Queue** - A queue is the name for a mailbox. It lives inside RabbitMQ.
  Although messages flow through RabbitMQ and your applications, they can be
  stored only inside a queue. A queue is not bound by any limits, it can store
  as many messages as you like ‒ it's essentially an infinite buffer. Many
  producers can send messages that go to one queue, many consumers can try to
  receive data from one queue.

* **Consumer** - Consuming has a similar meaning to receiving. A consumer is a
  program that mostly waits to receive messages.

Note that the producer, consumer, and broker do not have to reside on the same
machine; indeed in most applications they don't.


## Getting Set Up

Here's what you will need:

* A running RabbitMQ server - [instructions here](https://www.rabbitmq.com/download.html)
* The Kanin / RabbitMQ [starter project](https://github.com/billosys/kanin-tutorials-starter)

Followt the RabbitMQ download and installation instructions linked above.
Similarly, by following the instructions on the Kanin starter project Github
page, you will get the rest of the dependencies needed for these tutorials.

These tutorials assume that you have done the following:

```bash
$ git clone \
    https://github.com/billosys/kanin-tutorials-starter.git \
    kanin-tutorials
$ cd kanin-tutorials
$ make compile
```

All instructions in the tutorials are given from the
context of the ``kanin-tutorials`` directory.

Shall we begin?

