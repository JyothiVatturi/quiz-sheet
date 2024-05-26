<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap">

    <title>Quiz Paper</title>
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            background-color: #e6ffe6;
            text-align:center;
            margin-top: 150px;
            position: relative;    
        }
        
       
        .question {
            display: none;
            position: absolute;
            
        }
        
        .question.active {
            width: 100%;
            display: block;
            animation: transform 1s ease-in-out;
            
        }
        @keyframes transform{
            from {left: 0%;}
            to {left: -100%}
        }
        .button {
            
            padding: 5px 10px;
            font-size: 16px;
            cursor: pointer;
            color: white;
            background-color: rgb(12, 240, 12);
            

        }
       
        .button:hover{
            background-color: rgb(4, 94, 4);
            
            
        }
        .right {
                float: right;
                
    
        }
        .left {
            float: left;
        }
    </style>
</head>
<body>
    
        <div class="question active" id="question1"  >
            <h1 align="center">QUIZ</h1>
        <h4>please fill up with your answers</h4>
        <h2>1.what are formatting tags?</h2>
        <input type="radio" name="A" value="a">H1 H2 H7 H9<br>
        <input type="radio" name="A" value="b">H1 H2 H3 H9<br>
        <input type="radio" name="A" value="c">H1 H2 H5 H6<br>
        <input type="radio" name="A" value="d">H4 H7 H8 H9<br>
    
    <br>
     <!--<button class="button" onclick="nextQuestion('question2')">Next</button>*/-->
     <button class="button right" onclick="nextQuestion('question2')">&#10095</button>
            
        </div>

        <div class="question" id="question2" >
            <h4>Question 2</h4>
            <h2>2.what is the abbrivation of HTML?</h2>
            <input type="text" name="A" placeholder="enter your answer" requried style="background-color: rgb(186, 219, 186)"><br><br>
            
            <button class="button left" onclick="prevQuestion('question1')">&#10094</button>
            <button class="button right" onclick="nextQuestion('question3')">&#10095</button>
         </div>

        <div class="question" id="question3" >
            <h4>Question 3</h4>
        <h2>3.what are the another names for html?</h2>
        <input type="checkbox" name="A" value="a">Scripting Language<br>
        <input type="checkbox" name="B" value="b">Formatting Language<br>
        <input type="checkbox" name="C" value="c">Formal Language<br>
        <input type="checkbox" name="D" value="d">Presentation Language<br>
        
        <button class="button left" onclick="prevQuestion('question2')">&#10094</button>
        <button class="button right" onclick="nextQuestion('question4')">&#10095</button>
        </div>
        <div class="question" id="question4" >
            <h4>Question 4</h4>
            <h2>4.write a brief description about html?</h2>
            <textarea name="question" rows="5" cols="30" style="background-color: rgb(186, 219, 186)">Enter your answer</textarea ><br><br>
            
            <button class="button left" onclick="prevQuestion('question3')">&#10094</button>
            <button class="button right" onclick="nextQuestion('question5')">&#10095</button>
        </div>
        <div class="question" id="question5" >
            <h1>your answers are submited</h1>
            <h6>Thank You</h6>
        </div>
    

    
    

    <script>
        const greenShades = [
            '#ccffcc', 
            '#b3ffb3', 
            '#66ff66', 
            '#00cc00', 
            '#009900'  
        ];

        let Index = 0;
        function nextQuestion(nextQuestionId) {
           // Array.from(document.getElementsByClassName('active')).forEach(ele=> ele.classList.remove('active'));
            document.querySelector('.question.active').classList.remove('active');
            document.getElementById(nextQuestionId).classList.add('active');
            //document.querySelector('.question.active').classList.remove('active');
            document.body.style.backgroundColor = greenShades[Index];
            Index++;

        }
        function prevQuestion(prevQuestionId) {
            document.querySelector('.question.active').classList.remove('active');
            document.getElementById(prevQuestionId).classList.add('active');
            Index--;
            document.body.style.backgroundColor = greenShades[Index];
            


        }
    </script>
</body>
</html>
