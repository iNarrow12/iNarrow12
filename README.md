<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1"/>
<title>iNarrow12 — GitHub Profile</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;700&family=Orbitron:wght@700;900&display=swap');

  *{margin:0;padding:0;box-sizing:border-box;}

  body{
    background:#0d1117;
    color:#c9d1d9;
    font-family:'Fira Code',monospace;
    min-height:100vh;
  }

  /* ── WAVE HEADER ── */
  .wave-header{
    background:linear-gradient(135deg,#0f3460,#16213e,#1a1a2e,#0f3460);
    background-size:400% 400%;
    animation:gradShift 6s ease infinite;
    padding:50px 20px 30px;
    text-align:center;
    position:relative;
    overflow:hidden;
  }
  .wave-header::after{
    content:'';
    position:absolute;
    bottom:-2px;left:0;right:0;height:60px;
    background:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1440 60'%3E%3Cpath fill='%230d1117' d='M0,30 C360,60 1080,0 1440,30 L1440,60 L0,60Z'/%3E%3C/svg%3E") no-repeat bottom;
    background-size:cover;
  }
  @keyframes gradShift{0%{background-position:0% 50%}50%{background-position:100% 50%}100%{background-position:0% 50%}}

  /* ── 3D NAME ── */
  .big-name{
    font-family:'Orbitron',monospace;
    font-size:clamp(2.4rem,8vw,5.5rem);
    font-weight:900;
    letter-spacing:4px;
    background:linear-gradient(90deg,#00f7ff,#a855f7,#ff6b6b,#00f7ff);
    background-size:300%;
    -webkit-background-clip:text;
    -webkit-text-fill-color:transparent;
    background-clip:text;
    animation:nameShimmer 3s linear infinite;
    text-shadow:none;
    filter:drop-shadow(0 0 30px #00f7ff88);
  }
  @keyframes nameShimmer{0%{background-position:0%}100%{background-position:300%}}

  .subtitle{
    font-size:1rem;
    color:#a0aec0;
    letter-spacing:3px;
    margin-top:10px;
    text-transform:uppercase;
  }

  /* ── TYPING ── */
  .typing-wrap{
    text-align:center;
    margin:24px auto 0;
    height:36px;
  }
  .typing{
    font-size:1.1rem;
    color:#00f7ff;
    border-right:2px solid #00f7ff;
    white-space:nowrap;
    overflow:hidden;
    display:inline-block;
    animation:blink .7s step-end infinite;
  }
  @keyframes blink{50%{border-color:transparent}}

  /* ── NEON DIVIDER ── */
  .divider{
    height:2px;
    margin:36px auto;
    max-width:900px;
    background:linear-gradient(90deg,transparent,#00f7ff,#a855f7,#ff6b6b,#00f7ff,transparent);
    background-size:200%;
    animation:divMove 2s linear infinite;
    border-radius:2px;
    box-shadow:0 0 12px #00f7ff66;
  }
  @keyframes divMove{0%{background-position:0%}100%{background-position:200%}}

  /* ── MAIN CONTAINER ── */
  .container{max-width:900px;margin:0 auto;padding:0 20px 60px;}

  /* ── SECTION TITLE ── */
  .sec-title{
    font-family:'Orbitron',monospace;
    font-size:1.1rem;
    color:#00f7ff;
    letter-spacing:2px;
    margin-bottom:20px;
    display:flex;align-items:center;gap:10px;
  }
  .sec-title::after{
    content:'';flex:1;height:1px;
    background:linear-gradient(90deg,#00f7ff44,transparent);
  }

  /* ── WHOAMI CARD ── */
  .whoami-grid{
    display:grid;
    grid-template-columns:1fr auto;
    gap:24px;
    align-items:start;
  }
  .terminal{
    background:#010409;
    border:1px solid #30363d;
    border-radius:12px;
    overflow:hidden;
    box-shadow:0 0 30px #00f7ff22, 0 8px 32px #00000088;
    transform:perspective(800px) rotateY(-2deg);
    transition:transform .3s;
  }
  .terminal:hover{transform:perspective(800px) rotateY(0deg);}
  .term-bar{
    background:#161b22;
    padding:10px 16px;
    display:flex;align-items:center;gap:8px;
  }
  .dot{width:12px;height:12px;border-radius:50%;}
  .dot-r{background:#ff5f57;} .dot-y{background:#febc2e;} .dot-g{background:#28c840;}
  .term-title{flex:1;text-align:center;font-size:.75rem;color:#6e7681;}
  .term-body{padding:20px;font-size:.82rem;line-height:1.9;}
  .prompt{color:#a855f7;} .cmd{color:#00f7ff;} .val{color:#7ee787;}
  .key{color:#ff79c6;} .arrow{color:#6e7681;}

  .hacker-gif{
    border-radius:12px;
    border:2px solid #00f7ff44;
    box-shadow:0 0 30px #00f7ff33;
    width:220px;
    object-fit:cover;
    transform:perspective(600px) rotateY(4deg);
    transition:transform .3s;
  }
  .hacker-gif:hover{transform:perspective(600px) rotateY(0deg);}

  /* ── PYTHON CARD ── */
  .code-block{
    background:#010409;
    border:1px solid #30363d;
    border-radius:12px;
    overflow:hidden;
    box-shadow:0 0 30px #a855f722, 0 8px 32px #00000088;
  }
  .code-bar{
    background:#161b22;
    padding:10px 16px;
    display:flex;align-items:center;gap:10px;
    font-size:.75rem;color:#6e7681;
  }
  .lang-dot{width:10px;height:10px;border-radius:50%;background:#3572A5;}
  .code-body{padding:20px;font-size:.82rem;line-height:1.9;overflow-x:auto;}
  .kw{color:#ff79c6;} .fn{color:#d2a8ff;} .st{color:#a5d6ff;}
  .cm{color:#6e7681;font-style:italic;} .num{color:#79c0ff;}

  /* ── BADGES ── */
  .badge-grid{
    display:flex;flex-wrap:wrap;gap:10px;justify-content:center;
  }
  .badge{
    display:inline-flex;align-items:center;gap:6px;
    padding:7px 14px;border-radius:8px;
    font-size:.78rem;font-weight:700;letter-spacing:.5px;
    border:1px solid #30363d;
    transition:transform .2s,box-shadow .2s;
    cursor:default;
  }
  .badge:hover{transform:translateY(-3px) scale(1.05);box-shadow:0 6px 20px #00f7ff33;}
  .badge-icon{font-size:1rem;}

  /* ── STATS GRID ── */
  .stats-grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:20px;
  }
  .stat-card{
    background:#010409;
    border:1px solid #30363d;
    border-radius:12px;
    padding:22px;
    text-align:center;
    position:relative;
    overflow:hidden;
    transition:transform .3s,box-shadow .3s;
  }
  .stat-card:hover{
    transform:translateY(-6px) perspective(600px) rotateX(4deg);
    box-shadow:0 16px 40px #00f7ff33;
  }
  .stat-card::before{
    content:'';position:absolute;top:0;left:0;right:0;height:2px;
    background:linear-gradient(90deg,#00f7ff,#a855f7);
  }
  .stat-num{font-family:'Orbitron',monospace;font-size:2rem;color:#00f7ff;font-weight:700;}
  .stat-label{font-size:.75rem;color:#6e7681;margin-top:4px;letter-spacing:1px;text-transform:uppercase;}
  .stat-icon{font-size:1.6rem;margin-bottom:8px;}

  /* ── TROPHIES ── */
  .trophy-row{display:flex;gap:14px;flex-wrap:wrap;justify-content:center;}
  .trophy{
    background:linear-gradient(135deg,#1a1a2e,#16213e);
    border:1px solid #30363d;
    border-radius:12px;
    padding:16px 20px;
    text-align:center;
    min-width:100px;
    transition:transform .3s,box-shadow .3s;
  }
  .trophy:hover{
    transform:translateY(-8px) rotateZ(-1deg);
    box-shadow:0 12px 30px #a855f744;
    border-color:#a855f7;
  }
  .trophy-icon{font-size:2rem;display:block;margin-bottom:6px;}
  .trophy-name{font-size:.7rem;color:#a0aec0;letter-spacing:.5px;}

  /* ── QUOTE ── */
  .quote-box{
    border:1px solid #00f7ff44;
    border-left:4px solid #00f7ff;
    border-radius:0 12px 12px 0;
    padding:20px 28px;
    background:#010409;
    text-align:center;
    color:#a0aec0;
    font-style:italic;
    font-size:1rem;
    letter-spacing:.5px;
    box-shadow:0 0 30px #00f7ff11;
  }
  .quote-box span{color:#00f7ff;font-style:normal;font-weight:700;}

  /* ── WAVE FOOTER ── */
  .wave-footer{
    background:linear-gradient(135deg,#1a1a2e,#0f3460,#16213e);
    background-size:400% 400%;
    animation:gradShift 6s ease infinite;
    padding:30px 20px;
    text-align:center;
    margin-top:60px;
    position:relative;
    overflow:hidden;
  }
  .wave-footer::before{
    content:'';
    position:absolute;
    top:-2px;left:0;right:0;height:60px;
    background:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1440 60'%3E%3Cpath fill='%230d1117' d='M0,30 C360,0 1080,60 1440,30 L1440,0 L0,0Z'/%3E%3C/svg%3E") no-repeat top;
    background-size:cover;
  }
  .views-badge{
    display:inline-block;
    background:#00f7ff11;
    border:1px solid #00f7ff44;
    border-radius:20px;
    padding:6px 18px;
    font-size:.8rem;
    color:#00f7ff;
    letter-spacing:1px;
    margin-top:16px;
  }

  @media(max-width:640px){
    .whoami-grid{grid-template-columns:1fr;}
    .hacker-gif{width:100%;height:180px;}
    .stats-grid{grid-template-columns:1fr;}
  }
</style>
</head>
<body>

<!-- WAVE HEADER -->
<div class="wave-header">
  <div class="big-name">iNarrow12</div>
  <div class="subtitle">Network Engineer &nbsp;|&nbsp; Ethical Hacker &nbsp;|&nbsp; NIBM 🇱🇰</div>
</div>

<!-- TYPING ANIMATION -->
<div class="typing-wrap">
  <span class="typing" id="typer"></span>
</div>

<div class="container">

  <div class="divider"></div>

  <!-- WHOAMI -->
  <div class="sec-title">👾 &nbsp;whoami</div>
  <div class="whoami-grid">
    <div class="terminal">
      <div class="term-bar">
        <div class="dot dot-r"></div><div class="dot dot-y"></div><div class="dot dot-g"></div>
        <div class="term-title">iNarrow12㉿NIBM — bash</div>
      </div>
      <div class="term-body">
        <div><span class="prompt">┌──(</span><span class="cmd">iNarrow12㉿NIBM</span><span class="prompt">)-[</span><span class="val">~</span><span class="prompt">]</span></div>
        <div><span class="prompt">└─$</span> <span class="cmd">cat profile.json</span></div>
        <br>
        <div><span class="arrow">{</span></div>
        <div>&nbsp;&nbsp;<span class="key">"name"</span>       : <span class="val">"iNarrow12"</span>,</div>
        <div>&nbsp;&nbsp;<span class="key">"institute"</span>  : <span class="val">"NIBM — Sri Lanka 🇱🇰"</span>,</div>
        <div>&nbsp;&nbsp;<span class="key">"major"</span>      : <span class="val">"Network Engineering 📡"</span>,</div>
        <div>&nbsp;&nbsp;<span class="key">"passion"</span>    : <span class="val">"Ethical Hacking 🔐"</span>,</div>
        <div>&nbsp;&nbsp;<span class="key">"certs_goal"</span> : <span class="val">["CEH", "OSCP", "Security+"]</span>,</div>
        <div>&nbsp;&nbsp;<span class="key">"status"</span>     : <span class="val">"▓▓▓▓▓▓▓░░ Grinding 🔥"</span></div>
        <div><span class="arrow">}</span></div>
      </div>
    </div>
    <img class="hacker-gif"
      src="https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif"
      alt="hacking gif"
      onerror="this.src='https://media.giphy.com/media/ZVik7pIo9KB3UA/giphy.gif'"/>
  </div>

  <div class="divider"></div>

  <!-- ABOUT CODE -->
  <div class="sec-title">💻 &nbsp;about.py</div>
  <div class="code-block">
    <div class="code-bar">
      <div class="lang-dot"></div> profile.py
    </div>
    <div class="code-body">
      <div><span class="kw">class</span> <span class="fn">iNarrow12</span>:</div>
      <div>&nbsp;&nbsp;<span class="kw">def</span> <span class="fn">__init__</span>(<span class="st">self</span>):</div>
      <div>&nbsp;&nbsp;&nbsp;&nbsp;<span class="st">self</span>.name        = <span class="st">"iNarrow12"</span></div>
      <div>&nbsp;&nbsp;&nbsp;&nbsp;<span class="st">self</span>.institute   = <span class="st">"NIBM — Network Engineering 🎓"</span></div>
      <div>&nbsp;&nbsp;&nbsp;&nbsp;<span class="st">self</span>.skills      = [<span class="st">"Ethical Hacking"</span>, <span class="st">"Networking"</span>, <span class="st">"Linux"</span>, <span class="st">"Python"</span>]</div>
      <div>&nbsp;&nbsp;&nbsp;&nbsp;<span class="st">self</span>.tools       = [<span class="st">"Kali Linux"</span>, <span class="st">"Wireshark"</span>, <span class="st">"Nmap"</span>, <span class="st">"Burp Suite"</span>]</div>
      <div>&nbsp;&nbsp;&nbsp;&nbsp;<span class="st">self</span>.certs_todo  = [<span class="st">"CEH"</span>, <span class="st">"CompTIA Security+"</span>, <span class="st">"OSCP"</span>]</div>
      <div>&nbsp;&nbsp;&nbsp;&nbsp;<span class="st">self</span>.hobbies     = [<span class="st">"CTFs 🚩"</span>, <span class="st">"Packet Analysis 📡"</span>, <span class="st">"Breaking things legally 😅"</span>]</div>
      <br>
      <div>&nbsp;&nbsp;<span class="kw">def</span> <span class="fn">mission</span>(<span class="st">self</span>):</div>
      <div>&nbsp;&nbsp;&nbsp;&nbsp;<span class="kw">return</span> <span class="st">"🚀 Turning curiosity into capability — one exploit at a time."</span></div>
      <br>
      <div><span class="cm"># Run me!</span></div>
      <div>me = <span class="fn">iNarrow12</span>()</div>
      <div><span class="fn">print</span>(me.mission())</div>
      <div><span class="cm"># 🚀 Turning curiosity into capability — one exploit at a time.</span></div>
    </div>
  </div>

  <div class="divider"></div>

  <!-- ARSENAL -->
  <div class="sec-title">🛠️ &nbsp;Arsenal</div>
  <div class="badge-grid">
    <span class="badge" style="background:#268BEE22;color:#268BEE;border-color:#268BEE44"><span class="badge-icon">🐉</span>Kali Linux</span>
    <span class="badge" style="background:#FCC62422;color:#FCC624;border-color:#FCC62444"><span class="badge-icon">🐧</span>Linux</span>
    <span class="badge" style="background:#3776AB22;color:#3776AB;border-color:#3776AB44"><span class="badge-icon">🐍</span>Python</span>
    <span class="badge" style="background:#4EAA2522;color:#4EAA25;border-color:#4EAA2544"><span class="badge-icon">💻</span>Bash</span>
    <span class="badge" style="background:#1679A722;color:#1679A7;border-color:#1679A744"><span class="badge-icon">🦈</span>Wireshark</span>
    <span class="badge" style="background:#FF663322;color:#FF6633;border-color:#FF663344"><span class="badge-icon">🔥</span>Burp Suite</span>
    <span class="badge" style="background:#E34F2622;color:#E34F26;border-color:#E34F2644"><span class="badge-icon">💣</span>Metasploit</span>
    <span class="badge" style="background:#1BA0D722;color:#1BA0D7;border-color:#1BA0D744"><span class="badge-icon">📡</span>Cisco</span>
    <span class="badge" style="background:#00417022;color:#5baaff;border-color:#5baaff44"><span class="badge-icon">🗺️</span>Nmap</span>
    <span class="badge" style="background:#18171722;color:#ccc;border-color:#ffffff33"><span class="badge-icon">🐙</span>GitHub</span>
  </div>

  <div class="divider"></div>

  <!-- STATS -->
  <div class="sec-title">📊 &nbsp;Stats</div>
  <div class="stats-grid">
    <div class="stat-card">
      <div class="stat-icon">🔥</div>
      <div class="stat-num" id="streak">0</div>
      <div class="stat-label">Day Streak</div>
    </div>
    <div class="stat-card">
      <div class="stat-icon">📦</div>
      <div class="stat-num" id="commits">0</div>
      <div class="stat-label">Total Commits</div>
    </div>
    <div class="stat-card">
      <div class="stat-icon">⭐</div>
      <div class="stat-num" id="stars">0</div>
      <div class="stat-label">Stars Earned</div>
    </div>
    <div class="stat-card">
      <div class="stat-icon">📡</div>
      <div class="stat-num" id="repos">0</div>
      <div class="stat-label">Public Repos</div>
    </div>
  </div>

  <div class="divider"></div>

  <!-- TROPHIES -->
  <div class="sec-title">🏆 &nbsp;Trophy Room</div>
  <div class="trophy-row">
    <div class="trophy"><span class="trophy-icon">🥇</span><div class="trophy-name">First Commit</div></div>
    <div class="trophy"><span class="trophy-icon">🔐</span><div class="trophy-name">Security Mind</div></div>
    <div class="trophy"><span class="trophy-icon">🚩</span><div class="trophy-name">CTF Player</div></div>
    <div class="trophy"><span class="trophy-icon">📡</span><div class="trophy-name">Network Pro</div></div>
    <div class="trophy"><span class="trophy-icon">🐍</span><div class="trophy-name">Pythonista</div></div>
    <div class="trophy"><span class="trophy-icon">💀</span><div class="trophy-name">Root Access</div></div>
  </div>

  <div class="divider"></div>

  <!-- QUOTE -->
  <div class="quote-box">
    <span>❝</span> &nbsp;Every packet tells a story. I just listen.&nbsp; <span>❞</span>
    <br><br>
    <span style="font-size:.8rem;color:#6e7681;font-style:normal;">— iNarrow12</span>
  </div>

</div>

<!-- FOOTER -->
<div class="wave-footer">
  <div style="font-family:'Orbitron',monospace;font-size:1.2rem;color:#00f7ff;letter-spacing:3px;">iNarrow12</div>
  <div style="color:#6e7681;font-size:.8rem;margin-top:6px;">NIBM · Network Engineering · Ethical Hacking</div>
  <div class="views-badge">👁️ &nbsp;PROFILE VIEWS: <span id="pv">0</span></div>
</div>

<script>
  // Typing animation
  const lines = [
    "🔐 Ethical Hacking Student",
    "📡 Network Engineering @ NIBM",
    "💻 Always in the terminal...",
    "🚀 Breaking things legally!",
    "🎯 CTF Player | Packet Sniffer"
  ];
  let li=0,ci=0,del=false;
  const el=document.getElementById('typer');
  function type(){
    const cur=lines[li];
    if(!del){
      el.textContent=cur.slice(0,++ci);
      if(ci===cur.length){del=true;setTimeout(type,1800);return;}
    } else {
      el.textContent=cur.slice(0,--ci);
      if(ci===0){del=false;li=(li+1)%lines.length;}
    }
    setTimeout(type,del?40:70);
  }
  type();

  // Counter animation
  function counter(id,target,dur){
    const el=document.getElementById(id);
    let start=0,step=target/dur*16;
    const t=setInterval(()=>{
      start=Math.min(start+step,target);
      el.textContent=Math.round(start);
      if(start>=target)clearInterval(t);
    },16);
  }
  counter('streak',42,1500);
  counter('commits',187,1800);
  counter('stars',23,1200);
  counter('repos',12,1000);
  counter('pv',1337,2000);
</script>
</body>
</html>
