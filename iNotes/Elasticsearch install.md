
https://www.elastic.co/guide/en/elasticsearch/reference/current/deb.html
Check available versions.
```
apt-cache showpkg elasticsearch
```

```
wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-8.15.2-amd64.deb
sudo dpkg -i elasticsearch-8.15.2-amd64.deb
```

```
wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-8.15.2-amd64.deb.sha512
shasum -a 512 -c elasticsearch-8.15.2-amd64.deb.sha512  
```

install specific version
```
apt-get install elasticsearch=7.10.0
```

how to check elastic search version on your system
```
curl -X GET 'http://localhost:9200'
```

Check Elasticsearch status----
```
sudo /etc/init.d/elaticsearch status
```

If you want to set fix memory to Elasticsearch ----
> So please edit this file-----
```  
vi /etc/elaticsearch/jvm.options
```

```
#Xms4g
#Xms4g 
```

after edit this file restart Elasticsearch service
```
sudo /etc/init.d/elaticsearch start
```


- New versions of Elasticsearch  configurations.
```
vi /etc/elasticsearch/elasticsearch.yml 
```

```
======================== Elasticsearch Configuration =========================
#
# NOTE: Elasticsearch comes with reasonable defaults for most settings.
#       Before you set out to tweak and tune the configuration, make sure you
#       understand what are you trying to accomplish and the consequences.
#
# The primary way of configuring a node is via this file. This template lists
# the most important settings you may want to configure for a production cluster.
#
# Please consult the documentation for further information on configuration options:
# https://www.elastic.co/guide/en/elasticsearch/reference/index.html
#
# ---------------------------------- Cluster -----------------------------------
#
# Use a descriptive name for your cluster:
#
#cluster.name: my-application
#
# ------------------------------------ Node ------------------------------------
#
# Use a descriptive name for the node:
#
#node.name: node-1
#
# Add custom attributes to the node:
#
#node.attr.rack: r1
#
# ----------------------------------- Paths ------------------------------------
#
# Path to directory where to store the data (separate multiple locations by comma):
#
path.data: /var/lib/elasticsearch
#
# Path to log files:
#
path.logs: /var/log/elasticsearch
#
# ----------------------------------- Memory -----------------------------------
#
# Lock the memory on startup:
#
#bootstrap.memory_lock: true
#
# Make sure that the heap size is set to about half the memory available
# on the system and that the owner of the process is allowed to use this
# limit.
#
# Elasticsearch performs poorly when the system is swapping the memory.
#
# ---------------------------------- Network -----------------------------------
#
# By default Elasticsearch is only accessible on localhost. Set a different
# address here to expose this node on the network:
#
network.host: localhost
#
# By default Elasticsearch listens for HTTP traffic on the first free port it
# finds starting at 9200. Set a specific HTTP port here:
#
http.port: 9200
#
# For more information, consult the network module documentation.
#
# --------------------------------- Discovery ----------------------------------
#
# Pass an initial list of hosts to perform discovery when this node is started:
# The default list of hosts is ["127.0.0.1", "[::1]"]
#
#discovery.seed_hosts: ["host1", "host2"]
#
# Bootstrap the cluster using an initial set of master-eligible nodes:
#
#cluster.initial_master_nodes: ["node-1", "node-2"]
#
# For more information, consult the discovery and cluster formation module documentation.
#
# ---------------------------------- Various -----------------------------------
#
# Allow wildcard deletion of indices:
#
#action.destructive_requires_name: false

#----------------------- BEGIN SECURITY AUTO CONFIGURATION -----------------------
#
# The following settings, TLS certificates, and keys have been automatically      
# generated to configure Elasticsearch security features on 02-12-2024 06:27:19
#
# --------------------------------------------------------------------------------

# Enable security features
xpack.security.enabled: false

xpack.security.enrollment.enabled: false

# Enable encryption for HTTP API client connections, such as Kibana, Logstash, and Agents
xpack.security.http.ssl:
  enabled: true
  keystore.path: certs/http.p12

# Enable encryption and mutual authentication between cluster nodes
xpack.security.transport.ssl:
  enabled: true
  verification_mode: certificate
  keystore.path: certs/transport.p12
  truststore.path: certs/transport.p12
# Create a new cluster with the current node only
# Additional nodes can still join the cluster later
cluster.initial_master_nodes: ["rahul189"]

# Allow HTTP API connections from anywhere
# Connections are encrypted and require user authentication
http.host: 0.0.0.0

# Allow other nodes to join the cluster from anywhere
# Connections are encrypted and mutually authenticated
#transport.host: 0.0.0.0

#----------------------- END SECURITY AUTO CONFIGURATION -------------------------

```

