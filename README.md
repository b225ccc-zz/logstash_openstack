# logstash_openstack

This assumes you already have a logstash server.  [This](https://www.digitalocean.com/community/tutorials/how-to-install-elasticsearch-logstash-and-kibana-4-on-ubuntu-14-04) is a great guide.

### server


### agents
install logstash-forwarder:

* `wget https://download.elastic.co/logstash-forwarder/binaries/logstash-forwarder_0.4.0_amd64.deb`
* `sudo dpkg -i logstash-forwarder_0.4.0_amd64.deb`
* `sudo apt-get install -f`

install logstash-forwarder.conf and start the agent:

* `/opt/logstash-forwarder/bin/logstash-forwarder -config logstash-forwarder.conf`
