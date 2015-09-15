# Supported tags and respective `Dockerfile` links

-	[`5.3.0`, `5.3`, `5`, `latest` (*5.3/Dockerfile*)](https://github.com/mbutkereit/docker-solr/blob/master/5.x/Dockerfile)

# What is Solr?
Solr is highly reliable, scalable and fault tolerant, providing distributed indexing, replication and load-balanced querying, automated failover and recovery, centralized configuration and more. Solr powers the search and navigation features of many of the world's largest internet sites.

Learn more on [Apache Solr homepage](http://lucene.apache.org/solr/) and in the [Apache Solr Reference Guide](https://www.apache.org/dyn/closer.cgi/lucene/solr/ref-guide/).

> [wikipedia.org/wiki/Apache_Solr](https://en.wikipedia.org/wiki/Apache_Solr)

![Solr Logo](https://raw.githubusercontent.com/makuk66/docker-solr/master/logo.png)

# How to use this Docker image

To run a single Solr server:

    SOLR_CONTAINER=$(docker run -d -p 8983:8983 -t marvinb8/search-api-solr)

Then with a web browser go to `http://localhost:8983/` to see the Admin Console (adjust the hostname for your docker host).

In the web UI if you click on "Core Admin" you should now see the "myindex" core.

To learn more about Solr, see the [Apache Solr Reference Guide](https://cwiki.apache.org/confluence/display/solr/Apache+Solr+Reference+Guide).

# About this repository

This repository is available on [github.com/mbutkereit/search-api-solr](https://github.com/mbutkereit/search-api-solr), and the automated build is on the [Docker Registry](https://registry.hub.docker.com/u/makuk66/docker-solr/).

## Supported Docker versions

This image has been tested with Docker version 1.5.0.

# User Feedback

## Issues

If you have any problems with or questions about this image, please submit a [GitHub issue](https://github.com/mbutkereit/search-api-solr/issues).

## Contributing

If you have have a contribution for this repository, please send a pull request.

If you want to contribute to Solr, see the [Solr Resources](http://lucene.apache.org/solr/resources.html).

# License

Solr is licensed under the [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0), and this repository:

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
