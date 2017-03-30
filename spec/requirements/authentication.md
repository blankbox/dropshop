# Authentication Requirements

- MUST use JWT
- MUST use SSL/HTTPS for ALL transactions
- May use REST to manage User registration and token requests rather than GraphQL

## JWT

JSON Web Tokens MUST be used. The payload should contain all authentication and permissions required to transact.

JWT should use blacklisting and expiry - in that every token MUST expire, and all tokens that need to be revolked MUST be blacklisted.

The blacklist should use a in memory cache for performance (REDIS for example) but MUST use a persistant method to ensure that list is not lost.

The blacklist should garbage collect those tokens that are expired.

## SSL / HTTPS

Development should be done using SSL and ensure that no transactions can occur over HTTP. All transactions, with not exception, MUST be over HTTPS - or where sockets are used WSS.

## REST

GraphQL is the prefered method of communication, however, if there are valid technical reasons to use REST for the perpose of registering a user or generating a new token - then REST can be used.
