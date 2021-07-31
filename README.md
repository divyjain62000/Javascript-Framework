# JavaScript-Framework
It is a javaScript framework using this user can create some components as well as user can validate form and handle ajax (GET/POST) request.Using this framework user able to do his / her work in very fast and simple manner.

## Features:
1) User can create modal in very easy way.
2) User can create accordion pan in very simple way.
3) User can fill combobox by writing a very little code.
4) User able to do form validation by writing a some lines code.
5) Handle ajax GET and POST request.

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

### Fill combobox:
````
<script>
function populateDesignations()
{
$$$.ajax({
"url": "servletOne",
"methodType": "GET",
"success": function(responseData){
var designations=JSON.parse(responseData);
$$$("designationCode").fillComboBox({
"dataSource": designations,
"text" : "title",
"value": "code",
"firstOption" : {
"text": "<select designation>",
"value" : "-1"
}
});
},
"failure": function(){
alert("Some problem");
}
});
}
window.addEventListener('load',populateDesignations);
</script>
````

````
<body>
<h1>Fill ComboBox Example</h1>
<select id='designationCode'>
</select>
</body>
````

### Output:
![image](https://user-images.githubusercontent.com/82946769/116789624-5968f380-aacd-11eb-83a4-945f85914741.png)


### Form validation:
````
<script>
// TMJRock user script starts here
function doSomething()
{
return $$$("someForm").isValid({
"nm":{
"required":true,
"maxLength":20,
"errorPane":"nmErrorSection",
"errors":{
"required":"Name required",
"maxLength":"Name cannot exceed 20 characters"
}
},
"ad":{
"required":true,
"errorPane":"adErrorSection",
"errors":{
"required":"Address required"
}
},
"ct":{
"invalid":-1,
"errorPane":"ctErrorSection",
"errors":{
"invalid":"Select city"
}
},
"gender":{
"required":true,
"errorPane":"genderErrorSection",
"errors":{
"required":"select gender"
}
},
"agree":{
"requiredState":true,
"displayAlert":true,
"errors":{
"requiredState":"Select I agree checkbox"
}
}
});
}
</script>
````

````
<body>
<h1>Form validation example</h1>
<form id='someForm' onsubmit='return doSomething()'>
<label>Name</label> <br><input type='text' name='nm' id='nm'> <span id='nmErrorSection'></span><br><br>
<label>Address</label> <br><textarea id='ad' name='ad'></textarea> <span id='adErrorSection'></span><br><br>
<label>Select city</label><br>
<select id='ct' name='ct'>
<option value='-1'>select city</option>
<option value='1'>Ujjain</option>
<option value='2'>Dewas</option>
<option value='3'>Indore</option>
</select>
 <span id='ctErrorSection'></span><br>
<br><br>
<label>Gender &nbsp;&nbsp;&nbsp;</label><br>
Male <input type='radio' name='gender' id='ml' value='M'>&nbsp;&nbsp;&nbsp;
Female <input type='radio' name='gender' id='fe' value='F'>&nbsp;&nbsp;&nbsp;
 <span id='genderErrorSection'></span>
<br><br>
<input type='checkbox' name='agree' id='ag' value='y'> I agree?
<br><br>
<button type='submit'>Registor</button>
</form>
</body>
````

### Output:
![image](https://user-images.githubusercontent.com/82946769/116789765-270bc600-aace-11eb-9b88-9711ce63eb57.png)


### Sending GET type request:

````
<script>
function getDesignation()
{
let titleSpan=$$$("title");
titleSpan.html("");
let code=$$$("code").value();
$$$.ajax({
"url":"servletTwo",
"data":{
"code":code
},
"methodType":"GET",
"success":function(responseData){
// code 
},
"failure":function(){
//code
}
});
}
</script>
````

````
<h1>GET Type request with data Example</h1>
Enter code <input type='text' id='code'>
<button type='button' onclick='getDesignation()'>Get Designation</button><br>
<br>
Title <span id='title'></span>
<br>
<a href='index.html'>Home</a>
````

### Sending POST type request:

````
<script>
function saveEnquiry()
{
var firstName=$$$("firstName").value();
var lastName=$$$("lastName").value();
var age=$$$("age").value();
var customer={
"firstName" : firstName,
"lastName" :  lastName,
"age" : age
};
var whatever=$$$("whatever");
whatever.html("");
$$$.ajax({
"methodType":"POST",
"url":"servletThree",
"data":customer,
"sendJSON":true,
"success":function(responseData){
var customer=JSON.parse(responseData);
var a="First Name: "+customer.firstName+"<br>";
a=a+"Last Name: "+customer.lastName+"<br>";
a=a+"Age: "+customer.age;
whatever.html(a);
},
"failure":function(){
alert("Some problem");
}
});
}
</script>
````

````
<body>
<h1>Post type request Example</h1> 
<label>First Name </label><br><input type='text' id='firstName'><br><br>
<label>Last Name </label><br><input type='text' id='lastName'><br><br>
<label>Age </label><br><input type='text' id='age'><br><br>
<button type='button' onclick='saveEnquiry()'>Save</button><br>
<br>
<div id='whatever'></div>
</body>
````
