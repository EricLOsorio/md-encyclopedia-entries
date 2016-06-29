# top

*Defines where, from the top, to position a positioned element*

The `top` CSS property specifies part of the position of an element. Namely, how far "from the *top*" the element should be placed.

If the element's *position attribute* is set to **absolute** or **fixed** then the "*top*" refers to the distance between the element's top edge of the `margin` and the top edge of the containing block.

If the elements *position attribute* is set to **relative** then, the "*top*" determines how far down to move the element from its normal position.


## Syntax

Introduction to the syntax/usage. A example of CSS syntax is below:

```
    top: <length> | <percentage> | auto | inherit;
```

### Values

This is a CSS example, so each value would need it's own sub-section below.

#### &lt;length>

This value can be positive, negative or null and valid units include: `rem`, `em`, and `px`. Depending on the element's *positioning*,  &lt;length> will represent:

- If the element is *absolutely positioned* the distance to the top edge of the containing block.

- If the element is set to *relative positioning* the distance the element should move down from its normal position.


#### &lt;percentage>

A percentage value based on the containing block's **height**. A valid value is a positive or negative integer followed by `%` symbol. The *positioning* with percentages follows the same guildelines as in &lt;length>

#### auto

The `auto` keyword lets the browser calculate the `top` position. It bases the calculations on the element's `bottom` property.

#### inherit

`inhert` indicates that the value for `top` is the same as the element's containing block.

## Example 1

Setting the `position` to `absolute` will move the element relative to the parent block. The following example will position the element, `#el`, 10px down from the parent block's top edge.

```css
#el{
    position: absolute;
    top: 10px;
}
```

## Example 2

Using `relative` positioning, the following example with move the element, `#el` down 10px from where it would have been in the normal flow.
```css
    #el{
        position: relative;
        top:10px;
```

## Example 3 - Complex

The `top` property is quite simple to understand on its own. It's only when combined with the different *positioning* properties that it becomes much less obvious. To demonstrate how the `top` property reacts to the different `position` properties, let's look at them together and within a larger context. 

In this example we have two elements within a third, parent, element. Using the same `top` property value we can observe the different results of our elements positions.

`#el1` is set to `absolute` positioning, so it is positioned exactly `20px` from the top edge of the `parent` container.

`el2` is set to `relative` positioning so it is positioned 20px down from where it would have been positioned normally.


**HTML**
```html
<div id='parent'>
  Parent Element
  <div id='el1'>Element 1</div>
  <div id='el2'>Element 2</div>
</div>
```

**CSS**
```css
#parent{
  position: relative;
  background-color: #aa8239;
  width: 20em;
  height: 20em;
}

#el1{
  position: absolute;
  top: 20px;
  background-color: #609732;
  width: 5em;
  height: 5em;
}

#el2{
  position: relative;
  top: 20px;
  background-color: #29506d;
  width: 5em;
  height: 5em;
}
    
```
## Special Notes

- If an *absolute* positioned item has no positioned ancestors, it used the document body. In this case the element will scroll with the page, keeping its position on the page.

- `auto` and `inhert` values are calculated. Once the calculation is complete they are handled as if they were a &lt;length> or &lt;percentage>.