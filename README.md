

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Panna – Full Interactive Worksheet</title>
<style>
body{font-family:Arial, sans-serif;background:#f4f6f8;padding:20px;line-height:1.5}
.container{max-width:1000px;margin:auto;background:white;padding:25px;border-radius:12px;box-shadow:0 2px 10px rgba(0,0,0,0.1)}
h1{margin-top:0}
h2{margin-top:30px}
.question{margin:14px 0;padding:14px;background:#fafafa;border-radius:8px}
.correct{color:green;font-weight:bold}
.wrong{color:#c0392b;font-weight:bold}
.feedback{margin-top:6px}
input,select{padding:6px;font-size:15px;margin-top:4px}
button{margin-top:25px;padding:14px 22px;border:none;border-radius:10px;background:#2c3e50;color:white;font-size:16px;cursor:pointer}
.score{font-size:20px;margin-top:20px;font-weight:bold}
</style>
</head>
<body>
<div class="container">
<h1>Panna – FULL Interactive Worksheet</h1>
<p>Complete all exercises. Click <b>Submit</b> to see correct answers.</p>

<form id="quizForm">

<h2>1️⃣ Choose the correct article</h2>

<div class="question">1. Panna is both ___ football move and ___ competitive game.<br>
<select name="q1a"><option></option><option>a</option><option>an</option><option>the</option></select>
<select name="q1b"><option></option><option>a</option><option>an</option><option>the</option></select>
<div class="feedback" id="f1"></div></div>

<div class="question">2. Panna originated in ___ Suriname, in ___ early 2000s.<br>
<select name="q2a"><option></option><option>a</option><option>the</option><option>-</option></select>
<select name="q2b"><option></option><option>a</option><option>the</option><option>-</option></select>
<div class="feedback" id="f2"></div></div>

<div class="question">3. ___ rules of the competitive game were formally agreed in 2007.<br>
<select name="q3"><option></option><option>a</option><option>an</option><option>the</option></select>
<div class="feedback" id="f3"></div></div>

<div class="question">4. Panna is played inside ___ circular court.<br>
<select name="q4"><option></option><option>a</option><option>an</option><option>the</option></select>
<div class="feedback" id="f4"></div></div>

<div class="question">5. ___ most skilled players demonstrate complicated moves.<br>
<select name="q5"><option></option><option>A</option><option>An</option><option>The</option></select>
<div class="feedback" id="f5"></div></div>

<div class="question">6. Spectators create ___ exciting atmosphere.<br>
<select name="q6"><option></option><option>a</option><option>an</option><option>the</option></select>
<div class="feedback" id="f6"></div></div>

<h2>2️⃣ Complete the rules about articles</h2>

<div class="question">7. We use <input name="q7" type="text" placeholder="a / an / the"> when there is only one of something.
<div class="feedback" id="f7"></div></div>

<div class="question">8. We use zero article when we talk about something <input name="q8" type="text" placeholder="general / specific">.
<div class="feedback" id="f8"></div></div>

<div class="question">9. We use the with superlatives, e.g. <input name="q9" type="text" placeholder="the best / the biggest">.
<div class="feedback" id="f9"></div></div>

<h2>3️⃣ Correct the article mistakes</h2>

<div class="question">10. Road tennis is <input name="q10" type="text" placeholder="article"> exciting sport to watch.
<div class="feedback" id="f10"></div></div>

<div class="question">11. Snowboarding is not <input name="q11" type="text" placeholder="article"> sport for you.
<div class="feedback" id="f11"></div></div>

<h2>4️⃣ Quantifiers</h2>

<div class="question">12. A game of panna doesn’t take <input name="q12" type="text" placeholder="quantifier"> of time.
<div class="feedback" id="f12"></div></div>

<div class="question">13. <input name="q13" type="text" placeholder="quantifier"> famous football teams use yoga.
<div class="feedback" id="f13"></div></div>

<div class="question">14. <input name="q14" type="text" placeholder="quantifier"> people here have tried climbing.
<div class="feedback" id="f14"></div></div>

<h2>5️⃣ Your opinion (no automatic checking)</h2>

<div class="question">15. The team sport I like best is <input type="text"> because <input type="text"></div>
<div class="question">16. If I could add one new sport to school, it would be <input type="text"> because <input type="text"></div>

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
q6:"an",
q7:"the",
q8:"general",
q9:"the best",
q10:"an",
q11:"a",
q12:"a lot",
q13:"Several",
q14:"Not many"
};

let total=0;let correct=0;
for(let key in answers){
let el=document.querySelector(`[name=${key}]`);
if(!el)continue;
total++;
if(el.value.trim()==answers[key]) correct++;
}

function mark(id,val,ans){
const el=document.getElementById(id);
if(!el)return;
el.innerHTML=(val==ans)?"<span class='correct'>✔ Correct</span>":`<span class='wrong'>✘ Correct: ${ans}</span>`;
}

mark("f1",document.querySelector('[name=q1a]').value+"/"+document.querySelector('[name=q1b]').value,"a/a");
mark("f2",document.querySelector('[name=q2a]').value+"/"+document.querySelector('[name=q2b]').value,"-/the");
mark("f3",document.querySelector('[name=q3]').value,"the");
mark("f4",document.querySelector('[name=q4]').value,"a");
mark("f5",document.querySelector('[name=q5]').value,"The");
mark("f6",document.querySelector('[name=q6]').value,"an");
mark("f7",document.querySelector('[name=q7]').value,"the");
mark("f8",document.querySelector('[name=q8]').value,"general");
mark("f9",document.querySelector('[name=q9]').value,"the best");
mark("f10",document.querySelector('[name=q10]').value,"an");
mark("f11",document.querySelector('[name=q11]').value,"a");
mark("f12",document.querySelector('[name=q12]').value,"a lot");
mark("f13",document.querySelector('[name=q13]').value,"Several");
mark("f14",document.querySelector('[name=q14]').value,"Not many");

document.getElementById("score").innerText=`Score: ${correct} / ${total}`;
}
</script>
</body>
</html>
