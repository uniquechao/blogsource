title: 密码生成器
date: 2015-12-1 11:26:44
tags: 
- tools
categories:
- tools
  
----------

<title> 密码生成器</title>
<style>
@import url(http://fonts.useso.com/css?family=Open+Sans:400,600,300);
body,
html {
    background-image: url('http://cool.techbrood.com/uploads/150501/city-hazy-blurred-unsharp-night-rain-1920x1080.jpg');
    background-repeat: no-repeat;
    margin: 0 auto;
    height: 100%;
    overflow: hidden;
}
#overlay {
    background: rgba(0, 29, 49, 0.8);
    height: 100%;
    overflow: hidden;
}
#wrap {
    width: auto;
    height: 200px;
    margin-left: auto;
    margin-right: auto;
    margin-top: 100px;
}
hr {
    width: 35px;
    height: 2px;
    background-color: #8aaadf;
    border: none;
    margin-top: 10px;
}
h2 {
    color: white;
    font-family: 'Karla', sans-serif;
    text-transform: uppercase;
    text-align: center;
    font-size: 18px;
}
h1 {
    color: #3570b8;
    font-family: 'Open Sans', sans-serif;
    font-weight: 300;
    text-align: center;
    font-size: 25px;
    /* Boxes */
    
    width: 400px;
    margin-left: auto;
    margin-right: auto;
}
input[type=text] {
    background-color: rgba(0, 0, 0, 0.4);
    width: 200px;
    height: 40px;
    margin-left: auto;
    margin-right: auto;
    display: block;
    font-size: 30px;
    color: rgba(250, 250, 250, 0.7);
    text-align: center;
    border-radius: 5px;
    border: none;
}
input[type=button] {
    width: 100px;
    height: 40px;
    background-color: rgba(220, 20, 60, 0.8);
    margin-top: 20px;
    margin-left: auto;
    margin-right: auto;
    display: block;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}
input[type=text]:focus {
    box-shadow: 0px 0px 7px rgba(250, 250, 250, 0.3);
    outline: 0;
}
input[type=button]:focus {
    outline: 0;
}
</style>
<script>
var chars = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z', '0', '1', '2', '3', '4', '5', '6', '7', '8', '9', '@', '#', '!', '.', '&', '$'];

var exclure = ['azerty', 'qwerty']

function generer() {
    document.getElementById('add').value = main();
}

function randomize() {
    var index = Math.floor((Math.random() * 68));
    return index;
}

function generate() {
    var word = chars[randomize()] + chars[randomize()] + chars[randomize()] + chars[randomize()] + chars[randomize()] + chars[randomize()] + chars[randomize()] + chars[randomize()];
    return word;
}

function main() {
    var result = "";
    var trials = "";
    var counter = 0;
    do {
        result = generate();
        trials += result;
    } while (exclure.indexOf(result) >= 0);
    return trials;
}
</script>

<div id="overlay">
    <div id="wrap"> 
        <h2>Password generator</h2> 
        <h1>Generate your password!</h1>
        <INPUT TYPE="text" ID="add" NAME="result" ReadOnly VALUE="">
        <input type="button" value="Generate!" onclick="generer()">
    </div>
</div>