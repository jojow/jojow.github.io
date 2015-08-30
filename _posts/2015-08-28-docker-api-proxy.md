---
layout: post
title: Docker API Proxy
---

I'm working intensively with [Docker](https://www.docker.com) for development, testing, and deployment in my research projects. It does an excellent job there! During the next couple of weeks we run a lab course for students in which they learn modeling and implementing business processes. Each team gets access to a separate VM, which hosts a Docker daemon to run and manage containers. One container runs the business process engine, which is honestly not the most stable and robust one. It's a research prototype. So, Docker with its lightweight container virtualization approach provides a great means to quickly and easily throw away the running container (if the engine breaks or ends up in an inconsistent state) and spin up a fresh one with a well-defined and consistent state.

By default, the [Docker remote API](https://docs.docker.com/reference/api/docker_remote_api) exposes a broad variety of operations to interact with the underlying Docker daemon. However, in the special use case of our lab course we want to restrict what the students can do with their Docker environment (hosted on the institute's infrastructure). Therefore, we implemented the **[Docker API proxy](https://github.com/jojow/docker-api-proxy)** in JavaScript/Node to filter requests based on a simple set of rules. The default configuration only allows to start and stop containers based on images that are already on the server. However, you can easily adapt the filtering logic by customizing the *filter.js* file. Happy filtering! :-)
