# CSS Basics

## Introduction to CSS

* CSS is used to style an HTML page and the corresponding elements
* CSS file has 2 parts:
    1. Selector
    2. Declaration Block
* Declarations are made in property / value pairs where the property selects the type and the value changes the value
* A CSS rule set has a selector part and a declaration
    * Ex.
    ```
    p {
        font-size: 20px;
    }
    ```
* Can select more than one tag at a time
* For classes use "." before name
    * Ex.
    ```
    .my-class {

    }
    ```
* For Id us "#" before name
    * Ex.
    ```
    #my-id {

    }
    ```

## Adding CSS to HTML page

* CSS can be added to an HTML page in 3 ways:
    1. Using the ```<link>``` tag
        * Adds an external CSS file rules to the HTML page
        * Ex.
            ```
            <link rel="stylesheet" type="text/css" href="myfile.css">
            ```
    2. Using the ```<style>``` tag
        * Allow for adding some custom CSS tags to an HTML file
        * Ex.
            ```
            <style>
                CSS Rules
            </style>
            ```
    3. Inline styles
        * Can add specific inline styling to specific HTML elements
        * Ex.
            ```
            <div style="background-color: yellow">...</div>
            ```

## Selectors

* Selectors is the idea of selecting elements in the HTML tree to target for the CSS declaration rules
* Selectors can range from very basic to very specific

### Basic Selectors

* Basic selectors entail selecting a single HTML element either by tag, class name, or id
* Ex. To target ```<p>``` elements,
```
p {
    font-size: 20px;
}
```
* The same works for classes and Id
* Class
```
.class-name {
    rules...
}
```
* Ids
```
#id-name {
    rules...
}
```

### Combining Selectors

* Can target an element by class-name or id
* Ex.
    ```
        <p class="dog-name>
            Roger
        </p>
        ...
        p.dog-name {
            rules...
        }
    ```

* For targetting multiple classes, combine the class-names in the selector without spaces
* Ex.
```
.dog-name.roger {
    rules...
}
```

### Grouping Selectors

* Can combine selectors so that the rules apply to multiple elements by having a comma in between
* Ex.
```
p, .dog-name {
  color: yellow;
}
```

### Selectors by following Document Tree Structure

* Use spaces in between to target children of a targeted element
* Ex.
```
p span {
  color: yellow;
}
```
* This targets span elements that are children of p elements

## Cascade

* Cascading is an important topic within the realm of CSS in styling HTML pages
* There is a certain order and priority that gets applied for rules because sometimes there can be conflicting rules
* What it considers in the algorithm to figure the cascading are:
    * specificity
    * importance
    * inheritance
    * order in the file

## Specificity

* Specificity is determined by a system where the more specific rule will win
    * If two rules have the same specificity, the one that appears later in the file wins

### Specificity Calculation

* Specificity is calculated by utilizing a 4 number system
* There are 4 slots and all of them starts at 0
    * 0 0 0 0
    * The slot at the leftmost is the most important and the rightmost is the least important
    * Ex. 1 0 0 0 is higher specificity than 0 1 0 0
* Slot 1:
    * Slot 1 is incremented when there is an element selector
    * Ex.
    ```
    p {}                    /* 0 0 0 1 */
    span {} 				/* 0 0 0 1 */
    p span {} 			    /* 0 0 0 2 */
    p > span {} 			/* 0 0 0 2 */
    div p > span {} 		/* 0 0 0 3 */
    ```
* Slot 2:
    * Slot 2 is incremented by:
        1. class selectors
        2. pseudo-class selectors
        3. attribute selectors
    * Ex.
    ```
    .name {}				/* 0 0 1 0 */
    .users .name {}		    /* 0 0 2 0 */
    [href$='.pdf'] {}	    /* 0 0 1 0 */
    :hover {}				/* 0 0 1 0 */
    ```
* Slot 3:
    * Slot 3 is incremented by id selectors
    * Ex.
    ```
    #name {}					/* 0 1 0 0 */
    .user #name {}			    /* 0 1 1 0 */
    #name span {}			    /* 0 1 0 1 */
    ```
* Slot 4:
    * Slot 4 is incremented by inline styling
    * Inline styling will have the most precedence over any rule 
    * Ex.
    ```
    <p style="color: red">Test</p> /* 1 0 0 0 */
    ```

* !important can be used to override any styling precedence
* Ex.
```
p {
  font-size: 20px!important;
}
```
* By making this rule, this will take precendence over any CSS rule except for those that also have !important, which in that case will resolve using the specificity rules above
* Generally its better to not utilize id rules and !important as this can create issues if multiple CSS files are utilized in one HTML page
* Rather, more specific rules should be creating by combining selectors
* !important should only be utilized to see some kind of effect when testing

## Inheritance

* Some CSS properties inherit from parent to child without having to explicitly state the rule in the child while others don't
* For example, "font-family" gets inherited from the parent to child by default but "background-color" does not get inherited from parent to child
* To force properties to inherit, create a property rule in the parent and then have "inherit" as the value in the child
* Ex.
```
body {
    background-color: yellow;
}
p {
    background-color: inherit;
}
```
* There are also methods to prevent inheriting in the children or reverting

## Attribute Selectors

* There are also ways to specify selectors to target HTML elements by their attributes
* It is possible to target a certain element tag with a id attribute utilizing the "[]" syntax
* Ex.
```
p[id] {
    rules...
}
```
* This will select all ```<p>``` elements that have an "id" attribute regardless of value
* Attribute selectors can also be matching to some regex pattern or exact
* Ex.
```
p[id="my-id] {
    rules...
}
```
* In this case the CSS will only apply when the element is a ```<p>``` tag and the id attribute matches that string

## Pseudo Classes

* Pseudo classes are predefined keywords that are used to select elements based on their state or to target a specific child
* One of the most popular ones that are used is ":hover"
    * This targets an element if it is hovered over
* Ex. When links are clicked, they switch state to ":active" and ":visited"
```
a,
a:visited,
a:active {
  color: yellow;
}
```
* Can write the CSS selector utilizing pseudo-classes to make sure that the CSS stays regardless of the element's state
* :nth-child() is another option as it allows for targeting odd and even children
    * Often utilized to style lists such that the style is different for adjacent children