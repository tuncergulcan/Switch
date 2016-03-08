### Three State Switch

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
