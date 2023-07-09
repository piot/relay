# Relay

A simplified datagram relay system. Is designed for internal development and testing, not for production use.

It consists of the following libraries:

* [relay-serialize-c](https://github.com/piot/relay-serialize-c). Serialization of the protocol.
* [relay-server-lib](https://github.com/piot/relay-server-lib). Server library. Can be embedded in another application. Depends on:
  * [guise-session-client-c](https://github.com/piot/guise-session-client-c). Used for authentication for the connecting users (Verify Guise User Session IDs). 
* [relay-daemon](https://github.com/piot/relay-daemon). Daemon used for deploying. Depends on:
  * [guise-client-c](https://github.com/piot/guise-client-c). for authentication of the relay-daemon itself.
    * [udp-client-c](https://github.com/piot/udp-client-c). for guise-session-client-c and guise-client-c.
  * [udp-server-c](https://github.com/piot/udp-server-c). receiving and sending UDP datagrams.
* [relay-client-c](https://github.com/piot/relay-client-c). The client library that can request listen, connect and send and receive datagrams.

Check out the details of the [relay protocol](https://github.com/piot/relay-serialize-c/blob/main/docs/index.adoc).
