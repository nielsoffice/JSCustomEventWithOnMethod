# JSCustomEventWithOnMethod
JavaScript custom event with on() jQuery method

```JS
 jQuery(document).ready(function(){
   
   // Select elem where custom event will reflected
   jQuery("#main").on("boldText", function(event, makeBold){
    
   // assigned where the magic will happened  
   jQuery('p').html(function(i, currentText ) {
  
       return  makeBold + ' ' + currentText;

    }).css( 'font-weight' , 'bolder' ).show();
   });

   // triggered the custom event 
   jQuery("#event").click(function(){ jQuery("p").trigger("boldText", ["Niel"]); });
   
 });
```

```HTML
<button id="event">Implement</button>

<div id="main">

  <p> Is Web Developer </p>

</div>
```
