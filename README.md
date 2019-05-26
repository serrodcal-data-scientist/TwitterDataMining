# TwitterDataMining

This repository consist of an example for mining data from Twitter by streaming.
Here, I follow [this tutorial](https://marcobonzanini.com/2015/03/02/mining-twitter-data-with-python-part-1/)
and the goal is to move this example to a Scala project using Akka Streams, Alpakka
and Apache Kafka.

## Getting Started

### Prerequisites

First of all, install Python 3.X from [the official site](https://www.python.org/).

Also, install [Pip](https://pip.pypa.io/en/stable/installing/).

Then, install [tweepy](https://tweepy.readthedocs.io/en/latest/index.html) as given below:

```bash
~$ pip install tweepy
```

Finally, register your application on [http://apps.twitter.com](http://apps.twitter.com).
Twitter will provide you all information you need to be able to consume twits.

### Config

A `config.py` file is needed in order to provide the configuration for the application. Please,
create one as follow and save as `config.py`:

```python
consumer_key = 'your-consumer-key'
consumer_secret = 'your-consumer-secret'
access_token = 'your-access-token'
access_secret = 'your-access-secret'
```

Change the values according with your properly account data.

### Running

Run as given below:

```bash
~$ python app.py
```

## Built With

* [Python 3](https://www.python.org/)
* [Pip v3](https://pip.pypa.io/en/stable/)
* [Tweepy](https://www.tweepy.org/)

## Authors

* Sergio Rodríguez.
