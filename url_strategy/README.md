# url_strategy [![GitHub stars](https://img.shields.io/github/stars/simpleclub/url_strategy.svg)](https://github.com/simpleclub/url_strategy)

Package for Flutter apps that allows setting the web URL strategy with a single line of code.

## Usage

To use this plugin, follow the [installing guide](https://pub.dev/packages/url_strategy/install).

### Setting the URL strategy

If you want to remove the leading hash (`#`) from the URL of your Flutter web app, you can simply
call `setPathUrlStrategy` in the `main` function of your app:

```dart
import 'package:url_strategy/url_strategy.dart';

void main() {
  // Here we set the URL strategy for our web app.
  // It is safe to call this function when running on mobile or desktop as well.
  setPathUrlStrategy();
  runApp(MyApp());
}
```

Now, your Flutter web app will not have a leading `#` in the URL anymore.

It is safe to call the function even when running on any other platform than web (which is the point
of this package). That means that you can safely call `setPathUrlStrategy` when running on mobile
or desktop - it will simply be a noop.

#### Base

Make sure that you have `<base href="/">` included inside the `<head>` section of your
`web/index.html` if you want to use the path URL strategy.  
This is included by default when you create a new Flutter project.

Furthermore, you need to ensure that your production HTTP server always serves your `web/index.html`
file for all paths.

See [this more detailed StackOverflow answer][answer] for more information.

#### Hash strategy

You can also use a hash URL strategy instead (which is the default) by calling `setHashUrlStrategy`.

[answer]: https://stackoverflow.com/a/65709246/6509751
