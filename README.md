# Three State Switch
## javascript

    function filterme(val) {

      if (val === 1) {

        $('#RangeFilter').removeClass('rangeAll').removeClass('rangePassive').addClass('rangeActive');
        $("span").text("Active");
      }
      else if (val === 2) {

        $('#RangeFilter').removeClass('rangeActive').removeClass('rangePassive').addClass('rangeAll');
        $("span").text("All");
      }
      else if (val === 3) {

        $('#RangeFilter').removeClass('rangeAll').removeClass('rangeActive').addClass('rangePassive');
        $("span").text("Passive");
      }

    }

### HTML
```
   < p class="range-field" style=" width:60px">
   < input type="range" id="RangeFilter" name="points" onchange="filterme(this.value);" min="1" class="rangeAll" max="3" value="2" ></ p>
 
   < span > All </ span >
``` 
 

### Browser Compatibility

    /* Crome*/
    .rangeActive::-webkit-slider-thumb { background-color: #4caf50 !important;}
    .rangeAll::-webkit-slider-thumb { background-color: #6F6F6F !important;}
    .rangePassive::-webkit-slider-thumb { background-color: #C94553 !important;}
 
    /* Mozilla*/
    .rangeActive::-moz-range-thumb { background-color: #4caf50 !important;}
    .rangeAll::-moz-range-thumb { background-color: #6F6F6F !important;}
    .rangePassive::-moz-range-thumb { background-color: #C94553 !important;}
 
    /* IE and Ms Edge*/
    input[type=range]::-ms-track{ border: 10px solid #E1E1E1;border-radius: 12px;}
    input[type=range]::-ms-tooltip{display:none !important;}
