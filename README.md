# **DEPRECATED** 

The [sockjs-client](https://github.com/sockjs/sockjs-client) project now supports running in node, and supports more transports than this project does. I strongly encourage you to use that instead.

# SockJS Client Node

Node client for [SockJS](https://github.com/sockjs). Currently, only
the XHR Streaming transport is supported.

## Usage

    var sjsc = require('sockjs-client');
    var client = sjsc.create("http://localhost/sjsServer");
    client.on('connection', function () { // connection is established });
    client.on('data', function (msg) { // received some data });
    client.on('error', function (e) { // something went wrong });
    client.write("Have some text you mighty SockJS server!");
