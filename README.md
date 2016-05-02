# Meteor - Stub Collections

## Intro

Easily stub out Meteor collections with in-memory local collections. The idea here is to allow the use of things like Factories for unit tests and styleguides without having to restrict ourselves to making components "pure". So a component (ie. a template) can still call `Widgets.findOne(widgetId)`, it's just that we will have stubbed out `Widgets` to point to a local collection that we can completely control in our test.

## API

- `StubCollections.add([collection1, collection2, ...])` - register the default list of collections to stub.
- `StubCollections.stub()` - stub all collections that have been previously enabled for stubbing via `add()`.
- `StubCollections.stub([collection1, collection2, ...])` - stub a specific list of collections, overriding the list registered via `add()`. 
- `StubCollections.restore()` - undo stubbing (call at the end of tests, on routing away, etc.)

## Examples

See this packages [tests]().

## History

This project was originally created by MDG, and shipped with the [Meteor Guide's](http://guide.meteor.com) [todos](https://github.com/meteor/todos) reference application (thanks MDG!). If you have any questions/comments, open an issue [here](https://github.com/hwillson/meteor-stub-collections/issues).
