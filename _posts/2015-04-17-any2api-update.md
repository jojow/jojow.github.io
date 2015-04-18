---
layout: post
title: Updates on any2api
---

The [any2api](http://any2api.org) framework made some nice progress in the last few months.
As of today, you can generate REST APIs (including a Web-based [API console](https://github.com/mulesoft/api-console)) as well as SOAP/WSDL APIs for arbitrary executables of very different kinds such as Shell scripts, Ruby scripts, Python scripts, and Chef cookbooks.
Further generators and invokers are on their way to continuously broaden the variety of supported APIs and executables.

I'm going to give a talk on any2api at [CLOSER 2015](http://closer.scitevents.org) (5th International Conference on Cloud Computing and Services Science) in May. :-)

There is still a lot of work to do such as optimizing some of any2api's interfaces to better utilize [streams](https://nodejs.org/api/stream.html) to make things faster and more efficient.
Alternative formats to define [API specs](http://www.any2api.org/apispec) such as YAML, XML, and WSDL are also in the making.
