# Middleman-Heroku

`middleman-heroku` is an example on how to use [Middleman] and [Heroku] together. Following the installation you should have Middleman precompiling when pushed to Heroku, then served statically via [Puma].

The only expectation is that `middleman build` will generate your site into `./build` which is where [Rack::TryStatic] will look.

### [Demo](http://middleman-heroku-static-app.herokuapp.com)

## Installation

```
$ git clone http://github.com/middleman/middleman-heroku.git --depth=1 mysite && cd mysite
$ heroku create && git push heroku master
$ heroku open
```

## Configuration

- `/` will try to serve your `build/index.html` file.
- `/foo` will try to serve `build/foo` or `build/foo.html` in that order.
- if a file can't be found it will serve `build/404/index.html`.

## Community

The official community forum is available at: http://forum.middlemanapp.com

## Bug Reports

Github Issues are used for managing bug reports and feature requests. If you run into issues, please search the issues and submit new problems: https://github.com/middleman/middleman-heroku/issues

The best way to get quick responses to your issues and swift fixes to your bugs is to submit detailed bug reports, include test cases and respond to developer questions in a timely manner. Even better, if you know Ruby, you can submit [Pull Requests](https://help.github.com/articles/using-pull-requests) containing Cucumber Features which describe how your feature should work or exploit the bug you are submitting.

## License

Copyright (c) 2012-2014 André Arko. MIT Licensed, see [LICENSE] for details.

[middleman]: http://middlemanapp.com
[heroku]: http://heroku.com
[rack::trystatic]: https://github.com/rack/rack-contrib/blob/master/lib/rack/contrib/try_static.rb
[puma]: http://puma.io
[LICENSE]: https://github.com/middleman/middleman/middleman-heroku/blob/master/LICENSE.md