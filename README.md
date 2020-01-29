# Javascript-ES6-101-
![Artboard 1@2x](https://github.com/topkoka/Javascript-ES6-101-/blob/master/Ai%20info/2x/Artboard%201%402x.png)

## Object
```js
 let clone = Object.assign({},user);
```

## JQuery Method
![Artboard 1@2x](http://codewithme.us/dc/reveal.js/images/document-ready.png)
``` js
 // $(selectors).method("parameter1","parameter2")
$(document).ready(function() {
// javascript code here!!
});
    
```
####  selectors
```js

    <script type="text/javascript" language="javascript">
        $(document).ready(function(){
            // $ (selectors).method("parameter1","parameter2")
            $('#div2,.small').css("background-color","blue");
            $('div.small span').css("background-color","red");
            $('.big').css("background-color","yellow");
        });
    </script>

    <div class="big" id="div1">
        <p>This is first division of the DOM.</p>
    </div>
    <div class="medium" id="div2">
        <p>This is second division of the DOM.</p>
    </div>
    <div class="small" id="div3">
        <span>This is third division of the DOM</span>
    </div>
```

#### attributes
```js

    <div>
        <em title="Bold and BraveSSS">This is first paragraph.</em>
        <p id="myid"  >This is second paragraph.</p>
        <div id="divid"></div>
    </div>

    <script type="text/javascript" language="javascript">
        $(document).ready(function () {
            var title = $("em").attr("title");
            $("#divid").text(title);
        });
    </script>

```
```html
This is first paragraph.
This is second paragraph.

Bold and BraveSSS
```
```
  <div>
        <img src="images/dog1.jpg" alt="Sample image" />
        <img id="myimg" src="images/dog1.jpg" alt="Sample image" />
    </div>

    <script type="text/javascript" language="javascript">
        $(document).ready(function () {
            
            $("#myimg").attr("src", "images/dog2.jpg");
        });
    </script>
  
```
# NEW
    51219.01 info=> arrow function
    51219.02 update readme show info
    61219.01 update info v0.1f
