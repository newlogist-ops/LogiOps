
//  LO – LogiOps (GOL) 
// version      beta-1.0

(function () {
  'use strict';
  const SPRITES_EMBED = {
  "waiting": "data:image/png;base64,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",
  "moving": "data:image/png;base64,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",
  "stopped": "data:image/png;base64,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",
  "loading": "data:image/png;base64,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",
  "loaded": "data:image/png;base64,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"
  };

  /*** CONFIG ***/
  const PASSWORD = '312789';

  /*** STORAGE ***/
  const STORAGE_KEY = 'nl:golfleet:v11';
  const ASSETS_KEY  = 'nl:assets:v1'; // legado (pode ignorar se usar sprites embutidos)
  function todayKey(d=new Date()){ return d.toISOString().slice(0,10); }
  function defaultState(){
    return {
      frentes: ['FRENTE 1','FRENTE 2','FRENTE 3','FRENTE 4','FRENTE 5','FRENTE 6','FRENTE 7'],
      rows: [],   
      history: {} 
    };
  }
  function load(){ try{ return JSON.parse(localStorage.getItem(STORAGE_KEY)||'null') || defaultState(); }catch{ return defaultState(); } }
  function save(s){ localStorage.setItem(STORAGE_KEY, JSON.stringify(s)); }
  function loadAssets(){ try{ return JSON.parse(localStorage.getItem(ASSETS_KEY)||'{}'); }catch{ return {}; } }
  function saveAssets(a){ localStorage.setItem(ASSETS_KEY, JSON.stringify(a)); }

  const S = load();
  const A = loadAssets();

  const COLORS = {
    header:    '#0d2e23',
    grid:      '#d7e9df',
    zebra:     '#f4fbf7',
    text:      '#0f172a',
    muted:     '#6b7280',
    accent:    '#1f8a5b',
    btn:       '#0f4b3a',
    danger:    '#ef4444',
    white:     '#ffffff',
    select:    '#b7e6cf'
  };

  const qs  = (s, r=document) => r.querySelector(s);
  const qsa = (s, r=document) => Array.from(r.querySelectorAll(s));
  const nowISO = () => new Date().toISOString();
  const fmtDT  = (d) => d ? new Date(d).toLocaleString() : '—';
  function download(name, text){
    const a = document.createElement('a');
    a.href = URL.createObjectURL(new Blob([text],{type:'text/csv;charset=utf-8;'}));
    a.download = name; a.click(); URL.revokeObjectURL(a.href);
  }

  const PH = k => `data:image/svg+xml;utf8,${encodeURIComponent(
    `<svg xmlns='http://www.w3.org/2000/svg' width='120' height='24' viewBox='0 0 120 24'>
      <rect x='1' y='1' width='118' height='22' rx='4' fill='#c9f0dc' stroke='#1f8a5b' stroke-width='2'/>
      <text x='60' y='16' font-family='Arial' font-size='10' text-anchor='middle' fill='#0f4b3a' font-weight='700'>${k.toUpperCase()}</text>
    </svg>` )}`;

  function iconDataURI(state){
    return SPRITES_EMBED[state] || A[state] || PH(state);
  }

  const style = document.createElement('style');
  style.textContent = `
  .nl-float{position:fixed;top:10px;right:10px;z-index:999999;background:${COLORS.accent};color:#fff;border:1px solid ${COLORS.grid};
    width:40px;height:40px;border-radius:8px;font-weight:700;display:flex;align-items:center;justify-content:center;cursor:pointer}
  .nl-panel{position:fixed;top:58px;right:10px;z-index:999999;width:min(96vw,1300px);max-height:82vh;
    display:none;flex-direction:column;border-radius:10px;overflow:hidden;box-shadow:0 16px 36px rgba(0,0,0,.45)}
  .nl-panel.open{display:flex}
  .nl-head{background:${COLORS.header};color:#fff;display:flex;gap:8px;align-items:center;padding:8px 10px}
  .nl-head h3{margin:0;font-size:13px;font-weight:700}
  .nl-head .sp{flex:1}
  .nl-head button{background:${COLORS.btn};border:none;color:#fff;border-radius:6px;padding:6px 10px;cursor:pointer;font-size:12px}

  .nl-body{background:${COLORS.white};overflow:auto}
  table.nl-table{width:100%;border-collapse:collapse;font-size:12px;background:${COLORS.white}}
  table.nl-table thead th{background:${COLORS.header};color:#fff;border-bottom:1px solid rgba(255,255,255,.2);padding:8px 6px;text-align:center;font-weight:700;position:sticky;top:0;z-index:1}
  table.nl-table tbody td{padding:6px;border-bottom:1px solid ${COLORS.grid};border-right:1px solid ${COLORS.grid};color:${COLORS.text}; text-align:center; vertical-align:middle}
  table.nl-table tbody td:last-child{border-right:none}
  table.nl-table tbody tr:nth-child(odd){background:${COLORS.white}}
  table.nl-table tbody tr:nth-child(even){background:${COLORS.zebra}}
  tr.nl-section th{background:${COLORS.white}; color:${COLORS.text}; text-align:left; font-weight:700; padding:8px 6px;border-top:2px solid ${COLORS.grid}; border-bottom:1px solid ${COLORS.grid}}
  tr.nl-row:hover{outline:2px solid ${COLORS.accent}; outline-offset:-2px}
  tr.nl-row.selected{background:${COLORS.select} !important}
  .nl-sprite{height:24px;width:auto;image-rendering:pixelated;vertical-align:middle}

  /* MODAIS */
  .nl-modal{position:fixed;inset:0;background:rgba(0,0,0,.45);display:none;align-items:center;justify-content:center;z-index:1000000}
  .nl-modal.open{display:flex}
  .nl-box{background:${COLORS.white};color:${COLORS.text};border:1px solid ${COLORS.grid};border-radius:10px;overflow:hidden;box-shadow:0 16px 40px rgba(0,0,0,.5)}
  .nl-box header{background:${COLORS.header};color:#fff;padding:8px 10px;display:flex;justify-content:space-between;align-items:center}
  .nl-box .content{padding:10px;max-height:65vh;overflow:auto}
  .nl-box .row{display:flex;gap:8px;align-items:center;margin-bottom:8px}
  .nl-box input,.nl-box select,.nl-box textarea{flex:1;border:1px solid ${COLORS.grid};border-radius:6px;padding:6px 8px}
  .nl-box button{background:${COLORS.btn};color:#fff;border:none;border-radius:6px;padding:6px 10px;cursor:pointer}
  .nl-box .danger{background:${COLORS.danger}}
  .nl-modal-add .nl-box{width:min(92vw,440px)}
  .nl-modal-conf .nl-box{width:min(92vw,500px)}
  .nl-modal-stop .nl-box{width:min(92vw,500px)}
  .nl-modal-assets .nl-box{width:min(92vw,680px)}
  .nl-confirm{font-size:18px;line-height:1.4}
  .nl-confirm strong{background:${COLORS.select};padding:0 4px;border-radius:4px}
  table.nl-hist{width:100%;border-collapse:collapse;font-size:12px;background:${COLORS.white}}
  table.nl-hist th, table.nl-hist td{padding:6px;border-bottom:1px solid ${COLORS.grid};text-align:center}
  table.nl-hist thead th{background:${COLORS.zebra};font-weight:700}
  `;
  document.head.appendChild(style);

  /*** UI BASE ***/
  const btn = document.createElement('button');
  btn.className='nl-float'; btn.textContent='nL'; btn.title='newLog';
  document.body.appendChild(btn);

  const panel = document.createElement('div');
  panel.className='nl-panel';
  panel.innerHTML = `
    <div class="nl-head">
      <h3>Controle de Caminhões – nL</h3>
      <div class="sp"></div>
      <button id="nl-add-open" title="F8">Lançar (F8)</button>
      <button id="nl-arrive">Chegada na Frente</button>
      <button id="nl-stop">Parada</button>
      <button id="nl-stop-clear-top">Limpar Parada</button>
      <button id="nl-hist">Histórico</button>
      <button id="nl-conf">Configurar</button>
      <button id="nl-close">Fechar</button>
    </div>
    <div class="nl-body">
      <table class="nl-table" id="nl-table">
        <thead>
          <tr>
            <th style="width:180px">Frente</th>
            <th style="width:90px">Caminhão</th>
            <th style="width:140px">Despacho</th>
            <th style="width:160px">Chegada Lavoura</th>
            <th style="width:150px">Saída Lavoura</th>
            <th>Status</th>
          </tr>
        </thead>
        <tbody></tbody>
      </table>
    </div>`;
  document.body.appendChild(panel);

  const modalAdd = document.createElement('div');
  modalAdd.className='nl-modal nl-modal-add';
  modalAdd.innerHTML = `
    <div class="nl-box">
      <header><strong>Lançar despacho</strong><button id="nl-add-close">Fechar</button></header>
      <div class="content">
        <div class="row">
          <label style="width:100px">Frente</label>
          <select id="nl-add-frente"></select>
        </div>
        <div class="row">
          <label style="width:100px">Frota</label>
          <input id="nl-add-cam" placeholder="Somente números" inputmode="numeric" autocomplete="off"/>
        </div>
        <div class="row" style="justify-content:flex-end;gap:10px">
          <button id="nl-add-next">Continuar</button>
        </div>
        <div style="font-size:11px;color:#6b7280;text-align:center">Atalhos: Enter continua · Esc cancela</div>
      </div>
    </div>`;
  document.body.appendChild(modalAdd);

  const modalConf = document.createElement('div');
  modalConf.className='nl-modal nl-modal-conf';
  modalConf.innerHTML = `
    <div class="nl-box">
      <header><strong>Confirmar decisão</strong><button id="nl-conf-close">Fechar</button></header>
      <div class="content">
        <div class="nl-confirm" id="nl-conf-text"></div>
        <div class="row" style="justify-content:flex-end;gap:10px;margin-top:12px">
          <button id="nl-conf-cancel" class="danger">Cancelar</button>
          <button id="nl-conf-ok">Confirmar</button>
        </div>
      </div>
    </div>`;
  document.body.appendChild(modalConf);

  // Parada
  const modalStop = document.createElement('div');
  modalStop.className='nl-modal nl-modal-stop';
  modalStop.innerHTML = `
    <div class="nl-box">
      <header><strong>Registrar parada</strong><button id="nl-stop-close">Fechar</button></header>
      <div class="content">
        <div class="row"><label style="width:110px">Caminhão</label><input id="nl-stop-cam" disabled/></div>
        <div class="row"><label style="width:110px">Frente</label><input id="nl-stop-fr" disabled/></div>
        <div class="row"><label style="width:110px">Motivo</label><textarea id="nl-stop-note" rows="3" placeholder="Ex.: Pneu furado, aguardando ordem..."></textarea></div>
        <div class="row" style="justify-content:flex-end;gap:10px">
          <button id="nl-stop-clear">Limpar parada</button>
          <button id="nl-stop-save">Salvar</button>
        </div>
      </div>
    </div>`;
  document.body.appendChild(modalStop);

  const modalCfg = document.createElement('div');
  modalCfg.className='nl-modal nl-modal-assets';
  modalCfg.innerHTML = `
    <div class="nl-box" style="width:min(92vw,760px)">
      <header><strong>Configurar</strong><button id="nl-conf2-close">Fechar</button></header>
      <div class="content">
        <h4 style="margin:0 0 8px 0">Frentes</h4>
        <div class="row"><input id="nl-new-front" placeholder="Nova frente (ex.: FRENTE 8)"><button id="nl-add-front">Adicionar</button></div>
        <div id="nl-fronts-list" style="margin-bottom:10px"></div>
        <div class="row" style="justify-content:flex-end">
          <button id="nl-save-fronts">Salvar</button>
          <button id="nl-reset-fronts" class="danger">Resetar 7 frentes</button>
        </div>

        <hr style="margin:12px 0;border:none;border-top:1px solid ${COLORS.grid}">
        <h4 style="margin:0 0 8px 0">Ícones locais (opcional)</h4>
        <div style="margin-bottom:8px;color:${COLORS.muted}">
          Se não colar o SPRITES_EMBED, você pode enviar arquivos PNG/WebP/SVG aqui.
        </div>
        ${['waiting','moving','stopped','loading','loaded'].map(key=>`
          <div class="row" data-key="${key}">
            <label style="width:160px;text-transform:capitalize">${key}</label>
            <input type="file" accept=".png,.webp,.svg" />
            <input type="text" placeholder="ou cole data:image;base64,..." value="${A[key]||''}"/>
            <button data-act="save">Salvar</button>
            <button data-act="clear" class="danger">Limpar</button>
          </div>
        `).join('')}
        <div class="row" style="justify-content:flex-end">
          <button id="nl-assets-saveall">Salvar tudo</button>
        </div>
      </div>
    </div>`;
  document.body.appendChild(modalCfg);

  // Histórico
  const modalHist = document.createElement('div');
  modalHist.className='nl-modal';
  modalHist.innerHTML = `
    <div class="nl-box" style="width:min(92vw,860px)">
      <header><strong>Histórico de despachos</strong><button id="nl-hist-close">Fechar</button></header>
      <div class="content">
        <div class="row" style="gap:10px;justify-content:flex-start">
          <label style="width:100px">Dia</label>
          <select id="nl-hist-day"></select>
          <button id="nl-hist-export">Exportar CSV</button>
          <button id="nl-hist-delete" class="danger" title="Admin: excluir dia">Excluir dia</button>
        </div>
        <div id="nl-hist-wrap"></div>
      </div>
    </div>`;
  document.body.appendChild(modalHist);

  function effectiveState(r){
    if (r.state === 'stopped') return 'stopped';
    if (r.saidaFrente && !r.chegadaPatio) return 'loaded';
    if (r.chegadaFrente && !r.saidaFrente) {
      const list = S.rows
        .filter(x => x.frente===r.frente && x.chegadaFrente && !x.saidaFrente && x.state!=='stopped')
        .sort((a,b)=> new Date(a.chegadaFrente) - new Date(b.chegadaFrente));
      const pos = list.findIndex(x => x.cam===r.cam);
      if (pos === 0) return 'loading'; // 1º da fila
      if (pos >= 1) return 'waiting';  // 2º+
    }
    return 'moving';
  }
  function statusLabel(st){
    return st==='waiting' ? 'AGUARD. FILA' :
           st==='moving'  ? 'EM DESLOC.'   :
           st==='stopped' ? 'PARADO'       :
           st==='loading' ? 'CARREGANDO'   :
           st==='loaded'  ? 'VOLTANDO'     : '';
  }
  function spriteFor(r){ return iconDataURI(effectiveState(r)); }

    let selected = null; // {frente, cam}
  function renderTable(){
    const tb = qs('#nl-table tbody');
    const by = {}; S.frentes.forEach(f=>by[f]=[]);
    S.rows.forEach(r=>{ if (by[r.frente]) by[r.frente].push(r); });

    const rowsHtml = S.frentes.map(fr=>{
      const items = by[fr];
      const header = `<tr class="nl-section"><th colspan="6">${fr} — <span style="color:#6b7280;font-weight:400">${items.length} caminhão(ões)</span></th></tr>`;
      if (!items.length) return header;
      const lines = items.map(r=>{
        const st = effectiveState(r);
        const isSel = selected && selected.frente===r.frente && selected.cam===r.cam;
        return `
          <tr class="nl-row ${isSel?'selected':''}" data-fr="${fr}" data-cam="${r.cam}" title="Clique p/ selecionar · C=Chegada · S=Saída · P=Pátio">
            <td style="text-align:left"><img class="nl-sprite" src="${spriteFor(r)}" alt=""/> &nbsp;${fr}</td>
            <td><strong>${r.cam}</strong></td>
            <td>${fmtDT(r.despacho)}</td>
            <td>${fmtDT(r.chegadaFrente)}</td>
            <td>${fmtDT(r.saidaFrente)}</td>
            <td style="color:${COLORS.btn};font-weight:700">${statusLabel(st)}</td>
          </tr>`;
      }).join('');
      return header + lines;
    }).join('');

    tb.innerHTML = rowsHtml;

    qsa('tr.nl-row', tb).forEach(tr=>{
      tr.addEventListener('click', ()=>{
        selected = {frente: tr.dataset.fr, cam: tr.dataset.cam};
        renderTable();
      });
    });
  }

  function fillAddFrentes(){ qs('#nl-add-frente').innerHTML = S.frentes.map(f=>`<option value="${f}">${f}</option>`).join(''); }
  function openAdd(){
    if (!panel.classList.contains('open')) panel.classList.add('open');
    fillAddFrentes(); qs('#nl-add-cam').value=''; modalAdd.classList.add('open'); setTimeout(()=>qs('#nl-add-cam').focus(),0);
  }
  function closeAdd(){ modalAdd.classList.remove('open'); }
  let _pendingAdd = null;
  function continueAdd(){
    const frente = qs('#nl-add-frente').value;
    let cam = (qs('#nl-add-cam').value||'').trim().replace(/\D+/g,'');
    if (!frente || !cam) return alert('Selecione a Frente e digite a Frota (apenas números).');
    const exists = S.rows.find(r => r.frente===frente && r.cam.toLowerCase()===cam.toLowerCase());
    if (exists) return alert('Caminhão já listado nessa frente.');
    _pendingAdd = {frente, cam};
    qs('#nl-conf-text').innerHTML = `Deseja realmente despachar o caminhão <strong>${cam}</strong> para a frente <strong>${frente}</strong>?`;
    modalConf.classList.add('open');
  }
  function confirmAddOk(){
    if (!_pendingAdd) return;
    const {frente, cam} = _pendingAdd;
    S.rows.push({ frente, cam, despacho: nowISO(), state: 'moving' });
    save(S); _pendingAdd=null; modalConf.classList.remove('open'); closeAdd(); renderTable();
  }

  function doArrivalForSelected(){
    if (!selected) { alert('Selecione um caminhão na tabela.'); return; }
    const i = S.rows.findIndex(r=>r.frente===selected.frente && r.cam===selected.cam);
    if (i<0) return;
    if (!S.rows[i].chegadaFrente) S.rows[i].chegadaFrente = nowISO();
    if (S.rows[i].state === 'stopped') S.rows[i].state = null;
    save(S); renderTable();
  }
  function openStopForSelected(){
    if (!selected) { alert('Selecione um caminhão na tabela.'); return; }
    const r = S.rows.find(x=>x.frente===selected.frente && x.cam===selected.cam);
    if (!r) return;
    qs('#nl-stop-cam').value = r.cam;
    qs('#nl-stop-fr').value = r.frente;
    qs('#nl-stop-note').value = r.stopNote || '';
    modalStop.classList.add('open');
  }
  function saveStop(){
    if (!selected) return;
    const i = S.rows.findIndex(x=>x.frente===selected.frente && x.cam===selected.cam);
    if (i<0) return;
    S.rows[i].state = 'stopped';
    S.rows[i].stopNote = (qs('#nl-stop-note').value||'').trim();
    save(S); modalStop.classList.remove('open'); renderTable();
  }
  function clearStop(){
    if (!selected) return;
    const i = S.rows.findIndex(x=>x.frente===selected.frente && x.cam===selected.cam);
    if (i<0) return;
    S.rows[i].state = null;
    S.rows[i].stopNote = '';
    save(S); renderTable();
  }

  /*** HISTÓRICO ***/
  function fillHistDays(){
    const sel = qs('#nl-hist-day');
    const days = Object.keys(S.history).sort().reverse();
    sel.innerHTML = days.length ? days.map(d=>`<option value="${d}">${d}</option>`).join('') : `<option value="">(sem histórico)</option>`;
    return days;
  }
  function renderHistTable(day){
    const wrap = qs('#nl-hist-wrap');
    if (!day || !S.history[day] || !S.history[day].length){
      wrap.innerHTML = `<div style="color:${COLORS.muted};text-align:center">Sem registros para este dia.</div>`; return;
    }
    const rows = S.history[day];
    wrap.innerHTML = `
      <table class="nl-hist">
        <thead><tr><th>Frente</th><th>Caminhão</th><th>Despacho</th><th>Chegada Lavoura</th><th>Saída Lavoura</th><th>Chegada Pátio</th></tr></thead>
        <tbody>${rows.map(r=>`
          <tr><td>${r.frente}</td><td><strong>${r.cam}</strong></td><td>${fmtDT(r.despacho)}</td><td>${fmtDT(r.chegadaFrente)}</td><td>${fmtDT(r.saidaFrente)}</td><td>${fmtDT(r.chegadaPatio)}</td></tr>
        `).join('')}</tbody>
      </table>`;
  }
  function exportHist(day){
    if (!day || !S.history[day] || !S.history[day].length) return alert('Nada para exportar.');
    const cols = ['Dia','Frente','Caminhao','Despacho','ChegadaFrente','SaidaFrente','ChegadaPatio'];
    const csv = [cols.join(';')].concat(S.history[day].map(r =>
      [day,r.frente,r.cam,r.despacho,r.chegadaFrente,r.saidaFrente,r.chegadaPatio].map(v=>(v??'').toString().replace(/;/g,',')).join(';')
    )).join('\n');
    download(`nl-historico-${day}.csv`, csv);
  }
  function deleteHist(day){
    if (!day || !S.history[day]) return;
    const p = prompt(`Excluir histórico do dia ${day}?\nSenha de administrador:`);
    if (p !== PASSWORD) return alert('Senha incorreta. Operação cancelada.');
    if (!confirm(`Tem certeza que deseja apagar o histórico de ${day}?`)) return;
    delete S.history[day]; save(S);
    const days = fillHistDays(); renderHistTable(days[0]||'');
  }

  /*** CONFIG (frentes + assets) ***/
  function renderFrontsList(){
    const el = qs('#nl-fronts-list');
    el.innerHTML = S.frentes.map((f,i)=>`
      <div class="row" data-i="${i}">
        <input value="${f}" data-edit />
        <button data-mv="up">↑</button>
        <button data-mv="down">↓</button>
        <button data-del class="danger">Remover</button>
      </div>
    `).join('');
    qsa('[data-mv]', el).forEach(b=>{
      b.onclick=()=>{
        const i=+b.parentElement.dataset.i, j=b.dataset.mv==='up'?i-1:i+1;
        if (j<0||j>=S.frentes.length) return;
        const t=S.frentes[i]; S.frentes[i]=S.frentes[j]; S.frentes[j]=t; renderFrontsList();
      };
    });
    qsa('[data-del]', el).forEach(b=>{
      b.onclick=()=>{
        const i=+b.parentElement.dataset.i;
        if (S.frentes.length<=1) return alert('Deve haver pelo menos 1 frente.');
        S.frentes.splice(i,1); renderFrontsList();
      };
    });
  }
  function openConfig(){
    const p = prompt('Senha do menu de configuração:');
    if (p !== PASSWORD) return alert('Senha incorreta.');
    renderFrontsList();

    // handlers de ícones (opcional, se não colar SPRITES_EMBED)
    qsa('.nl-modal-assets .row[data-key]').forEach(row=>{
      const key = row.getAttribute('data-key');
      const text = row.querySelector('input[type="text"]');
      const file = row.querySelector('input[type="file"]');
      const saveBtn = row.querySelector('button[data-act="save"]');
      const clrBtn  = row.querySelector('button[data-act="clear"]');

      if (text) text.value = A[key] || '';

      file.onchange = (ev)=>{
        const f = ev.target.files && ev.target.files[0];
        if (!f) return;
        const rd = new FileReader();
        rd.onload = ()=>{ A[key] = rd.result; if (text) text.value = rd.result; saveAssets(A); renderTable(); };
        rd.readAsDataURL(f);
      };
      saveBtn.onclick = ()=>{
        const v = (text && text.value.trim()) || '';
        if (!/^data:image\//i.test(v)) return alert('Cole um data:image;base64 válido ou envie um arquivo.');
        A[key] = v; saveAssets(A); renderTable(); alert('Ícone salvo.');
      };
      clrBtn.onclick = ()=>{
        delete A[key]; saveAssets(A); renderTable(); alert('Ícone limpo.');
      };
    });

    modalCfg.classList.add('open');
  }
  function saveFronts(){
    const edits = qsa('[data-edit]', modalCfg).map(i=>i.value.trim()).filter(Boolean);
    if (!edits.length) return alert('Informe ao menos uma frente.');
    S.frentes = edits;
    const set = new Set(S.frentes);
    S.rows = S.rows.filter(r => set.has(r.frente));
    save(S); renderTable(); modalCfg.classList.remove('open');
  }

  /*** BINDINGS ***/
  // painel
  const btnClose = () => panel.classList.remove('open');
  const btnOpen  = () => { panel.classList.add('open'); renderTable(); };

  btn.onclick = ()=>{ panel.classList.toggle('open'); if (panel.classList.contains('open')) renderTable(); };
  qs('#nl-close').onclick = btnClose;

  // topo
  qs('#nl-add-open').onclick = ()=> openAdd();
  qs('#nl-arrive').onclick  = ()=> doArrivalForSelected();
  qs('#nl-stop').onclick    = ()=> openStopForSelected();
  qs('#nl-stop-clear-top').onclick = ()=> clearStop();
  qs('#nl-hist').onclick    = ()=>{ const d=fillHistDays(); renderHistTable(d[0]||''); modalHist.classList.add('open'); };
  qs('#nl-conf').onclick    = openConfig;

  // modal add
  qs('#nl-add-close').onclick = ()=> modalAdd.classList.remove('open');
  qs('#nl-add-cam').addEventListener('input', e => e.target.value = e.target.value.replace(/\D+/g,''));
  qs('#nl-add-next').onclick = continueAdd;
  modalAdd.addEventListener('keydown', e=>{
    if (e.key==='Enter'){ e.preventDefault(); continueAdd(); }
    if (e.key==='Escape'){ e.preventDefault(); modalAdd.classList.remove('open'); }
  });

  // modal confirm
  qs('#nl-conf-close').onclick = ()=> modalConf.classList.remove('open');
  qs('#nl-conf-cancel').onclick= ()=> modalConf.classList.remove('open');
  qs('#nl-conf-ok').onclick    = confirmAddOk;

  // modal stop
  qs('#nl-stop-close').onclick = ()=> modalStop.classList.remove('open');
  qs('#nl-stop-save').onclick  = saveStop;
  qs('#nl-stop-clear').onclick = clearStop;

  // modal histórico
  qs('#nl-hist-close').onclick = ()=> modalHist.classList.remove('open');
  qs('#nl-hist-day').onchange  = ()=> renderHistTable(qs('#nl-hist-day').value);
  qs('#nl-hist-export').onclick= ()=> exportHist(qs('#nl-hist-day').value);
  qs('#nl-hist-delete').onclick= ()=> deleteHist(qs('#nl-hist-day').value);

  // modal config
  qs('#nl-conf2-close').onclick= ()=> modalCfg.classList.remove('open');
  qs('#nl-add-front').onclick  = ()=>{ const v=(qs('#nl-new-front').value||'').trim(); if(!v) return; S.frentes.push(v); qs('#nl-new-front').value=''; renderFrontsList(); };
  qs('#nl-save-fronts').onclick= saveFronts;
  qs('#nl-reset-fronts').onclick= ()=>{
    if(!confirm('Voltar às 7 frentes padrão?')) return;
    const d=defaultState();
    S.frentes=d.frentes.slice();
    const set=new Set(S.frentes);
    S.rows=S.rows.filter(r=>set.has(r.frente));
    save(S); renderTable(); modalCfg.classList.remove('open');
  };

  /*** TECLAS ***/
  document.addEventListener('keydown', (e)=>{
    if (e.key === 'F8'){ e.preventDefault(); openAdd(); return; }
    if (!panel.classList.contains('open') || !selected) return;
    const k = e.key.toLowerCase();
    const i = S.rows.findIndex(r => r.frente===selected.frente && r.cam===selected.cam);
    if (i<0) return;
    if (k==='c'){ doArrivalForSelected(); }
    if (k==='s'){ S.rows[i].saidaFrente = nowISO(); if (S.rows[i].state === 'stopped') S.rows[i].state=null; save(S); renderTable(); }
    if (k==='p'){
      const reg = S.rows[i], day = todayKey();
      if (!S.history[day]) S.history[day] = [];
      S.history[day].push({ frente: reg.frente, cam: reg.cam, despacho: reg.despacho||nowISO(), chegadaFrente: reg.chegadaFrente||'', saidaFrente: reg.saidaFrente||'', chegadaPatio: nowISO() });
      S.rows.splice(i,1); save(S); selected=null; renderTable();
    }
  });

  // inicial
  renderTable();
})();
