# Opeyemi-Faleye-Lending-App
Opeyemi Faleye Lending App
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>OPEYEMI LOAN APP</title>
<style>
nav {
      margin-top: 10px;
    }
    nav a {
      color: #ffd700;
      margin: 0 15px;
      text-decoration: through-line;
      font-weight: bold;
    }
    nav a:hover {
      text-decoration: through-line;
    }
  :root{
    --accent:#1e90ff;
    --card-radius:12px;
  }
  *{box-sizing:border-box}
  body{font-family:Inter,Arial,Helvetica,sans-serif;margin:0;background:#0f1720;color:#e6eef8;min-height:100vh}
  body.light{background:#f4f7fb;color:#0b1220}
  .wrap{max-width:980px;margin:16px auto;padding:14px}
  header{display:flex;flex-wrap:wrap;justify-content:space-between;align-items:center;gap:12px}
  h1{margin:0;font-size:18px}
  .controls{display:flex;gap:8px;flex-wrap:wrap}
  button{background:var(--accent);color:#fff;border:0;padding:8px 10px;border-radius:8px;cursor:pointer;font-size:14px}
  button.ghost{background:transparent;color:inherit;border:1px solid rgba(255,255,255,0.08)}
  .card{background:rgba(255,255,255,0.03);padding:12px;border-radius:var(--card-radius);margin-top:12px}
  body.light .card{background: #fff;border:1px solid #e6eef8}
  label{display:block;font-size:13px;margin-bottom:6px}
  input,select,textarea{width:100%;padding:8px;border-radius:8px;border:1px solid rgba(0,0,0,0.08);font-size:14px}
  .grid{display:grid;grid-template-columns:1fr 1fr;gap:10px}
  .row{display:flex;gap:8px}
  .muted{opacity:0.75;font-size:13px}
  table{width:100%;border-collapse:collapse;margin-top:10px}
  th,td{padding:8px;border-bottom:1px solid rgba(255,255,255,0.04);text-align:left;font-size:14px}
  .actions button{background:transparent;border:0;color:var(--accent);padding:6px;cursor:pointer}
  .status-paid{color:#2ecc71;font-weight:600}
  .status-unpaid{color:#ff9f1c;font-weight:600}
  @media(max-width:720px){.grid{grid-template-columns:1fr}.row{flex-direction:column}}
  footer{margin-top:12px;font-size:13px;color:inherit;opacity:0.9}
  .small{padding:6px 8px;font-size:13px}
</style>
</head>
 <nav>
      <a href="#">Home</a>
      <a href="#">Articles</a>
      <a href="https://wa.link/b2x5ni">About</a>
      <a href="+2347971812772, +2348028350534">Contact</a>
      <a href="#">Blog</a>
    </nav>
<div class="wrap">
  <header>
    <h1>Opeyemi Faleye Lending App </h1>
    <div class="controls">
      <button id="exportBtn" class="small">Export CSV</button>
      <button id="importBtn" class="small">Import CSV</button>
      <button id="sendWhatsBtn" class="small">Submit (WhatsApp)</button>
      <button id="clearBtn" class="small ghost">Clear All</button>
      <button id="modeBtn" class="small ghost">Dark/Light</button>
      <button id="restartBtn" class="small ghost">Restart App</button>
    </div>
  </header>

  <section class="card" aria-label="Add borrower">
    <strong>Add / Update Borrower</strong>
    <div style="margin-top:10px" class="grid">
      <div>
        <label for="name">Full name</label>
        <input id="name" placeholder="John Doe" />
      </div>
      <div>
        <label for="phone">Phone (required)</label>
        <input id="phone" placeholder="+234..." />
      </div>
      <div>
          <label for="gmail">Gmail (required)</label>
          <input id="gmail" type="gmail" placeholder="e.g. gbenguloflavour@gmail.com" />
      </div>
      <div>
          <label for="nin">Nin (required)</label>
          <input id="nin" type="number" placeholder="e.g. 1234567890" />
      </div>
      <div>
          <label for="bvn">Bvn (required)</label>
          <input id="bvn" type="number" placeholder="e.g. 1234567890" />
      </div>
      <div>
      <label for="address">Address</label>
      <input id="address" type="number,text" placeholder="e.g. 16 Mogaji Street" />
      </div>
      <div>
      <label for="state">State:</label>
      <select id="state" text="state">
      <option value="oyo">Oyo</option>
      <option value="osun">Osun</option>
      <option value="abia">Abia</option>
      <option value="lagos">Lagos</option>
      </select>
      <input id="state" type="text" placeholder="e.g. Lagos" />
      </div>
      <div>
        <label for="amount">Amount (NGN)</label>
        <input id="amount" type="number" placeholder="e.g. 5000" />
      </div>
      <div>
        <label for="due">Due date</label>
        <input id="due" type="date" />
      </div>
      <div>
          <label for="account to be credited">Account To Be Credited</label>
          <input id="account to be credited" type="number" placeholder="e.g. 1234567890" />
      </div>
      <div>
          <label for="bank account"> Bank Account</label>
          <select id="bank account" text="bank account:">
          <option value="bank account">Bank Account</option>
          <option value="uba bank">Uba Bank</option>
          <option value="gtb bank">Gtb Bank</option>
          <option value="moniepoint">Moniepoint</option>
          <option value="access bank">Access Bank</option>
          <option value="union bank">Union Bank</option>
          <option value="palmpay">Palmpay</option>
          <option value="opay">Opay</option>
          <input id="bank account" type="number" placeholder="e.g. Polaris Bank" />
      </div>
      <div style="grid-column:1 / -1">
        <label for="notes">Notes / Terms</label>
        <textarea id="notes" rows="2" placeholder="Reason or notes..."></textarea>
      </div>
    </div>
    <div style="margin-top:10px;display:flex;gap:8px;flex-wrap:wrap">
      <button id="addBtn">Summit</button>
      <button id="addAndMessageBtn" class="ghost">Add & Message via WhatsApp</button>
      <div style="flex:1"></div>
      <div class="muted">Storage: localStorage (this browser)</div>
    </div>
  </section>

  <section class="card" aria-label="Filters">
    <div style="display:flex;gap:8px;align-items:center;flex-wrap:wrap">
      <div class="muted">Filter:</div>
      <select id="filterSelect">
        <option value="all">All</option>
        <option value="unpaid">Unpaid</option>
        <option value="paid">Paid</option>
        <option value="overdue">Overdue</option>
      </select>
      <input id="search" placeholder="Search name or phone" style="min-width:160px" />
      <div style="flex:1"></div>
      <div class="muted">Tier:</div>
      <select id="levelSelect">
        <option value="1">Tier 1</option>
        <option value="2">Tier 2</option>
        <option value="3">Tier 3</option>
      </select>
    </div>
  </section>

  <section class="card" aria-label="Records">
    <strong>Records</strong>
    <div id="summary" class="muted" style="margin-top:8px"></div>
    <table id="table" aria-live="polite">
      <thead><tr><th>Name</th><th>Phone</th><th>Amount</th><th>Due</th><th>Status</th><th>Notes</th><th>Actions</th></tr></thead>
      <tbody></tbody>
    </table>
  </section>

  <footer class="muted">Tip: Export CSV to backup to the system. "Send Summary" opens WhatsApp with a prefilled message to +2347071812772.</footer>
</div>

<!-- Sounds -->
<audio id="okSound" src="https://www.soundjay.com/buttons/sounds/button-4.mp3"></audio>
<audio id="errSound" src="https://www.soundjay.com/buttons/sounds/button-10.mp3"></audio>

<script>
(() => {
  const STORAGE_KEY = "borrower_ledger_v1";
  const WHATSAPP_NUMBER = "+2347071812772"; // pre-fill recipient (message is not sent automatically)
  const okSound = document.getElementById('okSound');
  const errSound = document.getElementById('errSound');

  // elements
  const nameEl = document.getElementById('name');
  const phoneEl = document.getElementById('phone');
  const amountEl = document.getElementById('amount');
  const dueEl = document.getElementById('due');
  const notesEl = document.getElementById('notes');
  const addBtn = document.getElementById('addBtn');
  const addAndMessageBtn = document.getElementById('addAndMessageBtn');
  const tableBody = document.querySelector('#table tbody');
  const summaryEl = document.getElementById('summary');
  const exportBtn = document.getElementById('exportBtn');
  const importBtn = document.getElementById('importBtn');
  const clearBtn = document.getElementById('clearBtn');
  const modeBtn = document.getElementById('modeBtn');
  const sendWhatsBtn = document.getElementById('sendWhatsBtn');
  const filterSelect = document.getElementById('filterSelect');
  const searchEl = document.getElementById('search');
  const levelSelect = document.getElementById('levelSelect');
  const restartBtn = document.getElementById('restartBtn');

  // data
  let records = []; // {id,name,phone,amount,dueISO,notes,paidAmount,createdISO}
  let dark = true;

  // helpers
  function uid(){ return Date.now().toString(36) + Math.random().toString(36).slice(2,7); }
  function save(){ try { localStorage.setItem(STORAGE_KEY, JSON.stringify(records)); } catch(e){ console.error(e); } }
  function load(){ try { const raw = localStorage.getItem(STORAGE_KEY); records = raw ? JSON.parse(raw) : []; } catch(e){ records = []; } }
  function formatCurrency(n){ return Number(n).toLocaleString(undefined,{style:'currency',currency:'NGN',maximumFractionDigits:0}); }
  function todayISO(){ const d=new Date(); d.setHours(0,0,0,0); return d.toISOString(); }

  // actions
  function addRecord(){
    const name = nameEl.value.trim();
    const phone = phoneEl.value.trim();
    const amount = Number(amountEl.value) || 0;
    const due = dueEl.value || null;
    const notes = notesEl.value.trim();
    if(!name || amount <= 0){ errSound.play(); alert("Please enter a valid name and positive amount."); return; }
    const rec = { id: uid(), name, phone, amount, dueISO: due, notes, paidAmount: 0, createdISO: new Date().toISOString() };
    records.push(rec);
    save(); render(); okSound.play();
    // reset form
    nameEl.value=''; phoneEl.value=''; amountEl.value=''; dueEl.value=''; notesEl.value='';
  }

  function addRecordAndMessage(){
    addRecord();
    // send prefilled message about last added record
    const r = records[records.length-1];
    if(r) openWhatsAppForRecord(r);
  }

  function openWhatsAppForRecord(r){
    const owed = Math.max(0, r.amount - (r.paidAmount||0));
    const lines = [
      `New borrower record:`,
      `Name: ${r.name}`,
      `Phone: ${r.phone || 'N/A'}`,
      `Amount: ${r.amount}`,
      `Outstanding: ${owed}`,
      `Due: ${r.dueISO ? (new Date(r.dueISO).toLocaleDateString()) : 'N/A'}`,
      `Notes: ${r.notes || '-'}`,
    ];
    const txt = encodeURIComponent(lines.join("\n"));
    const num = WHATSAPP_NUMBER.replace(/\D/g,'');
    const url = `https://wa.me/${num}?text=${txt}`;
    window.open(url,'_blank');
  }

  function recordPayment(id){
    const r = records.find(x=>x.id===id);
    if(!r) return;
    const amtStr = prompt(`Enter payment amount for ${r.name}:`, String(Math.max(1, r.amount - (r.paidAmount||0))));
    if(amtStr === null) return;
    const amt = Number(amtStr);
    if(isNaN(amt) || amt <= 0){ errSound.play(); alert('Invalid payment amount'); return; }
    r.paidAmount = Math.min(r.amount, (Number(r.paidAmount||0) + amt));
    save(); render(); okSound.play();
  }

  function markPaid(id){
    const r = records.find(x=>x.id===id);
    if(!r) return;
    r.paidAmount = r.amount;
    save(); render(); okSound.play();
  }

  function delRecord(id){
    if(!confirm('Delete this record?')) return;
    records = records.filter(x=>x.id!==id);
    save(); render();
  }

  // render UI
  function render(){
    const filter = filterSelect.value;
    const q = searchEl.value.trim().toLowerCase();
    const tier = levelSelect.value;
    let rows = records.slice();

    if(filter === 'unpaid') rows = rows.filter(r=> (r.paidAmount||0) < r.amount);
    if(filter === 'paid') rows = rows.filter(r=> (r.paidAmount||0) >= r.amount);
    if(filter === 'overdue') rows = rows.filter(r=> r.dueISO && new Date(r.dueISO) < new Date() && (r.paidAmount||0) < r.amount);
    if(q) rows = rows.filter(r=> r.name.toLowerCase().includes(q) || (r.phone||'').includes(q));

    rows.sort((a,b) => {
      if(a.dueISO && b.dueISO) return new Date(a.dueISO) - new Date(b.dueISO);
      if(a.dueISO) return -1;
      if(b.dueISO) return 1;
      return new Date(b.createdISO) - new Date(a.createdISO);
    });

    tableBody.innerHTML = '';
    rows.forEach(r=>{
      const tr = document.createElement('tr');
      const status = (r.paidAmount||0) >= r.amount ? 'paid' : (r.dueISO && new Date(r.dueISO) < new Date() ? 'overdue' : 'unpaid');
      tr.innerHTML = `
        <td>${escapeHTML(r.name)}</td>
        <td class="muted">${escapeHTML(r.phone || '-')}</td>
        <td>${formatCurrency(r.amount)}</td>
        <td class="muted">${r.dueISO ? new Date(r.dueISO).toLocaleDateString() : '-'}</td>
        <td class="${status==='paid' ? 'status-paid' : 'status-unpaid'}">${status.toUpperCase()}</td>
        <td class="muted">${escapeHTML(r.notes || '')}</td>
        <td class="actions">
          <button title="Add payment" onclick="window.__ledger.recordPayment('${r.id}')">Pay</button>
          <button title="Mark fully paid" onclick="window.__ledger.markPaid('${r.id}')">Mark Paid</button>
          <button title="Message via WhatsApp" onclick="window.__ledger.messageRecord('${r.id}')">Message</button>
          <button title="Delete" onclick="window.__ledger.delRecord('${r.id}')">Delete</button>
        </td>`;
      tableBody.appendChild(tr);
    });

    // summary
    const total = records.reduce((s,x)=>s + Number(x.amount||0),0);
    const outstanding = records.reduce((s,x)=> s + Math.max(0, Number(x.amount||0) - Number(x.paidAmount||0)), 0);
    const unpaidCount = records.filter(r=> (r.paidAmount||0) < r.amount).length;
    summaryEl.textContent = `Total lent: ${formatCurrency(total)} • Outstanding: ${formatCurrency(outstanding)} • Unpaid: ${unpaidCount} • Tier: ${tier}`;
  }

  // export / import CSV
  function exportCSV(){
    if(!records.length){ alert('No records to export'); return; }
    const header = ['id','name','phone','amount','dueISO','notes','paidAmount','createdISO'];
    const rows = records.map(r => header.map(h => `"${String(r[h]||'').replace(/"/g,'""')}"`).join(','));
    const csv = [header.join(','), ...rows].join('\n');
    const blob = new Blob([csv], {type:'text/csv'});
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url; a.download = 'borrowers.csv'; a.click();
    URL.revokeObjectURL(url);
    okSound.play();
  }

  function importCSV(){
    const inp = document.createElement('input');
    inp.type = 'file'; inp.accept = '.csv,text/csv';
    inp.onchange = e => {
      const file = e.target.files[0]; if(!file) return;
      const reader = new FileReader();
      reader.onload = ev => {
        try {
          const text = ev.target.result;
          const lines = text.split(/\r?\n/).filter(Boolean);
          const header = parseCSVLine(lines.shift());
          const parsed = lines.map(line => {
            const parts = parseCSVLine(line);
            const obj = {};
            header.forEach((h,i)=> obj[h.trim()] = parts[i] === undefined ? '' : parts[i]);
            return obj;
          });
          parsed.forEach(p => {
            if(!p.id) p.id = uid();
            p.amount = Number(p.amount) || 0;
            p.paidAmount = Number(p.paidAmount) || 0;
            records.push(p);
          });
          save(); render(); okSound.play();
        } catch (err) { console.error(err); alert('Import failed'); errSound.play(); }
      };
      reader.readAsText(file);
    };
    inp.click();
  }

  // simple CSV parse for quoted fields
  function parseCSVLine(line){
    const parts = [];
    let cur = ''; let inQuotes = false;
    for(let i=0;i<line.length;i++){
      const ch = line[i];
      if(ch === '"' ){
        if(inQuotes && line[i+1] === '"'){ cur += '"'; i++; } else { inQuotes = !inQuotes; }
      } else if(ch === ',' && !inQuotes){
        parts.push(cur); cur = '';
      } else cur += ch;
    }
    parts.push(cur);
    return parts.map(s => s.replace(/^"|"$/g,''));
  }

  // clear and restart
  function clearAll(){
    if(!confirm('Clear all stored data? This cannot be undone.')) return;
    records = []; save(); render(); okSound.play();
  }
  function restartApp(){
    if(!confirm('Restart app: will remove local storage and reload the page?')) return;
    localStorage.removeItem(STORAGE_KEY);
    location.reload();
  }

  // send WhatsApp summary (prefill, open WhatsApp app/web)
  function sendWhatsApp(){
    if(!records.length){ alert('No records to send'); return; }
    const lines = ['Borrower Ledger Summary:'];
    records.slice(0,20).forEach(r => {
      const owed = Math.max(0, Number(r.amount||0) - Number(r.paidAmount||0));
      lines.push(`${r.name} (${r.phone || 'no-phone'}): owes ${owed} due ${r.dueISO ? new Date(r.dueISO).toLocaleDateString() : 'N/A'}`);
    });
    if(records.length > 20) lines.push(`...and ${records.length - 20} more records`);
    const txt = encodeURIComponent(lines.join('\n'));
    const num = WHATSAPP_NUMBER.replace(/\D/g,'');
    const url = `https://wa.me/${num}?text=${txt}`;
    window.open(url,'_blank');
  }

  // message a single record
  function messageRecord(id){
    const r = records.find(x=>x.id===id);
    if(!r) return;
    openWhatsAppForRecord(r);
  }

  // small utility to escape HTML
  function escapeHTML(s){ return String(s).replace(/[&<>"']/g, c => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c])); }

  // expose some functions for inline onclicks
  window.__ledger = {
    recordPayment: recordPayment,
    markPaid: markPaid,
    delRecord: delRecord,
    messageRecord: messageRecord
  };

  // events
  addBtn.addEventListener('click', addRecord);
  addAndMessageBtn.addEventListener('click', addRecordAndMessage);
  exportBtn.addEventListener('click', exportCSV);
  importBtn.addEventListener('click', importCSV);
  clearBtn.addEventListener('click', clearAll);
  modeBtn.addEventListener('click', ()=> {
    dark = !dark;
    document.body.className = dark ? '' : 'light';
  });
  sendWhatsBtn.addEventListener('click', sendWhatsApp);
  filterSelect.addEventListener('change', render);
  searchEl.addEventListener('input', render);
  levelSelect.addEventListener('change', render);
  restartBtn.addEventListener('click', restartApp);

  // init
  load();
  render();
})();
</script>
</body>
</html>
