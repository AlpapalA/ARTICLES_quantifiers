<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Panna – Full Interactive Worksheet (Articles & Quantifiers)</title>
<style>
  body{font-family:Arial, sans-serif;background:#f4f6f8;padding:20px;line-height:1.45}
  .container{max-width:1100px;margin:auto;background:#fff;padding:26px 26px 10px;border-radius:14px;box-shadow:0 2px 10px rgba(0,0,0,.1)}
  h1{margin:0 0 6px}
  p{margin:6px 0 16px}
  h2{margin:26px 0 10px}
  .question{margin:12px 0;padding:14px;background:#fafafa;border-radius:10px;border:1px solid #eee}
  .qline{margin-bottom:8px}
  .grid2{display:grid;grid-template-columns:1fr 1fr;gap:10px}
  .grid3{display:grid;grid-template-columns:1fr 1fr 1fr;gap:10px}
  .small{font-size:14px;color:#555}
  .feedback{margin-top:8px}
  .correct{color:green;font-weight:bold}
  .wrong{color:#c0392b;font-weight:bold}
  input[type="text"], select{padding:7px;font-size:15px;border-radius:8px;border:1px solid #cfd6dd;width:100%;box-sizing:border-box}
  select{width:auto;min-width:110px}
  .inline{display:inline-block;vertical-align:middle}
  .nowrap{white-space:nowrap}
  .actions{display:flex;gap:10px;flex-wrap:wrap;margin:18px 0 10px}
  button{padding:12px 18px;border:none;border-radius:10px;background:#2c3e50;color:white;font-size:16px;cursor:pointer}
  button.secondary{background:#7f8c8d}
  .score{font-size:18px;margin:10px 0 18px;font-weight:bold}
  .locked input, .locked select{pointer-events:none;opacity:.85}
  .legend{display:flex;gap:14px;flex-wrap:wrap;margin:8px 0 0}
  .pill{padding:4px 10px;border-radius:999px;background:#eef2f5;font-size:13px;color:#34495e}
  .pill b{font-weight:700}
</style>
</head>
<body>
<div class="container" id="wrap">
  <h1>Panna – Interactive Worksheet (Full Page)</h1>
  <p class="small">Fill in all tasks. Click <b>Submit</b> to see feedback and the correct answers. (Task 6 is opinion-based → no automatic marking.)</p>
  <div class="legend">
    <div class="pill"><b>Tip:</b> Write short answers exactly (e.g., <span class="nowrap">the move</span>, <span class="nowrap">at school</span>).</div>
    <div class="pill"><b>Case:</b> Not important ("The" = "the").</div>
  </div>

  <form id="quizForm" autocomplete="off">

    <h2>1️⃣ Read the fact file and choose the correct alternative</h2>

    <div class="question" data-q="q1">
      <div class="qline">1. Panna is both ___ football move and ___ competitive game.</div>
      <div class="grid2">
        <div>
          <select name="q1a">
            <option value="">—</option><option value="a">a</option><option value="an">an</option><option value="the">the</option>
          </select>
          <span class="small">football move</span>
        </div>
        <div>
          <select name="q1b">
            <option value="">—</option><option value="a">a</option><option value="an">an</option><option value="the">the</option>
          </select>
          <span class="small">competitive game</span>
        </div>
      </div>
      <div class="feedback" id="f_q1"></div>
    </div>

    <div class="question" data-q="q2">
      <div class="qline">2. Panna originated in ___ Suriname, in ___ early 2000s.</div>
      <div class="grid2">
        <div>
          <select name="q2a">
            <option value="">—</option><option value="-">(no article)</option><option value="the">the</option><option value="a">a</option>
          </select>
          <span class="small">Suriname</span>
        </div>
        <div>
          <select name="q2b">
            <option value="">—</option><option value="the">the</option><option value="-">(no article)</option><option value="a">a</option>
          </select>
          <span class="small">early 2000s</span>
        </div>
      </div>
      <div class="feedback" id="f_q2"></div>
    </div>

    <div class="question" data-q="q3">
      <div class="qline">3. ___ rules of the competitive game were formally agreed in 2007.</div>
      <select name="q3"><option value="">—</option><option value="a">a</option><option value="an">an</option><option value="the">the</option></select>
      <div class="feedback" id="f_q3"></div>
    </div>

    <div class="question" data-q="q4">
      <div class="qline">4. Panna is played inside ___ six-metre circle, with a short fence or net.</div>
      <select name="q4"><option value="">—</option><option value="a">a</option><option value="an">an</option><option value="the">the</option></select>
      <div class="feedback" id="f_q4"></div>
    </div>

    <div class="question" data-q="q5">
      <div class="qline">5. ___ pitch is a six-metre circle.</div>
      <select name="q5"><option value="">—</option><option value="a">a</option><option value="an">an</option><option value="the">the</option></select>
      <div class="feedback" id="f_q5"></div>
    </div>

    <div class="question" data-q="q6">
      <div class="qline">6. ___ most skilled players demonstrate complicated moves.</div>
      <select name="q6"><option value="">—</option><option value="a">a</option><option value="an">an</option><option value="the">the</option></select>
      <div class="feedback" id="f_q6"></div>
    </div>

    <div class="question" data-q="q7">
      <div class="qline">7. Loud street music, live commentary and close proximity of the spectators all give matches ___ exciting atmosphere.</div>
      <select name="q7"><option value="">—</option><option value="a">a</option><option value="an">an</option><option value="the">the</option></select>
      <div class="feedback" id="f_q7"></div>
    </div>


    <h2>2️⃣ Complete the rules about the use of articles</h2>
    <p class="small">Choose the correct alternative and add the <b>highlighted examples</b> from the fact file in Ex 1.</p>

    <div class="question" data-q="q2A">
      <div class="qline">A. We use <select name="q2A_art"><option value="">—</option><option value="a">a/an</option><option value="the">the</option><option value="-">zero (no article)</option></select>
      <span class="small">when there is only one of something, or for a specific example, e.g.</span></div>
      <input type="text" name="q2A_ex" placeholder="Type an example from Ex 1 (e.g. the move)" />
      <div class="feedback" id="f_q2A"></div>
    </div>

    <div class="question" data-q="q2B">
      <div class="qline">B. We use <select name="q2B_first"><option value="">—</option><option value="a">a/an</option><option value="the">the</option><option value="-">zero</option></select>
      <span class="small">when we mention something for the first time, and then</span>
      <select name="q2B_next"><option value="">—</option><option value="a">a/an</option><option value="the">the</option><option value="-">zero</option></select>
      <span class="small">for further references to the same thing, e.g.</span></div>
      <div class="grid2">
        <input type="text" name="q2B_ex1" placeholder="first mention (e.g. a six-metre circle)" />
        <input type="text" name="q2B_ex2" placeholder="later reference (e.g. the pitch)" />
      </div>
      <div class="feedback" id="f_q2B"></div>
    </div>

    <div class="question" data-q="q2C">
      <div class="qline">C. We use <select name="q2C_art"><option value="">—</option><option value="a">a/an</option><option value="the">the</option><option value="-">zero</option></select>
      <span class="small">when we mean an example of something and we don’t need to be more definite, e.g.</span></div>
      <input type="text" name="q2C_ex" placeholder="Type an example from Ex 1 (e.g. a football move)" />
      <div class="feedback" id="f_q2C"></div>
    </div>

    <div class="question" data-q="q2D">
      <div class="qline">D. We use <select name="q2D_art"><option value="">—</option><option value="a">a/an</option><option value="the">the</option><option value="-">zero</option></select>
      <span class="small">with superlatives, e.g.</span></div>
      <input type="text" name="q2D_ex" placeholder="Type an example from Ex 1 (e.g. the most skilled players)" />
      <div class="feedback" id="f_q2D"></div>
    </div>

    <div class="question" data-q="q2E">
      <div class="qline">E. We use <select name="q2E_art"><option value="">—</option><option value="a">a/an</option><option value="the">the</option><option value="-">zero</option></select>
      <span class="small">with words like school/college/work when we talk about their purpose as an institution, e.g.</span></div>
      <input type="text" name="q2E_ex" placeholder="Type an example from Ex 1 (e.g. at school)" />
      <div class="feedback" id="f_q2E"></div>
    </div>

    <div class="question" data-q="q2F">
      <div class="qline">F. We use <select name="q2F_art"><option value="">—</option><option value="a">a/an</option><option value="the">the</option><option value="-">zero</option></select>
      <span class="small">for most towns, cities, regions and countries, e.g.</span></div>
      <input type="text" name="q2F_ex" placeholder="Type an example from Ex 1 (e.g. Suriname / South America / the Netherlands)" />
      <div class="feedback" id="f_q2F"></div>
    </div>

    <div class="question" data-q="q2G">
      <div class="qline">G. We use <select name="q2G_art"><option value="">—</option><option value="a">a/an</option><option value="the">the</option><option value="-">zero</option></select>
      <span class="small">when we talk about something in general, e.g.</span></div>
      <input type="text" name="q2G_ex" placeholder="Type an example from Ex 1 (e.g. Panna is gaining popularity.)" />
      <div class="feedback" id="f_q2G"></div>
    </div>

    <div class="question" data-q="q2H">
      <div class="qline">H. We use <select name="q2H_art"><option value="">—</option><option value="a">a/an</option><option value="the">the</option><option value="-">zero</option></select>
      <span class="small">with an adjective to refer to everyone who has that characteristic, e.g.</span></div>
      <input type="text" name="q2H_ex" placeholder="Type an example from Ex 1 (e.g. the elite)" />
      <div class="feedback" id="f_q2H"></div>
    </div>


    <h2>3️⃣ Correct the article mistakes</h2>
    <p class="small">Rewrite each sentence by correcting only the article mistakes.</p>

    <div class="question" data-q="q3_1">
      <div class="qline">1. Road tennis is exciting sport to watch. Spectators can get very close to an action.</div>
      <input type="text" name="q3_1" placeholder="Type the corrected sentence" />
      <div class="feedback" id="f_q3_1"></div>
    </div>

    <div class="question" data-q="q3_2">
      <div class="qline">2. Martin goes swimming after a work on Tuesdays. He particularly likes an outdoor pool near his office.</div>
      <input type="text" name="q3_2" placeholder="Type the corrected sentence" />
      <div class="feedback" id="f_q3_2"></div>
    </div>

    <div class="question" data-q="q3_3">
      <div class="qline">3. In ski jumping competitions, you score the points for a longest jump.</div>
      <input type="text" name="q3_3" placeholder="Type the corrected sentence" />
      <div class="feedback" id="f_q3_3"></div>
    </div>

    <div class="question" data-q="q3_4">
      <div class="qline">4. Panna is extremely popular in Netherlands, which has the large Surinamese population.</div>
      <input type="text" name="q3_4" placeholder="Type the corrected sentence" />
      <div class="feedback" id="f_q3_4"></div>
    </div>

    <div class="question" data-q="q3_5">
      <div class="qline">5. Snowboarding is not for a shy. You need a self-confidence.</div>
      <input type="text" name="q3_5" placeholder="Type the corrected sentence" />
      <div class="feedback" id="f_q3_5"></div>
    </div>

    <div class="question" data-q="q3_6">
      <div class="qline">6. Georgia can do football move called ‘around the world’. What’s best move you can do?</div>
      <input type="text" name="q3_6" placeholder="Type the corrected sentence" />
      <div class="feedback" id="f_q3_6"></div>
    </div>

    <div class="question" data-q="q3_7">
      <div class="qline">7. Because a pitch is small, panna is great for the players who cannot run long distances.</div>
      <input type="text" name="q3_7" placeholder="Type the corrected sentence" />
      <div class="feedback" id="f_q3_7"></div>
    </div>

    <div class="question" data-q="q3_8">
      <div class="qline">8. ‘Can you play a basketball this evening?’ ‘No, I have to stay in a college until 6.30.’</div>
      <input type="text" name="q3_8" placeholder="Type the corrected sentence" />
      <div class="feedback" id="f_q3_8"></div>
    </div>


    <h2>4️⃣ Find quantifiers</h2>
    <p class="small">Read the first two paragraphs of the fact file again. Write five examples of <b>quantifiers</b> you can find.</p>

    <div class="question" data-q="q4q">
      <div class="grid3">
        <input type="text" name="q4_1" placeholder="Quantifier 1" />
        <input type="text" name="q4_2" placeholder="Quantifier 2" />
        <input type="text" name="q4_3" placeholder="Quantifier 3" />
        <input type="text" name="q4_4" placeholder="Quantifier 4" />
        <input type="text" name="q4_5" placeholder="Quantifier 5" />
      </div>
      <div class="feedback" id="f_q4"></div>
    </div>


    <h2>5️⃣ Quantifiers – replace the bold words</h2>
    <p class="small">Use the phrases below so that the meaning does not change:<br>
      <b>a great deal</b> · <b>every one of us</b> · <b>few</b> · <b>much</b> · <b>none of us</b> · <b>some</b>
    </p>

    <div class="question" data-q="q5_1">
      <div class="qline">1. A game of panna doesn’t take up <b>a lot of</b> time, but mastering the skills takes real commitment.</div>
      <input type="text" name="q5_1" placeholder="Replace the bold part" />
      <div class="feedback" id="f_q5_1"></div>
    </div>

    <div class="question" data-q="q5_2">
      <div class="qline">2. <b>Several</b> famous football teams use yoga to increase their players’ flexibility.</div>
      <input type="text" name="q5_2" placeholder="Replace the bold part" />
      <div class="feedback" id="f_q5_2"></div>
    </div>

    <div class="question" data-q="q5_3">
      <div class="qline">3. Gymnastics requires <b>a lot of</b> skill.</div>
      <input type="text" name="q5_3" placeholder="Replace the bold part" />
      <div class="feedback" id="f_q5_3"></div>
    </div>

    <div class="question" data-q="q5_4">
      <div class="qline">4. <b>Everyone</b> wants squash to be an Olympic sport.</div>
      <input type="text" name="q5_4" placeholder="Replace the bold part" />
      <div class="feedback" id="f_q5_4"></div>
    </div>

    <div class="question" data-q="q5_5">
      <div class="qline">5. <b>Not many</b> people around here have tried the sport of climbing.</div>
      <input type="text" name="q5_5" placeholder="Replace the bold part" />
      <div class="feedback" id="f_q5_5"></div>
    </div>

    <div class="question" data-q="q5_6">
      <div class="qline">6. We love watching tennis, but <b>no one here</b> has ever played a tennis match.</div>
      <input type="text" name="q5_6" placeholder="Replace the bold part" />
      <div class="feedback" id="f_q5_6"></div>
    </div>


    <h2>6️⃣ Complete the sentences using your own opinions</h2>
    <p class="small">Include articles where necessary. (No automatic checking.)</p>

    <div class="question">
      1. The team sport I like best is <input type="text" /> because <input type="text" />
    </div>
    <div class="question">
      2. Brand new sports, like panna, are interesting because <input type="text" />
    </div>
    <div class="question">
      3. Sport provision at school is vital because <input type="text" />
    </div>
    <div class="question">
      4. If I could add one new sport to my school curriculum, it would be <input type="text" /> because <input type="text" />
    </div>


    <div class="actions">
      <button type="button" onclick="checkAnswers()">Submit</button>
      <button type="button" class="secondary" onclick="resetAll()">Try again</button>
    </div>

    <div class="score" id="score"></div>

  </form>
</div>

<script>
  const norm = (s) => (s ?? "").toString().trim().toLowerCase().replace(/\s+/g," ");
  const normSentence = (s) => norm(s).replace(/[“”"'’]/g, "'").replace(/\s*([,?.!])\s*/g, "$1 ").trim();

  function mark(elId, ok, correctText){
    const el = document.getElementById(elId);
    if(!el) return;
    el.innerHTML = ok
      ? `<span class="correct">✔ Correct</span>`
      : `<span class="wrong">✘ Correct answer: ${correctText}</span>`;
  }

  function anyMatch(user, accepted){
    const u = norm(user);
    return accepted.map(norm).includes(u);
  }

  function checkAnswers(){
    const wrap = document.getElementById('wrap');
    wrap.classList.add('locked');

    // Exercise 1 (articles)
    const ex1 = {
      q1a: {type:'select', accepted:['a']},
      q1b: {type:'select', accepted:['a']},
      q2a: {type:'select', accepted:['-']},
      q2b: {type:'select', accepted:['the']},
      q3:  {type:'select', accepted:['the']},
      q4:  {type:'select', accepted:['a']},
      q5:  {type:'select', accepted:['the']},
      q6:  {type:'select', accepted:['the']},
      q7:  {type:'select', accepted:['an']}
    };

    // Exercise 2 (rules + examples from the fact file)
    const ex2 = {
      q2A_art:{type:'select', accepted:['the']},
      q2A_ex:{type:'text', accepted:['the move']},

      q2B_first:{type:'select', accepted:['a']},
      q2B_next:{type:'select', accepted:['the']},
      q2B_ex1:{type:'text', accepted:['a six-metre circle','a six metre circle']},
      q2B_ex2:{type:'text', accepted:['the pitch']},

      q2C_art:{type:'select', accepted:['a']},
      q2C_ex:{type:'text', accepted:['a football move','a competitive game']},

      q2D_art:{type:'select', accepted:['the']},
      q2D_ex:{type:'text', accepted:['the most skilled players','the elite']},

      q2E_art:{type:'select', accepted:['-']},
      q2E_ex:{type:'text', accepted:['at school']},

      q2F_art:{type:'select', accepted:['-']},
      q2F_ex:{type:'text', accepted:['suriname','south america','the netherlands']},

      q2G_art:{type:'select', accepted:['-']},
      q2G_ex:{type:'text', accepted:['panna is gaining popularity','panna is designed for urban life']},

      q2H_art:{type:'select', accepted:['the']},
      q2H_ex:{type:'text', accepted:['the elite']}
    };

    // Exercise 3 (corrected sentences) — article mistakes only
    const ex3 = {
      q3_1:{accepted:["road tennis is an exciting sport to watch. spectators can get very close to the action."]},
      q3_2:{accepted:["martin goes swimming after work on tuesdays. he particularly likes an outdoor pool near his office."]},
      q3_3:{accepted:["in ski jumping competitions, you score the points for the longest jump."]},
      q3_4:{accepted:["panna is extremely popular in the netherlands, which has a large surinamese population."]},
      q3_5:{accepted:["snowboarding is not for the shy. you need self-confidence."]},
      q3_6:{accepted:["georgia can do a football move called 'around the world'. what's the best move you can do?"]},
      q3_7:{accepted:["because the pitch is small, panna is great for players who cannot run long distances."]},
      q3_8:{accepted:["'can you play basketball this evening?' 'no, i have to stay in college until 6.30.'"]}
    };

    // Exercise 5 replacements
    const ex5 = {
      q5_1:{accepted:['much']},
      q5_2:{accepted:['some']},
      q5_3:{accepted:['a great deal of','a great deal']},
      q5_4:{accepted:['every one of us']},
      q5_5:{accepted:['few']},
      q5_6:{accepted:['none of us']}
    };

    let total=0, correct=0;

    // ---- Marking helper
    function checkField(name, accepted){
      const el = document.querySelector(`[name="${name}"]`);
      if(!el) return {ok:true, skipped:true};
      const val = el.value;
      if(el.tagName.toLowerCase()==='select'){
        return {ok: anyMatch(val, accepted), val};
      }
      return {ok: anyMatch(val, accepted), val};
    }

    // ---- Exercise 1 feedback
    total += 9;
    const q1a = document.querySelector('[name=q1a]').value;
    const q1b = document.querySelector('[name=q1b]').value;
    const ok1 = (norm(q1a)==='a' && norm(q1b)==='a');
    if(ok1) correct++;
    mark('f_q1', ok1, 'a / a');

    const ok2 = (norm(document.querySelector('[name=q2a]').value)==='-' && norm(document.querySelector('[name=q2b]').value)==='the');
    if(ok2) correct++;
    mark('f_q2', ok2, '(no article) / the');

    ['q3','q4','q5','q6','q7'].forEach((q, idx)=>{
      const accepted = ex1[q].accepted;
      const res = checkField(q, accepted);
      if(res.ok) correct++;
      const mapId = {q3:'f_q3',q4:'f_q4',q5:'f_q5',q6:'f_q6',q7:'f_q7'}[q];
      mark(mapId, res.ok, accepted[0]);
    });

    // ---- Exercise 2 feedback
    const ex2Keys = Object.keys(ex2);
    total += ex2Keys.length;
    ex2Keys.forEach(k=>{
      const res = checkField(k, ex2[k].accepted);
      if(res.ok) correct++;
    });

    mark('f_q2A', checkField('q2A_art', ex2.q2A_art.accepted).ok && checkField('q2A_ex', ex2.q2A_ex.accepted).ok,
      'the + example: the move');

    const okB = checkField('q2B_first', ex2.q2B_first.accepted).ok && checkField('q2B_next', ex2.q2B_next.accepted).ok &&
                checkField('q2B_ex1', ex2.q2B_ex1.accepted).ok && checkField('q2B_ex2', ex2.q2B_ex2.accepted).ok;
    mark('f_q2B', okB, 'a … / the … (e.g. a six-metre circle → the pitch)');

    const okC = checkField('q2C_art', ex2.q2C_art.accepted).ok && checkField('q2C_ex', ex2.q2C_ex.accepted).ok;
    mark('f_q2C', okC, 'a/an + example: a football move');

    const okD = checkField('q2D_art', ex2.q2D_art.accepted).ok && checkField('q2D_ex', ex2.q2D_ex.accepted).ok;
    mark('f_q2D', okD, 'the + example: the most skilled players');

    const okE = checkField('q2E_art', ex2.q2E_art.accepted).ok && checkField('q2E_ex', ex2.q2E_ex.accepted).ok;
    mark('f_q2E', okE, 'zero + example: at school');

    const okF = checkField('q2F_art', ex2.q2F_art.accepted).ok && checkField('q2F_ex', ex2.q2F_ex.accepted).ok;
    mark('f_q2F', okF, 'zero + e.g. Suriname / South America');

    const okG = checkField('q2G_art', ex2.q2G_art.accepted).ok && checkField('q2G_ex', ex2.q2G_ex.accepted).ok;
    mark('f_q2G', okG, 'zero + e.g. Panna is gaining popularity.');

    const okH = checkField('q2H_art', ex2.q2H_art.accepted).ok && checkField('q2H_ex', ex2.q2H_ex.accepted).ok;
    mark('f_q2H', okH, 'the + example: the elite');

    // ---- Exercise 3 feedback
    const ex3Keys = Object.keys(ex3);
    total += ex3Keys.length;
    ex3Keys.forEach(k=>{
      const user = normSentence(document.querySelector(`[name=${k}]`).value);
      const ok = ex3[k].accepted.map(normSentence).includes(user);
      if(ok) correct++;
      mark(`f_${k}`, ok, ex3[k].accepted[0]);
    });

    // ---- Exercise 4 feedback (flexible: match any 3 of 5)
    // Model quantifiers from the first two paragraphs (as used on the page)
    const modelQuant = ['several','a number of','two','three','just'];
    const userQuant = ['q4_1','q4_2','q4_3','q4_4','q4_5'].map(n=>norm(document.querySelector(`[name=${n}]`).value)).filter(Boolean);
    const hits = [...new Set(userQuant)].filter(q=>modelQuant.includes(q)).length;
    // Count Exercise 4 as 5 items in total score, but give partial credit
    total += 5;
    correct += Math.min(hits,5);
    const ok4 = hits >= 3;
    document.getElementById('f_q4').innerHTML = ok4
      ? `<span class="correct">✔ Good! You found ${hits} model quantifier(s).</span> <span class="small">(Model answers: ${modelQuant.join(', ')})</span>`
      : `<span class="wrong">✘ You found ${hits} model quantifier(s).</span> <span class="small">Try: ${modelQuant.join(', ')}</span>`;

    // ---- Exercise 5 feedback
    const ex5Keys = Object.keys(ex5);
    total += ex5Keys.length;
    ex5Keys.forEach(k=>{
      const user = norm(document.querySelector(`[name=${k}]`).value);
      const ok = ex5[k].accepted.map(norm).includes(user);
      if(ok) correct++;
      mark(`f_${k}`, ok, ex5[k].accepted[0]);
    });

    document.getElementById('score').innerText = `Score: ${correct} / ${total} (Task 6 is not marked)`;
  }

  function resetAll(){
    const form = document.getElementById('quizForm');
    form.reset();
    document.getElementById('wrap').classList.remove('locked');
    // clear feedback
    [...document.querySelectorAll('.feedback')].forEach(el=>el.innerHTML='');
    document.getElementById('score').innerText='';
    // scroll to top
    window.scrollTo({top:0, behavior:'smooth'});
  }
</script>
</body>
</html>
