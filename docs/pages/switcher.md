# Switcher

<p class="uk-text-lead">Dynamically transition through different content panes.</p>

## Usage

The switcher component consists of a number of toggles and their related content items. Add the `uk-switcher` attribute to the element which contains the toggles. Add the `.uk-switcher` class to the element containing the content items.

Typically, the switcher is combined with other components, some of which will be shown here.

```html
<!-- This is the nav containing the toggling elements -->
<ul uk-switcher>
    <li><a href=""></a></li>
</ul>

<!-- This is the container of the content items -->
<ul class="uk-switcher">
    <li></li>
</ul>
```

```example
<ul class="uk-subnav uk-subnav-pill" uk-switcher>
    <li><a href="#">Item</a></li>
    <li><a href="#">Item</a></li>
    <li><a href="#">Item</a></li>
</ul>

<ul class="uk-switcher uk-margin">
    <li>Hello!</li>
    <li>Hello again!</li>
    <li>Bazinga!</li>
</ul>
```

***

## Switch items from within content

In some cases you want to switch to another content section from within the active content. This is possible using the `uk-switcher-item` attribute. To target the items, you need to set the attribute to the number of the respective content item.

Setting the attribute to `next` and `previous` will switch to the adjacent items.

```html
<ul class="uk-switcher uk-margin">
    <li>...<a href="" uk-switcher-item="0"></a>...</li>
    <li>...<a href="" uk-switcher-item="1"></a>...</li>
    <li>...<a href="" uk-switcher-item="next"></a>...</li>
    <li>...<a href="" uk-switcher-item="previous"></a>...</li>
</ul>
```

```example
<ul class="uk-subnav uk-subnav-pill" uk-switcher>
    <li><a href="#">Item</a></li>
    <li><a href="#">Item</a></li>
    <li><a href="#">Item</a></li>
</ul>
<ul class="uk-switcher uk-margin">
    <li>Hello! <a href="#" uk-switcher-item="2">Switch to tab 3</a></li>
    <li>Hello again! <a href="#" uk-switcher-item="next">Next tab</a></li>
    <li>Bazinga! <a href="#" uk-switcher-item="previous">Previous tab</a></li>
</ul>
```

***

## Connect multiple items

It is also possible to connect multiple content containers. Just add the `connect` parameter to the `uk-switcher` attribute and target their selectors.

```html
<!-- This is the nav containing the toggling elements -->
<ul uk-switcher="connect: my-class">...</ul>

<!-- These are the containers of the content items -->
<ul class="uk-switcher my-class">...</ul>

<ul class="uk-switcher my-class">...</ul>
```

```example
<ul class="uk-subnav uk-subnav-pill" uk-switcher="connect: .switcher-container">
    <li><a href="#">Active</a></li>
    <li><a href="#">Item</a></li>
    <li><a href="#">Item</a></li>
</ul>
<h4>Container 1</h4>
<ul class="uk-switcher switcher-container uk-margin">
    <li>Hello!</li>
    <li>Hello again!</li>
    <li>Bazinga!</li>
</ul>
<h4>Container 2</h4>
<ul class="uk-switcher switcher-container uk-margin">
    <li>Hello! The first item.</li>
    <li>Hello again! The second item.</li>
    <li>Bazinga! The third item.</li>
</ul>
```

***

## Animations

You can apply all animations from the [Animation component](animation) to switcher items. To do so, add the `animation` parameter with the relevant class to the `uk-switcher` attribute.

```html
<ul uk-switcher="animation: uk-animation-fade">...</ul>
```

