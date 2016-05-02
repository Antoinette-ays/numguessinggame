<!DOCTYPE html>
<html>
<head>
<style>
body
{
    background-color:#59727e;
}
h3
{
    background-color:132734;
    line-height:2.3;
    opacity: 0.5;
    color: white;
}
.txt
{
   width: 200px;
   height: 30px;
   border: solid 2px #132734;
   padding: 2px;
   border-radius: 5px;
   font-size: 12px;
   background-color: #FFFFFF;
   color: #474747;
   font-family: TimesNewRoman;
}
#txt1
{
   width: 350px;
   height: 30px;
   border: solid 2px #132734;
   padding: 2px;
   border-radius: 5px;
   font-size: 15px;
   color: #474747;
   font-family: TimesNewRoman;
}
.btn {
	background-color:#599bb3;
	border-radius:8px;
	display:inline-block;
	color:#ffffff;
	font-family:Arial;
	font-size:12px;
	font-weight:bold;
	padding:5px 9px;
	text-decoration:none;
	text-shadow:0px 1px 0px #3d768a;
}
</style>
<title>
</title>
<h3><center>Higher or Lower? (Number Guessing Game)</center></h3>
</head>
<body>
<br>
<center> 
<form name="NGG">
<input type="text" id="txt1" name="hint" value="Good Luck :D" size="37" disabled>
<br>
<br>
<input type="text" class="txt" name="guess1" size="5">
<input type="BUTTON" class="btn" value="Guess"  onClick="Guess()">
</form>
</center>
<script>
var gnum = Math.round(Math.random() * 100) + 1;
var guesting = 0;
function Guess() {
var g = document.NGG.guess1.value;
guesting++;
status = "Tries: " + guesting;
if ( g == "")
    {
        document.NGG.hint.value = "You didn't guess anything hmm o.O";
        }
else if (g < gnum)
    {
    document.NGG.hint.value = "HIGHER :)";
    }
else if (g > gnum)
    {
    document.NGG.hint.value = "LOWER :D";
    }
else if (g == gnum) 
    {
    window.alert("Correct! You guessed it in " + guesting + " tries.") ;
    }
else
{
    document.NGG.hint.value = "Input Error!";
}
if (guesting == 5) {
    window.alert("Sorry, you reach the limits in guesting :(, The number was: " + gnum);
    location.reload();
    }
}
</script>
</body>
</html>
