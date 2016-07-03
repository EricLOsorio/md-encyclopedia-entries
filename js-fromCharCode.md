
# String.prototype.fromCharCode()

*A built in static method of the String object that creates a string from decimal char codes (Unicode values).*

The `fromCharCode()` method takes in as parameters decimal char code numbers separated by commas and creates a string of characters corresponding to those char codes (Unicode values).

This Method is compatible with all browsers.

## Syntax

The `fromChcarCode()` method takes an unlimited number of parameters and is always called as `String.fromCharCode()`, rather than as the method of a string object that might have been previously created.

```javascript
        String.fromCharCode(num1,......,numN);
```

### Parameters


#### number

The number represents the decimal char code, i.e. Unicode value,

## Example 1

The method will return a string of the decimal unicodes passed as parameters.

```javascript
       String.fromCharCode(65,66,67);  // "ABC"
```

## Example 2

Strings of messages can be created by looking up the decimal char codes

```javascript
       String.fromCharCode(72,69,76,76,79,33);  // "HELLO!"
```

## Example 3 - Complex

Special character char codes can be included such as carriage return and horizontal tab

```
       String.fromCharCode(72,69,76,76,79,33,9,45,69,82,73,67,13,72,73,33,9,45,75,65,84);  // "HELLO! -ERIC
                                                                                          // HI!  -KAT"
```

## Special Notes
Copy of Unicode table can be found here: http://unicode-table.com/en/#control-character 

As noted in the Mozilla Developer Network site: https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/String/fromCharCode 

"Although most common Unicode values can be represented with one 16-bit number (as expected early on during JavaScript standardization) and fromCharCode() can be used to return a single character for the most common values (i.e., UCS-2 values which are the subset of UTF-16 with the most common characters), in order to deal with ALL legal Unicode values (up to 21 bits), fromCharCode() alone is inadequate. Since the higher code point characters use two (lower value) "surrogate" numbers to form a single character, String.fromCodePoint() (part of the ES6 draft) can be used to return such a pair and thus adequately represent these higher valued characters."
