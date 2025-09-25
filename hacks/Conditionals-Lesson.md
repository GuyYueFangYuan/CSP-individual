---
permalink: /studentBlogs/conditionals
title: All About Conditionals — Beginner to Pro
---

<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>{{ page.title }}</title>
  <style>
    body { background-color: black; color: white; font-family: Arial, sans-serif; margin: 0; padding: 0; }
    a { color: white; text-decoration: none; }
    a:visited { color: grey; }
    .wrap { width: min(1100px, 94%); margin: 40px auto; }
    .header { display: flex; align-items: center; justify-content: space-between; padding: 10px 0; }
    .back-button { background-color: black; color: white; border: 1px solid white; padding: 10px 20px; cursor: pointer; font-size: 16px; text-decoration: none; }
    .back-button:hover { background-color: gray; }

    .card { background-color: #111; border: 1px solid #333; border-left: 5px solid #777; padding: 18px; margin: 16px 0; }
    .title { font-size: clamp(28px, 4vw, 40px); font-weight: 800; margin: 0 0 6px; }
    .sub { color: #bbb; margin: 4px 0 14px; }
    h2 { margin: 10px 0; }
    h3 { margin: 10px 0; }
    pre { background: #0b1526; color: #e6eef6; padding: 14px; border-radius: 8px; border: 1px solid #1e2a44; overflow: auto; }
    code { font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Courier New", monospace; }
    .pill { display: inline-block; padding: 6px 10px; border-radius: 999px; font-size: 12px; border: 1px solid #555; color: #ccc; }
    .btn { appearance: none; border: 1px solid #444; background: #1d2533; color: #fff; padding: 8px 12px; border-radius: 10px; cursor: pointer; font-weight: 600; }
    .btn:active { transform: translateY(1px); }
    input, select { background: #0b1526; color: #fff; border: 1px solid #23324f; border-radius: 8px; padding: 6px 8px; }
    .row { display: flex; gap: 10px; align-items: center; flex-wrap: wrap; }
    .muted { color: #bbb; }
    .ok { color: #22c55e; }
    .warn { color: #f59e0b; }
    .bad { color: #ef4444; }
  </style>
</head>
<body>
  <div class="wrap">
    <div class="header">
      <h1 class="title">🌟 All About <span style="color:#7dd3fc">Conditionals</span></h1>
      <a class="back-button" href="{{ site.baseurl }}/studentBlogs/">← Back to Blogs</a>
    </div>
    <p class="sub">Make your programs think and choose — a complete beginner‑friendly guide with interactive demos.</p>

    <div class="card">
      <h2>Core Idea</h2>
      <p class="muted">Conditionals let programs make decisions. They check if something is <code>True</code> or <code>False</code> and choose which path to run.</p>
      <h3>Generic Structure (Pseudocode)</h3>
<pre><code>IF &lt;condition&gt; THEN
    &lt;do something&gt;
ELSE
    &lt;do something else&gt;
END IF
</code></pre>
      <h3>Python</h3>
<pre><code>if condition:
    # do something
else:
    # do something else
</code></pre>
      <h3>JavaScript</h3>
<pre><code>if (condition) {
  // do something
} else {
  // do something else
}
</code></pre>
    </div>

    <div class="card">
      <h2>Building Blocks</h2>
      <h3>IF only</h3>
<pre><code>age = 18
if age &gt;= 16:
    print("You can drive!")
</code></pre>
      <h3>IF–ELSE</h3>
<pre><code>age = 14
if age &gt;= 16:
    print("You can drive!")
else:
    print("Not yet.")
</code></pre>
      <h3>IF–ELIF–ELSE</h3>
<pre><code>score = 85
if score &gt;= 90:
    print("A")
elif score &gt;= 80:
    print("B")
elif score &gt;= 70:
    print("C")
else:
    print("D or F")
</code></pre>
      <h3>Nested</h3>
<pre><code>is_raining = True
has_umbrella = False

if is_raining:
    if has_umbrella:
        print("You stay dry")
    else:
        print("You get wet")
else:
    print("Clear skies")
</code></pre>
      <h3>Combining Logic</h3>
<pre><code>age = 20
has_ticket = True

if age &gt;= 18 and has_ticket:
    print("Welcome in!")
</code></pre>
    </div>

    <div class="card">
      <h2>Interactive Playground</h2>
      <h3>1) Grade Decider (IF–ELIF–ELSE)</h3>
      <div class="row" style="margin:8px 0 10px">
        <label for="score">Score</label>
        <input id="score" type="number" min="0" max="100" value="85" />
        <button class="btn" id="btnGrade">Evaluate</button>
        <span id="gradeOut" class="pill">Grade: —</span>
      </div>

      <h3>2) Weather Choice (Nested IF)</h3>
      <div class="row" style="margin:8px 0 10px">
        <label><input type="checkbox" id="isRaining" checked> Raining</label>
        <label><input type="checkbox" id="hasUmbrella"> Have umbrella</label>
        <button class="btn" id="btnWeather">Decide</button>
        <span id="weatherOut" class="pill">Decision: —</span>
      </div>

      <h3>3) Logic Lab (and / or / not)</h3>
      <div class="row" style="gap:14px; margin:8px 0 10px">
        <label>A <select id="A"><option>true</option><option>false</option></select></label>
        <label>B <select id="B"><option>true</option><option>false</option></select></label>
        <label>Expr
          <select id="expr">
            <option value="A && B">A and B</option>
            <option value="A || B">A or B</option>
            <option value="!(A && B)">not (A and B)</option>
            <option value="!(A || B)">not (A or B)</option>
            <option value="A && !B">A and not B</option>
            <option value="A ^ B">A xor B</option>
          </select>
        </label>
        <button class="btn" id="btnLogic">Run</button>
        <span id="logicOut" class="pill">Result: —</span>
      </div>
      <p class="muted">Use these like a mini REPL to see how branching behaves.</p>
    </div>

    <div class="card">
      <h2>Common Pitfalls</h2>
      <ul>
        <li><strong>Assignment vs comparison:</strong> <code>=</code> sets a value; <code>==</code> compares.</li>
        <li><strong>Order matters:</strong> First true branch in IF–ELIF–ELSE runs; later branches are ignored.</li>
        <li><strong>Truthiness:</strong> Empty strings, 0, and <code>None/null</code> are often treated as false.</li>
        <li><strong>Deep nesting:</strong> Hard to read. Consider combining logic or returning early.</li>
      </ul>
    </div>

    <div class="card">
      <h2>Practice Prompts</h2>
      <ol>
        <li>Ask for age and output child/teen/adult.</li>
        <li>Ticket gate: allow entry if paid <em>and</em> has ID.</li>
        <li>Calculator: apply discounts based on subtotal tiers.</li>
        <li>Game: print "LEVEL UP" if XP ≥ 1000; else show XP needed.</li>
      </ol>
    </div>

    <p class="muted">© Your Name — Conditionals Primer</p>
  </div>

  <script>
    // Grade Decider
    function gradeFrom(score){
      if (score >= 90) return "A";
      else if (score >= 80) return "B";
      else if (score >= 70) return "C";
      else if (score >= 60) return "D";
      else return "F";
    }
    const scoreEl = document.getElementById('score');
    const btnGrade = document.getElementById('btnGrade');
    const gradeOut = document.getElementById('gradeOut');
    btnGrade?.addEventListener('click', () => {
      const n = Number(scoreEl.value);
      if (Number.isNaN(n) || n < 0 || n > 100){
        gradeOut.textContent = 'Grade: invalid score';
        gradeOut.className = 'pill warn';
        return;
      }
      gradeOut.textContent = 'Grade: ' + gradeFrom(n);
      gradeOut.className = 'pill ok';
    });

    // Weather Choice (nested)
    const isRaining = document.getElementById('isRaining');
    const hasUmbrella = document.getElementById('hasUmbrella');
    const btnWeather = document.getElementById('btnWeather');
    const weatherOut = document.getElementById('weatherOut');
    btnWeather?.addEventListener('click', () => {
      if (isRaining.checked){
        if (hasUmbrella.checked){
          weatherOut.textContent = 'Decision: Go outside with umbrella';
          weatherOut.className = 'pill ok';
        } else {
          weatherOut.textContent = 'Decision: Stay inside or you\'ll get wet';
          weatherOut.className = 'pill bad';
        }
      } else {
        weatherOut.textContent = 'Decision: Clear skies — enjoy!';
        weatherOut.className = 'pill ok';
      }
    });

    // Logic Lab
    function xor(a,b){ return (a || b) && !(a && b); }
    const A = document.getElementById('A');
    const B = document.getElementById('B');
    const expr = document.getElementById('expr');
    const btnLogic = document.getElementById('btnLogic');
    const logicOut = document.getElementById('logicOut');
    btnLogic?.addEventListener('click', () => {
      const a = A.value === 'true';
      const b = B.value === 'true';
      let val = false;
      switch(expr.value){
        case 'A && B': val = a && b; break;
        case 'A || B': val = a || b; break;
        case '!(A && B)': val = !(a && b); break;
        case '!(A || B)': val = !(a || b); break;
        case 'A && !B': val = a && !b; break;
        case 'A ^ B': val = xor(a,b); break;
      }
      logicOut.textContent = 'Result: ' + val;
      logicOut.className = 'pill ' + (val ? 'ok' : 'bad');
    });
  </script>
</body>
</html>
