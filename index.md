# Sonata Frontend RFC

## BEM Global Namespaces

All class names should start with the kebab-cased bundle name with the "bundle" suffix removed.
* SonataAdminBundle: `.sonata-admin`
* SonataClassificationBundle: `.sonata-classification`
* SonataMediaBundle: `.sonata-media`
* and so on.

The bundles providing the `sonata-project/admin-bundle-persistency-layer` virtual package
MUST use the sonata-admin namespace.

## Components

* [The Admin List](components/list-view/index.md)
