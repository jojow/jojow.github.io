---
layout: post
title: Gateway for Docker API Proxy
---

The [Docker API proxy](https://github.com/jojow/docker-api-proxy) now supports the usage of an external gateway to make container ports available to the outside world through reverse SSH tunneling. This is motivated by a specific use case we had in our labs setup: The entire environment including the Docker engine is running on a machine, which sits behind a firewall. As a result, containers that expose endpoints through specific ports cannot be accessed directly. Therefore, we are running a small virtual server (the gateway) at a public cloud provider. The Docker API proxy transparently configures the SSH tunneling in the background when containers are started and stopped by managing corresponding SSH connections to the gateway server. Containers can expose their functionality to the outside world this way without changing the firewall configuration.
