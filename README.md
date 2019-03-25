# Redditlastic
Elastisearch on Reddit data

# Install the packages in requirements.txt


# Setting up the elastisearch instance

1. From the utils directory the docker-compose.yml file is in, call:

docker-compose up -d

This should install and start Elasticsearch 6 together with a tool
called cerebro, which we are going to use during the workshop to
formulate queries and inspect results. Note that both Elasticsearch and
cerebro will be started and kept alive in the background. If you want to
stop them, use

docker-compose stop

To start them again, use

docker-compose start

If you want to destroy both processes, use

docker-compose down

2. You should now be able to call and use Elasticsearch. We will learn
how to talk to Elasticsearch in the course, so let us now focus on
verifying that you are setup correctly.

Use curl (or something similar) like this:

curl "http://localhost:9200/"

Alternatively, you may use a browser of your choice and type
http://localhost:9200/ into your address bar.

This should return to you something like this:

{
  "name" : "eatuXBs",
  "cluster_name" : "docker-cluster",
  "cluster_uuid" : "WeMMpShkRjypQKAzqfo6uw",
  "version" : {
    "number" : "6.5.4",
    "build_flavor" : "default",
    "build_type" : "tar",
    "build_hash" : "d2ef93d",
    "build_date" : "2018-12-17T21:17:40.758843Z",
    "build_snapshot" : false,
    "lucene_version" : "7.5.0",
    "minimum_wire_compatibility_version" : "5.6.0",
    "minimum_index_compatibility_version" : "5.0.0"
  },
  "tagline" : "You Know, for Search"
}

Open a browser of your choice and type the following into your address bar:

http://localhost:9000/

This should load a page that asks for a node address. To make sure you
are properly connected, type in the following as node address and press
"Connect":

http://elasticsearch:9200

3. add ELASTICSEARCH_URL=http://localhost:9200 to the environmental variable.
