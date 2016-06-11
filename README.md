w3csspag - dynamic pagination
============================

This jQuery plugin helps you create dynamic pagination with [W3.css](http://www.w3schools.com/w3css/) or in any other html pages.

```html
<p id="content">Dynamic page content</p>
<p id="pagination-here"></p>
```

```javascript
$('#pagination-here').w3csspag({
    total: 7,          // total pages
    page: 1,            // default page
    maxVisible: 5,     // visible pagination
    leaps: true         // next/prev leaps through maxVisible
}).on("page", function(event, num){
    $("#content").html("Page " + num); // or some ajax content loading...
    // ... after content load -> change total to 10
    $(this).w3csspag({total: 10, maxVisible: 10});
});

```
#License

Plugin available under MIT license (See LICENSE file)
