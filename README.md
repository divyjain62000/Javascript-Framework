# JavaScript-Framework
It is a javaScript framework using this user can create some components as well as user can validate form and send post and get request.Using this framework user able to do his / her work in very fast and simple manner.

## Features:
1) User can create modal in very easy way.
2) User can create accordian pan in very simple way.
3) User can fill combobox by writing a very little code.
4) User able to do form validation by writing a some lines code.
5) User able to send GET and POST request in very simple way.

## Steps to use this framework:-
1) Download framework.js file and framework_style.css file 
2) include this JS and CSS file:
````
<script src='js/framework.js'></script>
<link rel="stylesheet" href="css/framework_style.css">
````

### Creating modal:
code to write in between <script> tag
````
<script>
// user written functions
function abBeforeOpening()
{
return true;
}
function abOpened()
{
}
function abBeforeClosing()
{
return true;
}
function abClosed()
{
}
function createModal1()
{
$$$.modals.show("ab");
}
</script>
````
code to write in between <body> tag
````
<button style='background:#0047b3;border:none;border-radius:2px;padding:10px;font-size:18px;color:#FFF' onclick='createModal1()'>Show modal</button>
<div id='ab' style='display:none' forModal='true' size="600x300" header="Some Heading" footer="Some Footer" maskColor="#41EAD4" modalBackgroundColor="#EEF1EF	" closeButton="true" beforeOpening="abBeforeOpening()" afterOpening="abOpened()" beforeClosing="abBeforeClosing()" afterClosing="abClosed()">
God is great<br>
God is great<br>
God is great<br>
God is great<br>
God is great<br>
<input type='text' id='myTextBox' value='Great'>
God is great<br>
God is great<br>
God is great<br>
God is great<br>
God is great<br>
God is great<br>
God is great<br>
God is great<br>
God is great<br>
The End
</div>
````
 ### output
 
 ![image](https://user-images.githubusercontent.com/82946769/116775045-319e6f00-aa7e-11eb-967b-b4c184f1aae7.png)

