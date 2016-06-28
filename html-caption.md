# &lt;caption>

Defines a table caption.

The &lt;caption> tag places a centered caption, above a table. A &lt;caption> is used to explain the purpose of or use of the table. 

## Syntax

The &lt;caption> tag is supported in all browsers and goes back to HTML 4.01. The &lt;caption> tag must be the first descendant of the &lt;table> tag and only one &lt;caption> tag can be used per table. The &lt;caption> tag accepts standard [flow content](https://html.spec.whatwg.org/multipage/dom.html#flow-content-2).

#####Simple
```html
        <caption>caption goes here</caption>
```

#####Advanced
```html
        <caption>
            <p><em>fig 1.</em></p>
            <p>This table describes a ...</p>
        </caption>
```

### Attributes

The &lt;caption> element includes all [global attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes).

####align [*depricated since HTML 4.01*]

`align` can be used to indicate how the caption is to be aligned with the parent `table` and can contain the following values.

- `top` - displayed above the table.
- `bottom` - displayed below the table.
- `left` - displayed to the left of the `table`.
-  `right` - displayed to the right of the table.

** *NOTE: Use CSS to style your &lt;caption> elements**

## Example 1

A simple `table` with a simple `caption` element. Notice that the &lt;caption> element immediately follows the &lt;table> element.

```html
<table>
  <caption>Numbers</caption>
  <tr>
    <td>1</td> <td>2</td> <td>3</td>
  </tr>
  <tr>
    <td>4</td> <td>5</td> <td>6</td>
  </tr>
</table>
```

## Example 2 - Complex

A simple `table` with a much more elaborate `caption` element.

```html
<table>
  <caption><em>table 1.1</em>
    <p>
        This table shows the first 6 <em>six</em> numbers in the 
        <a href="https://en.wikipedia.org/wiki/Arabic_numerals">arabic number system</a>.
    </p>
  </caption>
  <tr>
    <td>1</td> <td>2</td> <td>3</td>
  </tr>
  <tr>
    <td>4</td> <td>5</td> <td>6</td>
  </tr>
</table>
```