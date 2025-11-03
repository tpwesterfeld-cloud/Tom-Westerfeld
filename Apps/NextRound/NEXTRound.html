<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1" />
  <title>NextRound – Wer holt die nächste Runde?</title>
  <style>
    :root{
      --bg:#0b0f1a;
      --glass:rgba(255,255,255,0.08);
      --glass-strong:rgba(255,255,255,0.14);
      --text:#e9ecf1;
      --muted:#a8b2c1;
      --accent-pink:#ff3cac;
      --accent-cyan:#87f5ff;
      --accent-orange:#ffb86b;
      --accent-green:#6bff95;
      --error:#ff6574;
      --ok:#6bff95;
      --focus:#c7f0ff;
      --shadow:0 10px 30px rgba(0,0,0,0.35);
      --radius:22px;
      --radius-lg:28px;
      --blur:14px;
      --transition: all .3s ease;
    }

    * { box-sizing: border-box; }
    html, body { height:100%; }

    body{
      margin:0; font-family: system-ui, -apple-system, Segoe UI, Roboto, Ubuntu, "Helvetica Neue", Arial, Noto Sans, "Apple Color Emoji", "Segoe UI Emoji";
      color:var(--text); background: radial-gradient(1200px 800px at 80% -10%, rgba(255,60,172,.15), transparent 60%),
                         radial-gradient(900px 700px at -10% 10%, rgba(135,245,255,.12), transparent 55%),
                         radial-gradient(800px 700px at 50% 120%, rgba(255,184,107,.1), transparent 60%),
                         var(--bg);
    }

    .app{
      display:flex; flex-direction:column; gap:12px; min-height:100dvh; padding:14px 14px 80px;
      max-width: 720px; margin: 0 auto;
    }

    header{
      position:sticky; top:0; z-index:5;
      padding:10px 8px; border-radius: var(--radius);
      background: linear-gradient(120deg, rgba(255,60,172,.18), rgba(135,245,255,.18));
      backdrop-filter: blur(var(--blur)); -webkit-backdrop-filter: blur(var(--blur));
      box-shadow: var(--shadow);
    }
    .title{ display:flex; align-items:center; gap:12px; }
    .title h1{ margin:0; font-size:clamp(20px, 5vw, 28px); }
    .subtitle{ margin:2px 0 0; color:var(--muted); font-size:14px; }

    .current-card{
      position:relative; flex:0 0 auto; padding:18px; border-radius: var(--radius-lg);
      background: linear-gradient(160deg, rgba(255,60,172,.22), rgba(135,245,255,.18) 50%, rgba(255,184,107,.18));
      backdrop-filter: blur(var(--blur)); -webkit-backdrop-filter: blur(var(--blur));
      box-shadow: var(--shadow);
      overflow:hidden;
    }
    .current-inner{ display:grid; grid-template-columns: 1fr auto; align-items:center; gap:12px; }
    .badge{ justify-self:start; font-size:12px; padding:6px 10px; border-radius:999px; background: rgba(255,255,255,.12); border:1px solid rgba(255,255,255,.18); }
    .buyer-name{ grid-column:1/-1; font-size: clamp(28px, 8vw, 44px); font-weight:800; margin:4px 0 10px; text-shadow: 0 4px 18px rgba(0,0,0,.35); }

    .emoji{ font-size: clamp(38px, 10vw, 56px); animation: bounce 1.8s infinite; }
    @keyframes bounce{ 0%,20%,53%,80%,100%{transform: translateY(0);} 40%,43%{transform: translateY(-8px);} 70%{transform: translateY(-4px);} 90%{transform: translateY(-2px);} }

    .pulse{ animation: pulse 1.8s infinite ease-in-out; }
    @keyframes pulse{ 0%{ box-shadow: 0 0 0 0 rgba(255,60,172,.4);} 70%{ box-shadow: 0 0 0 16px rgba(255,60,172,0);} 100%{ box-shadow: 0 0 0 0 rgba(255,60,172,0);} }

    .primary-action{
      position:sticky; inset-inline:0; bottom:14px; margin:10px auto 0; width:min(560px, 100%);
      display:flex; justify-content:center;
    }
    .btn-primary{
      width:100%; padding:18px 20px; border-radius: 999px;
      background: radial-gradient(80% 120% at 20% 0%, rgba(255,60,172,.75), rgba(255,184,107,.75));
      color:#0b0f1a; font-weight:800; font-size: clamp(18px, 6vw, 22px); cursor:pointer; transition: var(--transition);
    }

    .controls{ display:grid; grid-template-columns:repeat(4,1fr); gap:10px; margin-top:8px; }
    .btn{
      padding:12px 10px; border-radius: 16px;
      background: var(--glass); color:var(--text); font-weight:700; cursor:pointer; transition: var(--transition);
      backdrop-filter: blur(var(--blur));
      box-shadow: var(--shadow);
      display:flex; align-items:center; justify-content:center; gap:8px; min-height:52px;
    }

    .stats{ display:none; }

    .players{ margin-top:10px; }
    .players-header{ display:flex; align-items:center; justify-content:space-between; }
    .player-list{ margin-top:8px; display:flex; flex-direction:column; gap:8px; max-height: 42vh; overflow:auto; }
    .player{ display:grid; grid-template-columns: auto 1fr auto auto; align-items:center; gap:10px; padding:12px; border-radius:16px; background: rgba(255,255,255,.06); }
    .player.current{ outline:2px solid var(--accent-pink); }
    .avatar{ width:38px; height:38px; border-radius:12px; display:grid; place-items:center; font-weight:800; background: linear-gradient(135deg, rgba(255,60,172,.35), rgba(135,245,255,.35)); }
    .pname{ font-weight:800; }
    .pcounter{ font-size:12px; color:var(--muted); }
    .badge-rounds{ font-size:12px; padding:6px 8px; border-radius:999px; background: rgba(255,255,255,.1); }

    .add{ display:grid; grid-template-columns: 1fr auto; gap:8px; margin-top:10px; }
    .input{ padding:14px; border-radius:14px; border:1px solid rgba(255,255,255,.18); background: rgba(0,0,0,.25); color:var(--text); }
  </style>
