# url_strategy [![Pub version](https://img.shields.io/pub/v/url_strategy.svg)](https://pub.dev/packages/url_strategy) [![Twitter Follow](https://img.shields.io/twitter/follow/creativemaybeno?label=Follow&style=social)](https://twitter.com/creativemaybeno) 

Package for Flutter apps that allows setting the web URL strategy with a single line of code.

## Usage

See the [`url_strategy` package README](https://github.com/creativecreatorormaybenot/url_strategy/tree/master/url_strategy)
for usage documentation.

## Implementation

The package is basically a wrapper around the [`flutter_web_plugins`](https://github.com/flutter/flutter/tree/master/packages/flutter_web_plugins)
`setUrlStrategy`. The reason it exists is that using the function from `flutter_web_plugins`
requires conditional imports.  
The problem is solved by using a conditional export from the `url_strategy` package.
