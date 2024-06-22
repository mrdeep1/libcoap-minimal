Minimal CoAP Client and Server Examples for libcoap
===================================================

These examples require [libcoap-3](https://github.com/obgm/libcoap) with a
minimum version of 4.3.2 to compile and execute.

`client.cc` is a minimal libcoap client that sends a confirmable
UDP `GET /hello` request to a pre-defined CoAP server
([coap.me](http://coap.me) in this example) and outputs a received
response. It supports an optional argument which can be a different
CoAP URI to send the request to.  If the host is a multicast address,
then this is handled by a NON-confirmable request.

`server.cc` is a minimal CoAP server that binds on
`::5683`, as well as the multicast IPs 224.0.1.187 and ff02::fd.
It has two defined resources `/hello` and `hello/my` along with the
inbuilt resource `.well-known/core`.

Copyright (C) 2018-2024 Olaf Bergmann <bergmann@tzi.org>

License
=======

This work has been licensed under MIT. See file LICENSE for details.
