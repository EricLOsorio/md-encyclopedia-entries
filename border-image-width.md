
# border-image-width

*border-image-width is a CSS property that specifies the width of the border image*

An image can be used as a border to surround an HTML element, instead of using one of the standard borders consising of, for example, solid or dashed lines of a specified color and width. When an image is used as a border, the border-image-width is used to specify the width of that image around the element.


## Syntax

Introduction to the syntax/usage. A example of CSS syntax is below:

```
        border-image-width: number| % | auto | initial | inherit;
```

### Values

#### number

The number value can be one of 3 choices:
        • A number with pixel units defined the width in pixels, i.e. `px` after the number
        • A number by itself, no unix suffix, which represents multiples of the default border-image-width.
          The default is 1, so a value of `2` would make the border-image-width twice as wide as the origina

#### %
        • The `%` sign after the number, represents the percentage of the area being enclosed
          by the border image that the border itself will take. If it is not used, then the number will be either followed by
          `px` or will be by itself
#### auto

The `auto` value will display the intrinsic width or height of the corresponding image slice. So, what this means is taht when  specified, the auto settings will use whatever the number is specified for the border-image-slice property and use that as the horizontal and vertical widths in px units.

#### initial

This value sets the property to its default value, which is 1.

#### inherit
This value makes the border-image-width inherit the value from the parent element

## Example 1

There isn't much to using this CSS property, just the property followed by the number of pixels as below

```
          border-image-width: 20px;
```

## Example 2

Or, specifying the property as a multiple of an original width of 1, as below:

```
            border-image-width: 3;
```

## Example 3 - Complex

Or specifying the value as a percentage of the

```
           border-image-width: 30% 15% 5% 10%;
```

## Special Notes
The complex example above demonstrates that if only one number is used to specify the border-image-width, then that means that the value will apply to both the horizontal and the vertical components of the image, however, if two or more numbers are used, then the following rules apply:

If two values are used:
first value will apply to the top and bottom horizontal borders, 
the second value will apply to the right and left vertical borders

If three values are used:
first value will apply to the top and bottom horizontal borders, 
the second value will apply to the right and left vertical borders
the third value will apply to the bottom horizontal border

If four values are used:
first value will apply to the top horizontal border, 
the second value will apply to the right vertical borders
the third value will apply to the bottom horizontal border
the fourth value will apply to the left vertical border
