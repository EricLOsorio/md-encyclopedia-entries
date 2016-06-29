# String.prototype.split()

*A built in method of the String object that divides a String object into substrings.

The `split()` method divides up the current string into an array of substrings based on a suppied seperator.


## Syntax

The `split()` method takes 2 optional parameters and is called directly off of a String object using dot notation.

```javascript
        str.split([seperator, [limit]]);
```

### Parameters


#### seperator

*Optional* A string or regular expression that determines which character(s) when encountered, mark where a string is to be divided. If no seperator is supplied, `split()` returns the whole string back in a single element array. If the seperator is an empty String (`""`), the String is divided into individual characters.

#### limit

An optional integer parameter that limits the number of 'splits' to be found. The string will still be divided based on the `seperator`, however, once the number of times string has been divided reaches the `limit` it will stop.

## Example 1

Often a string is divided into individual words. In this case, we want to split the string using a `space` as the seperator.

```javascript
        "The quick brown fox jumped over the lazy dog.".split(" ");

        //["The", "quick", "brown", "fox", "jumped", "over", "the", "lazy", "dog."]
```

## Example 2

If, for some reason we only wanted to seperate the first three words, we could add a `limit` to our expression.

```javascript
        "The quick brown fox jumped over the lazy dog.".split(" ", 3);
        //["The", "quick", "brown"]
```

## Example 3 - Complex

The `seperator` parameter also handles [regular expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions) which can add a lot of power to our expressions. The following is an example of some irregularly seperated input. Our regular expression, `[,//-]` ,looks for each of the listed `seperators` (, / -) and will divide when it comes across any of them. 

```
        "Kirk,Picard/Janeway-Archer-Sisco".split(/[,//-]/)
```

## Special Notes
It's important to note that `split()` **removes the seperator** from the string. If you wanted to split() a string using capital letters, for example, the capital letter it split on would be removed from the string.