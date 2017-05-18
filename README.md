# kolla
Kolla can build and deploy Docker containers.

## Setting up Kolla using Vagrant environment ("all-in-one" deployment)

## Kolla notes
* Kolla provides production-ready containers and deployment tools for operating OpenStack clouds that are scalable, fast, reliable, and upgradable using community best practices.
* Kolla provides Docker containers, Ansible playbooks to deploy OpenStack on baremetal or virtual machine, and Kubernetes templates to deploy OpenStack on Kubernetes to meet Kolla's mission.
* Kolla provides images to deploy the following infrastructure components:
1. Ceph implementation for Cinder, Glance and Nova
2. Collectd, InfluxDB, and Grafana for performance monitoring.
3. Elasticsearch and Kibana to search, analyze, and visualize log messages.
4. Etcd a distributed key value store that provides a reliable way to store data across a cluster of machines.
5. Fluentd as an open source data collector for unified logging layer.
6. HAProxy and Keepalived for high availability of services and their endpoints.
7. Kafka A distributed streaming platform.
8. MariaDB and Galera Cluster for highly available MySQL databases.
9. Memcached a distributed memory object caching system.
10. MongoDB as a database back end for Ceilometer and Gnocchi.
11. Open vSwitch and Linuxbridge back ends for Neutron.
12. RabbitMQ as a messaging back end for communication between services.
13. Telegraf as a plugin-driven server agent for collecting & reporting metrics.
* Two container-focused OpenStack projects, Magnum and Kolla, have evolved significantly through the Kilo development cycle. Kolla formed shortly before the Kilo Design Summit, while Magnum was created shortly afterward. Both projects use Docker for containers, but leverage the technology for different purposes. Magnum is a Container-as-a-Service (CaaS) system, allowing users to build and run container-based applications in OpenStack clouds, while Kolla.s mission is to simplify the OpenStack operational experience.
* Kolla improves OpenStack operations by containerizing OpenStack into micro services and providing additional tooling to simplify management. Containerizing OpenStack services improves operations such as providing deployment consistency, simplified upgrades, portability, scaling, etc.. These capabilities are achieved by encompassing the entire application runtime for each OpenStack service into a lightweight, portable unit. Each micro service becomes an atomic unit of management such as deployment, upgrading, scaling, etc. Kolla was developed as an integration project, allowing other tools such as TripleO, Heat, Ansible, etc.. to manage OpenStack at scale using Docker containers.
* Magnum is an API service developed for OpenStack to make container management tools such as Docker, Kubernetes, etc. available as first class resources in OpenStack. Magnum uses Heat to orchestrate an operating system image that includes the container management tools and runs the image in a Nova instance cluster. Magnum is meant to launch a minimalistic host operating system such as Fedora Atomic, CoreOS, or Ubuntu Snappy. The operating system includes enough tools to launch Docker, Kubernetes, etc.. Once the operating system is launched, Magnum configures the  clusters to run a Container Orchestration Environment for multi-tenancy.
