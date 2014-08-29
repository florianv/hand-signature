# hand-signature

> Polymer element for hand signatures

## Installation

```bash
$ bower install hand-signature --save
```

## Usage

### Import

```html
<link rel="import" href="hand-signature.html">
```

### Basic

```html
<hand-signature></hand-signature>
```

Adding a title:

```html
<hand-signature>
    <h1>Please sign below</h1>
</hand-signature>
```

### Data binding

In order to get the signature image, you can bind the `data` attribute to a property of your element.
While the user is signing, the property will be updated with the image data encoded in base64.

```html
<polymer-element name="hand-signature-demo">
    <template>
        <hand-signature data="{{signature}}"></hand-signature>
    </template>

    <script>
        Polymer('hand-signature-demo', {
            signatureChanged: function (oldValue, newValue) {
                // The newValue contains the image data
            }
        });
    </script>
</polymer-element>
```

### Attributes

| Attribute       | Description                       | Default
|-----------------|-----------------------------------|---------
| format          | Image format                      | png
| data            | Bound to the image data           | undefined
| width           | Width of the element              | 200px
| height          | Height of the canvas              | 200px
| lineColor       | Line color                        | #212121
| lineJoin        | Line join                         | mitter
| lineWidth       | Line width (in pixels)            | 2
| backgroundColor | Canvas background color           | white
| clearable       | Allow the signature to be cleared | true

## Browser Support

- Chrome 24+
- Internet Explorer 11+
- Firefox 24+
- Safari 6.1+
- Opera 16+

:warning: Mobiles not supported yet

## License

[MIT](https://github.com/florianv/hand-signature/blob/master/LICENSE)
