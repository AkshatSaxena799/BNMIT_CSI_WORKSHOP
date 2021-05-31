# BNMIT_CSI_WORKSHOP
This Project is Based on Workshop held on Cloud Computing AWS, Firebase.

REFERENCE CODE(FOR LEARNING PURPOSE, It is not linked with Firebase Database):

<!DOCTYPE html><html lang="en"><head>
<meta charset="utf-8">
<title>ABC</title>

<script type="text/javascript">
	
  function userid_validation()
  {
  var uid = document.registration.userid;
  var uid_len = uid.value.length;
  if (uid_len == 0 || uid_len >= 12 || uid_len < 5)
  {
  alert("User Id should not be empty / length be between 5,12");
  return false;
  }
  return true;
  }


// This function will validate Password.
  function passid_validation()
  {
  var passid = document.registration.passid;
  var passid_len = passid.value.length;
  if (passid_len == 0 ||passid_len >= 12 || passid_len < 5)
  {
  alert("Password should not be empty / length be between 5-12");

  return false;
  }
  return true;
  }


// This function will validate Name.
  function allLetter()
  { 
  var uname = document.registration.username;
  var letters = /^[A-Za-z]+$/;
  if(uname.value.match(letters))
  {
  return true;
  }
  else
  {
  alert('Username must have alphabet characters only');

  return false;
  }
  }


  // This function will validate Address.
  function alphanumeric()
  { 
  var uadd = document.registration.address;
  var letters = /^[0-9a-zA-Z]+$/;
  if(uadd.value.match(letters))
  {
  return true;
  }
  else
  {
  alert('User address must have alphanumeric characters only');
  return false;
  }
  }


  // This function will select country name.
  function countryselect()
  {
  var ucountry = document.registration.country;
  if(ucountry.value == "Default")
  {
  alert('Select your country from the list');
  return false;
  }
  else
  {
  return true;
  }
  }

 // This function will validate Email.
  function ValidateEmail()
  {
  var uemail = document.registration.email;
  var mailformat = /^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/;
  if(uemail.value.match(mailformat))
  {
  return true;
  }
  else
  {
  alert("You have entered an invalid email address!");
  return false;
  }
  }

</script>
<style type="text/css">
	 h1{
  margin-left: 50px;
  color: navy;
  }
 h2{
  margin-left: 50px;
  color: navy;
  margin-top: -20px;
  }
  form li{
  list-style: none;
  margin-bottom: 5px;
  }
  form ul li label
  {
  float: left;
  clear: left;
  width: 265px;
  text-align: right;
  margin-right: 10px;
  font-family:Verdana, Arial, Helvetica, sans-serif;
  font-size:14px;
  }
 form ul li input, select, span 
  {
  float: left;
  margin-bottom: 10px;
  border: 1px solid maroon;
  }
  form textarea 
  {
  float: left;
  width: 350px;
  height: 150px;
  }
 [type="submit"] 
 {
  clear: left;
  margin: 20px 0 0 300px;
  font-size:18px
  }

</style>
</head>
<body>
<h1>JavaScript Field Label Form Validation using a registration form</h1>
<h2>Use tab key or mouse to go next field</h2>
<form name='registration'>
<ul>
<li><label>User id [5 to 12 characters] :</label></li>
<li><input type="text" name="userid" size="12" onblur="userid_validation()"/></li>
<li><label>Password [7 to 12 characters] :</label></li>
<li><input type="password" name="passid" size="12" onblur="passid_validation()"/></li>
<li><label>Name [Alphabates characters] :</label></li>
<li><input type="text" name="username" size="50" onblur="allLetter()"/></li>
<li><label>Address [alphanumeric characters] :</label></li>
<li><input type="text" name="address" size="50" onblur="alphanumeric()"/></li>
<li><label>Country [Must select a country] :</label></li>
<li><select name="country" onblur="countryselect()">
<option selected="" value="Default">(Please select a country)</option>
<option value="AF">Australia</option>
<option value="AL">Canada</option>
<option value="DZ">India</option>
<option value="AS">Russia</option>
<option value="AD">USA</option>
</select></li>
<li><label for="email">Email [Valid email] :</label></li>
<li><input type="text" name="email" size="50" onblur="ValidateEmail()" /></li>
<li><label id="gender">Sex [Select Male or Female] :</label></li>
<li><input type="radio" name="sex" value="Male" checked /><span>Male</span></li>
<li><input type="radio" name="sex" value="Female" /><span>Female</span></li>
<img src="path">
<li><label>Language [Optional] :</label></li>
<li><input type="checkbox" name="en" value="en" checked /><span>English</span></li>
<li><input type="checkbox" name="nonen" value="noen" /><span>Non English</span></li>
<li><input type="submit" name="submit" value="Submit" onclick="alert('Form submitted successfully')" /></li>
</ul>
</form>
</body>
</html>



