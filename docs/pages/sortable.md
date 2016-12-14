# Sortable

<p class="uk-text-lead">Create sortable grids and lists to rearrange the order of its elements.</p>

Drag and drop an element to a new location within the the sortable grid, while the other items adjust to fit. This is great, if you want to sort items like gallery or menu items, for example.

***

## Usage

To apply this component, add the `uk-sortable` attribute to a container and create child elements.

```html
<div uk-sortable>
    <div></div>
    <div></div>
</div>
```

```example
<ul class="uk-grid-small uk-child-width-1-2@s uk-child-width-1-4@m uk-text-center" uk-sortable="handle: .uk-card" uk-grid>
    <li><div class="uk-card uk-card-default uk-card-body">Item 1</div></li>
    <li><div class="uk-card uk-card-default uk-card-body">Item 2</div></li>
    <li><div class="uk-card uk-card-default uk-card-body">Item 3</div></li>
    <li><div class="uk-card uk-card-default uk-card-body">Item 4</div></li>
    <li><div class="uk-card uk-card-default uk-card-body">Item 5</div></li>
    <li><div class="uk-card uk-card-default uk-card-body">Item 6</div></li>
    <li><div class="uk-card uk-card-default uk-card-body">Item 7</div></li>
    <li><div class="uk-card uk-card-default uk-card-body">Item 8</div></li>
</ul>
```

***

## Handle

By default, the entire sortable element can be used for drag and drop sorting. To create a handle which will be used instead, just add the `handle: SELECTOR` option to the attribute and add the handle class to the element that you want to use as a handle.

```html
<ul uk-sortable="handle: .uk-sortable-handle">
    <li><div class="uk-sortable-handle"></div></li>
</ul>
```

```example
<ul class="uk-grid-small uk-child-width-1-2@s uk-child-width-1-4@m uk-text-center" uk-sortable="handle: .uk-sortable-handle" uk-grid>
    <li><div class="uk-card uk-card-default uk-card-body"><span class="uk-sortable-handle uk-margin-small-right" uk-icon="icon: move"></span>Item 1</div></li>
    <li><div class="uk-card uk-card-default uk-card-body"><span class="uk-sortable-handle uk-margin-small-right" uk-icon="icon: move"></span>Item 2</div></li>
    <li><div class="uk-card uk-card-default uk-card-body"><span class="uk-sortable-handle uk-margin-small-right" uk-icon="icon: move"></span>Item 3</div></li>
    <li><div class="uk-card uk-card-default uk-card-body"><span class="uk-sortable-handle uk-margin-small-right" uk-icon="icon: move"></span>Item 4</div></li>
    <li><div class="uk-card uk-card-default uk-card-body"><span class="uk-sortable-handle uk-margin-small-right" uk-icon="icon: move"></span>Item 5</div></li>
    <li><div class="uk-card uk-card-default uk-card-body"><span class="uk-sortable-handle uk-margin-small-right" uk-icon="icon: move"></span>Item 6</div></li>
    <li><div class="uk-card uk-card-default uk-card-body"><span class="uk-sortable-handle uk-margin-small-right" uk-icon="icon: move"></span>Item 7</div></li>
    <li><div class="uk-card uk-card-default uk-card-body"><span class="uk-sortable-handle uk-margin-small-right" uk-icon="icon: move"></span>Item 8</div></li>
</ul>
```

***

## Group

```example
<div class="uk-child-width-1-3@s uk-grid-match" uk-grid>
    <div>
        <h4>Group 1</h4>
        <div class="uk-text-center" uk-sortable="group: sortable-group">
            <div class="uk-card uk-card-default uk-card-body uk-margin">Item 1</div>
            <div class="uk-card uk-card-default uk-card-body uk-margin">Item 2</div>
            <div class="uk-card uk-card-default uk-card-body uk-margin">Item 3</div>
            <div class="uk-card uk-card-default uk-card-body uk-margin">Item 4</div>
        </div>
    </div>
    <div>
        <h4>Group 2</h4>
        <div class="uk-text-center" uk-sortable="group: sortable-group">
            <div class="uk-card uk-card-default uk-card-body uk-margin">Item 1</div>
            <div class="uk-card uk-card-default uk-card-body uk-margin">Item 2</div>
            <div class="uk-card uk-card-default uk-card-body uk-margin">Item 3</div>
            <div class="uk-card uk-card-default uk-card-body uk-margin">Item 4</div>
        </div>
    </div>
    <div>
        <h4>Empty Group</h4>
        <div class="uk-text-center uk-height-1-1" uk-sortable="group: sortable-group">
    </div>
</div>
```

***

## Custom Class

You can also apply one or more custom classes to items when they are being dragged. To do so, add the `clsCustom: MY-CLASS` option to the attribute.

```html
<ul uk-sortable="clsCustom: my-class">...</ul>
```

Note: In this example, we are using a nav from the [Nav component](nav.md). When dragging an item it will change color and background.

```example
<ul class="uk-nav uk-nav-default uk-width-medium" uk-sortable="clsCustom: uk-background-primary; uk-light">
    <li class="uk-active"><a href="#">Active</a></li>
    <li><a href="#">Item</a></li>
    <li><a href="#">Item</a></li>
    <li><a href="#">Item</a></li>
    <li><a href="#">Item</a></li>
</ul>
```

***

##Component options

| Option           | Value  | Default                 | Description                                   |
|------------------|--------|-------------------------|-----------------------------------------------|
| `group`          | String | ''                      | The group                                     |
| `animation`      | Number | 150                     | The animation duration.                       |
| `threshold`      | Number | 10                      | Mouse move threshold before dragging starts.  |
| `clsItem`        | String | uk-sortable-item        | The item class.                               |
| `clsPlaceholder` | String | uk-sortable-placeholder | The placeholder class.                        |
| `clsDrag`        | String | uk-sortable-drag        | The ghost class.                              |
| `clsDragState`   | String | uk-sortable-dragging    | The body's dragging class.                    |
| `clsBase`        | String | uk-sortable             | The list's class.                             |
| `clsNoDrag`      | String | uk-sortable-nodrag      | Disable dragging on elements with this class. |
| `clsEmpty`       | String | uk-sortable-empty       | The empty list class.                         |
| `clsCustom`      | String | ''                      | The ghost's custom class.                     |
| `handle`         | String | false                   | The handle selector.                          |