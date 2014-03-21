jquery vs vanilla js
=========


<h2>selectors</h2>

``` javascript
// jquery 
$(selector);

// javascript
document.querySelectorAll(selector); // return an array of dom element
document.querySelector(selector); // return the first dom element found

// even better performance
document.getElementsByClassName('myClass');
document.getElementsById('myId');
document.getElementsByTagName('div');
document.getElementsByName('myTagName');

```

<h2>get / set attribute</h2>

``` javascript
// jquery
var el = $('#element');
$(el).attr('data');
$(el).attr('data', 'myData');

//javascript
var el = document.getElementsById('myId');
el.getAttribute('data');
el.setAttribute('data', 'myData');

```

<h2>dom ready</h2>

``` javascript
//jquery 
$(function () {
  // place code here
});

//javascript
document.addEventListener('DOMContentLoaded', function() {
  // place code here
});

```

<h2>Class</h2>

``` javascript
//jquery
$(element).addClass('wrap');

//javascript
document.querySelector(element).classList.add('wrap');
```

``` javascript
//jquery
$(element).hasClass(className)

//javascript
function hasClass( element, className ) {
  return new RegExp('(\\s|^)' + className + '(\\s|$)').test(target.className);
}
```

<h2>events</h2>

<h3>live / on event</h3>

``` javascript
//jquery 
$( document ).on( eventType, classSelector, data, handler );  

//javascript
function live(eventType, elementClassName, cb) {
  document.addEventListener(eventType, function (event) {
    if (hasClass(event.target, elementClassName)) {
      cb.call(event.target, event);
    }
  });
}

function hasClass( target, className ) {
  return new RegExp('(\\s|^)' + className + '(\\s|$)').test(target.className);
}


```

<h2>click event</h2>

``` javascript
// jquery
$(element).bind(eventType, function() {...}, )

//javascript
element.addEventListener(eventType, function() { ... }, false);

```

<h2>dom manipulation</h2>

``` javascript
//jquery
$(element).append($('<div/>'));

//javascript
document.querySelector(selector).innerHTML += "<div></div>";
```

``` javascript
//jquery 
$(element).empty();

//javascript
document.querySelector(selector).innerHTML = null;
```

``` javascript
//jquery 
$(selector).remove();

//javascript
var element = document.querySelector(selector);
element.parentNode.removeChild(c);
```

<h2>ajax</h2>

<h3>get</h3>

``` javascript
//jquery
$.get(url, function (data) {
  // place code here
})

//javascript
var httpRequest = new XMLHttpRequest();
httpRequest.onreadystatechange = function (data) {
  // code
}
httpRequest.open('GET', url);
httpRequest.send();
```

<h3>post</h3>
``` javascript
var dataObject = {param1: value1};

//jquery
$.post('//example.com', dataObject, function (data) {
  // place code here
})

//javascript
var httpRequest = new XMLHttpRequest()
httpRequest.onreadystatechange = function (data) {
  // place code here
}
httpRequest.setRequestHeader('Content-Type', 'application/x-www-form-urlencoded')
httpRequest.open('POST', url)
httpRequest.send('param1=' + encodeURIComponent(value1))
```


