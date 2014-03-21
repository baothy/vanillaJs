vanillaJs
=========

jquery vs vanilla js

selectors

```
// jquery 
$('.myClass');

// javascript

document.querySelectorAll('.myClass'); // return an array of dom element

document.querySelector('.myClass'); // return the first dom element found

// even better performance
document.getElementsByClassName('myClass');
document.getElementsById('myId');
document.getElementsByTagName('div');
document.getElementsByName('myTagName');

```

get / set attribute

```
// jquery attribute
var el = $('#element');
$(el).attr('data');
$(el).attr('data', 'myData');

//javascript
var el = document.getElementsById('myId');
el.getAttribute('data');
el.setAttribute('data', 'myData');

```

```
```
```
```
```


