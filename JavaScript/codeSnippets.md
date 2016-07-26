### Get details of DNS
```js
console.log('document.URL : ', document.URL);
console.log('document.location.href : ', document.location.href);
console.log('document.location.origin : ', document.location.origin);
console.log('document.location.hostname : ', document.location.hostname);
console.log('document.location.host : ', document.location.host);
console.log('document.location.pathname : ', document.location.pathname);
```

#### indexOf() and splice() method
this.swords.indexOf(val) >== 0  
- swords is an array. The indexOf() will return the first found index of a value, or -1 if it's not found. 

this.swords.splice(this.swords.indexOf(val), 1)
- If the right sword is available, we will remove it from the swords array with some index cleverness. `[0]` denote from where search would be start and `1` denotes how many item(s) we want to remove.
- const soldiers = ["Knights", "Pikemen", "Archers"];
- soldiers.splice(1, 2); will delete "Pekemen" and "Archers" and returns ["Pekemen" , "Archers"]
 
#### jQuery `.clone()` method
- Create a deep copy of the set of matched elements.
- `clone()` vs `append()`
```js
// html 
<div class="container">
    <div class="hello">Hello</div>
    <div class="goodbye">Goodbye</div>
</div>

// .append() normally when an element is inserted somewhere in the DOM, it is moved from its old location
$('.hello').appendTo('.goodbye');

// The resulting DOM structure would be: (removed from previous location and in new position)
<div class="container">
  <div class="goodbye">
    Goodbye
    <div class="hello">Hello</div>
  </div>
</div>

// To prevent this and instead create a copy of the element, we could write the following:
$( ".hello" ).clone().appendTo( ".goodbye" );

// This would produce 
<div class="container">
  <div class="hello">Hello</div>
  <div class="goodbye">
    Goodbye
    <div class="hello">Hello</div>
  </div>
</div>
```
 
### Fancy Codes
```js
// Create a new object (server response)
const o = Object.create(null);

// set the context for a function by .call() or .apply()
myfunc.call(this);
myfunc.apply(this);

```