</head>
<body>
  <div class="app">
    <header>
      <div class="title">
        <div class="emoji">🍻</div>
        <div>
          <h1>NextRound</h1>
          <p class="subtitle">Wer holt die nächste Runde?</p>
        </div>
      </div>
    </header>

    <section class="current-card">
      <div class="current-inner">
        <span class="badge" id="round-badge">Runde #<span id="round-number">1</span></span>
        <h2 id="current-label" class="buyer-name">–</h2>
      </div>
      <div class="primary-action">
        <button id="btn-next" class="btn-primary pulse">🍺 Runde geholt!</button>
      </div>
    </section>

    <section class="controls">
      <button id="btn-skip" class="btn">⏭️ Überspringen</button>
      <button id="btn-reset" class="btn">🔄 Reset</button>
      <button id="btn-random" class="btn">🎲 Zufall</button>
    </section>

    <section class="players">
      <div class="players-header">
        <h3>Spieler</h3>
        <div class="pcounter" id="player-count">0 Teilnehmer</div>
      </div>
      <div id="player-list" class="player-list"></div>
    </section>

    <section class="add">
      <input id="name-input" class="input" maxlength="18" placeholder="Name hinzufügen…" />
      <button id="btn-add">Hinzufügen</button>
    </section>
  </div>

  <script>
    const STORE_KEY = 'round_robin_v2';
    const defaultState = {
      players: [
        { name: 'Max', total: 0, rounds: 0 },
        { name: 'Lisa', total: 0, rounds: 0 },
      ],
      currentPlayerIndex: 0,
      totalRounds: 0,
    };

    function loadState(){
      const raw = localStorage.getItem(STORE_KEY);
      if(!raw) return structuredClone(defaultState);
      return JSON.parse(raw);
    }
    function saveState(){ localStorage.setItem(STORE_KEY, JSON.stringify(state)); }

    let state = loadState();

    const els = {
      buyerName: document.getElementById('current-label'),
      roundBadgNum: document.getElementById('round-number'),
      playerCount: document.getElementById('player-count'),
      list: document.getElementById('player-list'),
      btnNext: document.getElementById('btn-next'),
      btnSkip: document.getElementById('btn-skip'),
      btnReset: document.getElementById('btn-reset'),
      btnRandom: document.getElementById('btn-random'),
      nameInput: document.getElementById('name-input'),
      btnAdd: document.getElementById('btn-add'),
    };

    function nextIndex(idx, list){ return (idx + 1) % list.length; }

    function nextRound(){
      const p = state.players[state.currentPlayerIndex];
      p.rounds++; p.total++; state.totalRounds++;
      state.currentPlayerIndex = nextIndex(state.currentPlayerIndex, state.players);
      saveState(); updateDisplay();
    }

    function skipPlayer(){
      state.currentPlayerIndex = nextIndex(state.currentPlayerIndex, state.players);
      saveState(); updateDisplay();
    }

    function resetRounds(){
      state.players.forEach(p=> p.rounds = 0);
      state.totalRounds = 0;
      saveState(); updateDisplay();
    }

    function randomPlayer(){
      const minRounds = Math.min(...state.players.map(p=>p.rounds));
      const candidates = state.players.map((p,i)=>({p,i})).filter(obj => obj.p.rounds === minRounds);
      const pick = candidates[Math.floor(Math.random() * candidates.length)];
      state.currentPlayerIndex = pick.i;
      saveState(); updateDisplay();
    }

    function addPlayer(name){
      const clean = name.trim();
      if(!clean) return;
      if(state.players.some(p => p.name.toLowerCase() === clean.toLowerCase())) return;
      state.players.push({ name: clean, total: 0, rounds: 0 });
      saveState(); updateDisplay();
      els.nameInput.value = '';
    }

    function deletePlayer(index){
      if(state.players.length <= 2) return;
      state.players.splice(index, 1);
      if(state.currentPlayerIndex >= state.players.length){ state.currentPlayerIndex = 0; }
      saveState(); updateDisplay();
    }

    function updateDisplay(){
      const { players, currentPlayerIndex, totalRounds } = state;
      const current = players[currentPlayerIndex];

      els.buyerName.textContent = current?.name ?? '–';
      els.roundBadgNum.textContent = Math.max(1, totalRounds + 1);

      els.playerCount.textContent = `${players.length} Teilnehmer`;
      els.list.innerHTML = '';
      players.forEach((p, i)=>{
        const item = document.createElement('div');
        item.className = 'player' + (i === currentPlayerIndex ? ' current' : '');

        const avatar = document.createElement('div');
        avatar.className = 'avatar';
        avatar.textContent = p.name.slice(0,2).toUpperCase();

        const textWrap = document.createElement('div');
        const name = document.createElement('div'); name.className='pname'; name.textContent = p.name;
        const small = document.createElement('div'); small.className='pcounter'; small.textContent = `${p.rounds} Runden`;
        textWrap.appendChild(name); textWrap.appendChild(small);

        const badge = document.createElement('div'); badge.className='badge-rounds'; badge.textContent = `#${i+1}`;

        const del = document.createElement('button'); del.textContent='🗑️'; del.onclick=()=>deletePlayer(i);

        item.appendChild(avatar); item.appendChild(textWrap); item.appendChild(badge); item.appendChild(del);
        els.list.appendChild(item);
      });
    }

    els.btnNext.addEventListener('click', nextRound);
    els.btnSkip.addEventListener('click', skipPlayer);
    els.btnReset.addEventListener('click', resetRounds);
    els.btnRandom.addEventListener('click', randomPlayer);
    els.btnAdd.addEventListener('click', ()=> addPlayer(els.nameInput.value));
    els.nameInput.addEventListener('keydown', e=>{ if(e.key==='Enter') addPlayer(els.nameInput.value); });

    updateDisplay();
  </script>
</body>
</html>
