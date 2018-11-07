# NodeInfo2

NodeInfo2 is an effort to create a standardized way of exposing metadata about a server. This might be necessary to expose ownership and organization details, usage statistics and protocol capabilities.

## Protocol

Please see the [protocol definition](PROTOCOL.md).

## Versioning

Current version is 1.0. Version upgrade shall happen only in backwards incompatible major changes. Forward changes, ie adding keys will not cause a version upgrading. This means implementors can be guaranteed a stable basic implementation that will not have to be changed all the time.

## Support

Implemented in the following platforms:

* [The Federation.info](https://the-federation.info)
* [Socialhome](https://socialhome.network)
* [Prismo](https://gitlab.com/mbajur/prismo)
* [Juick](https://juick.com/)

Library support is available for the following:

* [Federation](https://github.com/jaywink/federation) (Python)

Have a server or library you have added support to? Send a PR!

## License

All content in this repository is under [CC0](http://creativecommons.org/publicdomain/zero/1.0/) unless otherwise noted.

## Contributing

Please open issues and pull requests if you want to suggest a change. If you open a pull request you agree for your work to be released under CC0.

## History

NodeInfo2 is a fork of [NodeInfo](https://github.com/jhass/nodeinfo) which was seen as too complex for the problem it is solving. NodeInfo2 is interested in controlling *structure* of the document, not content. Additionally, discovery and strict versioning has been dropped for simpler implementation.

NodeInfo emerged from it's predecessor `/statistics.json` that was added to the diaspora* software to be able to built a statistics collection and aggregation service, it was quickly supported by Friendica and RedMatrix. As more and more metadata was added and modifications occurred that would break backward compatibility, we felt the need to make this a more coordinated effort.
