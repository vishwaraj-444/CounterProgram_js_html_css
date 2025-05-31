# CounterProgram_js_html_css

# HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Intreview</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <label id="countlabel">0</label> <br>
    <div id="btncontainer">
    <button id="decreseBtn" class="buttons" >decrese</button>
    <button id="resetBtn" class="buttons" >reset</button>
    <button id="increseBtn" class="buttons" >increse</button>
    </div>
    
<!-- --------------------------------------------------->
    <script src="index.js" defer></script>
</body>
</html> 

# CSS

#countlabel{
    display: block;
    text-align: center;
    font-size: 10em;
    font-family: Arial, Helvetica, sans-serif;
}
#btncontainer{
    text-align: center;
}
.buttons{
    padding: 10px 20px;
    font-size: 1.5em;
    color: whitesmoke;
    background-color: blueviolet;
    border-radius: 7px;
    cursor: pointer;
    transition: background-color 0.30s;
}
.buttons:hover{
    background-color: violet;
}

# JS

const decreseBtn = document.getElementById("decreseBtn");
const resetBtn = document.getElementById("resetBtn");
const increseBtn = document.getElementById("increseBtn");

let count=0;

increseBtn.onclick = function(){
    count++;
    countlabel.textContent = count;
}

decreseBtn.onclick = function(){
    count--;
    countlabel.textContent = count;
}

resetBtn.onclick = function(){
    count = 0;
    countlabel.textContent = count;
}
