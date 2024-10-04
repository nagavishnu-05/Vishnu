# BMI Calculator
A simple BMI Calculator using HTML, CSS and JS
<!DOCTYPE html>
<html>
    <head>
        <title>BMI Calculator</title>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <style>
            body, html{
                background-color: whitesmoke;
                font-family: Trebuchet MS, sans-serif;
            }
            #main{
                border: 2px solid white;
                background-color: white;
                border-color: whitesmoke;
                width: 500px;
                height: 600px;
                box-shadow: rgb(204, 219, 232) 3px 3px 6px 0px;
                position: relative;
                top: 100px;
                left: 670px;
            }
            #line{
                border: 1px solid black;
                border-color: whitesmoke;
                box-shadow: rgb(204, 219, 232) 3px 3px 6px 0px;
                position: relative;
                top: 0px;
            }
            #title{
                font-size: 30px;
                color: red;   
                position: relative;
                left: 145px;
            }
            #text{
                position: relative;
                margin: 20px;
                margin-top: 30px;
                font-size: 30px;
                left: 10px;
                top: 10px;
                font-family: Trebuchet MS, sans-serif;
            }
            #winput{
                position: relative;
                top: -45px;
                left: 200px;
                width: 250px;
                height: 35px;
                padding-left: 10px;
                font-size: 26px;
                font-family: Trebuchet MS, sans-serif;
            }
            #hinput{
                position: relative;
                top: -45px;
                left: 200px;
                width: 250px;
                height: 35px;
                padding-left: 10px;
                font-size: 26px;
                font-family: Trebuchet MS, sans-serif;
            }
            #button{
                font-family: Trebuchet MS, sans-serif;
                position: relative;
                width: 150px;
                height: 40px;
                outline-width: 2px;
                padding-bottom: 5px;
                top: 30px;
                left: -90px;
                background-color: orange;
                font-size: 20px;
                border: 2px solid white;
                border-radius: 15px;
            }
            #weight{
                position: relative;
                font-size: 20px;
                margin-left: 15px;
                margin-top: 55px;
                left: 30px;
            }
            #weightb{
                width: 50px;
                height: 30px;
                position: relative;
                top: -60px;
                left: 180px;
                font-size: 15px;
                font: bolder;
                color: black;
                border: none;
            }
            #height{
                position: relative;
                font-size: 20px;
                margin-left: 15px;
                margin-top: -40px;
                top: -50px;
                left: 265px;
            }
            #heightb{
                width: 50px;
                height: 30px;
                position: relative;
                top: -60px;
                left: 150px;
                font-size: 18px;
                font: bolder;
                color: black;
                border: none;
                top: -108px;
                left: 415px;
            }
            #ans{
                position: relative;
                margin-top: -20px;
                top: -50px;
                left: 50px;
                font-size: 26px;
            }
            #ansb{
                position: relative;
                top: -105px;
                left: 290px;
                height: 30px;
                width: 50px;
                font-size: 20px;
                font: bolder;
                border: none;
            }
            #stat{
                position: relative;
                margin-top: -20px;
                top: -50px;
                left: 50px;
                font-size: 22px;
            }
            #statb{
                position: relative;
                top: -100px;
                left: 290px;
                height: 30px;
                width: 130px;
                font-size: 30px;
                font: bolder;
                border: none;
            }
        </style>
    </head>
    <body>
        <div id="main">
            <h1 id="title">BMI CALCULATOR</h1>
            <hr id="line">
            
            <h3 id="text">Weight :</h3>
            <input id="winput" type="text" placeholder="Enter Weight in Kgs">
            
            <h3 id="text">Height :</h3>
            <input id="hinput" type="text" placeholder="Enter Height in cms">
            
            <button id="button">Calculate</button>
            
            <h5 id="weight">Your Weight : </h5>
            <input id="weightb" placeholder="in  Kgs" readonly>
            
            <h5 id="height">Your Height : </h5>
            <input id="heightb" placeholder="in  cms" readonly>
            
            <h3 id="ans">Your BMI Value is :</h3>
            <input id="ansb" type="text" readonly>
            
            <h3 id="stat">Your Weight Status is :</h3>
            <input id="statb" type="text" readonly>
        </div>
        <script>
            let button = document.getElementById("button");
            button.onclick = function(){
                let weight = document.getElementById("winput").value;
                let height = document.getElementById("hinput").value;
                
                document.getElementById("weightb").value = weight;
                document.getElementById("heightb").value = height;
                
                let heights = height / 100;
                
                let bmi = weight / (heights * heights);
                document.getElementById("ansb").value = bmi.toFixed(3);
                
                if(bmi < 18.5){
                    document.getElementById("statb").value = "Underweight";
                }
                else if(bmi >= 18.5 && bmi <= 24.9 ){
                    document.getElementById("statb").value = "Normal";
                }
                else if(bmi > 24.9 && bmi <= 29.9){
                    document.getElementById("statb").value = "Overweight";
                }
                else{
                    document.getElementById("statb").value = "Obese";
                }
            };            
        </script>
    </body>
</html>
