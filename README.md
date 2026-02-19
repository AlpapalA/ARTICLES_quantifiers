# AR<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Panna – Interactive Articles Worksheet</title>
<style>
body{font-family:Arial, sans-serif; background:#f4f6f8; padding:20px;}
.container{max-width:900px; margin:auto; background:white; padding:25px; border-radius:10px; box-shadow:0 2px 10px rgba(0,0,0,0.1);} 
h1{margin-top:0}
.question{margin:18px 0; padding:15px; background:#fafafa; border-radius:8px;}
.correct{color:green; font-weight:bold}
.wrong{color:#c0392b; font-weight:bold}
button{margin-top:20px; padding:12px 18px; border:none; border-radius:8px; background:#2c3e50; color:white; font-size:16px; cursor:pointer;}
.feedback{margin-top:8px;}
select, input{padding:6px; font-size:15px;}
.score{font-size:18px; margin-top:20px; font-weight:bold}
</style>
</head>
<body>
<div class="container">
<h1>Panna – Articles Interactive Worksheet</h1>
<p>Choose the correct articles. Click <b>Submit</b> to see feedback and correct answers.</p>

<form id="quizForm">

<div class="question">
1. Panna is both ___ football move and ___ competitive game.
<br>
<select name="q1a">
<option value="">--choose--</option>
<option>a</option>
<option>an</option>
<option>the</option>
</select>
<select name="q1b">
<option value="">--choose--</option>
<option>a</option>
<option>an</option>
<option>the</option>
</select>
<div class="feedback" id="f1"></div>
</div>

<div class="question">
2. Panna originated in ___ Suriname, in ___ early 2000s.
<br>
<select name="q2a">
<option value="">--choose--</option>
<option>a</option>
<option>the</option>
<option>-</option>
</select>
<select name="q2b">
<option value="">--choose--</option>
<option>a</option>
<option>the</option>
<option>-</option>
</select>
<div class="feedback" id="f2"></div>
</div>

<div class="question">
3. ___ rules of the competitive game were formally agreed in 2007.
<br>
<select name="q3">
<option value="">--choose--</option>
<option>a</option>
<option>an</option>
<option>the</option>
</select>
<div class="feedback" id="f3"></div>
</div>

<div class="question">
4. Panna is played inside ___ circular court.
<br>
<select name="q4">
<option value="">--choose--</option>
<option>a</option>
<option>an</option>
<option>the</option>
</select>
<div class="feedback" id="f4"></div>
</div>

<div class="question">
5. ___ most skilled players demonstrate complicated moves.
<br>
<select name="q5">
<option value="">--choose--</option>
<option>A</option>
<option>An</option>
<option>The</option>
</select>
<div class="feedback" id="f5"></div>
</div>

<div class="question">
6. Spectators create ___ exciting atmosphere.
<br>
<select name="q6">
<option value="">--choose--</option>
<option>a</option>
<option>an</option>
<option>the</option>
</select>
<div class="feedback" id="f6"></div>
</div>

<button type="button" onclick="checkAnswers()">Submit</button>

<div class="score" id="score"></div>

</form>
</div>

<script>
function checkAnswers(){

const answers={
q1a:"a",
q1b:"a",
q2a:"-",
q2b:"the",
q3:"the",
q4:"a",
q5:"The",
q6:"an"
};

let total=0;
let correct=0;

for(let key in answers){
 total++;
 let user=document.querySelector(`[name=${key}]`).value;
 if(user===answers[key]) correct++;
}

function mark(id,condition,text){
 const el=document.getElementById(id);
 el.innerHTML=condition?`<span class='correct'>✔ Correct</span>`:`<span class='wrong'>✘ Correct answer: ${text}</span>`;
}

mark("f1",document.querySelector('[name=q1a]').value==="a" && document.querySelector('[name=q1b]').value==="a","a / a");
mark("f2",document.querySelector('[name=q2a]').value==="-" && document.querySelector('[name=q2b]').value==="the","- / the");
mark("f3",document.querySelector('[name=q3]').value==="the","the");
mark("f4",document.querySelector('[name=q4]').value==="a","a");
mark("f5",document.querySelector('[name=q5]').value==="The","The");
mark("f6",document.querySelector('[name=q6]').value==="an","an");

 document.getElementById("score").innerText=`Score: ${correct} / ${total}`;
}
</script>

</body>
</html>
TICLES_quantifiers
