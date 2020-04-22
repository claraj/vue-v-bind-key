# v-bind:key 

v-bind:key is not needed if you will not change the order of the elements generated with a v-for loop.  Hovever, it is not incorrect to use it. 

v-bind:key should be used if you are displaying many elements in a table, and you will need to re-order them.  In this example, the table is re-drawn when the population of a city changes, to keep the table in order.  

However, it is not wrong to leave it out. Your app will be slighly slower. 

If your app is generating more complex HTML in a v-for loop, you may start to notice a delay when the data is updated.

Example: 
~74ms to re-draw table without v-bind:key.  About 5000 nodes (HTML elements) have to be re-drawn 
~5ms to re-draw table with v-bind:key.  13 nodes (HTML elements) have to be re-drawn 

Screenshots from performance tool in Chrome dev tools

## No v-bind:key
<img src="img/key.png">

## With v-bind:key
<img src="img/key.png">
