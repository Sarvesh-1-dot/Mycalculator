#calculater.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <link rel="stylesheet" href="calculator.css">
</head>
<body>
    <div id="Calculator">
        
        <input id="display" readonly>
        <div id="keys">
            <button onclick="appendtodisplay('+')" class="operator">+</button>
            <button onclick="appendtodisplay('7')">7</button>
            <button onclick="appendtodisplay('8')">8</button>
            <button onclick="appendtodisplay('9')">9</button>
            <button onclick="appendtodisplay('-')"class="operator">-</button>
            <button onclick="appendtodisplay('4')">4</button>
            <button onclick="appendtodisplay('5')">5</button>
            <button onclick="appendtodisplay('6')">6</button>
            <button onclick="appendtodisplay('*')"class="operator">*</button>
            <button onclick="appendtodisplay('1')">1</button>
            <button onclick="appendtodisplay('2')">2</button>
            <button onclick="appendtodisplay('3')">3</button>
            <button onclick="appendtodisplay('/')"class="operator">/</button>
            <button onclick="appendtodisplay('0')">0</button>
            <button onclick="appendtodisplay('.')">.</button>
            <button onclick="calculate()">=</button>
            <button onclick="cleardisplay()"class="operator">C</button>



        </div>
    </div>
    
</body>
<script src="calculator.js"></script>
</html>


2.#calculator.css

#keys{
    display: grid;
    grid-template-columns: repeat(4,1fr);
    gap: 5px;
    padding: 2px;
}

#display{
    width: 175px;
    padding: 20px;
    font-size: large;
    text-align: left;
    border: none;
    background-color: rgb(39, 36, 36);
    color: aliceblue;
}

body{
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: rgb(235, 230, 220);
}


button{
    width: 50px;
    height: 50px;
    border-radius:25px ;
    background-color: rgb(32, 32, 32);
    color: rgb(252, 252, 252);
    font-size: large;
    font-weight: bold;
    cursor: pointer;
}
button:hover{
    background-color: rgb(151, 141, 112);
}
.color{
    background-color: rgb(95, 94, 40);
}


#3.caculator.js 
let display=document.getElementById('display');

function appendtodisplay(input){
    display.value +=input;
}
function cleardisplay(){
    display.value='';
}
function calculate(){
    try{
        display.value=eval(display.value)

    }
    catch(error){
        display.value='error'
    }
}




