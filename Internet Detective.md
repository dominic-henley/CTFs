# Internet Detective

_Visit this website: 143.110.226.233 Can you figure out the flag? Try digging around..._

`curl`ing into the IP address gives us this code block


<html>

<meta http-equiv="content-type" content="text/html;charset=UTF-8" /><!-- /Added by HTTrack -->
<head>
<title>Secure Login Portal</title>
</head>
<body bgcolor=grey>
<!-- standard MD5 implementation -->
<script type="text/javascript" src="md5.js"></script>

<script type="text/javascript">
  function verify() {
    checkpass = document.getElementById("pass").value;
    split = 4;
    if (checkpass.substring(0, split) == 'flag') {
      if (checkpass.substring(split*6, split*7) == 'XDLO') {
        if (checkpass.substring(split, split*2) == '{mes') {
         if (checkpass.substring(split*4, split*5) == 'aldo') {
           if (checkpass.substring(split*3, split*4) == '>ron') {                                             
            if (checkpass.substring(split*5, split*6) == 'guys') {                                            
              if (checkpass.substring(split*2, split*3) == 'siis') {                                          
                if (checkpass.substring(split*7, split*8) == 'L}') {                                          
                        alert("Password Verified")                                                            
                  }
                }
              }
      
            }
          }
        }
      }
    }
    else {
      alert("Incorrect");
    }
    
  }
</script>
<div style="position:relative; padding:5px;top:50px; left:38%; width:500px; height:300px; background-color:green">
<div style="text-align:center">
<p>Sorry for the terrible colour scheme</p>
<p>Try crack in, if its the right password you won't get an alert!</p>

<input type="password" id="pass" size="8" />
<br/>
<input type="submit" value="verify" onclick="verify(); return false;" />
</form>
</div>
</div>
</body>


</html>

From this point, it's not difficult to piece together the substrings to form the flag

flag is flag{messiis>ronaldoguysXDLOL}
