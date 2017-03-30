# Core Interface

- Should be GraphQL
- Should accept secure web sokets in addition to HTTPS

## GraphQL

GraphQL is the prefered interface style. If the learning curve is too steep or it presents too many complications, then GraphQL can  be abandond in exchange for REST.

## Web Sockets

The API can exchange HTTPS for WSS - so long as the web soket module accepts JWT.

Business logic and anciliery code should be built so that it can be consumed by both a web socket type module and a HTTP type module.
