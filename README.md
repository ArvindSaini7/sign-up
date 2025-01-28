# sign-up
website page step by step

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
    <input type="text"  placeholder="enter the name" id="name">
    <input type="email"  placeholder="enter the email" id="email">
    <input type="password"  placeholder="enter the password" id="password">
    <button onclick="save()" >sumit</button>

    <script>

        function save(){
            let namevalue=document.getElementById("name").value
            let passwordvalue=document.getElementById("password").value
            let emailvalue=document.getElementById("email").value


           let data = {
                 "newname": namevalue,
                 "newpassword":passwordvalue,
                 "newemail": emailvalue
            }

            let users=JSON.parse(localStorage.getItem("sign up"))||[]
            
                users.push(data)
                localStorage.setItem("sign up",JSON.stringify(users))
                
            
            
            


            
        }


    </script>


</body>
</html>