```example
<div class="uk-child-width-1-2@s" uk-grid>
    <div>
        <h4>Fade</h4>

        <ul class="uk-subnav uk-subnav-pill" uk-switcher="animation: uk-animation-fade">
            <li><a href="#">Item</a></li>
            <li><a href="#">Item</a></li>
            <li><a href="#">Item</a></li>
        </ul>

        <ul class="uk-switcher uk-margin">
            <li>Hello!</li>
            <li>Hello again!</li>
            <li>Bazinga!</li>
        </ul>
    </div>
    <div>
        <h4>Scale up</h4>

        <ul class="uk-subnav uk-subnav-pill" uk-switcher="animation: uk-animation-scale-up">
            <li><a href="#">Item</a></li>
            <li><a href="#">Item</a></li>
            <li><a href="#">Item</a></li>
        </ul>

        <ul class="uk-switcher uk-margin">
            <li>Hello!</li>
            <li>Hello again!</li>
            <li>Bazinga!</li>
        </ul>
    </div>
    <div>
        <h4>Shake</h4>

        <ul class="uk-subnav uk-subnav-pill" uk-switcher="animation: uk-animation-shake">
            <li><a href="#">Item</a></li>
            <li><a href="#">Item</a></li>
            <li><a href="#">Item</a></li>
        </ul>

        <ul class="uk-switcher uk-margin">
            <li>Hello!</li>
            <li>Hello again!</li>
            <li>Bazinga!</li>
        </ul>
    </div>
    <div>
        <h4>Slide</h4>

        <ul class="uk-subnav uk-subnav-pill" uk-switcher="animation: uk-animation-slide-bottom">
            <li><a href="#">Item</a></li>
            <li><a href="#">Item</a></li>
            <li><a href="#">Item</a></li>
        </ul>

        <ul class="uk-switcher uk-margin">
            <li>Hello!</li>
            <li>Hello again!</li>
            <li>Bazinga!</li>
        </ul>
    </div>
</div>
```

***

### Custom animations

You can also apply multiple animations from the [Animation component](animation). That way you can even create your own custom class to apply a different transition to the switcher.

```html
<ul uk-switcher="animation: uk-animation-fade, uk-animation-slide-left">...</ul>
```

```example
<ul class="uk-subnav uk-subnav-pill" uk-switcher="animation: uk-animation-fade, uk-animation-slide-left">
    <li><a href="#">Item</a></li>
    <li><a href="#">Item</a></li>
    <li><a href="#">Item</a></li>
</ul>

<ul class="uk-switcher uk-margin">
    <li>Hello!</li>
    <li>Hello again!</li>
    <li>Bazinga!</li>
</ul>
```

***

## Switcher with subnavs

The switcher is easily applied to the [Subnav component](subnav).

```html
<!-- This is the subnav containing the toggling elements -->
<ul class="uk-subnav uk-subnav-pill" uk-switcher>...</ul>

<!-- This is the container of the content items -->
<ul class="uk-switcher"></ul>
```

```example
<ul class="uk-subnav uk-subnav-pill" uk-switcher>
    <li><a href="#">Item</a></li>
    <li><a href="#">Item</a></li>
    <li><a href="#">Item</a></li>
</ul>

<ul class="uk-switcher uk-margin">
    <li>Hello!</li>
    <li>Hello again!</li>
    <li>Bazinga!</li>
</ul>
```


***

## Switcher with tabs

As an exception to the rule, add the `uk-tab` attribute instead of `uk-switcher` to the tabbed navigation to combine the switcher with the [Tab component](tab).

```html
<!-- This is the subnav containing the toggling elements -->
<ul uk-tab>...</ul>

<!-- This is the container of the content items -->
<ul class="uk-switcher">...</ul>
```

```example
<ul uk-tab>
    <li><a href="#">Item</a></li>
    <li><a href="#">Item</a></li>
    <li><a href="#">Item</a></li>
</ul>

<ul class="uk-switcher uk-margin">
    <li>Hello!</li>
    <li>Hello again!</li>
    <li>Bazinga!</li>
</ul>
```

***

### Vertical tabs

Use the [Grid](grid) and [Width](width) components to display content correctly with a vertical tabbed navigation.

```html
<div uk-grid>
    <div class="uk-width-auto">
        <ul class="uk-tab-left" uk-tab="connect: #my-id">...</ul>
    </div>
    <div class="uk-width-expand">
        <ul id="my-id" class="uk-switcher">...</ul>
    </div>
</div>
```

