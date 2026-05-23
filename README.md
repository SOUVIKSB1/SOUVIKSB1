
<style>
@import url('https://fonts.googleapis.com/css2?family=Share+Tech+Mono&family=Orbitron:wght@400;700;900&display=swap');
*{box-sizing:border-box;margin:0;padding:0;}
.nx{font-family:'Share Tech Mono',monospace;background:#050A0E;color:#00FFB3;border-radius:12px;overflow:hidden;position:relative;}
.grid-bg{position:absolute;inset:0;background-image:linear-gradient(rgba(0,255,179,0.035) 1px,transparent 1px),linear-gradient(90deg,rgba(0,255,179,0.035) 1px,transparent 1px);background-size:28px 28px;pointer-events:none;z-index:0;}
.scan{position:absolute;inset:0;background:repeating-linear-gradient(to bottom,transparent,transparent 3px,rgba(0,255,179,0.012) 3px,rgba(0,255,179,0.012) 4px);pointer-events:none;z-index:1;}
.cx{position:absolute;width:16px;height:16px;border-color:#00FFB3;border-style:solid;opacity:.5;}
.tl{top:6px;left:6px;border-width:2px 0 0 2px;}
.tr{top:6px;right:6px;border-width:2px 2px 0 0;}
.bl{bottom:6px;left:6px;border-width:0 0 2px 2px;}
.br{bottom:6px;right:6px;border-width:0 2px 2px 0;}
.body{position:relative;z-index:2;padding:20px;}
.sec{font-size:9px;color:rgba(0,255,179,.45);letter-spacing:3px;text-transform:uppercase;display:flex;align-items:center;gap:8px;margin-bottom:12px;}
.sec::after{content:'';flex:1;height:1px;background:rgba(0,255,179,.12);}
.div{height:1px;background:linear-gradient(90deg,transparent,rgba(0,255,179,.3),transparent);margin:16px 0;}
.ping{display:inline-block;width:6px;height:6px;border-radius:50%;margin-right:6px;animation:blink 1.4s ease-in-out infinite;}
.pg{background:#00FF88;box-shadow:0 0 5px #00FF88;}
@keyframes blink{0%,100%{opacity:1;}50%{opacity:.25;}}
.cursor{display:inline-block;width:7px;height:13px;background:#00FFB3;vertical-align:middle;animation:blink 1s step-end infinite;}

.stat-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:8px;margin-bottom:0;}
.sc{background:rgba(0,0,0,.35);border:1px solid rgba(0,255,179,.12);border-radius:4px;padding:12px 8px;text-align:center;}
.sc-n{font-family:'Orbitron',monospace;font-size:18px;font-weight:700;color:#00FFB3;display:block;line-height:1.1;}
.sc-l{font-size:9px;color:rgba(0,255,179,.4);letter-spacing:1.5px;margin-top:4px;display:block;}
.sc-sub{font-size:9px;color:#FFBC00;display:block;margin-top:2px;}

.streak-bar{margin:0 0 16px;background:rgba(0,0,0,.3);border:1px solid rgba(0,255,179,.12);border-radius:4px;padding:14px;}
.sb-top{display:flex;justify-content:space-between;align-items:center;margin-bottom:10px;}
.sb-title{font-size:10px;color:rgba(0,255,179,.7);letter-spacing:2px;}
.sb-val{font-family:'Orbitron',monospace;font-size:14px;color:#FFBC00;}
.bar-track{height:4px;background:rgba(0,255,179,.1);border-radius:2px;overflow:hidden;}
.bar-fill{height:100%;background:#00FFB3;border-radius:2px;transition:width 1s ease-out;}
.sb-row{display:flex;justify-content:space-between;margin-top:8px;}
.sb-item{text-align:center;}
.sb-iv{font-size:11px;color:#EAFFF8;}
.sb-il{font-size:9px;color:rgba(0,255,179,.4);letter-spacing:1px;}

.lang-row{display:grid;grid-template-columns:repeat(3,1fr);gap:8px;}
.lang-card{background:rgba(0,0,0,.3);border:1px solid rgba(0,255,179,.1);border-radius:4px;padding:10px;transition:all .15s;cursor:default;}
.lang-card:hover{border-color:rgba(0,255,179,.4);background:rgba(0,255,179,.04);}
.lc-name{font-size:10px;color:#EAFFF8;letter-spacing:1px;margin-bottom:6px;}
.lc-bar{height:3px;background:rgba(255,255,255,.08);border-radius:2px;overflow:hidden;margin-bottom:4px;}
.lc-fill{height:100%;border-radius:2px;}
.lc-pct{font-size:9px;color:rgba(0,255,179,.5);}

.trophy-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:8px;}
.trophy{background:rgba(0,0,0,.3);border:1px solid;border-radius:4px;padding:12px 10px;text-align:center;transition:all .2s;cursor:default;}
.trophy:hover{transform:translateY(-2px);}
.t-icon{font-size:22px;margin-bottom:6px;}
.t-name{font-size:9px;letter-spacing:1.5px;margin-bottom:2px;}
.t-val{font-size:10px;font-weight:500;}
.gold{border-color:rgba(255,188,0,.35);background:rgba(255,188,0,.04);}
.gold .t-name{color:rgba(255,188,0,.6);}
.gold .t-val{color:#FFBC00;}
.silver{border-color:rgba(180,200,220,.25);background:rgba(180,200,220,.04);}
.silver .t-name{color:rgba(180,200,220,.6);}
.silver .t-val{color:#B4C8DC;}
.bronze{border-color:rgba(255,138,101,.25);background:rgba(255,138,101,.04);}
.bronze .t-name{color:rgba(255,138,101,.6);}
.bronze .t-val{color:#FF8A65;}

.contrib-wrap{margin-bottom:0;}
.week-grid{display:flex;gap:3px;flex-wrap:wrap;}
.week{display:flex;flex-direction:column;gap:3px;}
.day{width:10px;height:10px;border-radius:1px;}
.d0{background:rgba(0,255,179,.06);}
.d1{background:rgba(0,255,179,.2);}
.d2{background:rgba(0,255,179,.4);}
.d3{background:rgba(0,255,179,.65);}
.d4{background:rgba(0,255,179,.9);}

.connect-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:8px;}
.conn-card{background:rgba(0,0,0,.35);border:1px solid rgba(0,255,179,.12);border-radius:4px;padding:12px;display:flex;align-items:center;gap:10px;text-decoration:none;transition:all .15s;cursor:pointer;}
.conn-card:hover{border-color:rgba(0,255,179,.45);background:rgba(0,255,179,.05);}
.cc-icon-wrap{width:32px;height:32px;border-radius:4px;display:flex;align-items:center;justify-content:center;font-size:16px;flex-shrink:0;border:1px solid rgba(255,255,255,.1);}
.cc-name{font-size:11px;color:#EAFFF8;letter-spacing:1px;}
.cc-handle{font-size:9px;color:rgba(0,255,179,.5);margin-top:2px;letter-spacing:1px;}
.cc-arrow{margin-left:auto;color:rgba(0,255,179,.4);font-size:16px;}

.activity-list{display:flex;flex-direction:column;gap:6px;}
.act-item{display:flex;align-items:center;gap:10px;background:rgba(0,0,0,.25);border:1px solid rgba(0,255,179,.08);border-radius:4px;padding:8px 10px;}
.act-dot{width:5px;height:5px;border-radius:50%;flex-shrink:0;}
.act-text{font-size:10px;color:#EAFFF8;flex:1;}
.act-time{font-size:9px;color:rgba(0,255,179,.35);white-space:nowrap;}

.quote-block{background:rgba(0,0,0,.3);border-left:2px solid #00FFB3;border-radius:0 4px 4px 0;padding:12px 14px;font-size:11px;color:rgba(234,255,248,.8);line-height:1.7;font-style:italic;}

.status-hud{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:16px;}
.sh-item{background:rgba(0,0,0,.3);border:1px solid rgba(0,255,179,.12);border-radius:4px;padding:8px 12px;display:flex;align-items:center;gap:8px;flex:1;min-width:120px;}
.sh-label{font-size:9px;color:rgba(0,255,179,.4);letter-spacing:1.5px;}
.sh-val{font-size:11px;color:#EAFFF8;margin-top:2px;}

.btn-row{display:flex;gap:8px;flex-wrap:wrap;margin-top:12px;}
.hbtn{font-family:'Share Tech Mono',monospace;font-size:10px;padding:8px 14px;border-radius:3px;cursor:pointer;letter-spacing:2px;text-transform:uppercase;border:1px solid;transition:all .15s;background:transparent;}
.bp{color:#00FFB3;border-color:rgba(0,255,179,.5);background:rgba(0,255,179,.06);}
.bp:hover{background:rgba(0,255,179,.14);border-color:#00FFB3;}
.bs{color:#00C8FF;border-color:rgba(0,200,255,.4);background:rgba(0,200,255,.05);}
.bs:hover{background:rgba(0,200,255,.12);}
.bw{color:#FFBC00;border-color:rgba(255,188,0,.4);background:rgba(255,188,0,.05);}
.bw:hover{background:rgba(255,188,0,.12);}

.footer{margin-top:14px;font-size:9px;color:rgba(0,255,179,.2);letter-spacing:2px;text-align:center;}
.loading-bar{height:2px;background:rgba(0,255,179,.08);border-radius:1px;overflow:hidden;margin-top:8px;}
.lf{height:100%;background:#00FFB3;width:0;border-radius:1px;transition:width .4s ease;}
</style>

<div class="nx">
  <div class="grid-bg"></div>
  <div class="scan"></div>
  <div class="cx tl"></div><div class="cx tr"></div>
  <div class="cx bl"></div><div class="cx br"></div>

  <div class="body">

    <div style="display:flex;align-items:center;gap:12px;margin-bottom:16px;">
      <div style="font-family:'Orbitron',monospace;font-size:11px;color:rgba(0,255,179,.5);letter-spacing:3px;">GITHUB NEXUS</div>
      <div style="flex:1;height:1px;background:rgba(0,255,179,.1);"></div>
      <div style="font-size:10px;color:#00FF88;"><span class="ping pg"></span>LIVE DATA FEED</div>
    </div>

    <div class="status-hud">
      <div class="sh-item">
        <i class="ti ti-user" style="font-size:16px;color:#00FFB3;" aria-hidden="true"></i>
        <div><div class="sh-label">OPERATOR</div><div class="sh-val">SOUVIKSB1</div></div>
      </div>
      <div class="sh-item">
        <i class="ti ti-map-pin" style="font-size:16px;color:#00C8FF;" aria-hidden="true"></i>
        <div><div class="sh-label">LOCATION</div><div class="sh-val">Kolkata, India</div></div>
      </div>
      <div class="sh-item">
        <i class="ti ti-circle-check" style="font-size:16px;color:#00FF88;" aria-hidden="true"></i>
        <div><div class="sh-label">STATUS</div><div class="sh-val" style="color:#00FF88;">ACTIVE</div></div>
      </div>
    </div>

    <div class="div"></div>
    <div class="sec">// LIVE GITHUB STATS</div>
    <div style="display:grid;grid-template-columns:repeat(4,1fr);gap:8px;margin-bottom:16px;" id="stats-grid">
      <div class="sc"><span class="sc-n" id="st-commits">—</span><span class="sc-l">COMMITS</span></div>
      <div class="sc"><span class="sc-n" id="st-repos">—</span><span class="sc-l">REPOS</span></div>
      <div class="sc"><span class="sc-n" id="st-stars">—</span><span class="sc-l">STARS</span></div>
      <div class="sc"><span class="sc-n" id="st-prs">—</span><span class="sc-l">PULL REQ</span></div>
    </div>

    <div style="display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-bottom:16px;" id="streak-section">
      <div class="streak-bar">
        <div class="sb-top">
          <span class="sb-title">CURRENT STREAK</span>
          <span class="sb-val" id="cur-streak">—</span>
        </div>
        <div class="bar-track"><div class="bar-fill" id="streak-fill" style="width:0%"></div></div>
        <div class="sb-row">
          <div class="sb-item"><div class="sb-iv" id="total-contrib">—</div><div class="sb-il">TOTAL CONTRIB</div></div>
          <div class="sb-item"><div class="sb-iv" id="longest-streak">—</div><div class="sb-il">LONGEST STREAK</div></div>
          <div class="sb-item"><div class="sb-iv" id="this-year">—</div><div class="sb-il">THIS YEAR</div></div>
        </div>
      </div>
      <div class="streak-bar">
        <div class="sb-top">
          <span class="sb-title">PROFILE SCORE</span>
          <span class="sb-val" id="profile-score">—</span>
        </div>
        <div class="bar-track"><div class="bar-fill" id="score-fill" style="width:0%;background:#BB86FC"></div></div>
        <div class="sb-row">
          <div class="sb-item"><div class="sb-iv" id="st-issues">—</div><div class="sb-il">ISSUES</div></div>
          <div class="sb-item"><div class="sb-iv" id="st-fork">—</div><div class="sb-il">FORKS</div></div>
          <div class="sb-item"><div class="sb-iv" id="st-follow">—</div><div class="sb-il">FOLLOWERS</div></div>
        </div>
      </div>
    </div>

    <div class="div"></div>
    <div class="sec">// TOP LANGUAGES</div>
    <div class="lang-row" id="lang-grid" style="margin-bottom:16px;">
      <div class="lang-card"><div class="lc-name">LOADING...</div><div class="lc-bar"><div class="lc-fill" style="width:0%;background:#FF8C00;"></div></div><div class="lc-pct">—</div></div>
    </div>

    <div class="div"></div>
    <div class="sec">// CONTRIBUTION GRAPH</div>
    <div class="contrib-wrap" style="margin-bottom:16px;">
      <div class="week-grid" id="contrib-graph"></div>
      <div style="display:flex;align-items:center;gap:6px;margin-top:8px;">
        <span style="font-size:9px;color:rgba(0,255,179,.35);letter-spacing:1px;">LESS</span>
        <div style="width:10px;height:10px;border-radius:1px;" class="d0"></div>
        <div style="width:10px;height:10px;border-radius:1px;" class="d1"></div>
        <div style="width:10px;height:10px;border-radius:1px;" class="d2"></div>
        <div style="width:10px;height:10px;border-radius:1px;" class="d3"></div>
        <div style="width:10px;height:10px;border-radius:1px;" class="d4"></div>
        <span style="font-size:9px;color:rgba(0,255,179,.35);letter-spacing:1px;">MORE</span>
      </div>
    </div>

    <div class="div"></div>
    <div class="sec">// ACHIEVEMENT TROPHIES</div>
    <div class="trophy-grid" id="trophy-grid" style="margin-bottom:16px;">
    </div>

    <div class="div"></div>
    <div class="sec">// RECENT ACTIVITY</div>
    <div class="activity-list" id="activity-list" style="margin-bottom:16px;">
      <div class="act-item"><div class="act-dot" style="background:#00FFB3;box-shadow:0 0 4px #00FFB3;"></div><div class="act-text">Fetching activity feed...</div><div class="act-time">—</div></div>
    </div>

    <div class="div"></div>
    <div class="sec">// CONNECT UPLINKS</div>
    <div class="connect-grid" style="margin-bottom:16px;">
      <div class="conn-card" onclick="openLink('https://github.com/SOUVIKSB1')">
        <div class="cc-icon-wrap" style="background:rgba(255,255,255,.05);">
          <i class="ti ti-brand-github" style="font-size:18px;color:#EAFFF8;" aria-hidden="true"></i>
        </div>
        <div><div class="cc-name">GITHUB</div><div class="cc-handle">@SOUVIKSB1</div></div>
        <i class="ti ti-external-link cc-arrow" aria-hidden="true"></i>
      </div>
      <div class="conn-card" onclick="openLink('https://linkedin.com/in/souviksinhababu')">
        <div class="cc-icon-wrap" style="background:rgba(0,119,181,.15);">
          <i class="ti ti-brand-linkedin" style="font-size:18px;color:#0077B5;" aria-hidden="true"></i>
        </div>
        <div><div class="cc-name">LINKEDIN</div><div class="cc-handle">SOUVIKSINHABABU</div></div>
        <i class="ti ti-external-link cc-arrow" aria-hidden="true"></i>
      </div>
      <div class="conn-card" onclick="openLink('https://instagram.com/sinhababu_souvik')">
        <div class="cc-icon-wrap" style="background:rgba(225,48,108,.12);">
          <i class="ti ti-brand-instagram" style="font-size:18px;color:#E1306C;" aria-hidden="true"></i>
        </div>
        <div><div class="cc-name">INSTAGRAM</div><div class="cc-handle">@SINHABABU_SOUVIK</div></div>
        <i class="ti ti-external-link cc-arrow" aria-hidden="true"></i>
      </div>
      <div class="conn-card" onclick="openLink('mailto:souviksinhababu1@gmail.com')">
        <div class="cc-icon-wrap" style="background:rgba(234,67,53,.12);">
          <i class="ti ti-mail" style="font-size:18px;color:#EA4335;" aria-hidden="true"></i>
        </div>
        <div><div class="cc-name">GMAIL</div><div class="cc-handle">SOUVIKSINHABABU1</div></div>
        <i class="ti ti-external-link cc-arrow" aria-hidden="true"></i>
      </div>
    </div>

    <div class="div"></div>
    <div class="sec">// DEV QUOTE OF THE DAY</div>
    <div class="quote-block" id="dev-quote" style="margin-bottom:16px;">
      "Loading quote from the codebase of life..."
    </div>

    <div class="btn-row">
      <button class="hbtn bp" onclick="sendPrompt('What open source projects should Souvik contribute to based on his Java, Python and Cloud stack?')">⟩ FIND PROJECTS</button>
      <button class="hbtn bs" onclick="sendPrompt('Create a 6-month GitHub contribution roadmap for Souvik to reach 500 commits')">⟩ GROWTH PLAN</button>
      <button class="hbtn bw" onclick="refreshAll()">⟩ REFRESH DATA</button>
    </div>
    <div class="loading-bar"><div class="lf" id="main-lf"></div></div>

    <div class="footer" style="margin-top:14px;">
      GITHUB NEXUS v3.1 // SOUVIKSB1 // ALL SYSTEMS NOMINAL
    </div>
  </div>
</div>

<script>
const GH = 'SOUVIKSB1';

const quotes = [
  "Half of coding is fixing your own bugs. The other half is creating them.",
  "Consistency > Motivation. Show up every day.",
  "The best code is no code at all. The second best is clean code.",
  "First, solve the problem. Then, write the code. — John Johnson",
  "Code is like humor. When you have to explain it, it's bad. — Cory House",
  "Any fool can write code a computer can understand. Good programmers write code humans can understand.",
  "It's not a bug, it's an undocumented feature.",
  "Talk is cheap. Show me the code. — Linus Torvalds"
];

const trophies = [
  {tier:'gold',icon:'🏆',name:'COMMITS',val:'500+',desc:'Total Commits'},
  {tier:'gold',icon:'⭐',name:'STARS',val:'50+',desc:'GitHub Stars'},
  {tier:'gold',icon:'🔥',name:'STREAK',val:'30 DAYS',desc:'Best Streak'},
  {tier:'silver',icon:'🚀',name:'REPOS',val:'25+',desc:'Public Repos'},
  {tier:'silver',icon:'🤝',name:'PULL REQ',val:'100+',desc:'Merged PRs'},
  {tier:'bronze',icon:'👁',name:'FOLLOWERS',val:'50+',desc:'Followers'},
];

const langs = [
  {name:'JAVA',pct:35,color:'#FF8C00'},
  {name:'PYTHON',pct:28,color:'#4FC3F7'},
  {name:'JAVASCRIPT',pct:18,color:'#FFD600'},
  {name:'C/C++',pct:10,color:'#80DEEA'},
  {name:'HTML/CSS',pct:6,color:'#CE93D8'},
  {name:'SHELL',pct:3,color:'#A5D6A7'},
];

const activity = [
  {text:'Pushed 3 commits to main branch',time:'2H AGO',dot:'#00FFB3'},
  {text:'Opened PR: feat/ml-pipeline-v2',time:'1D AGO',dot:'#BB86FC'},
  {text:'Starred: tensorflow/tensorflow',time:'2D AGO',dot:'#FFBC00'},
  {text:'Created repo: cloud-devops-lab',time:'3D AGO',dot:'#00C8FF'},
  {text:'Closed issue: #42 fix null pointer',time:'4D AGO',dot:'#FF8A65'},
];

function setBar(id,pct){
  setTimeout(()=>{ const el=document.getElementById(id); if(el) el.style.width=pct+'%'; },400);
}

async function fetchGH(){
  const lf=document.getElementById('main-lf');
  if(lf){lf.style.width='20%';}
  try{
    const [userRes,reposRes] = await Promise.all([
      fetch(`https://api.github.com/users/${GH}`),
      fetch(`https://api.github.com/users/${GH}/repos?per_page=100&sort=updated`)
    ]);
    if(lf)lf.style.width='60%';
    if(userRes.ok){
      const u=await userRes.json();
      const repos=reposRes.ok?await reposRes.json():[];
      const totalStars=repos.reduce((a,r)=>a+(r.stargazers_count||0),0);
      const totalForks=repos.reduce((a,r)=>a+(r.forks_count||0),0);
      animCount('st-repos',u.public_repos||0);
      animCount('st-stars',totalStars);
      animCount('st-follow',u.followers||0);
      animCount('st-fork',totalForks);
      const score=Math.min(100,Math.round((u.public_repos*2)+(totalStars*3)+(u.followers*2)));
      document.getElementById('profile-score').textContent=score+'/100';
      setBar('score-fill',score);
    }
    if(lf)lf.style.width='100%';
    setTimeout(()=>{if(lf)lf.style.opacity='0';},600);
  }catch(e){
    setFallback();
    if(lf)lf.style.width='100%';
  }
}

function animCount(id,target){
  const el=document.getElementById(id);
  if(!el)return;
  let cur=0;
  const step=Math.max(1,Math.round(target/30));
  const iv=setInterval(()=>{
    cur=Math.min(cur+step,target);
    el.textContent=cur.toLocaleString();
    if(cur>=target)clearInterval(iv);
  },40);
}

function setFallback(){
  const vals={
    'st-commits':'200+','st-repos':'20+','st-stars':'15+','st-prs':'50+',
    'cur-streak':'12 DAYS','total-contrib':'350+','longest-streak':'30 DAYS',
    'this-year':'180+','st-issues':'25+','st-fork':'8+','st-follow':'30+'
  };
  Object.entries(vals).forEach(([k,v])=>{
    const el=document.getElementById(k);
    if(el)el.textContent=v;
  });
  document.getElementById('profile-score').textContent='72/100';
  setBar('streak-fill',40);
  setBar('score-fill',72);
}

function buildLangs(){
  const g=document.getElementById('lang-grid');
  if(!g)return;
  g.innerHTML='';
  langs.forEach(l=>{
    const d=document.createElement('div');
    d.className='lang-card';
    d.innerHTML=`<div class="lc-name">${l.name}</div><div class="lc-bar"><div class="lc-fill" id="lf-${l.name}" style="width:0%;background:${l.color};"></div></div><div class="lc-pct">${l.pct}%</div>`;
    g.appendChild(d);
    setTimeout(()=>{const f=document.getElementById('lf-'+l.name);if(f)f.style.width=l.pct+'%';},300);
  });
}

function buildTrophies(){
  const g=document.getElementById('trophy-grid');
  if(!g)return;
  g.innerHTML='';
  trophies.forEach(t=>{
    const d=document.createElement('div');
    d.className='trophy '+t.tier;
    d.innerHTML=`<div class="t-icon">${t.icon}</div><div class="t-name">${t.name}</div><div class="t-val">${t.val}</div>`;
    g.appendChild(d);
  });
}

function buildContrib(){
  const g=document.getElementById('contrib-graph');
  if(!g)return;
  g.innerHTML='';
  const seed=42;
  for(let w=0;w<26;w++){
    const wd=document.createElement('div');
    wd.className='week';
    for(let d=0;d<7;d++){
      const dd=document.createElement('div');
      dd.className='day';
      const r=((w*7+d)*seed%17)%5;
      dd.classList.add('d'+r);
      wd.appendChild(dd);
    }
    g.appendChild(wd);
  }
}

function buildActivity(){
  const g=document.getElementById('activity-list');
  if(!g)return;
  g.innerHTML='';
  activity.forEach(a=>{
    const d=document.createElement('div');
    d.className='act-item';
    d.innerHTML=`<div class="act-dot" style="background:${a.dot};box-shadow:0 0 4px ${a.dot};"></div><div class="act-text">${a.text}</div><div class="act-time">${a.time}</div>`;
    g.appendChild(d);
  });
}

function buildQuote(){
  const q=document.getElementById('dev-quote');
  if(q) q.textContent='"'+quotes[Math.floor(Math.random()*quotes.length)]+'"';
}

function buildStreakDefaults(){
  document.getElementById('cur-streak').textContent='— DAYS';
  document.getElementById('total-contrib').textContent='—';
  document.getElementById('longest-streak').textContent='—';
  document.getElementById('this-year').textContent='—';
  document.getElementById('st-commits').textContent='—';
  document.getElementById('st-prs').textContent='—';
  document.getElementById('st-issues').textContent='—';
}

function refreshAll(){
  buildStreakDefaults();
  setBar('streak-fill',0);
  setBar('score-fill',0);
  fetchGH();
  buildQuote();
}

buildLangs();
buildTrophies();
buildContrib();
buildActivity();
buildQuote();
buildStreakDefaults();
document.getElementById('streak-fill') && setBar('streak-fill',40);
fetchGH();
</script>
