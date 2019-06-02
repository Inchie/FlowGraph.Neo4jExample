# Neo4j Example with FLOW

This example shows how you can run the PHP framework [Flow](https://flow.neos.io) with the graph 
database [Neo4j](https://neo4j.com/).

### Installation

I highly recommend using **docker**. For this example I have created a repository 
with all the necessary docker containers. You can find it [here!!!!](https://github.com/Inchie/FlowGraph.Docker).

In this repository I set the following path to the *example application*. Feel free to change 
it (But don't forget to change it in the docker-compose.yaml too).

```bash
 /var/www/graph.app
```

To install this example it's best to use [Composer](https://getcomposer.org). 

- Execute into the docker container with 'docker exec -it graph-php-apache bash'
- Insert the composer.json and composer.lock of this example application in the directory '/var/www/htdocs'
- Finally run the command 'composer install' in the directory /var/www/htdocs

That's it. 

### Open the Application

Now you can open the application with the following url http://172.16.239.27

#### Installation without docker

If you don't want to use docker you have to change the storage settings. You can find them
in the distribution package.


```bash
FlowGraph:
  Neo4j:
    storage:
      protocol: http
      host: 172.16.239.29
      port: 7474
      user: neo4j
      password: test
```

