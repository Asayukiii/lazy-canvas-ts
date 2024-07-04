# TextLayer

A layer class that allows you to add text, both single line and multi-line text.

Extends [BaseLayer](./baselayer.md)

<br>

<table>
    <tr>
        <td>Method</td>
        <td>Description</td>
        <td>Data type</td>
        <td>Required</td>
        <td>Notes</td>
    </tr>
    <tr>
        <td>setText()</td>
        <td>Sets the displayed text</td>
        <td>string</td>
        <td>true</td>
        <td>-</td>
    </tr>
    <tr>
        <td>setFont()</td>
        <td>Sets the font to be used </td>
        <td>string</td>
        <td>false</td>
        <td>-</td>
    </tr>
    <tr>
        <td>setFontSize()</td>
        <td>Sets the size of the font used</td>
        <td>number</td>
        <td>false</td>
        <td>-</td>
    </tr>
    <tr>
        <td>setWeight()</td>
        <td>Sets the font weight</td>
        <td>string</td>
        <td>false</td>
        <td>Variants: normal, bold, italic, bold italic, regular</td>
    </tr>
    <tr>
        <td>setAlign()</td>
        <td>Sets the text alignment</td>
        <td>string</td>
        <td>false</td>
        <td>Variants: left, center, right, start, end</td>
    </tr>
    <tr>
        <td>setMultiline()</td>
        <td>Switches the text mode to multiline</td>
        <td>boolean</td>
        <td>false</td>
        <td>-</td>
    </tr>
    <tr>
        <td>setWidth()</td>
        <td>Sets the width of the zone in which the multiline and single line text will be located</td>
        <td>number</td>
        <td>false</td>
        <td>-</td>
    </tr>
    <tr>
        <td>setHeight()</td>
        <td>Sets the height of the zone in which the multiline text will be located</td>
        <td>number</td>
        <td>false</td>
        <td>-</td>
    </tr>
    <tr>
        <td>setColor()</td>
        <td>Sets the figure color</td>
        <td>string, Gradient* or Pattern*</td>
        <td>false</td>
        <td>-</td>
    </tr>
    <tr>
        <td>setDirection()</td>
        <td>Sets text direction</td>
        <td>string</td>
        <td>false</td>
        <td>values: ltr, rtl, inherit</td>
    </tr>
    <tr>
        <td>setBaseline()</td>
        <td>Sets the baseline of text</td>
        <td>string</td>
        <td>false</td>
        <td>values: top, hanging, middle, alphabetic, ideographic, bottom</td>
    </tr>
</table>

*[Gradient](./gradient.md)
*[Pattern](./pattern.md)

<br>

![](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text/baselines.png)

<br>

## Example

```js
const { LazyCanvas, TextLayer } = require('@hitomihiumi/lazy-canvas')
//...

// Multiline text
let textOne = new TextLayer()
.setText("This is a test of the LazyCanvas library.")
.setFont("JoeKubert")
.setFontSize(25)
.setWeight("regular")
.setColor("#fff")
.setMultiline(true)
.setX(50)
.setY(50)
.setHeight(100)
.setWidth(500)

// Single line text
let textTwo = new TextLayer()
.setText("Amazing text with amazing font!")
.setFont("Koulen")
.setFontSize(20)
.setWeight("regular")
.setColor("#fff")
.setMultiline(false)
.setAlign("start")
.setX(50)
.setY(130)

const lazy = new LazyCanvas()
.addLayers(textOne, textTwo)
//...
```