- If you facing this type issue
```
root@shorya186:~# curl -X GET 'http://localhost:9200
curl: (52) Empty reply from server
```
so go to the file .
```
vi /etc/elasticsearch/elasticsearch.yml
```
and false this `xpack.security`.
```
xpack.security.enabled: false
xpack.security.enrollment.enabled: false #turn these to false
```
- `elasticsearch.yml` file.
```
# ======================== Elasticsearch Configuration =========================
#
# NOTE: Elasticsearch comes with reasonable defaults for most settings.
#       Before you set out to tweak and tune the configuration, make sure you
#       understand what are you trying to accomplish and the consequences.
#
# The primary way of configuring a node is via this file. This template lists
# the most important settings you may want to configure for a production cluster.
#
# Please consult the documentation for further information on configuration options:
# https://www.elastic.co/guide/en/elasticsearch/reference/index.html
#
# ---------------------------------- Cluster -----------------------------------
#
# Use a descriptive name for your cluster:
#
#cluster.name: my-application
#
# ------------------------------------ Node ------------------------------------
#
# Use a descriptive name for the node:
#
#node.name: node-1
#
# Add custom attributes to the node:
#
#node.attr.rack: r1
#
# ----------------------------------- Paths ------------------------------------
#
# Path to directory where to store the data (separate multiple locations by comma):
#
path.data: /var/lib/elasticsearch
#
# Path to log files:
#
path.logs: /var/log/elasticsearch
#
# ----------------------------------- Memory -----------------------------------
#
# Lock the memory on startup:
#
#bootstrap.memory_lock: true
#
# Make sure that the heap size is set to about half the memory available
# on the system and that the owner of the process is allowed to use this
# limit.
#
# Elasticsearch performs poorly when the system is swapping the memory.
#
# ---------------------------------- Network -----------------------------------
#
# By default Elasticsearch is only accessible on localhost. Set a different
# address here to expose this node on the network:
#
#network.host: 192.168.0.1
#
# By default Elasticsearch listens for HTTP traffic on the first free port it
# finds starting at 9200. Set a specific HTTP port here:
#
#http.port: 9200
#
# For more information, consult the network module documentation.
#
# --------------------------------- Discovery ----------------------------------
#
# Pass an initial list of hosts to perform discovery when this node is started:
# The default list of hosts is ["127.0.0.1", "[::1]"]
#
#discovery.seed_hosts: ["host1", "host2"]
#
# Bootstrap the cluster using an initial set of master-eligible nodes:
#
#cluster.initial_master_nodes: ["node-1", "node-2"]
#
# For more information, consult the discovery and cluster formation module documentation.
#
# ---------------------------------- Various -----------------------------------
#
# Allow wildcard deletion of indices:
#
#action.destructive_requires_name: false

#----------------------- BEGIN SECURITY AUTO CONFIGURATION -----------------------
#
# The following settings, TLS certificates, and keys have been automatically      
# generated to configure Elasticsearch security features on 24-12-2024 13:58:14
#
# --------------------------------------------------------------------------------

# Enable security features
xpack.security.enabled: false

xpack.security.enrollment.enabled: false

# Enable encryption for HTTP API client connections, such as Kibana, Logstash, and Agents
xpack.security.http.ssl:
  enabled: true
  keystore.path: certs/http.p12

# Enable encryption and mutual authentication between cluster nodes
xpack.security.transport.ssl:
  enabled: true
  verification_mode: certificate
  keystore.path: certs/transport.p12
  truststore.path: certs/transport.p12
# Create a new cluster with the current node only
# Additional nodes can still join the cluster later
cluster.initial_master_nodes: ["shorya186"]

# Allow HTTP API connections from anywhere
# Connections are encrypted and require user authentication
http.host: 0.0.0.0

# Allow other nodes to join the cluster from anywhere
# Connections are encrypted and mutually authenticated
#transport.host: 0.0.0.0

#----------------------- END SECURITY AUTO CONFIGURATION -------------------------

```


*Add this line in opensearch installation*
```
vi /etc/opensearch/opensearch.yml
```

``` shell
plugins.security.ssl.http.enabled: false
plugins.security.disabled: true
```

### Elasticsearech setup with docker HTTPS and HTTP.

1. Hardened Docker images
edit
You can also use the hardened Wolfi image for additional security. Using Wolfi images requires Docker version 20.10.10 or higher.

To use the Wolfi image, append -wolfi to the image tag in the Docker command.

