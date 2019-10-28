---
title: "Tiny Http Released"
published: true
excerpt_separator: <!--more-->
repo: defold-tiny-http
tags: [defold, madewithdefold]
---

![defold-tiny-http](/assets/gfx/tiny_http_dark.png){: .fit-image}

Tiny Http Native Extension is a simple http server and client for the Defold Game Engine.

<!--more-->

Main purpose of this extension is simplifying the workflow with the external tools like level editors or IDEs. Reload your level files, change assets on the fly... You can easily trigger almost everything on the running game from everywhere.

This extension build by using [cpp-httplib](https://github.com/yhirose/cpp-httplib). Server runs on separate thread so it is not a blocker. I tested on Mac OS, Win 10 and iOS. It should work on Android too. Server endpoints are definable. You can define your GET/POST endpoints by using regex.

Client is here for simplify things when using Defold. But of course you can use build-in [http requests](https://defold.com/ref/http/). 
Since I don't need it, SSL not supported. But it is possible to add this feature, feel free to PR if you want to.

There is a simple Event ID passing from client to server. Event IDs are passed as header. Main purpose of this to track and group the triggers on the server easily.





