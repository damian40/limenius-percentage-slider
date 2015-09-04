# limenius-percentage-slider
Slider for percentages. Or segments that add up to a certain value.

## Usage

Suppose you have a number of input fields in a form and they represent segments of a total (for instance, **percentages** that add up to 100).

    <input id="percentage1" type="text"/>
    <input id="percentage2" type="text"/>
    <input id="percentage3" type="text"/>

Include somewhere `limperslider.js` and `css/limperslider.css`, and create the limperslider object. You can pass it a list of selectors:

    new limperslider(["#percentage1", "#percentage2", "#percentage3"]);

... or a list of HTMLElements, which is useful for instance it the elements are not inserted in the document:

    new limperslider([$("#percentage1")[0], $("#percentage2")[0], $("#percentage3")[0]]);

This code does not need jQuery nor any other library to run. It just uses raw JavaScript (>=IE8) and thus is compatible with AngularJS or whatever environment.

## Options

`new limperslider(selectors, options)` accepts a second argument `options`.

* **options.selector**: Selector where the slider will be inserted.
* **options.element**: HTMLElement where the slider will be inserted.

## RequireJs & AMD compatible

This library is AMD (requirejs) compatible. To use it:

    requirejs.config({
        paths: {
            limperslider: '../somepath/limenius-percentage-slider/limperslider',
            }
       }
    );