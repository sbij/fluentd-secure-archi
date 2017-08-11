# fluentd-secure-archi
Secure fluentd to fluentd architecture with multi-line support and categorization of logs with Docker and Kubernetes.

There are multiple architectures:

* Sender:
  * Docker: For an example, look at [Nginx-fluentd](https://github.com/sbij/fluentd-secure-archi/tree/master/nginx-fluentd)
  * Kubernetes: Look at a different repository, you have to use a "Normal version" daemonset: [fluentd-kubernetes-daemonset](https://github.com/sbij/fluentd-kubernetes-daemonset)

* Reciever:
  * Docker Kibana: [fluentd-elasticsearch-kibana](https://github.com/sbij/fluentd-secure-archi/tree/master/fluentd-elasticsearch-kibana)
  * Docker Graylog: [fluentd-elasticsearch-graylog](https://github.com/sbij/fluentd-secure-archi/tree/master/fluentd-elasticsearch-graylog)
  * Kubernetes Kibana: [efk-k8s-charts](https://github.com/sbij/efk-k8s-charts) (it is by default packed with the Kubernetes daemonset, that you can disable in ```central-logging/requirements.yaml```.
  

With Nginx and Fluentd in one Docker-compose file and Fluentd, Elasticsearch and Kibana or Graylog in another Docker-compose file.

This is made so you can have both instances on two different machines.

And there is a Fluentd instance on both sides so that we can have a secure sending of logs.
