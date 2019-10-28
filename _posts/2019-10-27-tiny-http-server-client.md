---
title: "Tiny Http Released"
published: true
excerpt_separator: <!--more-->
repo: defold-tiny-http
tags: [defold, madewithdefold]
---

![defold-tiny-http](/assets/gfx/tiny_http_dark.png){: .fit-image}

[Tiny Http](https://github.com/selimanac/defold-tiny-http) - Defold Native Extension is a simple http server and client for the Defold Game Engine.

<!--more-->

Main purpose of this extension is simplifying workflow with the external tools like level editors or IDEs. Reload your level files, change assets on the fly... You can easily trigger almost everything on the running game from everywhere.

<iframe width="560" height="315" src="https://www.youtube.com/embed/Joxp3cJadxI" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Server runs on separate thread so it is not a blocker. I tested on Mac OS, Win 10 and iOS. It should work on Android too. Client has a thread pool. But timeouts may block the UI for 5 sec.

Server [endpoints](https://github.com/selimanac/defold-tiny-http#endpoints) are definable. You can add your GET/POST [endpoints](https://github.com/selimanac/defold-tiny-http#endpoints) by using regex.

Client is here to simplify things when using Defold. But of course you can use build-in [http requests](https://defold.com/ref/http/). 

<iframe width="560" height="315" src="https://www.youtube.com/embed/smx5nbnTHQs" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

There is a simple Event ID passing from client to server. Event IDs are passed as header. Main purpose of this to track and group the triggers at the server easily.

If you want to use build-in http and Event-IDs, you can simply pass it like this:

```lua

local headers = {
    ["Event-ID"] = "1"
}

http.request("http://127.0.0.1:8800/monster/1", "GET", http_result, headers)

```

Or for Curl:

```Shell

curl --header \"Event-ID: 1\" http://localhost:8800/monster/1

```

<iframe width="560" height="315" src="https://www.youtube.com/embed/5G8O6dzLoVM" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Since I don't need it, SSL not supported. But it is [possible](https://github.com/yhirose/cpp-httplib#openssl-support) to add this feature, feel free to PR if you want to. 

This extension build by using [cpp-httplib](https://github.com/yhirose/cpp-httplib).





