# NodeInfo2 protocol 1.0

## Status

This document is still in early draft status.

## Definitions

The term "server" in this document refers to software providing metadata about itself on a host.

The term "client" in this document refers to software wishing to retrieve metadata about a host.

The term "schema" refers to a schema definition provided in the schemas subdirectory.

## Document location

Where possible a server should provide a NodeInfo2 document at the endpoint `/.well-known/x-nodeinfo2`.

For [ActivityPub](https://www.w3.org/TR/activitypub/) implementers, an URI to a NodeInfo2 document should be provided in the Actor object as property `nodeInfo2Url`.

## Retrieval

When accessing the metadata document, a client should set the Accept header to the `application/json` media type.

A server must provide the data at least in this media type. A server should set a Content-Type of `application/json`.

When accessing NodeInfo2 documents through an ActivityPub Actor, fetching client should not assume that each document will correspond to a different server. The key `server.baseUrl` should be compared against when collecting statistics of a server. If two NodeInfo2 documents fetched via two different Actor objects have the same `server.baseUrl`, any statistics should be treated as one instead of counting them together.

### baseUrl validation

Consumers should not blindly trust `server.baseUrl` and should always verify it is under the host that was initially called. For example, if a document fetched at host `foobar.local` contains a `server.baseUrl` of `barfoo.local`, it should be rejected.

## Schema

The [schema](https://github.com/jaywink/nodeinfo2/blob/master/schemas/1.0/schema.json) lists required and documented known optional keys.

Due to the versioning of NodeInfo2, which has no version change in forward changes, only major backwards incompatible changes, implementors should be prepared tho deal with situations where a key that has recently been added to the specification doesn't yet exist in all the NodeInfo2 documents created by servers implementing NodeInfo2.

### Data values

Below are some example key values. Using these will ensure interoperability between other nodes using NodeInfo2. Please provide additional items that are common in your implementation to these lists via PR's.

### `server.name`

* `diaspora`
* `friendica`
* `gnusocial`
* `hubzilla`
* `mastodon`
* `mediagoblin`
* `nextcloud`
* `pumpio`
* `redmatrix`
* `socialhome`
* `social-relay`
* `ganggo`
* `wordpress`

### `protocols`

* `activitypub`
* `diaspora`
* `dfrn`
* `libertree`
* `mediagoblin`
* `ostatus`
* `pumpio`
* `webmention`
* `zot`
