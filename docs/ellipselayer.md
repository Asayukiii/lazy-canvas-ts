# EllipseLayer

The class of the layer that allows to create an ellipse.

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
        <td>setWidth()</td>
        <td>Sets the width of the figure/td>
        <td>number</td>
        <td>true</td>
        <td>-</td>
    </tr>
    <tr>
        <td>setHeight()</td>
        <td>Sets the height of the figure</td>
        <td>number</td>
        <td>true</td>
        <td>-</td>
    </tr>
    <tr>
        <td>setRadius()</td>
        <td>Sets the rounding radius</td>
        <td>number</td>
        <td>true</td>
        <td>IMPORTANT! Use a value no greater than half the value of the smallest side</td>
    </tr>
    <tr>
        <td>setFilled()</td>
        <td>Indicates the presence of filling in the figure</td>
        <td>boolean</td>
        <td>false</td>
        <td>-</td>
    </tr>
    <tr>
        <td>setStroke()</td>
        <td>Sets the line thickness</td>
        <td>number</td>
        <td>false</td>
        <td>Specify only if the fill value is false</td>
    </tr>
    <tr>
        <td>setColor()</td>
        <td>Sets the figure color</td>
        <td>string, Gradient* or Pattern*</td>
        <td>false</td>
        <td>-</td>
    </tr>
</table>

*[Gradient](./gradient.md)
*[Pattern](./pattern.md)

<br>

## Example

```js
const { LazyCanvas, EllipseLayer } = require('@hitomihiumi/lazy-canvas')

let ellipse = new EllipseLayer()
.setX(100)
.setY(100)
.setWidth(300)
.setHeight(200)
.setRadius(100)
.setColor('red')

const lazy = new LazyCanvas()
.addLayers(ellipse)
//...
```