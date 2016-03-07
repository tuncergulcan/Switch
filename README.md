# Triple Switch

### HTML Code
<p class="range-field" style=" width:60px">
    <input type="range" id="RangeFilter" name="points" onchange="filterme(this.value);" min="1" class="rangeAll" max="3" value="2">
</p>
<span>All</span>

### Javascript Code
function filterme(val) 
{
    if (val == 1) 
    {
        $('#RangeFilter').removeClass('rangeAll').removeClass('rangePassive').addClass('rangeActive');
        $("span").text("Active");
    } 
    else if (val == 2)
    {
        $('#RangeFilter').removeClass('rangeActive').removeClass('rangePassive').addClass('rangeAll');
        $("span").text("All");
    } 
    else if(val==3)
    {
       $('#RangeFilter').removeClass('rangeAll').removeClass('rangeActive').addClass('rangePassive');
        $("span").text("Passive");
    }
}

### CSS Code
range-field{position:relative}
input[type=range],input[type=range] + .thumb{cursor:pointer}
input[type=range]{position:relative;background-color:transparent;border:none;outline:none;width:100%;margin:0;padding:0}
input[type=range] + .thumb{display:none;position:absolute;border:none;height:0;width:0;border-radius:50%;top:10px;margin-left:-6px;-webkit-transform-origin:50% 50%;-moz-transform-origin:50% 50%;-ms-transform-origin:50% 50%;-o-transform-origin:50% 50%;transform-origin:50% 50%;-webkit-transform:rotate(-45deg);-moz-transform:rotate(-45deg);-ms-transform:rotate(-45deg);-o-transform:rotate(-45deg);transform:rotate(-45deg)}
input[type=range] + .thumb .value{display:block;width:30px;text-align:center;font-size:0;-webkit-transform:rotate(45deg);-moz-transform:rotate(45deg);-ms-transform:rotate(45deg);-o-transform:rotate(45deg);transform:rotate(45deg)}
input[type=range] + .thumb.active{border-radius:50% 50% 50% 0}
input[type=range] + .thumb.active .value{color:#fff;margin-left:-1px;margin-top:8px;font-size:10px}
input[type=range]:focus{outline:none}
input[type=range]{-webkit-appearance:none}
input[type=range]::-webkit-slider-runnable-track{height:3px;background:#E1E1E1;border:none}
input[type=range]::-webkit-slider-thumb{-webkit-appearance:none;border:none;height:14px;width:14px;border-radius:50%;background-color:#C94553;transform-origin:50% 50%;margin:-5px 0 0;-webkit-transition:.3s;-moz-transition:.3s;-o-transition:.3s;-ms-transition:.3s;transition:.3s}
input[type=range]:focus::-webkit-slider-runnable-track{background:#E1E1E1}
input[type=range]{border:10px solid #E1E1E1;border-radius:12px}
input[type=range]::-moz-range-track{height:3px;background:#E1E1E1;border:none}
input[type=range]::-moz-range-thumb{border:none;height:14px;width:14px;border-radius:50%;background:#26a69a;margin-top:-5px}
input[type=range]:-moz-focusring{outline:1px solid #E1E1E1;outline-offset:-1px}
input[type=range]:focus::-moz-range-track{background:#E1E1E1}
input[type=range]::-ms-track{height:3px;background:transparent;border-color:transparent;border-width:6px 0;color:transparent}
input[type=range]::-ms-fill-lower{background:#E1E1E1}
input[type=range]::-ms-fill-upper{background:#E1E1E1}
input[type=range]::-ms-thumb{border:none;height:14px;width:14px;border-radius:50%;background:#E1E1E1}
input[type=range]:focus::-ms-fill-lower{background:#E1E1E1}input[type=range]:focus::-ms-fill-upper{background:#E1E1E1}

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
