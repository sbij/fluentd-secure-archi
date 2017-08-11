# fluentd-secure-archi
Secure fluentd->fluentd architecture with multi-line support and categorization of logs with Docker and Kubernetes.

There are multiple architectures:

* Sender:
  * Docker: For an example, look at [Nginx-fluentd](https://github.com/sbij/fluentd-secure-archi/tree/master/nginxfluentd)
  * Kubernetes: Look at a different repository, you have to use a daemonset: [fluentd-kubernetes-daemonset](https://github.com/sbij/fluentd-kubernetes-daemonset)

* Reciever:
  * Docker Kibana: [
* Docker:
  * Nginx + Fluentd -> Fluentd + Elasticsearch + Kibana
  * Nginx + Fluentd -> Fluentd + Elasticsearch + Graylog
* Kubernetes:
  

With Nginx and Fluentd in one Docker-compose file and Fluentd, Elasticsearch and Kibana or Graylog in another Docker-compose file.

This is made so you can have both instances on two different machines.

And there is a Fluentd instance on both sides so that we can have a secure sending of logs.
