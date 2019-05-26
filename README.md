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

A `config file is needed in order to provide the configuration for the application. Please,
create one as follow and save as `config.py`:

```python
consumer_key = 'your-consumer-key'
consumer_secret = 'your-consumer-secret'
access_token = 'your-access-token'
access_secret = 'your-access-secret'
```

Change the values according with your properly account data.

### Running

Before running, create a needed file: `~$ touch python.json`.

Then, run as given below:

```bash
~$ python app.py
```

This script keeps running, use `ctrl+c` to abort it. The results will be available
in `python.json` file. An example is given below:

```json
{
   "created_at":"Sun May 26 20:38:22 +0000 2019",
   "id":...,
   "id_str":"...",
   "text":". #SomeHashtag",
   "source":"\u003ca href=\"http:\/\/twitter.com\" rel=\"nofollow\"\u003eTwitter Web Client\u003c\/a\u003e",
   "truncated":false,
   "in_reply_to_status_id":null,
   "in_reply_to_status_id_str":null,
   "in_reply_to_user_id":null,
   "in_reply_to_user_id_str":null,
   "in_reply_to_screen_name":null,
   "user":{
      "id":...,
      "id_str":"...",
      "name":"...",
      "screen_name":"...",
      "location":"Somewhere",
      "url":null,
      "description":"...",
      "translator_type":"none",
      "protected":false,
      "verified":false,
      "followers_count":225,
      "friends_count":451,
      "listed_count":9,
      "favourites_count":8998,
      "statuses_count":29443,
      "created_at":"Mon May 10 20:37:48 +0000 2010",
      "utc_offset":null,
      "time_zone":null,
      "geo_enabled":false,
      "lang":null,
      "contributors_enabled":false,
      "is_translator":false,
      "profile_background_color":"000000",
      "profile_background_image_url":"http:\/\/abs.twimg.com\/images\/themes\/theme1\/bg.png",
      "profile_background_image_url_https":"https:\/\/abs.twimg.com\/images\/themes\/theme1\/bg.png",
      "profile_background_tile":false,
      "profile_link_color":"000000",
      "profile_sidebar_border_color":"000000",
      "profile_sidebar_fill_color":"000000",
      "profile_text_color":"000000",
      "profile_use_background_image":false,
      "profile_image_url":"...",
      "profile_image_url_https":"...",
      "profile_banner_url":"...",
      "default_profile":false,
      "default_profile_image":false,
      "following":null,
      "follow_request_sent":null,
      "notifications":null
   },
   "geo":null,
   "coordinates":null,
   "place":null,
   "contributors":null,
   "is_quote_status":false,
   "quote_count":0,
   "reply_count":0,
   "retweet_count":0,
   "favorite_count":0,
   "entities":{
      "hashtags":[
         {
            "text":"SomeHashtag",
            "indices":[
               2,
               8
            ]
         }
      ],
      "urls":[

      ],
      "user_mentions":[

      ],
      "symbols":[

      ]
   },
   "favorited":false,
   "retweeted":false,
   "filter_level":"low",
   "lang":"und",
   "timestamp_ms":"1558903102635"
}
```

## Built With

* [Python 3](https://www.python.org/)
* [Pip v3](https://pip.pypa.io/en/stable/)
* [Tweepy](https://www.tweepy.org/)

## Authors

* Sergio Rodríguez.
