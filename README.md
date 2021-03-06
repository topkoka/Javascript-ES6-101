# Javascript-ES6-101-
![Artboard 1@2x](https://github.com/topkoka/Javascript-ES6-101-/blob/master/Ai%20info/2x/Artboard%201%402x.png)

#ES6

### `variable  `
``` js
var x = 10;   // global
const y = {}; // แนะนำ  ค่าคงที่  
let z = x;    //  แนะนำ
```
### ` Multi-line String & Expression interpolation `
```js
ใช้เครื่องหมาย "  `  "
const fistname = 'Robot';
const lastname = "asdgfh";
const date = new Date();
const great = `hello ${fistname + '' + lastname},how are you ${date}`;

```
### ` Destructuring Assignment &  Array Destructuring `
```js
const arr = [1,2];

### แบบเก่า ###
const a = arr[0]; 
const b = arr[1];

### แบบใหม่ ###
const [c,d] = arr;

const oneToFive = [1,2,3,4,5];
const [a1,b1,c1] = oneToFive;
const [a2,b2, ...rest]  = oneToFive;

///  ...rest  = 3 4 5
```
###  ` Rest parameters ` 
```js
/// "...parameters"

const oneToFive = [1,2,3,4,5];
const [a1,b1,c1] = oneToFive;
console.log(c1)
const [a2,b2, ...rest]  = oneToFive;

function howManyArgs(...args){
    console.log(args.length);
 }


 let clone = Object.assign({},user);
 function howManyArgs(...args){
    console.log(args.length);
}
```
### ` Spread Operators `
```js

var obj1 = {foo : "bar" , x:42};
var obj2 = {foo : "baz" , y:13};

var clonedObj = {...obj1 ,...obj2} /// { foo: 'baz', x: 42, y: 13 }

var {foo : foo2, x : x2 , y :y2} = clonedObj;
console.log(foo2,x2,y2)  // baz 42 13
```
### `Class` 
```js
class Rectangle{    
    constructor(height,width) {
        this.height = height;
        this.width = width;
    }

    get color(){
        return this._color;
    }
    set color(c) {
        this._color = c;
    }

    get area(){
         return this.height * this.width;
    }

    static areas(obj) {
        return obj.height * obj.width;
    }

}

const r =  new Rectangle(100 , 50);

console.log(r.height,r.width);
r.color = "RED";
console.log(r.color);

// method
console.log(`method ${r.area}`);
console.log(`static method ${Rectangle.areas(r)}`)

```
### `inheritance `
```js

class square extends Rectangle {
    constructor (width) {
        super(width,width); 
    }
}

const s =  new square(100);
s._color = "Blue"
console.log(s.color);
console.log(s.area);

```
### ` Object `
```js
 let clone = Object.assign({},user);
 
const doBark = "bark";
const dog = {
    name : "Doggy",age:2 ,["bar"+"k"] : function(){
        console.log("hong");
    },doBark:function(){
        console.log("hong");

}};

dog.bark();
dog.doBark();
```
### ` function `

```js 
var greet1 = function (firstname , lastanme) {
    return firstname + '' + lastanme
}

var greet2 = (firstname , lastanme) => {
    return firstname+ ' ' + lastanme
}

var greet3 =  (firstname , lastanme) => firstname + ' ' + lastanme;
console.log(greet3("aditep","campira"));

```

### ` this `

```js
var person1 = {
    name: "luna",

    hasdlMessage: function (message, handler) {
        handler(message);
    },
    greet : function() {
        const _this = this;
        this.hasdlMessage("Hi",function (message) {
            console.log(message+ " " + _this.name)
        });
    }
};

person1.greet();

```
```js

var person1 = {
    name: "luna",

    hasdlMessage: (message, handler)=>{
        handler(message);
    },
    greet : function() {
        
        this.hasdlMessage("Hi",(message) =>{
            console.log(message+ " " + this.name)
        });
    }
};

person1.greet();

```

### ` Modules `
``` js
// math.1.js
const add = function(a,b) {
return a + b;
};

module.exports = {add};

##
//  math.2.js
module.exports.add = function(a,b) {
return a + b;
};

var math1 = require("./math.1.js");
var math2 = require("./math.2.js");

// solution 1 : math1
console.log("1|", math1.add(1, 2));

// solution 2 : math2
console.log("2|", math2.add(1, 2));

```
## JQuery Method
![Artboard 1@2x](http://codewithme.us/dc/reveal.js/images/document-ready.png)
``` js
 // $(selectors).method("parameter1","parameter2")
$(document).ready(function() {
// javascript code here!!
});
    
```
##  selectors
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

## attributes
```js
// ดึงค่า attributes
var title = $("em").attr("title");
 $("#divid").text(title);
 
 // set attributes
 $("#myimg").attr("src", "images/dog2.jpg");
 
 // ลบ attributes
 $("table").removeAttr("border");

```
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
### ` เปลี่ยนรูป `
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
### ` ลบ `
```js
    <table border="2">
        <tr>
            <td>This is first table</td>
        </tr>
    </table>

    <table border="3">
        <tr>
            <td>This is second table</td>
        </tr>
    </table>

    <table border="4">
        <tr>
            <td>This is third table</td>
        </tr>
    </table>
    
 <script type="text/javascript" language="javascript">
        $(document).ready(function () {
           $("table").removeAttr("border");
        });
    </script>

```
## Class
```
 // addclass
   $("em").addClass("selected");
 
 // removeClass
  $("p#pid1").removeClass("red");
  
  // toggleClass (มีเอาออก-ไม่มีใส่เข้าไป)
    $(this).toggleClass("red");
```
### ` add class`
```js
    <style>
        .selected {
            color: red;
        }
        .highlight {
            background: yellow;
        }
    </style>
<body>
    <em title="Bold and Brave">This is first paragraph.</em>
    <p id="myid">This is second paragraph.</p>
</body>
 <script type="text/javascript" language="javascript">
        $(document).ready(function () {
            $("em").addClass("selected");
            $("#myid").addClass("highlight");
        });
    </script>
```
### `removeClass`
```js
    <style>
        .red {
            color: red;
        }

        .green {
            color: green;
        }
    </style>


<body>
    <p class="red" id="pid1">This is first paragraph.</p>
    <p class="green" id="pid2">This is second paragraph.</p>
</body>
 <script type="text/javascript" language="javascript">
 $(document).ready(function () {
          $("p#pid1").removeClass("red");
          $("p#pid2").removeClass("green");
 });
    </script>
```
### `toggleClass `
```js
    <style>
        .red {
            color: red;
        }
    </style>
    
<body>
    <p class="green">Click following line to see the result</p>
    <p class="red" id="pid">This is first paragraph.</p>
</body>

<script>
  $(document).ready(function () {
            $("p#pid").click(function () {
                $(this).toggleClass("red");
            });
        });
    </script>
```
## Contents( ดึงค่า)
```
//   .text()  .html()  .val();

 var content = $("p").html();
            $("#pid2").html(content);
// .hasClass() เช็คว่ามี   class นั้นรึป่าว return : true/false           
```

## traversing
```js
// index เริ่ม 0 --> n   addClass ให้ตาม index
  ea(index)   

 $("li").eq(0).addClass("selected"); 
 
  filter(class)  หาว่า liตัวที่มี middel อยู่ที่ไหน แล้ว addClass ให้ li ตัวนั้น
 $("li").filter(".middle").addClass("selected");
 $("li.middle").addClass("selected");
 
  find(class) หาว่า class นั้นอยู่ไหน ex. หา span ใน p แล้ว addClass ให้ span 
  $("p").find("span").addClass("selected");
  
  
  $("li").eq(0).find(".middle").addClass("selected");
  
```
## DOM
```js

replaceWith เปลี่ยนค่า
  $("div").click(function () {
                $(this).replaceWith("<h1>JQuery is Great</h1>");
            });
 $('div#div3').remove();        
 $(this).before('<div class="div"></div>');            
 $(this).after('<div class="div"></div>');
```
## Events
```js
  $(document).ready(function () {
            // 1
            $('div').mousedown(function(event) {
                console.log('Hi there1!');
            });
            // 2
            $('div').bind('mouseout', function (event) {
                console.log('Hi there2!');
            });
        });

```

## Ajax
```ajax
// load
 $('#stage').load('result.html');
 
 
 

```
#### ดึงข้อมูลมากำหนด
```js
$.getJSON('result.1.json', function (jd) {
                    $('#stage').html('<p> Name: ' + jd.name + '</p>');
                    $('#stage').append('<p>Age : ' + jd.age + '</p>');
                    $('#stage').append('<p> Sex: ' + jd.sex + '</p>');
 });


```
``` 
Name: Sara

Age : 22

Sex: female
```
```js
 $("#driver").click(function (event) {
                $.getJSON('result.2.json', function (data) {
                    data.forEach(element =>  {
                        $('#stage').append('<p> Name: ' + element.name + '</p>');
                        $('#stage').append('<p>Age : ' + element.age + '</p>');
                        $('#stage').append('<p> Sex: ' + element.sex + '</p>');
                    });
                });
            });
```
```
STAGE
Name: Sara

Age : 22

Sex: female

Name: John

Age : 25

Sex: male
```
# NEW
    51219.01 info=> arrow function
    51219.02 update readme show info
    61219.01 update info v0.1f
