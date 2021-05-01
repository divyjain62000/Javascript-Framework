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
 ### Output
 
 ![image](https://user-images.githubusercontent.com/82946769/116775045-319e6f00-aa7e-11eb-967b-b4c184f1aae7.png)
 
 
 ### Creating accordian panel:
 code to write in between <body> tag
 ````
 <h1>Accordian Pan Example</h1>
<div accordian="true">
<h3 accordianHeadrerBackgroundColor="#b97a56">Heading 1</h3>
<div accordianBackgroundColor="#ffe3ec">
1 whatever whatever
2 whatever whatever
3 whatever whatever<br>
4 whatever whatever
5 whatever whatever
6 whatever whatever<br>
7 whatever whatever
8 whatever whatever
9 whatever whatever<br>
</div><br>
<h3 accordianHeadrerBackgroundColor="#b97a56">Heading 2</h3>
<div accordianBackgroundColor="#ffe3ec">
11 whatever whatever
22 whatever whatever
33 whatever whatever
44 whatever whatever
55 whatever whatever
66 whatever whatever
77 whatever whatever
</div><br>
<h3 accordianHeadrerBackgroundColor="#b97a56">Heading 3</h3>
<div accordianBackgroundColor="#ffe3ec">
111 whatever whatever
222 whatever whatever
333 whatever whatever
444 whatever whatever
555 whatever whatever
666 whatever whatever
777 whatever whatever
</div>
</div>
<br><br>


<div accordian='true'>
<h3>Heading 1000</h3>
<div>
1 whatever whatever
2 whatever whatever
3 whatever whatever
4 whatever whatever
5 whatever whatever
6 whatever whatever
7 whatever whatever
</div><br>
<h3>Heading 2000</h3>
<div>
11 whatever whatever
22 whatever whatever
33 whatever whatever
44 whatever whatever
55 whatever whatever
66 whatever whatever
77 whatever whatever
</div><br>
<h3>Heading 3000</h3>
<div>
111 whatever whatever
222 whatever whatever
333 whatever whatever
444 whatever whatever
555 whatever whatever
666 whatever whatever
777 whatever whatever
</div><br>
</div>
 ````
 
 ### Output
 ![image](https://user-images.githubusercontent.com/82946769/116775129-d620b100-aa7e-11eb-9005-c637be6ff0f1.png)


