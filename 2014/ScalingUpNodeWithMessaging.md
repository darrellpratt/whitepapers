# Scaling up Batch Processing using NodeJS, GoLang and RabbitMQ

> Darrell Pratt, Architect Leader, GBS


## Executive Summary

Newer frameworks, including NodeJS are leading the way on conquering I/O bound computing. While this is a great thing for those applications that can most benefit from this concept, traditional data cleansing applications, are a little more difficult to fully utilize available hardware because of this issue. This paper will detail how to use messaging software to scale out NodeJS applications and run through a sample appilcation that makes use of this.

## Problem Statement

NodeJS runs as a single threaded server.  To the experienced Java programmer this sounds a bit like heresy.  Java application servers have had thread management for some time, and the J2EE specs generally address how to handle concurrency in one's application through thread pools, mutlithreaded servlets and the like. NodeJS is an entirely different concept, in that it runs an execution loop, running tasks as they flow from the code into the server. With most APIs being asynchronous, this works great, but when the developer wants to make full use of the multicore servers that are prevalent in the data center, then this concept does not work too well.

## NodeJS Primer

The core tenant of the Node platform is the concept of the non-blocking single threaded event loop.  This might sound like an issue as compared to servers which can spawn and maintain thread pools of very large sizes, but in reality the spawning and maintenance of those thread pools adds overhead in both memory and performance to the servers which use the multi threaded model.  Node, on the other hand allows applications to add events to this loop, which are then executed asynchronously from the main loop and acted upon using the notion of callbacks in the main event loop. (Note that my paper on promises in JavaScript does cover the shift away from callbacks.)



## Fanning out



## Conclusion



[bowerHelp]: https://raw.githubusercontent.com/darrellpratt/b2at/master/client/app/images/bowerHelp.png

[grunt]: https://raw.githubusercontent.com/darrellpratt/b2at/master/client/app/images/grunt.png

[yo1]: https://raw.githubusercontent.com/darrellpratt/b2at/master/client/app/images/yo1.png

[yo2]: https://raw.githubusercontent.com/darrellpratt/b2at/master/client/app/images/yo2.png

[yo3]: https://raw.githubusercontent.com/darrellpratt/b2at/master/client/app/images/yo3.png
