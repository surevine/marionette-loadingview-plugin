marionette-loadingview-plugin
=============================

A plugin for Marionette to add support for a loadingView parameter

This plugin adds support in `CollectionView` for an optional `loadingView` parameter, in the same vein as `emptyView`, which appears when the `CollectionView` is first loaded, before any data has arrived, and which then removes itself when the first item in the collection is added, or when the collection's `sync` event is fired.

```js

NoItemsView = Backbone.Marionette.ItemView.extend({
  template: "#show-no-items-message-template"
});
LoadingItemsView = Backbone.Marionette.ItemView.extend({
  template: "#show-no-items-yet-template"
});

Backbone.Marionette.CollectionView.extend({
  // ...

  emptyView: NoItemsView,
  loadingView: LoadingItemsView
});

```