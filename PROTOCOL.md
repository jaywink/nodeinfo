# NodeInfo2 protocol 1.0

## Status

This document is still in early draft status.

## Definitions

The term "server" in this document refers to software providing metadata about itself on a host.

The term "client" in this document refers to software wishing to retrieve metadata about a host.

The term "schema" refers to a schema definition provided in the schemas subdirectory.

## Retrieval

A server must provide the metadata document at the endpoint `/.well-known/x-nodeinfo2`.

When accessing the metadata document, a client should set the Accept header to the `application/json` media type.

A server must provide the data at least in this media type. A server should set a Content-Type of `application/json`.

## Structure

Due to the versioning of NodeInfo2, which is no version change in forward changes, only major backwards incompatible changes, implementors should be prepared tho deal with situations where a key that has recently been added to the specification doesn't yet exist in all the NodeInfo2 documents created by servers implementing NodeInfo2.

## Data contents

Known data element values. Using these will ensure interoperatibility between other nodes using NodeInfo2. Please provide additional items that are common in your implementation to these lists via PR's.

### `software.name`

* `diaspora`
* `friendica`
* `hubzilla`
* `redmatrix`
* `socialhome`
* `social-relay`

### `protocols.inbound.items`

* `buddycloud`
* `diaspora`
* `friendica`
* `gnusocial`
* `libertree`
* `mediagoblin`
* `pumpio`
* `zot`
* `smtp`
* `tent`

### `protocols.outbound.items`

* `buddycloud`
* `diaspora`
* `friendica`
* `gnusocial`
* `libertree`
* `mediagoblin`
* `pumpio`
* `redmatrix`
* `smtp`
* `tent`

### `services.inbound.items`

* `appnet`
* `gnusocial`
* `pumpio`

### `services.outbound.items`

* `appnet`
* `blogger`
* `buddycloud`
* `diaspora`
* `dreamwidth`
* `drupal`
* `facebook`
* `friendica`
* `gnusocial`
* `google`
* `insanejournal`
* `libertree`
* `linkedin`
* `livejournal`
* `mediagoblin`
* `myspace`
* `pinterest`
* `posterous`
* `pumpio`
* `redmatrix`
* `smtp`
* `tent`
* `tumblr`
* `twitter`
* `wordpress`
* `xmpp`