``` shell
docker pull docker.elastic.co/elasticsearch/elasticsearch-wolfi:8.17.1
```

1.1. Start an Elasticsearch container.
``` shell 
docker run --name elasticsearch --net elastic -p 9200:9200 -it -m 512MB docker.elastic.co/elasticsearch/elasticsearch-wolfi:8.17.1
```
1.2.  SSL Encryption and Authentication can also be disabled via ENV variables. If you start a container with the following both are disabled.
``` shell
docker run -d --name elasticsearch01 --net elastic -p 9200:9200 -e "discovery.type=single-node" -e "xpack.security.http.ssl.enabled=false" -e "xpack.security.enabled=false" -e "xpack.security.enrollment.enabled=false" -m 512MB docker.elastic.co/elasticsearch/elasticsearch-wolfi:8.17.1
```
1.3 SSL Encryption and Authentication can also be disabled via ENV variables. If you start a container with the following both are disabled and always restart policy.
``` shell
docker run -d --name elasticsearch01 --restart always --net elastic -p 9200:9200 -e "discovery.type=single-node" -e "xpack.security.http.ssl.enabled=false" -e "xpack.security.enabled=false" -e "xpack.security.enrollment.enabled=false" -m 512MB docker.elastic.co/elasticsearch/elasticsearch-wolfi:8.17.1
```

- -d is for detached mode (run the container in the background).
- -it is for interactive mode (to allow interaction with the container's terminal).
You shouldn't use both -d and -it together, as they conflict. If you're running the container in detached mode (in the background), you don't need the -it flag.

*Note: After you run this command with out `-d` flag you get elasticsearch username, password and HTTP CA certificate*
``` shell
----------------------------------------------------------------------------------------------------
? Elasticsearch security features have been automatically configured!
? Authentication is enabled and cluster connections are encrypted.

??  Password for the elastic user (reset with `bin/elasticsearch-reset-password -u elastic`):
  0sdAJ=lLrr0ogGwBO2vD

??  HTTP CA certificate SHA-256 fingerprint:
  617719cb41234da98f56f2643efa781f01ace6295a4e753e9dbf70c0f90e1419

??  Configure Kibana to use this cluster:
? Run Kibana and click the configuration link in the terminal when Kibana starts.
? Copy the following enrollment token and paste it into Kibana in your browser (valid for the next 30 minutes):
  eyJ2ZXIiOiI4LjE0LjAiLCJhZHIiOlsiMTcyLjE4LjAuMjo5MjAwIl0sImZnciI6IjYxNzcxOWNiNDEyMzRkYTk4ZjU2ZjI2NDNlZmE3ODFmMDFhY2U2Mjk1YTRlNzUzZTlkYmY3MGMwZjkwZTE0MTkiLCJrZXkiOiJPWFhHa1pRQnRuTXR3Rk1pbU8tSjo2cC1aNDNGd1NRNmdCbDI1XzBYcmZ3In0=

?? Configure other nodes to join this cluster:
? Copy the following enrollment token and start new Elasticsearch nodes with `bin/elasticsearch --enrollment-token <token>` (valid for the next 30 minutes):
  eyJ2ZXIiOiI4LjE0LjAiLCJhZHIiOlsiMTcyLjE4LjAuMjo5MjAwIl0sImZnciI6IjYxNzcxOWNiNDEyMzRkYTk4ZjU2ZjI2NDNlZmE3ODFmMDFhY2U2Mjk1YTRlNzUzZTlkYmY3MGMwZjkwZTE0MTkiLCJrZXkiOiJPM1hHa1pRQnRuTXR3Rk1pbU8tTDpiVlRoZmVMalF3V19qOXpGdWJfdFF3In0=

  If you're running in Docker, copy the enrollment token and run:
  `docker run -e "ENROLLMENT_TOKEN=<token>" docker.elastic.co/elasticsearch/elasticsearch:8.17.1`
```

1.4.  Copy the http_ca.crt SSL certificate from the container to your local machine.
``` shell
wadmin@wadmin34:~$ docker cp elasticsearch:/usr/share/elasticsearch/config/certs/http_ca.crt .
```
output-
```
Successfully copied 3.58kB to /home/wadmin/.
```
1.5.  Make a REST API call to Elasticsearch to ensure the Elasticsearch container is running.
syntax: `curl --cacert http_ca.crt -u elastic:$ELASTIC_PASSWORD https://localhost:9200` 
``` shell
curl --cacert http_ca.crt -u elastic:0sdAJ=lLrr0ogGwBO2vD https://localhost:9200
```

