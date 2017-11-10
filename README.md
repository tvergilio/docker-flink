docker-flink
============

Docker packaging for Apache Flink

Use `add-version.sh` to rebuild the Dockerfiles and all variants for a
particular Flink release release. Before running this, you must first delete
the existing release directory.

    usage: ./add-version.sh -r flink-release -f flink-version

Example
-------

    $ rm -r 1.2
    $ ./add-version.sh -r 1.2 -f 1.2.1

License
-------

Licensed under the Apache License, Version 2.0: https://www.apache.org/licenses/LICENSE-2.0

Apache Flink, Flink®, Apache®, the squirrel logo, and the Apache feather logo are either registered trademarks or trademarks of The Apache Software Foundation.

Edited by tvergilio
-------------------

Edited flink:1.3.2-hadoop2-scala_2.10 alpine image.

### The original image configured the following ports:
* blob.server.port: 6124
* query.server.port: 6125

### I added the following configuration:
* taskmanager.data.port: 6126
* taskmanager.rpc.port: 6127
