# Adjustty, text resizing
Scale/resize the font-size of texts to fit in its parent element.

## Features
No dependencies
Easy setup
Minimum and maximum font sizes

## Installation
download assets/js/adjustty.min.js and include the script on your page like shown below.

## Usage
Use `adjustty()` as below and pass an element reference or a querySelector. For best performance include the script just before the closing \</body> element.

```HTML
<div class="adjust-text-parent">
    <div class="adjustment-text">The adjusted string by adjustty.</div>
</div>

<script src="adjustty.min.js"></script>
<script>
    adjustty('.adjustment-text');
</script>
```

The following options are available to pass to the adjustty method.
| Option        | Default           | Description  |
| ------------- |:-----------------:| -----:|
| minSize       | 10                | The minimum font size in pixels |
| maxSize       | 25                | The maximum font size in pixels |


You can pass the arguments for minimum and maximum font-size as below.

```javascript
adjustty('.adjustment-text', {
    minSize: 12,
    maxSize: 300,
});
```

## Requirements
The CSS properties of selected elements(to adjust) must have `white-space:nowrap` and `display:inline-block`. If not, the performance of adjustty may be slow by restyling the elements.
<br/>

You can simply apply as below:
```CSS
.adjustment-text {
    display:inline-block;
    white-space:nowrap;
}
```

## Note
The parent element of the selected element(to adjust) must not have horizontal padding the width calculation will make your app's UI broken. For in case, you can simply add the wrapping element to the selected element(to adjust).

```HTML
<!-- Broken UI -->
<div style="padding-left:50px;padding-right:50px;">
    <p class="adjustment-text">I'm the broken text.</p>
</div>
```

```HTML
<!-- Better UI -->
<div style="padding-left:50px;padding-right:50px;">
    <div>
        <p class="adjustment-text">I'm the better text.</p>
    </div>
</div>
```

## Version
1.0.0