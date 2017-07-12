# jQuery

## Intro

A library of functions in JavaScript.

* CDN: Content delivery network - url.
* Cross-platform: works well with all browsers.

Include a line in HTML header to enable JQuery:

```
<script src="https://code.jquery.com/jquery-3.1.0.min.js" 
integrity="sha256-cCueBR6CsyA4/9szpPfrX3s49M9vUU5BgtiJj06wt/s=" 
crossorigin="anonymous"></script>

```


Instead of writing an event listener to load JS we use a self running function which contains all the code.

```
$(function () {
});
```

## jQuery: Getting Elements and Methods

A method is a function that runs on a "jQueried" item. jQuery methods can only be used on jQuery elements.

```
$(function(){

  console.log('dom is ready');

  // change html of count span
  $("#count").html('5');

});
```

### CSS Selectors

``` ("#count") ``` gets the element by the id.  This is named a CSS selector.
``` ("li") ``` gets the element by tag name.
``` (".done") ``` gets the element by class.

### .html
``` .html ``` is a method.  It is equivalent to ``` .innerHTML = ```


### .addClass

```
 $("li").addClass('done');
```

This method adds a class of "done" to all of the list items.

Can select a specific list item by using array position.

``` $("li")[0]; ```  will return the first list element. This is a JS element.

``` $($("li")[0]).removeClass('done'); ``` We have to re-jQuery the element with $() before using a jQuery method upon it.

### .CSS

```
 $("#count").html("5").css('color' , '#BBCCAA');
```
Takes all the elements with an id of count, puts a number five in it and changes the colour to green.


```
.css({
"color": "green",
"font-size": "50px"
})
```

Create an object to change the style in multiple ways.  It's better to add a class like span in the CSS file, and add the class in jQuery.

### .prepend

```
$("#list").prepend($("<li>New Item</li>"));
```

Adds an item to the top of the list.  ``` .append ``` would add the new item to the bottom of the list.


``` console.log(event.target); ``` similar to this.
