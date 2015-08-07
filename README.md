# logstash_openstack

This assumes you already have a logstash server.  [This](https://www.digitalocean.com/community/tutorials/how-to-install-elasticsearch-logstash-and-kibana-4-on-ubuntu-14-04) is a great guide.

### server


### agents
install logstash-forwarder:

* `echo 'deb http://packages.elasticsearch.org/logstashforwarder/debian stable main' | sudo tee /etc/apt/sources.list.d/logstashforwarder.list`
* `wget -O - http://packages.elasticsearch.org/GPG-KEY-elasticsearch | sudo apt-key add -`
* `sudo apt-get update`
* `sudo apt-get install logstash-forwarder`


install logstash-forwarder.conf and start the agent:

* `curl -sO https://raw.githubusercontent.com/b225ccc/logstash_openstack/master/logstash-forwarder.conf`
* `/opt/logstash-forwarder/bin/logstash-forwarder -config logstash-forwarder.conf`
