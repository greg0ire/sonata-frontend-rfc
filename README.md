# Sonata Project's Frontend RFC

## Rationale

The [Sonata Project](http://sonata-project.org) is the most popular CRUD admin interface for the Symfony Framework.

Although very well architectured on the PHP level, the current situation regarding it's client-side user interface leaves much to be desired.

The Sonata frameworks gather a lot of data and metadata under the hood, which is just thrown away after the view is sent to the client.

This makes the creation of customized, dynamic, rich user interfaces much harder than it should be.
In order to pass data to the client-side, developers often need to override a fair amount of templates, write inline javascript, inline css, and other atrocities.
The resulting applications are likely to break on each minor Sonata update, which in turns makes each minor change in the templates a possible BC break for the Sonata core developers.

The purpose of this RFC is therefore to establish conventions, in order to enable:

* sonata core developers to consistently markup their views across all the project's bundle.
* sonata core developers to consistently pass data to the client-side, across all the project's bundle.
* sonata users to easily customize the style & behavior of existing user-interface components.
* sonata users to easily create new user-interface components.


The [RFC](index.md)