```example
<div class="uk-child-width-1-2@s" uk-grid>
    <div>
        <h4>Tab Left</h4>

        <div uk-grid>
            <div class="uk-width-auto@m">
                <ul class="uk-tab-left" uk-tab="connect: #component-tab-left; animation: uk-animation-fade">
                    <li><a href="#">Active</a></li>
                    <li><a href="#">Item</a></li>
                    <li><a href="#">Item</a></li>
                </ul>
            </div>
            <div class="uk-width-expand@m">
                <ul id="component-tab-left" class="uk-switcher">
                    <li>Hello!</li>
                    <li>Hello again!</li>
                    <li>Bazinga!</li>
                </ul>
            </div>
        </div>
    </div>
    <div>
        <h4>Tab Right</h4>

        <div uk-grid>
            <div class="uk-width-auto@m uk-flex-last@m">
                <ul class="uk-tab-right" uk-tab="connect: #component-tab-right; animation: uk-animation-fade">
                    <li><a href="#">Active</a></li>
                    <li><a href="#">Item</a></li>
                    <li><a href="#">Item</a></li>
                </ul>
            </div>
            <div class="uk-width-expand@m">
                <ul id="component-tab-right" class="uk-switcher">
                    <li>Hello!</li>
                    <li>Hello again!</li>
                    <li>Bazinga!</li>
                </ul>
            </div>
        </div>
    </div>
<div>
```

***

## Switcher with buttons

The switcher can also be applied to buttons or button groups from the [Button component](button). Just add the switcher attribute to a block around a group of buttons or to the element with the `.uk-button-group` class.

```html
<!-- This is a switcher using a number of buttons -->
<div uk-switcher>
    <button class="uk-button uk-button-default"></button>
    <button class="uk-button uk-button-default"></button>
</div>

<ul class="uk-switcher">...</ul>

<!-- This is a switcher using a button group -->
<div class="uk-button-group" uk-switcher="connect: #my-id">
    <button class="uk-button uk-button-default"></button>
    <button class="uk-button uk-button-default"></button>
</div>

<ul id="my-id" class="uk-switcher">...</ul>
```

```example
<div class="uk-child-width-1-2@m" uk-grid>
    <div>
        <p uk-switcher="animation: uk-animation-fade">
            <a class="uk-button uk-button-default" href="#">Link</a>
            <button class="uk-button uk-button-default">Button</button>
            <button class="uk-button uk-button-default">Button</button>
        </p>

        <ul class="uk-switcher">
            <li>Hello!</li>
            <li>Hello again!</li>
            <li>Bazinga!</li>
        </ul>
    </div>

    <div>
        <p class="uk-margin-remove">
            <div class="uk-button-group" uk-switcher="connect: #component-button-group; animation: uk-animation-fade">
                <a class="uk-button uk-button-default" href="#">Link</a>
                <button class="uk-button uk-button-default">Button</button>
                <button class="uk-button uk-button-default">Button</button>
            </div>
        </p>

        <ul id="component-button-group" class="uk-switcher">
            <li>Hello!</li>
            <li>Hello again!</li>
            <li>Bazinga!</li>
        </ul>
    </div>
</div>
```


***

## Switcher with navs

To apply the switcher to the [Nav component](nav), add the `uk-switcher` attribute to the nav `<ul>` element. Use the [Grid](grid) and [Width](width) components to arrange nav and content in a grid layout.

```html
<div uk-grid>
    <div class="uk-width-1-3">
        <ul class="uk-nav uk-nav-default" uk-switcher="connect: #my-id">...</ul>
    </div>
    <div class="uk-width-2-4">
        <ul id="my-id" class="uk-switcher">...</ul>
    </div>
</div>
```

```example
<div uk-grid>
    <div class="uk-width-1-3@m">

        <ul class="uk-nav uk-nav-default" uk-switcher="connect: #component-nav; animation: uk-animation-fade; toggle: > :not(.uk-nav-header)">
            <li><a href="#">Active</a></li>
            <li><a href="#">Item</a></li>
            <li><a href="#">Item</a></li>
        </ul>

    </div>
    <div class="uk-width-2-3@m">

        <ul id="component-nav" class="uk-switcher">
            <li>Hello!</li>
            <li>Hello again!</li>
            <li>Bazinga!</li>
        </ul>

    </div>
</div>
```

***

## Component options

| Option      | Value        | Default | Description                                                                                              |
|-------------|--------------|---------|----------------------------------------------------------------------------------------------------------|
| `connect`   | CSS selector | false   | Related item's container. By default, this is the next element with the 'uk-switcher' class.             |
| `toggle `   | CSS selector | > *     | The toggle selector, which triggers content switching on click.                                          |
| `active `   | Number       | 0       | Active index on init. Providing a negative number indicates a position starting from the end of the set. |
| `animation` | String       | false   | The space separated names of animations to use. Comma separate for animation out.                        |
| `duration`  | Number       | 200     | The animation duration.                                                                                  |
| `swiping`   | Boolean      | true    | Use swiping.                                                                                             |