[index_1.html](https://github.com/user-attachments/files/31817019/index_1.html)
<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>הובלות דניאל דוד</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Heebo:wght@400;500;600;700;800&display=swap">
<style>
:root {
  --navy:        #0E1C2F;
  --navy-mid:    #1C3350;
  --amber:       #F5A623;
  --amber-dark:  #D4890A;
  --income:      #16A34A;
  --income-bg:   #D1FAE5;
  --income-txt:  #065F46;
  --expense:     #DC2626;
  --expense-bg:  #FEE2E2;
  --expense-txt: #991B1B;
  --bg:          #F0F4F8;
  --card:        #FFFFFF;
  --border:      #D1D9E0;
  --border-soft: #E8EDF2;
  --txt:         #0E1C2F;
  --txt-sec:     #4A6080;
  --txt-muted:   #8A9BB0;
  --radius:      10px;
  --radius-lg:   16px;
  --shadow:      0 2px 8px rgba(14,28,47,.08), 0 0 0 1px rgba(14,28,47,.04);
  --shadow-lg:   0 8px 24px rgba(14,28,47,.14);
}
@media (prefers-color-scheme: dark) {
  :root:not([data-theme="light"]) {
    --bg:          #07111C; --card:        #0E1C2F;
    --border:      #1C3350; --border-soft: #162840;
    --txt:         #E2EBF4; --txt-sec:     #7A99BB; --txt-muted: #3D5570;
    --income-bg:   #064E2A; --income-txt:  #6EE7A0;
    --expense-bg:  #5A0F0F; --expense-txt: #FCA5A5;
    --shadow:      0 2px 8px rgba(0,0,0,.3), 0 0 0 1px rgba(255,255,255,.04);
    --shadow-lg:   0 8px 24px rgba(0,0,0,.4);
  }
}
:root[data-theme="dark"] {
  --bg:          #07111C; --card:        #0E1C2F;
  --border:      #1C3350; --border-soft: #162840;
  --txt:         #E2EBF4; --txt-sec:     #7A99BB; --txt-muted: #3D5570;
  --income-bg:   #064E2A; --income-txt:  #6EE7A0;
  --expense-bg:  #5A0F0F; --expense-txt: #FCA5A5;
  --shadow:      0 2px 8px rgba(0,0,0,.3), 0 0 0 1px rgba(255,255,255,.04);
  --shadow-lg:   0 8px 24px rgba(0,0,0,.4);
}

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
body { font-family: 'Heebo', system-ui, sans-serif; background: var(--bg); color: var(--txt); min-height: 100vh; line-height: 1.6; }
button { font-family: inherit; cursor: pointer; border: none; }
input, select, textarea { font-family: inherit; }
:focus-visible { outline: 2px solid var(--amber); outline-offset: 2px; }

/* HEADER */
.site-header { background: var(--navy); padding: 0 20px; display: flex; align-items: center; justify-content: space-between; position: sticky; top: 0; z-index: 50; min-height: 60px; box-shadow: 0 2px 16px rgba(0,0,0,.35); }
.site-header h1 { font-size: 1.05rem; font-weight: 800; color: #fff; display: flex; align-items: center; gap: 10px; line-height: 1.2; }
.site-header h1 .sub { font-weight: 500; font-size: .7rem; color: var(--amber); display: block; letter-spacing: .04em; text-transform: uppercase; }
.header-icon { width: 34px; height: 34px; background: var(--amber); border-radius: 8px; display: flex; align-items: center; justify-content: center; font-size: 1.1rem; flex-shrink: 0; }
.header-actions { display: flex; gap: 8px; align-items: center; }
.btn-header { background: rgba(255,255,255,.1); color: #fff; border: 1px solid rgba(255,255,255,.15); border-radius: 8px; padding: 6px 14px; font-size: .82rem; font-weight: 600; display: flex; align-items: center; gap: 6px; transition: background .15s; }
.btn-header:hover { background: rgba(255,255,255,.18); }
.btn-theme { background: rgba(255,255,255,.1); color: #fff; border: 1px solid rgba(255,255,255,.15); border-radius: 8px; width: 36px; height: 36px; display: flex; align-items: center; justify-content: center; font-size: 1rem; transition: background .15s; }
.btn-theme:hover { background: rgba(255,255,255,.18); }

/* MAIN TABS */
.tabs-bar { background: var(--navy-mid); display: flex; }
.tab-btn { flex: 1; padding: 14px 8px; background: transparent; color: rgba(255,255,255,.55); font-size: .9rem; font-weight: 600; border-bottom: 3px solid transparent; transition: color .15s, border-color .15s; text-align: center; }
.tab-btn:hover { color: rgba(255,255,255,.85); }
.tab-btn.active { color: var(--amber); border-bottom-color: var(--amber); }
.main-content { max-width: 780px; margin: 0 auto; padding: 20px 16px 60px; }
.tab-panel { display: none; }
.tab-panel.active { display: block; }
.section-title { font-size: 1.15rem; font-weight: 800; color: var(--txt); margin-bottom: 16px; display: flex; align-items: center; gap: 8px; }
.card { background: var(--card); border: 1px solid var(--border-soft); border-radius: var(--radius-lg); box-shadow: var(--shadow); padding: 20px; margin-bottom: 16px; }

/* QUICK ACTION BUTTONS (Entry tab) */
.quick-btns { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin-bottom: 20px; }
.quick-btn { border-radius: var(--radius-lg); padding: 20px 16px; font-size: 1rem; font-weight: 800; display: flex; flex-direction: column; align-items: center; gap: 8px; border: 2px solid transparent; transition: transform .12s, box-shadow .12s; }
.quick-btn:active { transform: scale(.97); }
.quick-btn .qb-icon { font-size: 1.8rem; }
.quick-btn .qb-label { font-size: .9rem; }
.quick-btn.income-btn { background: var(--income-bg); color: var(--income-txt); border-color: var(--income); box-shadow: 0 4px 12px rgba(22,163,74,.15); }
.quick-btn.income-btn:hover { box-shadow: 0 6px 18px rgba(22,163,74,.25); }
.quick-btn.expense-btn { background: var(--expense-bg); color: var(--expense-txt); border-color: var(--expense); box-shadow: 0 4px 12px rgba(220,38,38,.12); }
.quick-btn.expense-btn:hover { box-shadow: 0 6px 18px rgba(220,38,38,.2); }
@media (max-width: 380px) { .quick-btns { grid-template-columns: 1fr; } }

/* FORM */
.form-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 14px; }
.form-grid .full { grid-column: 1 / -1; }
@media (max-width: 480px) { .form-grid { grid-template-columns: 1fr; } .form-grid .full { grid-column: 1; } }
.form-group { display: flex; flex-direction: column; gap: 5px; }
.form-label { font-size: .82rem; font-weight: 700; color: var(--txt-sec); text-transform: uppercase; letter-spacing: .05em; }
.form-control { background: var(--bg); border: 1.5px solid var(--border); border-radius: var(--radius); padding: 10px 13px; font-size: .95rem; color: var(--txt); transition: border-color .15s, box-shadow .15s; width: 100%; }
.form-control:focus { border-color: var(--amber); box-shadow: 0 0 0 3px rgba(245,166,35,.15); outline: none; }
.form-control::placeholder { color: var(--txt-muted); }
select.form-control { appearance: none; cursor: pointer; }
.form-control.auto-filled { border-color: var(--income); background: var(--income-bg); color: var(--income-txt); font-weight: 700; }

/* Work type toggle (הובלה/הנפה) */
.work-toggle { display: grid; grid-template-columns: 1fr 1fr; gap: 8px; }
.work-btn { padding: 14px; border-radius: var(--radius); font-size: .95rem; font-weight: 700; border: 2px solid var(--border); background: var(--bg); color: var(--txt-muted); transition: all .15s; text-align: center; display: flex; flex-direction: column; align-items: center; gap: 4px; }
.work-btn .wb-icon { font-size: 1.4rem; }
.work-btn.active { background: var(--income-bg); border-color: var(--income); color: var(--income-txt); }
.work-btn:hover:not(.active) { border-color: var(--txt-muted); color: var(--txt); }

/* Amount wrap */
.amount-wrap { position: relative; }
.amount-wrap .currency { position: absolute; left: 12px; top: 50%; transform: translateY(-50%); color: var(--txt-muted); font-weight: 700; pointer-events: none; }
.amount-wrap .form-control { padding-left: 36px; }
.price-hint { font-size: .8rem; color: var(--income-txt); font-weight: 600; margin-top: 3px; display: none; }
.price-hint.visible { display: block; }

/* Expense type toggle */
.type-toggle { display: grid; grid-template-columns: 1fr 1fr; gap: 6px; }
.type-btn { padding: 11px; border-radius: var(--radius); font-size: .95rem; font-weight: 700; border: 2px solid var(--border); background: var(--bg); color: var(--txt-muted); transition: all .15s; }
.type-btn.income.active { background: var(--income-bg); border-color: var(--income); color: var(--income-txt); }
.type-btn.expense.active { background: var(--expense-bg); border-color: var(--expense); color: var(--expense-txt); }

/* Buttons */
.btn-primary { background: var(--amber); color: var(--navy); border-radius: var(--radius); padding: 13px 24px; font-size: 1rem; font-weight: 800; width: 100%; transition: background .15s, transform .1s; display: flex; align-items: center; justify-content: center; gap: 8px; }
.btn-primary:hover { background: var(--amber-dark); }
.btn-primary:active { transform: scale(.98); }
.btn-secondary { background: var(--bg); color: var(--txt); border: 1.5px solid var(--border); border-radius: var(--radius); padding: 10px 18px; font-size: .9rem; font-weight: 600; transition: background .15s; display: flex; align-items: center; gap: 6px; justify-content: center; }
.btn-secondary:hover { background: var(--border-soft); }

/* Sync badge */
.sync-badge { position: fixed; bottom: 20px; left: 16px; background: var(--card); border: 1.5px solid var(--border); border-radius: 20px; padding: 6px 14px 6px 10px; font-size: .78rem; font-weight: 700; color: var(--txt-sec); display: flex; align-items: center; gap: 7px; box-shadow: var(--shadow-lg); cursor: pointer; z-index: 90; transition: background .15s; user-select: none; }
.sync-badge:hover { background: var(--border-soft); }
.sync-dot { width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0; transition: background .3s; }
@keyframes syncPulse { 0%,100%{opacity:1} 50%{opacity:.25} }
.sync-dot.loading { animation: syncPulse .9s infinite; }

/* ── LOGIN SCREEN ────────────────────────────────────────── */
#loginScreen { position:fixed; inset:0; z-index:9999; background:var(--navy); display:flex; align-items:center; justify-content:center; }
.login-box { background:var(--card); border-radius:20px; padding:40px 36px 36px; width:100%; max-width:380px; box-shadow:var(--shadow-lg); text-align:center; }
.login-logo { font-size:2.4rem; margin-bottom:4px; }
.login-title { font-size:1.3rem; font-weight:800; color:var(--txt); margin-bottom:4px; }
.login-sub { font-size:.82rem; color:var(--txt-muted); margin-bottom:28px; }
.login-field { text-align:right; margin-bottom:14px; }
.login-field label { display:block; font-size:.78rem; font-weight:700; color:var(--txt-sec); margin-bottom:5px; }
.login-field input { width:100%; box-sizing:border-box; padding:12px 14px; border:1.5px solid var(--border); border-radius:var(--radius); font-family:inherit; font-size:.95rem; background:var(--bg); color:var(--txt); outline:none; transition:border .15s; }
.login-field input:focus { border-color:var(--amber); }
.login-btn { width:100%; padding:13px; background:var(--amber); color:var(--navy); border-radius:var(--radius); font-size:1rem; font-weight:800; margin-top:6px; transition:background .15s; }
.login-btn:hover { background:var(--amber-dark); }
.login-err { color:var(--expense); font-size:.82rem; margin-top:10px; min-height:18px; }

/* Toast */
.toast-wrap { position: fixed; bottom: 24px; left: 50%; transform: translateX(-50%); z-index: 200; display: flex; flex-direction: column; align-items: center; gap: 8px; pointer-events: none; }
.toast { background: var(--navy); color: #fff; padding: 11px 22px; border-radius: 100px; font-size: .9rem; font-weight: 600; box-shadow: var(--shadow-lg); opacity: 0; transform: translateY(12px); animation: toastIn .25s ease forwards, toastOut .3s ease 2.2s forwards; }
@keyframes toastIn  { to { opacity:1; transform:translateY(0); } }
@keyframes toastOut { to { opacity:0; transform:translateY(12px); } }

/* Filters */
.filters-bar { background: var(--card); border: 1px solid var(--border-soft); border-radius: var(--radius-lg); padding: 16px; margin-bottom: 14px; display: flex; flex-wrap: wrap; gap: 10px; align-items: flex-end; box-shadow: var(--shadow); }
.filter-group { display: flex; flex-direction: column; gap: 4px; min-width: 120px; flex: 1; }
.filter-label { font-size: .75rem; font-weight: 700; color: var(--txt-muted); text-transform: uppercase; letter-spacing: .05em; }
.filter-control { background: var(--bg); border: 1.5px solid var(--border); border-radius: var(--radius); padding: 8px 10px; font-size: .88rem; color: var(--txt); }
.filter-control:focus { border-color: var(--amber); outline: none; }
.btn-filter-reset { background: var(--bg); border: 1.5px solid var(--border); color: var(--txt-sec); border-radius: var(--radius); padding: 8px 14px; font-size: .85rem; font-weight: 600; align-self: flex-end; }
.btn-filter-reset:hover { background: var(--border-soft); }

/* Table */
.table-wrap { overflow-x: auto; border-radius: var(--radius-lg); box-shadow: var(--shadow); }
table { width: 100%; border-collapse: collapse; background: var(--card); font-size: .88rem; }
thead th { background: var(--navy); color: rgba(255,255,255,.75); font-size: .75rem; font-weight: 700; text-transform: uppercase; letter-spacing: .05em; padding: 11px 14px; white-space: nowrap; text-align: right; }
tbody tr { border-bottom: 1px solid var(--border-soft); transition: background .12s; }
tbody tr:last-child { border-bottom: none; }
tbody tr:hover { background: var(--bg); }
td { padding: 11px 14px; color: var(--txt); vertical-align: middle; }
.amount { font-weight: 700; font-variant-numeric: tabular-nums; }
.amount.income { color: var(--income); }
.amount.expense { color: var(--expense); }
.badge { display: inline-flex; align-items: center; padding: 3px 9px; border-radius: 100px; font-size: .77rem; font-weight: 700; white-space: nowrap; }
.badge.income { background: var(--income-bg); color: var(--income-txt); }
.badge.expense { background: var(--expense-bg); color: var(--expense-txt); }
.action-btns { display: flex; gap: 6px; }
.btn-icon { width: 30px; height: 30px; border-radius: 7px; display: flex; align-items: center; justify-content: center; font-size: .85rem; background: var(--bg); border: 1px solid var(--border); color: var(--txt-sec); transition: all .12s; }
.btn-icon.del:hover { background: var(--expense-bg); border-color: var(--expense); color: var(--expense); }
.empty-state { text-align: center; padding: 48px 20px; color: var(--txt-muted); font-size: .95rem; background: var(--card); border-radius: var(--radius-lg); border: 1px solid var(--border-soft); box-shadow: var(--shadow); }
.empty-state .icon { font-size: 2.5rem; margin-bottom: 12px; display: block; }

/* Summary cards */
.summary-grid { display: grid; grid-template-columns: repeat(3,1fr); gap: 12px; margin-bottom: 16px; }
@media (max-width: 500px) { .summary-grid { grid-template-columns: 1fr; } }
.summary-card { background: var(--card); border: 1px solid var(--border-soft); border-radius: var(--radius-lg); padding: 16px; box-shadow: var(--shadow); text-align: center; }
.summary-card .label { font-size: .75rem; font-weight: 700; text-transform: uppercase; letter-spacing: .05em; color: var(--txt-muted); margin-bottom: 6px; }
.summary-card .value { font-size: 1.4rem; font-weight: 800; font-variant-numeric: tabular-nums; line-height: 1.2; }
.summary-card.income-card .value { color: var(--income); }
.summary-card.expense-card .value { color: var(--expense); }
.summary-card.profit-card .value { color: var(--amber-dark); }
.summary-card.profit-card.negative .value { color: var(--expense); }

/* Report */
.report-table-wrap { overflow-x: auto; border-radius: var(--radius-lg); box-shadow: var(--shadow); margin-bottom: 16px; }
.report-table { width: 100%; border-collapse: collapse; background: var(--card); font-size: .88rem; }
.report-table thead th { background: var(--navy); color: rgba(255,255,255,.75); font-size: .75rem; font-weight: 700; text-transform: uppercase; letter-spacing: .05em; padding: 11px 14px; text-align: right; }
.report-table td { padding: 12px 14px; border-bottom: 1px solid var(--border-soft); font-variant-numeric: tabular-nums; }
.report-table tr:last-child td { border-bottom: none; }
.report-table tbody tr:hover { background: var(--bg); }
.report-table .total-row { background: var(--navy) !important; font-weight: 800; }
.report-table .total-row td { color: #fff; border: none; }
.income-col { color: var(--income); font-weight: 700; }
.expense-col { color: var(--expense); font-weight: 700; }
.profit-col { font-weight: 800; }
.profit-pos { color: var(--income); }
.profit-neg { color: var(--expense); }
.pct-badge { display: inline-flex; padding: 2px 8px; border-radius: 100px; font-size: .78rem; font-weight: 700; margin-left: 6px; }
.pct-pos { background: var(--income-bg); color: var(--income-txt); }
.pct-neg { background: var(--expense-bg); color: var(--expense-txt); }
.month-selector-row { display: flex; gap: 10px; align-items: flex-end; flex-wrap: wrap; margin-bottom: 16px; }
.btn-export { background: var(--navy); color: #fff; border-radius: var(--radius); padding: 10px 20px; font-size: .9rem; font-weight: 700; display: flex; align-items: center; gap: 7px; width: 100%; justify-content: center; margin-top: 16px; }
.btn-export:hover { background: var(--navy-mid); }
.breakdown-section { margin-top: 16px; }
.breakdown-title { font-size: .82rem; font-weight: 700; text-transform: uppercase; letter-spacing: .05em; color: var(--txt-muted); margin-bottom: 10px; }
.breakdown-bar-item { margin-bottom: 10px; }
.breakdown-bar-label { display: flex; justify-content: space-between; font-size: .85rem; font-weight: 600; color: var(--txt-sec); margin-bottom: 4px; }
.breakdown-bar-track { background: var(--border-soft); border-radius: 100px; height: 8px; overflow: hidden; }
.breakdown-bar-fill { height: 100%; border-radius: 100px; background: var(--amber); transition: width .4s ease; }

/* Modal */
.modal-overlay { display: none; position: fixed; inset: 0; background: rgba(0,0,0,.55); z-index: 100; align-items: center; justify-content: center; padding: 16px; }
.modal-overlay.open { display: flex; }
.modal-box { background: var(--card); border-radius: var(--radius-lg); box-shadow: var(--shadow-lg); width: 100%; max-width: 520px; max-height: 92vh; overflow-y: auto; }
.modal-header { padding: 18px 20px 14px; border-bottom: 1px solid var(--border-soft); display: flex; align-items: center; justify-content: space-between; position: sticky; top: 0; background: var(--card); z-index: 1; border-radius: var(--radius-lg) var(--radius-lg) 0 0; }
.modal-header h2 { font-size: 1.1rem; font-weight: 800; }
.modal-header .modal-sub { font-size: .78rem; color: var(--txt-muted); margin-top: 1px; }
.btn-close { width: 32px; height: 32px; border-radius: 8px; background: var(--bg); border: 1px solid var(--border); color: var(--txt-sec); font-size: 1.1rem; display: flex; align-items: center; justify-content: center; }
.btn-close:hover { background: var(--border); }
.modal-body { padding: 18px 20px; }
.modal-footer { padding: 12px 20px 20px; display: flex; flex-direction: column; gap: 10px; }

/* Settings inner tabs */
.settings-tabs { display: flex; border-bottom: 2px solid var(--border-soft); margin-bottom: 18px; }
.settings-tab { flex: 1; padding: 9px 8px; font-size: .88rem; font-weight: 700; background: none; color: var(--txt-muted); border-bottom: 2px solid transparent; margin-bottom: -2px; transition: color .15s, border-color .15s; text-align: center; }
.settings-tab.active { color: var(--amber-dark); border-bottom-color: var(--amber); }
.settings-panel { display: none; }
.settings-panel.active { display: block; }

/* Resources */
.resources-list { display: flex; flex-direction: column; gap: 8px; margin-bottom: 16px; }
.resource-item { display: flex; align-items: center; gap: 10px; background: var(--bg); border: 1px solid var(--border-soft); border-radius: var(--radius); padding: 10px 14px; }
.resource-item .res-name { flex: 1; font-weight: 600; font-size: .9rem; }
.resource-item .res-type { font-size: .75rem; color: var(--txt-muted); }
.btn-del-small { background: none; border: none; color: var(--txt-muted); width: 28px; height: 28px; border-radius: 6px; display: flex; align-items: center; justify-content: center; font-size: .95rem; }
.btn-del-small:hover { background: var(--expense-bg); color: var(--expense); }
.add-row { display: flex; gap: 8px; flex-wrap: wrap; }
.add-row select, .add-row input { background: var(--bg); border: 1.5px solid var(--border); border-radius: var(--radius); padding: 9px 12px; font-size: .9rem; color: var(--txt); flex: 1; min-width: 80px; }
.add-row select:focus, .add-row input:focus { border-color: var(--amber); outline: none; }
.btn-add { background: var(--amber); color: var(--navy); border-radius: var(--radius); padding: 9px 16px; font-weight: 800; font-size: .9rem; white-space: nowrap; }
.btn-add:hover { background: var(--amber-dark); }

/* Clients */
.client-card { background: var(--bg); border: 1px solid var(--border-soft); border-radius: var(--radius); margin-bottom: 10px; overflow: hidden; }
.client-card-header { display: flex; align-items: center; gap: 10px; padding: 12px 14px; cursor: pointer; }
.client-card-header .client-name { flex: 1; font-weight: 700; font-size: .92rem; }
.client-badge { font-size: .75rem; color: var(--txt-muted); background: var(--card); border: 1px solid var(--border-soft); border-radius: 100px; padding: 2px 9px; }
.toggle-icon { color: var(--txt-muted); transition: transform .2s; }
.client-card-header.open .toggle-icon { transform: rotate(180deg); }
.client-card-body { display: none; border-top: 1px solid var(--border-soft); padding: 12px 14px; }
.client-card-body.open { display: block; }
.origin-line { font-size: .82rem; color: var(--txt-muted); margin-bottom: 10px; display: flex; align-items: center; gap: 6px; }
.origin-line strong { color: var(--txt-sec); }
.prices-table { width: 100%; border-collapse: collapse; font-size: .85rem; margin-bottom: 12px; }
.prices-table th { font-size: .72rem; font-weight: 700; text-transform: uppercase; letter-spacing: .04em; color: var(--txt-muted); padding: 5px 8px; border-bottom: 1px solid var(--border-soft); text-align: right; }
.prices-table td { padding: 6px 8px; border-bottom: 1px solid var(--border-soft); }
.prices-table tr:last-child td { border-bottom: none; }
.price-val { font-weight: 700; font-variant-numeric: tabular-nums; color: var(--income); }
.btn-del-price { background: none; border: none; color: var(--txt-muted); font-size: .85rem; cursor: pointer; width: 22px; height: 22px; border-radius: 4px; display: flex; align-items: center; justify-content: center; }
.btn-del-price:hover { background: var(--expense-bg); color: var(--expense); }
.add-price-row { display: flex; gap: 6px; flex-wrap: wrap; margin-bottom: 8px; }
.add-price-row input { background: var(--card); border: 1.5px solid var(--border); border-radius: var(--radius); padding: 7px 10px; font-size: .85rem; color: var(--txt); flex: 1; min-width: 80px; }
.add-price-row input:focus { border-color: var(--amber); outline: none; }
.btn-add-price { background: var(--amber); color: var(--navy); border-radius: var(--radius); padding: 7px 12px; font-size: .82rem; font-weight: 800; }
.btn-add-price:hover { background: var(--amber-dark); }
.btn-del-client { color: var(--expense); font-size: .8rem; font-weight: 600; background: none; border: none; cursor: pointer; padding: 4px; }
.btn-del-client:hover { text-decoration: underline; }
.add-client-row { display: flex; gap: 8px; margin-top: 14px; }
.add-client-row input { background: var(--bg); border: 1.5px solid var(--border); border-radius: var(--radius); padding: 9px 12px; font-size: .9rem; color: var(--txt); flex: 1; }
.add-client-row input:focus { border-color: var(--amber); outline: none; }

/* Origin highlight in modal */
.origin-badge { display: inline-flex; align-items: center; gap: 5px; background: var(--navy); color: var(--amber); border-radius: 8px; padding: 6px 12px; font-size: .85rem; font-weight: 700; margin-bottom: 14px; }

::-webkit-scrollbar { width: 6px; height: 6px; }
::-webkit-scrollbar-track { background: transparent; }
::-webkit-scrollbar-thumb { background: var(--border); border-radius: 3px; }
@media (max-width: 480px) { .site-header h1 { font-size: .9rem; } .tab-btn { font-size: .82rem; padding: 12px 4px; } .main-content { padding: 14px 12px 60px; } }

/* ── EXCEL EXPORT MODAL ─────────────────────────────────────── */
.excel-steps { display:flex; align-items:center; gap:8px; background:var(--bg); border:1px solid var(--border-soft); border-radius:var(--radius); padding:12px 14px; margin-bottom:14px; flex-wrap:wrap; }
.excel-step { display:flex; align-items:center; gap:6px; font-size:.84rem; font-weight:700; color:var(--txt-sec); }
.excel-step .step-num { background:var(--amber); color:var(--navy); border-radius:50%; width:22px; height:22px; display:flex; align-items:center; justify-content:center; font-size:.78rem; font-weight:800; flex-shrink:0; }
.excel-arrow { color:var(--txt-muted); font-size:1.1rem; }
.excel-preview-wrap { overflow-x:auto; max-height:380px; overflow-y:auto; border:1px solid var(--border-soft); border-radius:var(--radius); background:var(--card); }
.excel-preview-wrap table { border-collapse:collapse; font-size:.82rem; min-width:100%; }
.excel-preview-wrap th { background:var(--navy); color:rgba(255,255,255,.85); padding:8px 12px; font-size:.73rem; font-weight:700; text-align:right; white-space:nowrap; border:1px solid var(--navy-mid); }
.excel-preview-wrap td { padding:6px 12px; border:1px solid var(--border-soft); color:var(--txt); white-space:nowrap; }
.excel-preview-wrap tr:nth-child(even) td { background:var(--bg); }
.excel-preview-wrap tr.xl-total td { background:var(--navy); color:#fff; font-weight:800; }
.excel-preview-wrap tr.xl-section td { background:var(--navy-mid); color:var(--amber); font-weight:800; font-size:.8rem; }
.xl-inc { color:var(--income); font-weight:700; }
.xl-exp { color:var(--expense); font-weight:700; }
.xl-profit-pos { color:var(--income); font-weight:800; }
.xl-profit-neg { color:var(--expense); font-weight:800; }
.btn-export-xl { background:#217346; color:#fff; border-radius:var(--radius); padding:12px 24px; font-size:.95rem; font-weight:800; width:100%; display:flex; align-items:center; justify-content:center; gap:8px; transition:background .15s; }
.btn-export-xl:hover { background:#185c37; }
.driver-new-row { margin-top:8px; }

/* ── CASH FLOW TAB ─────────────────────────────────────────── */
.banks-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(190px,1fr)); gap: 12px; margin-bottom: 16px; }
.bank-card { background: var(--card); border: 1px solid var(--border-soft); border-radius: var(--radius-lg); padding: 18px 16px 14px; box-shadow: var(--shadow); position: relative; }
.bank-card .bank-name { font-size: .78rem; font-weight: 700; text-transform: uppercase; letter-spacing: .05em; color: var(--txt-muted); margin-bottom: 6px; padding-left: 52px; }
.bank-card .bank-balance { font-size: 1.5rem; font-weight: 800; font-variant-numeric: tabular-nums; color: var(--income); line-height: 1.2; }
.bank-card .bank-updated { font-size: .7rem; color: var(--txt-muted); margin-top: 6px; }
.bank-card .bank-actions { position: absolute; top: 10px; left: 10px; display: flex; gap: 4px; }
.bank-total-card { background: var(--navy); border-radius: var(--radius-lg); padding: 16px 20px; display: flex; align-items: center; justify-content: space-between; margin-bottom: 12px; }
.bank-total-card .bt-label { font-size: .78rem; font-weight: 700; color: rgba(255,255,255,.6); text-transform: uppercase; letter-spacing: .05em; }
.bank-total-card .bt-value { font-size: 1.7rem; font-weight: 800; color: var(--amber); font-variant-numeric: tabular-nums; }
.cf-section { margin-bottom: 22px; }
.cf-header { display: flex; align-items: center; justify-content: space-between; margin-bottom: 10px; }
.cf-section-title { font-size: 1rem; font-weight: 800; display: flex; align-items: center; gap: 8px; color: var(--txt); }
.cf-table-wrap { border-radius: var(--radius-lg); box-shadow: var(--shadow); overflow: hidden; }
.cf-table { width: 100%; border-collapse: collapse; background: var(--card); font-size: .87rem; }
.cf-table thead th { background: var(--navy); color: rgba(255,255,255,.75); font-size: .73rem; font-weight: 700; text-transform: uppercase; letter-spacing: .05em; padding: 10px 13px; text-align: right; white-space: nowrap; }
.cf-table td { padding: 10px 13px; border-bottom: 1px solid var(--border-soft); color: var(--txt); vertical-align: middle; }
.cf-table tr:last-child td { border-bottom: none; }
.cf-table tbody tr:hover { background: var(--bg); }
.cf-table tr.paid-row { opacity: .5; }
.status-badge { display: inline-flex; align-items: center; gap: 4px; padding: 3px 10px; border-radius: 100px; font-size: .76rem; font-weight: 700; white-space: nowrap; cursor: pointer; border: none; font-family: inherit; transition: opacity .12s; }
.status-badge:hover { opacity: .8; }
.status-badge.pending-recv { background: var(--income-bg); color: var(--income-txt); }
.status-badge.pending-pay  { background: var(--expense-bg); color: var(--expense-txt); }
.status-badge.done { background: var(--border-soft); color: var(--txt-muted); }
.overdue-badge { display: inline-flex; padding: 2px 7px; border-radius: 100px; font-size: .7rem; font-weight: 700; background: var(--expense-bg); color: var(--expense-txt); }
.cf-summary-box { background: var(--card); border: 1px solid var(--border-soft); border-radius: var(--radius-lg); padding: 18px 20px; box-shadow: var(--shadow); margin-bottom: 20px; }
.cf-summary-box .cf-sum-title { font-size: .78rem; font-weight: 700; text-transform: uppercase; letter-spacing: .05em; color: var(--txt-muted); margin-bottom: 14px; }
.cf-sum-rows { display: flex; flex-direction: column; gap: 9px; }
.cf-sum-row { display: flex; justify-content: space-between; align-items: center; font-size: .9rem; }
.cf-sum-row .cf-sum-label { color: var(--txt-sec); }
.cf-sum-row .cf-sum-val { font-weight: 800; font-variant-numeric: tabular-nums; }
.cf-sum-divider { height: 1px; background: var(--border); margin: 6px 0; }
.cf-sum-row.total .cf-sum-label { font-weight: 800; color: var(--txt); font-size: .95rem; }
.cf-sum-row.total .cf-sum-val { font-size: 1.2rem; }
.cf-warn-strip { display: flex; gap: 8px; flex-wrap: wrap; margin-top: 12px; padding-top: 12px; border-top: 1px solid var(--border-soft); }
.btn-cf-add { background: var(--amber); color: var(--navy); border-radius: var(--radius); padding: 8px 15px; font-size: .84rem; font-weight: 800; display: flex; align-items: center; gap: 5px; transition: background .15s; }
.btn-cf-add:hover { background: var(--amber-dark); }
.btn-cf-add.danger { background: var(--expense); color: #fff; }
.btn-cf-add.danger:hover { background: #b91c1c; }

/* ── GOODS / MERCHANDISE ────────────────────────────────────── */
.entry-section-lbl { font-size:.72rem; font-weight:700; text-transform:uppercase; letter-spacing:.06em; color:var(--txt-muted); margin-bottom:8px; margin-top:16px; display:flex; align-items:center; gap:8px; }
.entry-section-lbl::after { content:''; flex:1; height:1px; background:var(--border-soft); }

.quick-btn.goods-sale-btn { background:#EEF2FF; color:#3730A3; border-color:#6366F1; box-shadow:0 4px 12px rgba(99,102,241,.12); }
.quick-btn.goods-sale-btn:hover { box-shadow:0 6px 18px rgba(99,102,241,.24); }
.quick-btn.goods-buy-btn  { background:#FFFBEB; color:#92400E; border-color:#D97706; box-shadow:0 4px 12px rgba(217,119,6,.12); }
.quick-btn.goods-buy-btn:hover  { box-shadow:0 6px 18px rgba(217,119,6,.24); }
@media (prefers-color-scheme: dark) {
  :root:not([data-theme="light"]) .quick-btn.goods-sale-btn { background:#1E1B4B; color:#C7D2FE; border-color:#6366F1; }
  :root:not([data-theme="light"]) .quick-btn.goods-buy-btn  { background:#2D1A00; color:#FCD34D; border-color:#D97706; }
}
:root[data-theme="dark"] .quick-btn.goods-sale-btn { background:#1E1B4B; color:#C7D2FE; border-color:#6366F1; }
:root[data-theme="dark"] .quick-btn.goods-buy-btn  { background:#2D1A00; color:#FCD34D; border-color:#D97706; }

.badge.goods-inc { background:#EEF2FF; color:#3730A3; }
.badge.goods-exp { background:#FFFBEB; color:#92400E; }
@media (prefers-color-scheme: dark) {
  :root:not([data-theme="light"]) .badge.goods-inc { background:#1E1B4B; color:#C7D2FE; }
  :root:not([data-theme="light"]) .badge.goods-exp { background:#2D1A00; color:#FCD34D; }
}
:root[data-theme="dark"] .badge.goods-inc { background:#1E1B4B; color:#C7D2FE; }
:root[data-theme="dark"] .badge.goods-exp { background:#2D1A00; color:#FCD34D; }

.pay-toggle3 { display:grid; grid-template-columns:1fr 1fr 1fr; gap:6px; }
.pay-btn3 { padding:9px 4px; border-radius:var(--radius); font-size:.8rem; font-weight:700; border:2px solid var(--border); background:var(--bg); color:var(--txt-muted); transition:all .15s; text-align:center; display:flex; flex-direction:column; align-items:center; gap:3px; }
.pay-btn3.active-inc { background:var(--income-bg); border-color:var(--income); color:var(--income-txt); }
.pay-btn3.active-exp { background:var(--expense-bg); border-color:var(--expense); color:var(--expense-txt); }
.pay-btn3.active-neu { background:#EEF2FF; border-color:#6366F1; color:#3730A3; }
@media (prefers-color-scheme: dark) {
  :root:not([data-theme="light"]) .pay-btn3.active-neu { background:#1E1B4B; border-color:#6366F1; color:#C7D2FE; }
}
:root[data-theme="dark"] .pay-btn3.active-neu { background:#1E1B4B; border-color:#6366F1; color:#C7D2FE; }

.cat-pills { display:flex; gap:6px; margin-bottom:14px; flex-wrap:wrap; }
.cat-pill { padding:6px 14px; border-radius:100px; font-size:.82rem; font-weight:700; border:1.5px solid var(--border); background:var(--bg); color:var(--txt-sec); cursor:pointer; transition:all .15s; }
.cat-pill.active { background:var(--navy); color:#fff; border-color:var(--navy); }
.cat-pill:hover:not(.active) { background:var(--border-soft); }

.pay-dot { display:inline-block; width:7px; height:7px; border-radius:50%; vertical-align:middle; margin-left:3px; }
.pay-dot.s-paid { background:var(--income); }
.pay-dot.s-pend { background:var(--amber-dark); }
.pay-dot.s-part { background:#6366F1; }

.report-cat-divider { display:flex; align-items:center; gap:10px; margin:22px 0 16px; }
.report-cat-divider span { font-size:.78rem; font-weight:700; text-transform:uppercase; letter-spacing:.05em; color:var(--txt-muted); white-space:nowrap; }
.report-cat-divider::before, .report-cat-divider::after { content:''; flex:1; height:1px; background:var(--border-soft); }
.goods-summary-row { display:flex; justify-content:space-between; align-items:center; padding:10px 0; border-bottom:1px solid var(--border-soft); font-size:.9rem; }
.goods-summary-row:last-child { border-bottom:none; }
.goods-pay-row { display:flex; gap:8px; flex-wrap:wrap; margin-top:10px; }
.goods-pay-chip { display:inline-flex; align-items:center; gap:5px; padding:3px 10px; border-radius:100px; font-size:.77rem; font-weight:700; }
.goods-pay-chip.c-paid { background:var(--income-bg); color:var(--income-txt); }
.goods-pay-chip.c-pend { background:var(--expense-bg); color:var(--expense-txt); }
.goods-pay-chip.c-part { background:#EEF2FF; color:#3730A3; }
@media (prefers-color-scheme: dark) {
  :root:not([data-theme="light"]) .goods-pay-chip.c-part { background:#1E1B4B; color:#C7D2FE; }
}
:root[data-theme="dark"] .goods-pay-chip.c-part { background:#1E1B4B; color:#C7D2FE; }
</style>
</head>
<body>

<header class="site-header">
  <h1>
    <span class="header-icon">🚚</span>
    <span>דניאל דוד הובלות ומסחר<span class="sub">מערכת ניהול</span></span>
  </h1>
  <div class="header-actions">
    <button class="btn-header" onclick="openSettingsModal()">⚙️ הגדרות</button>
    <button class="btn-theme" onclick="toggleTheme()" id="themeBtn">🌙</button>
  </div>
</header>

<nav class="tabs-bar" role="tablist">
  <button class="tab-btn active" onclick="switchTab('entry')"   data-tab="entry"   role="tab">📝 הכנסת נתונים</button>
  <button class="tab-btn"        onclick="switchTab('journal')" data-tab="journal" role="tab">📋 יומן</button>
  <button class="tab-btn"        onclick="switchTab('report')"   data-tab="report"   role="tab">📊 דוח חודשי</button>
  <button class="tab-btn"        onclick="switchTab('cashflow')" data-tab="cashflow" role="tab">💰 תזרים</button>
  <button class="tab-btn"        onclick="switchTab('notes')"    data-tab="notes"    role="tab">📄 תעודות</button>
</nav>

<main class="main-content">

  <!-- ENTRY TAB -->
  <section class="tab-panel active" id="panel-entry">
    <div class="section-title"><span>📝</span> הוספת פעולה</div>

    <!-- Transport buttons -->
    <div class="entry-section-lbl">🚛 הובלות ומשאיות</div>
    <div class="quick-btns">
      <button class="quick-btn income-btn" onclick="openIncomeModal()">
        <span class="qb-icon">📈</span>
        <span class="qb-label">הכנסה חדשה</span>
        <span style="font-size:.78rem;font-weight:500;opacity:.8">הובלה / הנפה</span>
      </button>
      <button class="quick-btn expense-btn" onclick="openExpenseModal()">
        <span class="qb-icon">📉</span>
        <span class="qb-label">הוצאה חדשה</span>
        <span style="font-size:.78rem;font-weight:500;opacity:.8">דלק, תיקון, אחר</span>
      </button>
    </div>

    <!-- Goods buttons -->
    <div class="entry-section-lbl">📦 סחורה ומסחר</div>
    <div class="quick-btns">
      <button class="quick-btn goods-sale-btn" onclick="openGoodsSaleModal()">
        <span class="qb-icon">💰</span>
        <span class="qb-label">מכירת סחורה</span>
        <span style="font-size:.78rem;font-weight:500;opacity:.8">לקוח, מסמך, מחיר</span>
      </button>
      <button class="quick-btn goods-buy-btn" onclick="openGoodsBuyModal()">
        <span class="qb-icon">🛒</span>
        <span class="qb-label">קנית סחורה</span>
        <span style="font-size:.78rem;font-weight:500;opacity:.8">ספק, מסמך, מחיר</span>
      </button>
    </div>

    <!-- Today summary -->
    <div class="section-title"><span>📅</span> סיכום להיום</div>
    <div class="summary-grid">
      <div class="summary-card income-card"><div class="label">הכנסות</div><div class="value" id="todayIncome">₪0</div></div>
      <div class="summary-card expense-card"><div class="label">הוצאות</div><div class="value" id="todayExpense">₪0</div></div>
      <div class="summary-card profit-card" id="todayProfitCard"><div class="label">רווח נקי</div><div class="value" id="todayProfit">₪0</div></div>
    </div>
  </section>

  <!-- JOURNAL TAB -->
  <section class="tab-panel" id="panel-journal">
    <div class="section-title"><span>📋</span> יומן עסקאות</div>
    <div class="filters-bar">
      <div class="filter-group">
        <label class="filter-label">משאית/קבלן</label>
        <select class="filter-control" id="filterResource" onchange="renderJournal()"><option value="">הכל</option></select>
      </div>
      <div class="filter-group">
        <label class="filter-label">לקוח</label>
        <select class="filter-control" id="filterClient" onchange="renderJournal()"><option value="">הכל</option></select>
      </div>
      <div class="filter-group">
        <label class="filter-label">מתאריך</label>
        <input type="date" class="filter-control" id="filterFrom" onchange="renderJournal()">
      </div>
      <div class="filter-group">
        <label class="filter-label">עד תאריך</label>
        <input type="date" class="filter-control" id="filterTo" onchange="renderJournal()">
      </div>
      <div class="filter-group">
        <label class="filter-label">סוג</label>
        <select class="filter-control" id="filterType" onchange="renderJournal()">
          <option value="">הכל</option>
          <option value="income">הכנסות</option>
          <option value="expense">הוצאות</option>
        </select>
      </div>
      <button class="btn-filter-reset" onclick="resetFilters()">↺ איפוס</button>
    </div>
    <div id="journalContainer"></div>
  </section>

  <!-- REPORT TAB -->
  <section class="tab-panel" id="panel-report">
    <div class="section-title"><span>📊</span> דוח חודשי</div>
    <div class="month-selector-row">
      <div class="form-group">
        <label class="form-label">חודש</label>
        <select class="form-control" id="reportMonth" onchange="renderReport()">
          <option value="1">ינואר</option><option value="2">פברואר</option><option value="3">מרץ</option>
          <option value="4">אפריל</option><option value="5">מאי</option><option value="6">יוני</option>
          <option value="7">יולי</option><option value="8">אוגוסט</option><option value="9">ספטמבר</option>
          <option value="10">אוקטובר</option><option value="11">נובמבר</option><option value="12">דצמבר</option>
        </select>
      </div>
      <div class="form-group">
        <label class="form-label">שנה</label>
        <select class="form-control" id="reportYear" onchange="renderReport()"></select>
      </div>
    </div>
    <div id="reportContainer"></div>
  </section>

  <!-- CASH FLOW TAB -->
  <section class="tab-panel" id="panel-cashflow">

    <!-- Weekly net summary -->
    <div id="cfSummaryContainer"></div>

    <!-- Banks -->
    <div class="cf-section">
      <div class="cf-header">
        <div class="cf-section-title">🏦 יתרות בנקים</div>
        <button class="btn-cf-add" onclick="openAddBankModal()">+ הוסף חשבון</button>
      </div>
      <div id="banksContainer"></div>
    </div>

    <!-- Receivables (חייבים) -->
    <div class="cf-section">
      <div class="cf-header">
        <div class="cf-section-title">📥 חייבים — טרם שולם</div>
        <button class="btn-cf-add" onclick="openAddCashItemModal('receivable')">+ הוסף חייב</button>
      </div>
      <div id="receivablesContainer"></div>
    </div>

    <!-- Payables (הורדות) -->
    <div class="cf-section">
      <div class="cf-header">
        <div class="cf-section-title">📤 הורדות קרובות</div>
        <button class="btn-cf-add danger" onclick="openAddCashItemModal('payable')">+ הוסף הורדה</button>
      </div>
      <div id="payablesContainer"></div>
    </div>

  </section>

  <!-- DELIVERY NOTES TAB -->
  <section class="tab-panel" id="panel-notes">
    <div class="section-title"><span>📄</span> תעודות משלוח</div>
    <div id="notesContainer"><p style="color:var(--txt-muted);text-align:center;padding:40px 0">אין תעודות עדיין</p></div>
  </section>

</main>

<!-- ═══════════════════════════════════════════════════════════ -->
<!-- INCOME MODAL — הכנסה חדשה                                 -->
<!-- ═══════════════════════════════════════════════════════════ -->
<div class="modal-overlay" id="incomeModal">
  <div class="modal-box">
    <div class="modal-header">
      <div>
        <h2>📈 הכנסה חדשה</h2>
        <div class="modal-sub">הובלה / הנפה</div>
      </div>
      <button class="btn-close" onclick="closeModal('incomeModal')">✕</button>
    </div>
    <div class="modal-body">
      <form id="incomeForm" onsubmit="handleIncome(event)">
        <div class="form-grid">

          <!-- Date & Resource -->
          <div class="form-group">
            <label class="form-label">תאריך</label>
            <input class="form-control" type="date" id="incDate" required>
          </div>
          <div class="form-group">
            <label class="form-label">משאית / קבלן</label>
            <select class="form-control" id="incResource" required>
              <option value="">— בחר —</option>
            </select>
          </div>

          <!-- Driver -->
          <div class="form-group full">
            <label class="form-label">נהג / מספר רכב</label>
            <select class="form-control" id="incDriver" onchange="pickDriver('incDriver','incDriverNewRow')">
              <option value="">— בחר נהג —</option>
            </select>
            <div class="driver-new-row" id="incDriverNewRow" style="display:none">
              <input class="form-control" type="text" id="incDriverNewVal" placeholder="שם ומספר (למשל: דני 050-1234567)">
            </div>
          </div>

          <!-- Work type -->
          <div class="form-group full">
            <label class="form-label">סוג עבודה</label>
            <div class="work-toggle">
              <button type="button" class="work-btn active" id="wbHovla" onclick="setWorkType('הובלה')">
                <span class="wb-icon">🚛</span>
                <span>הובלה</span>
              </button>
              <button type="button" class="work-btn" id="wbHanafa" onclick="setWorkType('הנפה')">
                <span class="wb-icon">🏗️</span>
                <span>הנפה</span>
              </button>
            </div>
            <input type="hidden" id="incWorkType" value="הובלה">
          </div>

          <!-- Client -->
          <div class="form-group full">
            <label class="form-label" style="display:flex;justify-content:space-between;align-items:center">
              לקוח
              <button type="button" style="font-size:.75rem;font-weight:700;background:var(--navy-mid);color:var(--amber);border:none;border-radius:6px;padding:3px 10px;cursor:pointer" onclick="quickAddClientInline()">+ הוסף לקוח</button>
            </label>
            <select class="form-control" id="incClient" onchange="handleIncClientChange()">
              <option value="">— ללא לקוח מוגדר —</option>
            </select>
            <div id="quickClientRow" style="display:none;margin-top:8px;display:none">
              <input class="form-control" type="text" id="quickClientName" placeholder="שם הלקוח החדש..." style="margin-bottom:6px">
              <div style="display:flex;gap:8px">
                <button type="button" class="btn-primary" style="flex:1;padding:8px" onclick="confirmQuickClient()">✅ שמור</button>
                <button type="button" class="btn-secondary" style="padding:8px 14px" onclick="cancelQuickClient()">ביטול</button>
              </div>
            </div>
          </div>

          <!-- Origin (auto-filled from client) -->
          <div class="form-group full" id="incOriginGroup">
            <label class="form-label">מוצא (נקודת יציאה)</label>
            <input class="form-control" type="text" id="incOrigin" placeholder="מאיפה?">
          </div>

          <!-- Destination -->
          <div class="form-group full" id="incDestGroup">
            <label class="form-label">יעד</label>
            <select class="form-control" id="incDestination" onchange="handleIncDestChange()">
              <option value="">— בחר יעד —</option>
            </select>
            <div class="price-hint" id="incPriceHint">💰 המחיר מולא אוטומטית לפי המחירון</div>
          </div>
          <!-- Free-text destination (shown when no price list) -->
          <div class="form-group full" id="incDestFreeGroup" style="display:none">
            <label class="form-label">יעד</label>
            <input class="form-control" type="text" id="incDestFree" placeholder="לאן?">
          </div>

          <!-- Amount -->
          <div class="form-group full">
            <label class="form-label">סכום (₪)</label>
            <div class="amount-wrap">
              <span class="currency">₪</span>
              <input class="form-control" type="number" id="incAmount" min="0" step="1" placeholder="0" required>
            </div>
          </div>

          <!-- Notes -->
          <div class="form-group full">
            <label class="form-label">הערות (אופציונלי)</label>
            <input class="form-control" type="text" id="incDesc" placeholder="מספר הזמנה, פרטים...">
          </div>

        </div>
      </form>
    </div>
    <div class="modal-footer">
      <button type="submit" form="incomeForm" class="btn-primary">✅ שמור הכנסה</button>
      <button type="button" class="btn-secondary" onclick="closeModal('incomeModal')">ביטול</button>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════════════════════════ -->
<!-- EXPENSE MODAL — הוצאה חדשה                                -->
<!-- ═══════════════════════════════════════════════════════════ -->
<div class="modal-overlay" id="expenseModal">
  <div class="modal-box">
    <div class="modal-header">
      <div>
        <h2>📉 הוצאה חדשה</h2>
        <div class="modal-sub">דלק, תיקון, אגרה ועוד</div>
      </div>
      <button class="btn-close" onclick="closeModal('expenseModal')">✕</button>
    </div>
    <div class="modal-body">
      <form id="expenseForm" onsubmit="handleExpense(event)">
        <div class="form-grid">

          <div class="form-group">
            <label class="form-label">תאריך</label>
            <input class="form-control" type="date" id="expDate" required>
          </div>
          <div class="form-group">
            <label class="form-label">משאית / קבלן</label>
            <select class="form-control" id="expResource" required>
              <option value="">— בחר —</option>
            </select>
          </div>

          <div class="form-group full">
            <label class="form-label">נהג / מספר רכב</label>
            <select class="form-control" id="expDriver" onchange="pickDriver('expDriver','expDriverNewRow')">
              <option value="">— בחר נהג —</option>
            </select>
            <div class="driver-new-row" id="expDriverNewRow" style="display:none">
              <input class="form-control" type="text" id="expDriverNewVal" placeholder="שם ומספר (למשל: דני 050-1234567)">
            </div>
          </div>

          <div class="form-group full">
            <label class="form-label">קטגוריה</label>
            <select class="form-control" id="expCategory">
              <option value="דלק">⛽ דלק</option>
              <option value="טיפולים/תיקונים">🔧 טיפולים / תיקונים</option>
              <option value="תשלום לקבלן משנה">🤝 תשלום לקבלן משנה</option>
              <option value="אגרות/רישוי">📄 אגרות / רישוי</option>
              <option value="אחר">📌 אחר</option>
            </select>
          </div>

          <div class="form-group full">
            <label class="form-label">סכום (₪)</label>
            <div class="amount-wrap">
              <span class="currency">₪</span>
              <input class="form-control" type="number" id="expAmount" min="0" step="1" placeholder="0" required>
            </div>
          </div>

          <div class="form-group full">
            <label class="form-label">תיאור / ספק</label>
            <input class="form-control" type="text" id="expDesc" placeholder="שם ספק, מספר חשבונית...">
          </div>

        </div>
      </form>
    </div>
    <div class="modal-footer">
      <button type="submit" form="expenseForm" class="btn-primary" style="background:var(--expense);color:#fff">✅ שמור הוצאה</button>
      <button type="button" class="btn-secondary" onclick="closeModal('expenseModal')">ביטול</button>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════════════════════════ -->
<!-- EDIT MODAL                                                  -->
<!-- ═══════════════════════════════════════════════════════════ -->
<div class="modal-overlay" id="editModal">
  <div class="modal-box">
    <div class="modal-header">
      <h2>✏️ עריכת פעולה</h2>
      <button class="btn-close" onclick="closeModal('editModal')">✕</button>
    </div>
    <div class="modal-body">
      <form id="editForm" onsubmit="saveEdit(event)">
        <div class="form-grid">
          <div class="form-group">
            <label class="form-label">תאריך</label>
            <input class="form-control" type="date" id="editDate" required>
          </div>
          <div class="form-group">
            <label class="form-label">משאית / קבלן</label>
            <select class="form-control" id="editResource" required><option value="">— בחר —</option></select>
          </div>
          <div class="form-group full">
            <label class="form-label">נהג / מספר רכב</label>
            <select class="form-control" id="editDriver" onchange="pickDriver('editDriver','editDriverNewRow')">
              <option value="">— בחר נהג —</option>
            </select>
            <div class="driver-new-row" id="editDriverNewRow" style="display:none">
              <input class="form-control" type="text" id="editDriverNewVal" placeholder="שם ומספר (למשל: דני 050-1234567)">
            </div>
          </div>

          <div class="form-group full">
            <label class="form-label">סוג פעולה</label>
            <div class="type-toggle">
              <button type="button" class="type-btn income" id="editTypeIncome"  onclick="setEditType('income')">📈 הכנסה</button>
              <button type="button" class="type-btn expense" id="editTypeExpense" onclick="setEditType('expense')">📉 הוצאה</button>
            </div>
            <input type="hidden" id="editType" value="income">
          </div>
          <div class="form-group full" id="editWorkTypeGroup">
            <label class="form-label">סוג עבודה</label>
            <div class="work-toggle">
              <button type="button" class="work-btn" id="ewbHovla"  onclick="setEditWorkType('הובלה')"><span class="wb-icon">🚛</span><span>הובלה</span></button>
              <button type="button" class="work-btn" id="ewbHanafa" onclick="setEditWorkType('הנפה')"><span class="wb-icon">🏗️</span><span>הנפה</span></button>
            </div>
            <input type="hidden" id="editWorkType" value="">
          </div>
          <div class="form-group full">
            <label class="form-label">לקוח</label>
            <select class="form-control" id="editClient" onchange="handleEditClientChange()"><option value="">— ללא לקוח —</option></select>
          </div>
          <div class="form-group full">
            <label class="form-label">מוצא</label>
            <input class="form-control" type="text" id="editOrigin" placeholder="נקודת מוצא">
          </div>
          <div class="form-group full" id="editDestGroup">
            <label class="form-label">יעד</label>
            <select class="form-control" id="editDestination" onchange="handleEditDestChange()"><option value="">— בחר יעד —</option></select>
          </div>
          <div class="form-group full" id="editDestFreeGroup" style="display:none">
            <label class="form-label">יעד</label>
            <input class="form-control" type="text" id="editDestFree" placeholder="יעד">
          </div>
          <div class="form-group">
            <label class="form-label">סכום (₪)</label>
            <div class="amount-wrap">
              <span class="currency">₪</span>
              <input class="form-control" type="number" id="editAmount" min="0" required>
            </div>
          </div>
          <div class="form-group" id="editCatGroup">
            <label class="form-label">קטגוריה</label>
            <select class="form-control" id="editCategory">
              <option value="דלק">⛽ דלק</option>
              <option value="טיפולים/תיקונים">🔧 טיפולים / תיקונים</option>
              <option value="תשלום לקבלן משנה">🤝 תשלום לקבלן משנה</option>
              <option value="אגרות/רישוי">📄 אגרות / רישוי</option>
              <option value="אחר">📌 אחר</option>
            </select>
          </div>
          <div class="form-group full">
            <label class="form-label">הערות</label>
            <input class="form-control" type="text" id="editDesc">
          </div>
          <div class="full">
            <button type="submit" class="btn-primary">💾 שמור שינויים</button>
          </div>
        </div>
      </form>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════════════════════════ -->
<!-- SETTINGS MODAL                                              -->
<!-- ═══════════════════════════════════════════════════════════ -->
<div class="modal-overlay" id="settingsModal">
  <div class="modal-box" style="max-width:560px">
    <div class="modal-header">
      <h2>⚙️ הגדרות</h2>
      <button class="btn-close" onclick="closeModal('settingsModal')">✕</button>
    </div>
    <div class="modal-body">
      <div class="settings-tabs">
        <button class="settings-tab active" onclick="switchSettingsTab('resources')">🚛 משאבים</button>
        <button class="settings-tab"        onclick="switchSettingsTab('clients')">👥 לקוחות ומחירון</button>
      </div>
      <div class="settings-panel active" id="sPanel-resources">
        <div class="breakdown-title" style="margin-bottom:10px">משאבים פעילים</div>
        <div class="resources-list" id="resourcesList"></div>
        <div class="breakdown-title" style="margin-bottom:10px;margin-top:18px">הוספת משאב</div>
        <div class="add-row">
          <select id="newResType">
            <option value="truck-fridge">❄️ משאית קירור</option>
            <option value="truck-crane-sm">🏗️ משאית מנוף קטן</option>
            <option value="truck-crane-lg">🏗️ משאית מנוף גדול</option>
            <option value="truck-curtain">🚛 משאית וילון</option>
            <option value="sub">🤝 קבלן משנה</option>
            <option value="other">🚛 אחר</option>
          </select>
          <input type="text" id="newResName" placeholder="שם...">
          <button class="btn-add" onclick="addResource()">+ הוסף</button>
        </div>
      </div>
      <div class="settings-panel" id="sPanel-clients">
        <div class="breakdown-title" style="margin-bottom:10px">לקוחות ומחירוני יעדים</div>
        <div id="clientsList"></div>
        <div class="breakdown-title" style="margin-bottom:8px;margin-top:14px">הוספת לקוח חדש</div>
        <div class="add-client-row">
          <input type="text" id="newClientName" placeholder="שם הלקוח...">
          <input type="text" id="newClientOrigin" placeholder="נקודת מוצא (כברירת מחדל)">
          <button class="btn-add" onclick="addClient()">+ הוסף</button>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════════════════════════ -->
<!-- GOODS SALE MODAL — מכירת סחורה                             -->
<!-- ═══════════════════════════════════════════════════════════ -->
<div class="modal-overlay" id="goodsSaleModal">
  <div class="modal-box" style="max-width:500px">
    <div class="modal-header">
      <div><h2>💰 מכירת סחורה</h2><div class="modal-sub">תיעוד מכירה — לקוח, סחורה, מסמך</div></div>
      <button class="btn-close" onclick="closeModal('goodsSaleModal')">✕</button>
    </div>
    <div class="modal-body">
      <form id="goodsSaleForm" onsubmit="handleGoodsSale(event)">
        <div class="form-grid">
          <div class="form-group">
            <label class="form-label">תאריך</label>
            <input class="form-control" type="date" id="gsSaleDate" required>
          </div>
          <div class="form-group">
            <label class="form-label">שם לקוח</label>
            <input class="form-control" type="text" id="gsSaleClient" placeholder="שם הלקוח...">
          </div>
          <div class="form-group full">
            <label class="form-label">פרטי הסחורה / מוצר</label>
            <input class="form-control" type="text" id="gsSaleGoods" placeholder="מה נמכר? (תיאור הסחורה...)" required>
          </div>
          <div class="form-group full">
            <label class="form-label">סכום (₪)</label>
            <div class="amount-wrap"><span class="currency">₪</span>
            <input class="form-control" type="number" id="gsSaleAmount" min="0" step="1" placeholder="0" required></div>
          </div>
          <div class="form-group full">
            <label class="form-label">סטטוס תשלום</label>
            <div class="pay-toggle3" id="gsSalePayToggle">
              <button type="button" class="pay-btn3" data-v="שולם"  onclick="setGoodsPay('sale','שולם')"><span>✅</span>שולם</button>
              <button type="button" class="pay-btn3" data-v="ממתין" onclick="setGoodsPay('sale','ממתין')"><span>⏳</span>ממתין</button>
              <button type="button" class="pay-btn3" data-v="בשותף" onclick="setGoodsPay('sale','בשותף')"><span>🤝</span>בשותף</button>
            </div>
            <input type="hidden" id="gsSalePayVal" value="שולם">
          </div>
          <div class="form-group">
            <label class="form-label">סוג מסמך</label>
            <select class="form-control" id="gsSaleDocType" onchange="toggleGoodsDocNum('gsSale',this.value)">
              <option value="חשבונית">📄 חשבונית</option>
              <option value="תעודת משלוח">📋 תעודת משלוח</option>
              <option value="ללא">∅ ללא מסמך</option>
            </select>
          </div>
          <div class="form-group" id="gsSaleDocNumGroup">
            <label class="form-label">מספר מסמך</label>
            <input class="form-control" type="text" id="gsSaleDocNum" placeholder="מס׳ חשבונית / ת. משלוח">
          </div>
          <div class="form-group full">
            <label class="form-label">הערות (אופציונלי)</label>
            <input class="form-control" type="text" id="gsSaleNote" placeholder="פרטים נוספים...">
          </div>
        </div>
      </form>
    </div>
    <div class="modal-footer">
      <button type="submit" form="goodsSaleForm" class="btn-primary" style="background:#6366F1;color:#fff">✅ שמור מכירה</button>
      <button type="button" class="btn-secondary" onclick="closeModal('goodsSaleModal')">ביטול</button>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════════════════════════ -->
<!-- GOODS BUY MODAL — קנית סחורה                               -->
<!-- ═══════════════════════════════════════════════════════════ -->
<div class="modal-overlay" id="goodsBuyModal">
  <div class="modal-box" style="max-width:500px">
    <div class="modal-header">
      <div><h2>🛒 קנית סחורה</h2><div class="modal-sub">תיעוד קנייה — ספק, סחורה, מסמך</div></div>
      <button class="btn-close" onclick="closeModal('goodsBuyModal')">✕</button>
    </div>
    <div class="modal-body">
      <form id="goodsBuyForm" onsubmit="handleGoodsBuy(event)">
        <div class="form-grid">
          <div class="form-group">
            <label class="form-label">תאריך</label>
            <input class="form-control" type="date" id="gsBuyDate" required>
          </div>
          <div class="form-group">
            <label class="form-label">שם ספק</label>
            <input class="form-control" type="text" id="gsBuySupplier" placeholder="שם הספק...">
          </div>
          <div class="form-group full">
            <label class="form-label">פרטי הסחורה / מוצר</label>
            <input class="form-control" type="text" id="gsBuyGoods" placeholder="מה נקנה? (תיאור הסחורה...)" required>
          </div>
          <div class="form-group full">
            <label class="form-label">סכום (₪)</label>
            <div class="amount-wrap"><span class="currency">₪</span>
            <input class="form-control" type="number" id="gsBuyAmount" min="0" step="1" placeholder="0" required></div>
          </div>
          <div class="form-group full">
            <label class="form-label">סטטוס תשלום</label>
            <div class="pay-toggle3" id="gsBuyPayToggle">
              <button type="button" class="pay-btn3" data-v="שולם"   onclick="setGoodsPay('buy','שולם')"><span>✅</span>שולם</button>
              <button type="button" class="pay-btn3" data-v="אשראי"  onclick="setGoodsPay('buy','אשראי')"><span>💳</span>אשראי/דחוי</button>
              <button type="button" class="pay-btn3" data-v="ממתין"  onclick="setGoodsPay('buy','ממתין')"><span>⏳</span>ממתין</button>
            </div>
            <input type="hidden" id="gsBuyPayVal" value="שולם">
          </div>
          <div class="form-group">
            <label class="form-label">סוג מסמך</label>
            <select class="form-control" id="gsBuyDocType" onchange="toggleGoodsDocNum('gsBuy',this.value)">
              <option value="חשבונית">📄 חשבונית</option>
              <option value="תעודת משלוח">📋 תעודת משלוח</option>
              <option value="ללא">∅ ללא מסמך</option>
            </select>
          </div>
          <div class="form-group" id="gsBuyDocNumGroup">
            <label class="form-label">מספר מסמך</label>
            <input class="form-control" type="text" id="gsBuyDocNum" placeholder="מס׳ חשבונית / ת. משלוח">
          </div>
          <div class="form-group full">
            <label class="form-label">הערות (אופציונלי)</label>
            <input class="form-control" type="text" id="gsBuyNote" placeholder="פרטים נוספים...">
          </div>
        </div>
      </form>
    </div>
    <div class="modal-footer">
      <button type="submit" form="goodsBuyForm" class="btn-primary" style="background:var(--expense);color:#fff">✅ שמור קנייה</button>
      <button type="button" class="btn-secondary" onclick="closeModal('goodsBuyModal')">ביטול</button>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════════════════════════ -->
<!-- EDIT GOODS MODAL                                            -->
<!-- ═══════════════════════════════════════════════════════════ -->
<div class="modal-overlay" id="editGoodsModal">
  <div class="modal-box" style="max-width:480px">
    <div class="modal-header">
      <h2 id="geModalTitle">✏️ עריכת סחורה</h2>
      <button class="btn-close" onclick="closeModal('editGoodsModal')">✕</button>
    </div>
    <div class="modal-body">
      <form id="editGoodsForm" onsubmit="saveGoodsEdit(event)">
        <div class="form-grid">
          <div class="form-group">
            <label class="form-label">תאריך</label>
            <input class="form-control" type="date" id="geDate" required>
          </div>
          <div class="form-group">
            <label class="form-label">שם לקוח / ספק</label>
            <input class="form-control" type="text" id="geParty" placeholder="">
          </div>
          <div class="form-group full">
            <label class="form-label">פרטי הסחורה</label>
            <input class="form-control" type="text" id="geGoods" required>
          </div>
          <div class="form-group full">
            <label class="form-label">סכום (₪)</label>
            <div class="amount-wrap"><span class="currency">₪</span>
            <input class="form-control" type="number" id="geAmount" min="0" required></div>
          </div>
          <div class="form-group full">
            <label class="form-label">סטטוס תשלום</label>
            <select class="form-control" id="gePayStatus">
              <option value="שולם">✅ שולם</option>
              <option value="ממתין">⏳ ממתין</option>
              <option value="בשותף">🤝 בשותף</option>
              <option value="אשראי">💳 אשראי/דחוי</option>
            </select>
          </div>
          <div class="form-group">
            <label class="form-label">סוג מסמך</label>
            <select class="form-control" id="geDocType" onchange="toggleGoodsDocNum('ge',this.value)">
              <option value="חשבונית">📄 חשבונית</option>
              <option value="תעודת משלוח">📋 תעודת משלוח</option>
              <option value="ללא">∅ ללא מסמך</option>
            </select>
          </div>
          <div class="form-group" id="geDocNumGroup">
            <label class="form-label">מספר מסמך</label>
            <input class="form-control" type="text" id="geDocNum" placeholder="">
          </div>
          <div class="form-group full">
            <label class="form-label">הערות</label>
            <input class="form-control" type="text" id="geNote">
          </div>
          <div class="full">
            <button type="submit" class="btn-primary">💾 שמור שינויים</button>
          </div>
        </div>
      </form>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════════════════════════ -->
<!-- ADD BANK MODAL                                               -->
<!-- ═══════════════════════════════════════════════════════════ -->
<div class="modal-overlay" id="addBankModal">
  <div class="modal-box" style="max-width:380px">
    <div class="modal-header">
      <div><h2>🏦 הוספת חשבון בנק</h2><div class="modal-sub">הוסף חשבון כדי לעקוב אחר היתרה</div></div>
      <button class="btn-close" onclick="closeModal('addBankModal')">✕</button>
    </div>
    <div class="modal-body">
      <div class="form-grid">
        <div class="form-group full">
          <label class="form-label">שם הבנק / חשבון</label>
          <input class="form-control" type="text" id="bankName" placeholder="לדוגמה: הפועלים ביזנס, לאומי...">
        </div>
        <div class="form-group full">
          <label class="form-label">יתרה נוכחית (₪)</label>
          <div class="amount-wrap"><span class="currency">₪</span>
          <input class="form-control" type="number" id="bankBalance" step="1" placeholder="0"></div>
        </div>
      </div>
    </div>
    <div class="modal-footer">
      <button class="btn-primary" onclick="addBank()">✅ הוסף חשבון</button>
      <button class="btn-secondary" onclick="closeModal('addBankModal')">ביטול</button>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════════════════════════ -->
<!-- UPDATE BANK BALANCE MODAL                                    -->
<!-- ═══════════════════════════════════════════════════════════ -->
<div class="modal-overlay" id="updateBankModal">
  <div class="modal-box" style="max-width:340px">
    <div class="modal-header">
      <div><h2>✏️ עדכון יתרה</h2><div class="modal-sub" id="updateBankName"></div></div>
      <button class="btn-close" onclick="closeModal('updateBankModal')">✕</button>
    </div>
    <div class="modal-body">
      <input type="hidden" id="updateBankId">
      <div class="form-group">
        <label class="form-label">יתרה נוכחית (₪)</label>
        <div class="amount-wrap"><span class="currency">₪</span>
        <input class="form-control" type="number" id="updateBankBalance" step="1" placeholder="0"></div>
      </div>
    </div>
    <div class="modal-footer">
      <button class="btn-primary" onclick="confirmUpdateBank()">✅ עדכן יתרה</button>
      <button class="btn-secondary" onclick="closeModal('updateBankModal')">ביטול</button>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════════════════════════ -->
<!-- ADD CASH ITEM MODAL (חייב / הורדה)                          -->
<!-- ═══════════════════════════════════════════════════════════ -->
<div class="modal-overlay" id="addCashItemModal">
  <div class="modal-box" style="max-width:440px">
    <div class="modal-header">
      <div>
        <h2 id="cashItemModalTitle">📥 הוסף חייב</h2>
        <div class="modal-sub" id="cashItemModalSub"></div>
      </div>
      <button class="btn-close" onclick="closeModal('addCashItemModal')">✕</button>
    </div>
    <div class="modal-body">
      <input type="hidden" id="cashItemType" value="receivable">
      <div class="form-grid">
        <div class="form-group full">
          <label class="form-label" id="cashItemDescLabel">שם לקוח / מה החוב</label>
          <input class="form-control" type="text" id="cashItemDesc" placeholder="">
        </div>
        <div class="form-group full">
          <label class="form-label">סכום (₪)</label>
          <div class="amount-wrap"><span class="currency">₪</span>
          <input class="form-control" type="number" id="cashItemAmount" step="1" placeholder="0"></div>
        </div>
        <div class="form-group full">
          <label class="form-label">תאריך צפוי / מועד אחרון</label>
          <input class="form-control" type="date" id="cashItemDue">
        </div>
        <div class="form-group full">
          <label class="form-label">הערות (אופציונלי)</label>
          <input class="form-control" type="text" id="cashItemNote" placeholder="">
        </div>
      </div>
    </div>
    <div class="modal-footer">
      <button class="btn-primary" id="cashItemSaveBtn" onclick="saveCashItem()">✅ שמור</button>
      <button class="btn-secondary" onclick="closeModal('addCashItemModal')">ביטול</button>
    </div>
  </div>
</div>

<!-- CSV MODAL -->
<div class="modal-overlay" id="csvModal">
  <div class="modal-box" style="max-width:720px">
    <div class="modal-header">
      <h2>📊 ייצוא ל-Excel — <span id="csvModalTitle"></span></h2>
      <button class="btn-close" onclick="closeModal('csvModal')">✕</button>
    </div>
    <div class="modal-body">
      <div class="excel-steps">
        <div class="excel-step"><span class="step-num">1</span>לחץ "העתק"</div>
        <div class="excel-arrow">←</div>
        <div class="excel-step"><span class="step-num">2</span>פתח Excel / Google Sheets</div>
        <div class="excel-arrow">←</div>
        <div class="excel-step"><span class="step-num">3</span>הדבק (Ctrl+V)</div>
      </div>
      <div class="excel-preview-wrap" id="excelPreview"></div>
      <!-- fallback textarea — shown if clipboard API fails -->
      <div id="tsvFallbackWrap" style="display:none;margin-top:12px">
        <p style="font-size:.85rem;color:var(--txt-sec);margin-bottom:6px">סמן הכל (Ctrl+A) → העתק (Ctrl+C) → הדבק ב-Excel</p>
        <textarea id="tsvTextarea" readonly onclick="this.select()" style="width:100%;height:160px;background:var(--bg);border:1.5px solid var(--border);border-radius:var(--radius);padding:10px;font-size:.78rem;color:var(--txt);direction:ltr;resize:vertical;font-family:monospace"></textarea>
        <button class="btn-export-xl" style="margin-top:8px" onclick="selectAllTsv()">🖱️ סמן הכל</button>
      </div>
    </div>
    <div class="modal-footer">
      <button class="btn-export-xl" onclick="copyExcelToClipboard()">📋 העתק ל-Excel</button>
      <button class="btn-secondary" onclick="closeModal('csvModal')">סגור</button>
    </div>
  </div>
</div>

<!-- Driver Screen -->
<div id="driverScreen">
  <!-- Top bar -->
  <div class="drv-header">
    <div class="drv-header-logo">🚛</div>
    <div style="flex:1">
      <div class="drv-header-title">דניאל דוד הובלות ומסחר</div>
      <div class="drv-name" id="driverNameDisplay">שטר מטען דיגיטלי</div>
    </div>
    <div class="drv-note-badge" id="drvNoteBadge">מס׳ 0233</div>
  </div>

  <!-- Form -->
  <div id="driverFormView" class="drv-form">

    <!-- פרטי שטר -->
    <div class="drv-card">
      <div class="drv-card-head"><span>📋</span> פרטי שטר</div>
      <div class="drv-card-body">
        <div class="drv-row2">
          <div class="drv-field"><label>מס׳ שטר מטען</label><input type="text" id="dnNoteNum" readonly></div>
          <div class="drv-field"><label>תאריך</label><input type="text" id="dnDate" readonly></div>
        </div>
        <div class="drv-row2">
          <div class="drv-field"><label>שעת הגעה</label><input type="time" id="dnArrival" dir="ltr"></div>
          <div class="drv-field"><label>שעת יציאה</label><input type="time" id="dnDeparture" dir="ltr"></div>
        </div>
      </div>
    </div>

    <!-- פרטי לקוח -->
    <div class="drv-card">
      <div class="drv-card-head"><span>👤</span> פרטי לקוח</div>
      <div class="drv-card-body">
        <div class="drv-field"><label>שם הלקוח</label><input type="text" id="dnClientName" placeholder="שם מלא..."></div>
        <div class="drv-row2">
          <div class="drv-field"><label>ע.מ. / ח.פ.</label><input type="text" id="dnClientVat" placeholder="מספר עוסק"></div>
          <div class="drv-field"><label>טלפון לקוח</label><input type="tel" id="dnClientPhone" placeholder="05X-XXXXXXX" dir="ltr"></div>
        </div>
        <div class="drv-field"><label>שם המזמין</label><input type="text" id="dnOrderer" placeholder="מי הזמין את העבודה"></div>
      </div>
    </div>

    <!-- נהג ורכב -->
    <div class="drv-card">
      <div class="drv-card-head"><span>🚗</span> נהג ורכב</div>
      <div class="drv-card-body">
        <div class="drv-row2">
          <div class="drv-field"><label>שם הנהג</label><input type="text" id="dnDriverName" readonly></div>
          <div class="drv-field"><label>מס׳ רכב</label><input type="text" id="dnVehicle" placeholder="XX-XXX-XX" dir="ltr"></div>
        </div>
      </div>
    </div>

    <!-- תאור מטען -->
    <div class="drv-card">
      <div class="drv-card-head"><span>📦</span> תאור מטען</div>
      <div class="drv-card-body">
        <div class="drv-field"><label>תאור המטען</label><textarea id="dnItems" placeholder="פרט את הסחורה / ציוד..."></textarea></div>
        <div class="drv-row2">
          <div class="drv-field"><label>מוצא (1)</label><input type="text" id="dnOrigin1" placeholder="כתובת מוצא"></div>
          <div class="drv-field"><label>מוצא (2)</label><input type="text" id="dnOrigin2" placeholder="כתובת מוצא שנייה"></div>
        </div>
        <div class="drv-field"><label>ת.מ. ספק</label><input type="text" id="dnSupplierRef" placeholder="תעודת משלוח ספק"></div>
        <div class="drv-row2">
          <div class="drv-field"><label>יעד (1)</label><input type="text" id="dnDest1" placeholder="כתובת יעד"></div>
          <div class="drv-field"><label>יעד (2)</label><input type="text" id="dnDest2" placeholder="כתובת יעד שנייה"></div>
        </div>
      </div>
    </div>

    <!-- עבודת מנוף -->
    <div class="drv-card">
      <div class="drv-card-head"><span>🏗️</span> עבודת מנוף</div>
      <div class="drv-card-body">
        <div class="drv-row3">
          <div class="drv-field"><label>משעה</label><input type="time" id="dnCraneFrom" dir="ltr"></div>
          <div class="drv-field"><label>עד שעה</label><input type="time" id="dnCraneTo" dir="ltr"></div>
          <div class="drv-field"><label>טון</label><input type="number" id="dnCraneTon" placeholder="טון"></div>
        </div>
        <div class="drv-field">
          <label>יום / לילה</label>
          <div class="drv-toggle-row">
            <button class="drv-toggle active" id="drvBtnDay" onclick="drvSetDayNight('day')">☀️ יום</button>
            <button class="drv-toggle" id="drvBtnNight" onclick="drvSetDayNight('night')">🌙 לילה</button>
          </div>
        </div>
        <div class="drv-field"><label>מחיר לא כולל מע״מ (ש״ח)</label><input type="number" id="dnPrice" placeholder="0.00"></div>
      </div>
    </div>

    <!-- מקבל וחתימה -->
    <div class="drv-card">
      <div class="drv-card-head"><span>✍️</span> פרטי מקבל וחתימה</div>
      <div class="drv-card-body" style="padding-bottom:0">
        <div class="drv-row2">
          <div class="drv-field"><label>שם המקבל</label><input type="text" id="dnRecipient" placeholder="שם מלא"></div>
          <div class="drv-field"><label>טלפון / נייד</label><input type="tel" id="dnRecipientPhone" placeholder="05X-XXXXXXX" dir="ltr"></div>
        </div>
        <div class="drv-field"><label>חתימת המקבל</label>
          <div class="sig-wrap">
            <canvas id="sigCanvas" style="width:100%;height:110px;background:#f8faff;display:block;cursor:crosshair;touch-action:none;border-radius:8px 8px 0 0;"></canvas>
            <div class="sig-overlay" id="sigOverlay"><span style="font-size:20px;opacity:.4">✍️</span><span>חתום כאן עם האצבע</span></div>
          </div>
          <div class="sig-bar">
            <span style="font-size:11px;color:var(--txt-muted);font-weight:600">חתימה דיגיטלית</span>
            <button class="sig-clear" onclick="clearSignature()">✕ נקה</button>
          </div>
        </div>
      </div>
    </div>

    <!-- תמונה -->
    <div class="drv-card">
      <div class="drv-card-head"><span>📷</span> תמונת תיעוד</div>
      <div class="drv-card-body">
        <div class="drv-photo-area" id="drvPhotoArea" onclick="document.getElementById('dnPhoto').click()">
          <img id="dnPhotoPreview" class="photo-preview-img" style="display:none;width:100%;border-radius:8px;object-fit:cover;max-height:150px;" />
          <div id="drvPhotoPlaceholder">
            <div style="font-size:26px">📷</div>
            <div style="font-size:13px;font-weight:700">צלם תמונה לתיעוד</div>
            <div style="font-size:11px;color:var(--txt-muted)">לחץ לצילום</div>
          </div>
          <input type="file" accept="image/*" capture="environment" id="dnPhoto" style="display:none" onchange="handleDriverPhoto(this)">
        </div>
      </div>
    </div>

    <!-- Buttons -->
    <div class="drv-btn-row">
      <button class="drv-btn-print" onclick="drvPrintNote()">🖨️ הדפס</button>
      <button class="drv-submit" onclick="submitDeliveryNote()">📤 שלח תעודה</button>
    </div>

  </div><!-- /driverFormView -->

  <!-- Success -->
  <div id="driverSuccessView" class="drv-success" style="display:none">
    <div class="si">✅</div>
    <h2>תעודה נשלחה!</h2>
    <p>השטר נשמר במערכת ויופיע במשרד</p>
    <button class="drv-new-btn" onclick="startNewDeliveryNote()">➕ תעודה חדשה</button>
  </div>
</div>

<!-- Login Screen -->
<div id="loginScreen">
  <div class="login-box">
    <div class="login-logo">🚛</div>
    <div class="login-title">הובלות דניאל דוד</div>
    <div class="login-sub">כניסה למערכת ניהול</div>
    <div class="login-field">
      <label>שם משתמש</label>
      <input type="text" id="loginUser" placeholder="שם משתמש" autocomplete="username" />
    </div>
    <div class="login-field">
      <label>סיסמה</label>
      <input type="password" id="loginPass" placeholder="סיסמה" autocomplete="current-password" onkeydown="if(event.key==='Enter')doLogin()" />
    </div>
    <button class="login-btn" onclick="doLogin()">כניסה</button>
    <div class="login-err" id="loginErr"></div>
  </div>
</div>

<div class="toast-wrap" id="toastWrap"></div>

<!-- Sync badge -->
<button class="sync-badge" id="syncBadge" onclick="openSyncSetup()" title="הגדרות שיתוף נתונים">
  <span class="sync-dot loading" id="syncDot" style="background:#3B82F6"></span>
  <span id="syncLabel">מתחבר...</span>
</button>

<!-- Google Sheets setup modal -->
<div class="modal-overlay" id="syncSetupModal">
  <div class="modal-box" style="max-width:480px">
    <h2 class="modal-title">⚙️ הגדרת שיתוף נתונים</h2>
    <p style="font-size:.9rem;color:var(--txt-sec);margin-bottom:16px;line-height:1.6">
      כדי ששניכם תראו אותם נתונים, הכנס את כתובת ה-Google Apps Script שיצרת. אם עדיין לא הגדרת — עיין בהוראות שקיבלת.
    </p>
    <div class="form-group" style="margin-bottom:14px">
      <label class="form-label">כתובת Google Apps Script (URL)</label>
      <input class="form-control" type="url" id="gsUrlInput" placeholder="https://script.google.com/macros/s/..." style="font-size:.82rem;direction:ltr">
    </div>
    <div id="gsTestResult" style="font-size:.83rem;margin-bottom:12px;min-height:20px"></div>
    <div style="display:flex;gap:10px;flex-wrap:wrap">
      <button class="btn-primary" style="flex:1" onclick="saveGsUrl()">💾 שמור וחבר</button>
      <button type="button" onclick="testGsUrl()" style="padding:10px 16px;background:var(--navy-mid);color:var(--amber);border:none;border-radius:var(--radius);font-weight:700;font-size:.9rem;cursor:pointer">🔍 בדוק חיבור</button>
      <button type="button" onclick="clearGsUrl()" style="padding:10px 12px;background:var(--expense-bg);color:var(--expense-txt);border:none;border-radius:var(--radius);font-weight:700;font-size:.83rem;cursor:pointer">✕ נתק</button>
    </div>
    <button class="modal-close" onclick="closeModal('syncSetupModal')">✕</button>
  </div>
</div>

<style>
/* ── DRIVER SCREEN ──────────────────────────────────────────── */
#driverScreen { position:fixed; inset:0; z-index:5000; background:var(--bg); display:none; overflow-y:auto; }
.drv-header { background:var(--navy); color:#fff; padding:12px 16px; display:flex; align-items:center; gap:10px; position:sticky; top:0; z-index:10; }
.drv-header-logo { font-size:24px; background:var(--amber); width:38px; height:38px; border-radius:9px; display:grid; place-items:center; flex-shrink:0; }
.drv-header-title { font-size:13px; font-weight:800; line-height:1.2; color:#fff; }
.drv-name { font-size:11px; opacity:.6; color:#fff; margin-top:2px; }
.drv-note-badge { background:rgba(255,255,255,.12); color:var(--amber); font-size:12px; font-weight:700; padding:4px 10px; border-radius:20px; white-space:nowrap; }
.drv-form { max-width:480px; margin:0 auto; padding:14px 14px 100px; display:flex; flex-direction:column; gap:12px; }
/* Cards */
.drv-card { border:1.5px solid var(--border); border-radius:12px; overflow:hidden; }
.drv-card-head { background:var(--navy); padding:8px 14px; display:flex; align-items:center; gap:7px; font-size:12px; font-weight:700; color:#fff; letter-spacing:.02em; }
.drv-card-body { padding:12px; display:flex; flex-direction:column; gap:10px; }
/* Fields */
.drv-field { display:flex; flex-direction:column; gap:4px; margin-bottom:0; }
.drv-field label { font-size:11px; font-weight:700; color:var(--txt-muted); text-transform:uppercase; letter-spacing:.05em; }
.drv-field input, .drv-field textarea, .drv-field select { width:100%; box-sizing:border-box; padding:9px 11px; border:1.5px solid var(--border); border-radius:8px; font-family:inherit; font-size:13.5px; background:var(--bg); color:var(--txt); outline:none; transition:border .15s; direction:rtl; }
.drv-field input:focus, .drv-field textarea:focus { border-color:var(--navy); }
.drv-field input[readonly] { background:rgba(245,166,35,.08); border-color:rgba(245,166,35,.3); color:var(--txt-muted); }
.drv-field textarea { resize:none; min-height:68px; line-height:1.5; }
/* Grids */
.drv-row2 { display:grid; grid-template-columns:1fr 1fr; gap:8px; }
.drv-row3 { display:grid; grid-template-columns:1fr 1fr 74px; gap:8px; }
/* Toggle */
.drv-toggle-row { display:flex; gap:8px; }
.drv-toggle { flex:1; padding:9px 6px; border-radius:8px; border:1.5px solid var(--border); background:var(--bg); font-family:inherit; font-size:13px; font-weight:700; cursor:pointer; color:var(--txt-muted); transition:all .15s; display:flex; align-items:center; justify-content:center; gap:5px; }
.drv-toggle.active { background:var(--navy); border-color:var(--navy); color:#fff; }
/* Signature */
.sig-wrap { border:1.5px solid var(--border); border-radius:10px; overflow:hidden; position:relative; }
.sig-overlay { position:absolute; top:50%; left:50%; transform:translate(-50%,-50%); font-size:12px; color:var(--txt-muted); pointer-events:none; display:flex; flex-direction:column; align-items:center; gap:4px; transition:opacity .2s; }
.sig-bar { display:flex; justify-content:space-between; align-items:center; padding:6px 10px; background:var(--bg); border-top:1px solid var(--border); }
.sig-clear { font-family:inherit; font-size:11px; color:var(--expense); background:none; border:none; cursor:pointer; font-weight:700; padding:2px 4px; }
/* Photo */
.drv-photo-area { border:2px dashed var(--border); border-radius:10px; min-height:90px; display:flex; flex-direction:column; align-items:center; justify-content:center; gap:6px; cursor:pointer; padding:14px; transition:border-color .15s; }
.drv-photo-area:hover { border-color:var(--amber); }
.photo-preview-img { width:100%; max-height:180px; object-fit:cover; border-radius:var(--radius); border:1.5px solid var(--border); display:none; margin-top:6px; }
/* Buttons */
.drv-btn-row { display:flex; gap:10px; }
.drv-submit { flex:1; padding:14px; background:var(--navy); color:#fff; border-radius:var(--radius-lg); font-size:1rem; font-weight:800; box-shadow:var(--shadow-lg); display:flex; align-items:center; justify-content:center; gap:8px; }
.drv-submit:active { opacity:.88; }
.drv-btn-print { background:var(--bg); border:1.5px solid var(--border); border-radius:var(--radius-lg); padding:14px 13px; font-family:inherit; font-size:13px; font-weight:700; color:var(--txt-muted); cursor:pointer; white-space:nowrap; }
.drv-btn-print:hover { border-color:var(--amber); color:var(--txt); }
/* Success */
.drv-success { text-align:center; padding:60px 20px; }
.drv-success .si { font-size:3.5rem; margin-bottom:14px; }
.drv-success h2 { font-size:1.3rem; font-weight:800; color:var(--income); margin-bottom:8px; }
.drv-success p { color:var(--txt-sec); margin-bottom:20px; }
.drv-new-btn { background:var(--amber); color:var(--navy); padding:13px 28px; border-radius:var(--radius-lg); font-size:.95rem; font-weight:800; }
/* delivery notes management view */
.dn-card { background:var(--card); border-radius:var(--radius-lg); box-shadow:var(--shadow); margin-bottom:14px; overflow:hidden; }
.dn-card-head { display:flex; align-items:center; gap:10px; padding:14px 16px; border-bottom:1px solid var(--border-soft); }
.dn-card-head .dn-date { font-size:.78rem; color:var(--txt-muted); }
.dn-card-head .dn-driver { font-weight:700; font-size:.9rem; flex:1; }
.dn-card-body { padding:14px 16px; font-size:.86rem; color:var(--txt-sec); line-height:1.6; }
.dn-card-body strong { color:var(--txt); }
.dn-sig-img, .dn-photo-img { max-width:100%; border-radius:8px; margin-top:8px; border:1px solid var(--border); }
.dn-sig-img { max-height:80px; }
.dn-photo-img { max-height:200px; object-fit:cover; }
.dn-toggle-btn { font-size:.8rem; color:var(--amber); font-weight:700; cursor:pointer; background:none; border:none; padding:0; margin-top:6px; }
</style>

<script>
/* ─── PRINT DELIVERY NOTE ────────────────────────────────── */
function printDeliveryNote(id) {
  let notes = []; try { notes = JSON.parse(localStorage.getItem('ddh_notes')||'[]'); } catch {}
  const n = notes.find(x => x.id === id); if (!n) return;
  const num = String(notes.findIndex(x=>x.id===id)+1).padStart(4,'0');
  const win = window.open('','_blank','width=800,height=900');
  win.document.write(`<!DOCTYPE html><html lang="he" dir="rtl"><head><meta charset="UTF-8">
  <title>תעודת משלוח ${num}</title>
  <style>
    * { box-sizing:border-box; margin:0; padding:0; }
    body { font-family: Arial, sans-serif; font-size:13px; color:#111; background:#fff; padding:20px; }
    .header { display:flex; justify-content:space-between; align-items:flex-start; border-bottom:3px solid #0E1C2F; padding-bottom:14px; margin-bottom:18px; }
    .logo-block h1 { font-size:22px; font-weight:900; color:#0E1C2F; }
    .logo-block p { font-size:11px; color:#555; margin-top:2px; }
    .note-num { text-align:left; }
    .note-num .label { font-size:11px; color:#888; }
    .note-num .num { font-size:20px; font-weight:900; color:#F5A623; }
    .note-num .date { font-size:11px; color:#555; margin-top:2px; }
    table { width:100%; border-collapse:collapse; margin-bottom:14px; }
    th { background:#0E1C2F; color:#fff; padding:8px 10px; text-align:right; font-size:12px; font-weight:700; }
    td { border:1px solid #d0d5dd; padding:8px 10px; font-size:12.5px; vertical-align:top; }
    .section-head { background:#f4f6f9; font-weight:700; font-size:12px; color:#333; border-bottom:2px solid #0E1C2F; padding:7px 10px; }
    .sig-area { display:flex; gap:20px; align-items:flex-start; margin-top:10px; }
    .sig-box { flex:1; border:1.5px solid #c5cdd8; border-radius:8px; overflow:hidden; }
    .sig-box img { max-width:100%; max-height:100px; display:block; }
    .sig-label { font-size:10px; color:#888; text-align:center; padding:4px; background:#f9f9f9; border-top:1px solid #e0e0e0; }
    .photo-box img { max-width:200px; max-height:160px; border-radius:8px; border:1.5px solid #d0d5dd; }
    .footer { margin-top:20px; border-top:1.5px solid #d0d5dd; padding-top:10px; font-size:10px; color:#888; text-align:center; }
    @media print { body { padding:10px; } button { display:none; } }
  </style>
  </head><body>
  <div class="header">
    <div class="logo-block">
      <h1>🚛 הובלות דניאל דוד</h1>
      <p>שירותי הובלה ומסחר</p>
    </div>
    <div class="note-num">
      <div class="label">תעודת משלוח</div>
      <div class="num">#${num}</div>
      <div class="date">תאריך: ${n.date}</div>
    </div>
  </div>

  <table>
    <tr><th colspan="2" style="background:#f4f6f9;color:#0E1C2F;border:1px solid #d0d5dd">פרטי הובלה</th></tr>
    <tr><td style="width:30%;font-weight:700;color:#555">נהג</td><td>${n.driverName||''}</td></tr>
    <tr><td style="font-weight:700;color:#555">לקוח</td><td>${n.clientName||''}</td></tr>
    ${n.fromAddress?`<tr><td style="font-weight:700;color:#555">כתובת איסוף</td><td>${n.fromAddress}</td></tr>`:''}
    ${n.toAddress?`<tr><td style="font-weight:700;color:#555">כתובת יעד</td><td>${n.toAddress}</td></tr>`:''}
    <tr><td style="font-weight:700;color:#555">שעת הגעה</td><td>${n.arrivalTime||'—'}</td></tr>
    <tr><td style="font-weight:700;color:#555">שעת יציאה</td><td>${n.departureTime||'—'}</td></tr>
  </table>

  ${n.items?`<table>
    <tr><th>פירוט סחורה / פריטים</th></tr>
    <tr><td style="min-height:60px;white-space:pre-wrap">${n.items}</td></tr>
  </table>`:''}

  ${n.notes?`<table>
    <tr><th>הערות</th></tr>
    <tr><td>${n.notes}</td></tr>
  </table>`:''}

  <div class="sig-area">
    ${n.signature?`<div style="flex:1"><div class="section-head">חתימת לקוח</div><div class="sig-box"><img src="${n.signature}"><div class="sig-label">חתימה דיגיטלית</div></div></div>`:'<div style="flex:1"><div class="section-head">חתימת לקוח</div><div style="border:1.5px dashed #c5cdd8;border-radius:8px;height:80px;display:flex;align-items:flex-end;padding:6px;"><span style="font-size:10px;color:#aaa">___________________</span></div></div>'}
    ${n.photo?`<div class="photo-box"><div class="section-head">תמונה</div><img src="${n.photo}"></div>`:''}
  </div>

  <div class="footer">
    הובלות דניאל דוד | תעודה מספר ${num} | ${n.date}
  </div>

  <div style="text-align:center;margin-top:16px">
    <button onclick="window.print()" style="background:#0E1C2F;color:#fff;padding:10px 28px;border-radius:8px;font-size:14px;cursor:pointer">🖨️ הדפס / שמור PDF</button>
  </div>
  </body></html>`);
  win.document.close();
}

/* ─── STORAGE (local) ─────────────────────────────────────── */
const LS = {
  get: (k,d) => { try { return JSON.parse(localStorage.getItem(k)) ?? d; } catch { return d; } },
  set: (k,v) => { try { localStorage.setItem(k, JSON.stringify(v)); } catch {} }
};

/* ─── GOOGLE SHEETS (shared) ──────────────────────────────── */
function GS_URL() { return LS.get('ddh_gs_url','') || ''; }

const DB = {
  set(k, v) {
    const url = GS_URL(); if (!url) return;
    fetch(url, { method:'POST', mode:'no-cors', body: new URLSearchParams({sheet:k, data:JSON.stringify(v)}) }).catch(()=>{});
  },
  async get(k) {
    const url = GS_URL(); if (!url) return null;
    try {
      const r = await fetch(`${url}?sheet=${encodeURIComponent(k)}&_t=${Date.now()}`);
      if (!r.ok) return null;
      const text = await r.text();
      const val = JSON.parse(text);
      return (val === null || val === undefined) ? null : val;
    } catch(e) { return null; }
  }
};

/* ─── DATA ────────────────────────────────────────────────── */
let resources, transactions, clients, banks, cashItems, drivers;

/* migrations run after data is loaded */
function uid() { return Date.now().toString(36) + Math.random().toString(36).slice(2,7); }

function loadFromLocalStorage() {
  resources    = LS.get('ddh_resources', null);
  transactions = LS.get('ddh_tx', []);
  clients      = LS.get('ddh_clients2', null);
  banks        = LS.get('ddh_banks', []);
  cashItems    = LS.get('ddh_cash',  []);
  drivers      = LS.get('ddh_drivers', [{name:'אורן 4867131'},{name:'דניאל 6084857'}]);
  runMigrations();
}

function runMigrations() {
  if (!resources) {
    resources = [
      { id: uid(), name: 'משאית קירור',      type: 'truck-fridge'   },
      { id: uid(), name: 'משאית מנוף קטן',  type: 'truck-crane-sm' },
      { id: uid(), name: 'משאית מנוף גדול', type: 'truck-crane-lg' },
      { id: uid(), name: 'משאית וילון',     type: 'truck-curtain'  },
    ];
    saveResources();
  } else {
    let changed = false;
    resources.forEach(r => { if (r.type === 'truck-crane') { r.type = 'truck-crane-sm'; changed = true; } });
    const existingTypes = new Set(resources.map(r => r.type));
    [{ name:'משאית מנוף גדול', type:'truck-crane-lg' }, { name:'משאית וילון', type:'truck-curtain' }]
      .forEach(e => { if (!existingTypes.has(e.type)) { resources.push({ id:uid(), ...e }); changed = true; } });
    if (changed) saveResources();
  }
  if (!clients) {
  clients = [
    {
      id: 'c_hovlam',
      name: 'הובלות למשא',
      defaultOrigin: 'מרלוג אושר עד',
      prices: [
        { destination:'נתניה',       price:1100 },
        { destination:'אשדוד',       price:850  },
        { destination:'כנות',        price:740  },
        { destination:'לוד',         price:740  },
        { destination:'פתח תקווה',   price:850  },
        { destination:'תל אביב',     price:850  },
        { destination:'בית שמש',     price:740  },
        { destination:'בני ברק',     price:850  },
        { destination:'עד הלום',     price:850  },
        { destination:'אשקלון',      price:935  },
        { destination:'ביתר עילית',  price:1100 },
        { destination:'גבעת שאול',   price:1100 },
        { destination:'קרית אונו',   price:850  },
        { destination:'רוממה',       price:1100 },
        { destination:'חיפה',        price:1650 },
        { destination:'קרית ים',     price:1650 },
        { destination:'קרית ביאליק', price:1650 },
        { destination:'עפולה',       price:1650 },
        { destination:'באר שבע',     price:1100 },
        { destination:'חדרה',        price:1100 },
        { destination:'כפר סבא',     price:850  },
        { destination:'ראשון לציון', price:850  },
      ]
    }
  ];
  saveClients();
  }
} // end runMigrations

function saveTx()        { LS.set('ddh_tx', transactions);        DB.set('ddh_tx', transactions); }
function saveResources() { LS.set('ddh_resources', resources);    DB.set('ddh_resources', resources); }
function saveClients()   { LS.set('ddh_clients2', clients);       DB.set('ddh_clients2', clients); }
function saveBanks()     { LS.set('ddh_banks', banks);            DB.set('ddh_banks', banks); }
function saveCashItems() { LS.set('ddh_cash',  cashItems);        DB.set('ddh_cash', cashItems); }
function saveDrivers()   { LS.set('ddh_drivers', drivers);        DB.set('ddh_drivers', drivers); }

/* ─── SHEETS SYNC ─────────────────────────────────────────── */
async function syncFromSheets() {
  const url = GS_URL(); if (!url) return false;
  try {
    const [res,tx,cli,bnk,csh,drv,nts] = await Promise.all([
      DB.get('ddh_resources'), DB.get('ddh_tx'), DB.get('ddh_clients2'),
      DB.get('ddh_banks'),     DB.get('ddh_cash'), DB.get('ddh_drivers'), DB.get('ddh_notes')
    ]);
    let hadData = false;
    if (Array.isArray(res))  { resources    = res; LS.set('ddh_resources', res); hadData=true; }
    if (Array.isArray(tx))   { transactions = tx;  LS.set('ddh_tx', tx);         hadData=true; }
    if (Array.isArray(cli))  { clients      = cli; LS.set('ddh_clients2', cli);  hadData=true; }
    if (Array.isArray(bnk))  { banks        = bnk; LS.set('ddh_banks', bnk);     hadData=true; }
    if (Array.isArray(csh))  { cashItems    = csh; LS.set('ddh_cash', csh);      hadData=true; }
    if (Array.isArray(drv))  { drivers      = drv; LS.set('ddh_drivers', drv);   hadData=true; }
    if (Array.isArray(nts))  { LS.set('ddh_notes', nts); hadData=true; }
    setSyncStatus('ok');
    return hadData;
  } catch(e) { setSyncStatus('error'); return false; }
}

function setSyncStatus(state) {
  const dot = document.getElementById('syncDot');
  const lbl = document.getElementById('syncLabel');
  if (!dot) return;
  const map = {
    loading: { color:'#3B82F6', text:'מסנכרן...' },
    ok:      { color:'#16A34A', text:'מסונכרן ✓' },
    offline: { color:'#F5A623', text:'מקומי בלבד' },
    error:   { color:'#DC2626', text:'שגיאת חיבור' }
  };
  const s = map[state] || map.offline;
  dot.style.background = s.color;
  dot.className = 'sync-dot' + (state==='loading' ? ' loading' : '');
  lbl.textContent = s.text;
}

function refreshCurrentTab() {
  const active = document.querySelector('.tab-panel.active'); if (!active) return;
  const id = active.id;
  if (id==='panel-journal')  renderJournal();
  if (id==='panel-report')   renderReport();
  if (id==='panel-entry')    renderTodaySummary();
  if (id==='panel-cashflow') renderCashFlow();
  if (id==='panel-notes')    renderDeliveryNotes();
}

/* ─── SYNC SETUP MODAL ────────────────────────────────────── */
function openSyncSetup() {
  document.getElementById('gsUrlInput').value = GS_URL();
  document.getElementById('gsTestResult').textContent = '';
  document.getElementById('syncSetupModal').classList.add('open');
}
async function testGsUrl() {
  const url = document.getElementById('gsUrlInput').value.trim();
  const res = document.getElementById('gsTestResult');
  if (!url) { res.textContent = '⚠️ הזן כתובת תחילה'; res.style.color='var(--amber)'; return; }
  res.textContent = '⏳ בודק...'; res.style.color='var(--txt-sec)';
  try {
    const r = await fetch(`${url}?sheet=ddh_test&_t=${Date.now()}`);
    if (r.ok) { res.textContent = '✅ החיבור תקין!'; res.style.color='var(--income)'; }
    else      { res.textContent = '❌ לא הצלחתי להתחבר (status '+r.status+')'; res.style.color='var(--expense)'; }
  } catch(e) { res.textContent = '❌ שגיאת חיבור: '+e.message; res.style.color='var(--expense)'; }
}
function saveGsUrl() {
  const url = document.getElementById('gsUrlInput').value.trim();
  LS.set('ddh_gs_url', url);
  closeModal('syncSetupModal');
  if (url) {
    setSyncStatus('loading');
    syncFromSheets().then(hadData => {
      if (!hadData) {
        // First time: push local data to Sheets
        saveTx(); saveResources(); saveClients(); saveBanks(); saveCashItems(); saveDrivers();
        toast('✅ נתונים הועלו ל-Google Sheets');
      } else {
        populateAll(); refreshCurrentTab();
        toast('✅ מחובר! הנתונים סונכרנו');
      }
    });
  } else {
    setSyncStatus('offline');
    toast('ניתוק משיתוף');
  }
}
function clearGsUrl() {
  LS.set('ddh_gs_url','');
  document.getElementById('gsUrlInput').value = '';
  setSyncStatus('offline');
  closeModal('syncSetupModal');
  toast('ניתוק משיתוף');
}

/* ─── HELPERS ─────────────────────────────────────────────── */
function resourceById(id) { return resources.find(r=>r.id===id); }
function clientById(id)   { return clients.find(c=>c.id===id); }
function resourceIcon(t)  { return {'truck-crane':'🏗️','truck-crane-sm':'🏗️','truck-crane-lg':'🏗️','truck-fridge':'❄️','truck-curtain':'🚛','sub':'🤝','other':'🚛'}[t]||'🚛'; }
function resTypeLabel(t)  { return {'truck-crane':'משאית מנוף','truck-crane-sm':'משאית מנוף קטן','truck-crane-lg':'משאית מנוף גדול','truck-fridge':'משאית קירור','truck-curtain':'משאית וילון','sub':'קבלן משנה','other':'אחר'}[t]||''; }
function fmtCurrency(n)   { return '₪'+Number(Math.abs(n)).toLocaleString('he-IL',{minimumFractionDigits:0,maximumFractionDigits:0}); }
function fmtDate(iso)     { if(!iso) return ''; const [y,m,d]=iso.split('-'); return `${d}.${m}.${y}`; }
const MONTHS = ['','ינואר','פברואר','מרץ','אפריל','מאי','יוני','יולי','אוגוסט','ספטמבר','אוקטובר','נובמבר','דצמבר'];
const today  = () => new Date().toISOString().slice(0,10);

/* ─── THEME ───────────────────────────────────────────────── */
function applyTheme(t) {
  document.documentElement.setAttribute('data-theme', t);
  document.getElementById('themeBtn').textContent = t==='dark'?'☀️':'🌙';
  LS.set('ddh_theme', t);
}
function toggleTheme() { applyTheme(document.documentElement.getAttribute('data-theme')==='dark'?'light':'dark'); }
(()=>{ const s=LS.get('ddh_theme',null); applyTheme(s||(window.matchMedia('(prefers-color-scheme:dark)').matches?'dark':'light')); })();

/* ─── MAIN TABS ───────────────────────────────────────────── */
function switchTab(name) {
  document.querySelectorAll('.tab-btn').forEach(b=>b.classList.toggle('active',b.dataset.tab===name));
  document.querySelectorAll('.tab-panel').forEach(p=>p.classList.toggle('active',p.id==='panel-'+name));
  if(name==='journal')  renderJournal();
  if(name==='report')   renderReport();
  if(name==='entry')    renderTodaySummary();
  if(name==='cashflow') renderCashFlow();
}

/* ─── SETTINGS TABS ───────────────────────────────────────── */
function switchSettingsTab(name) {
  document.querySelectorAll('.settings-tab').forEach((b,i)=>b.classList.toggle('active',['resources','clients'][i]===name));
  document.querySelectorAll('.settings-panel').forEach(p=>p.classList.toggle('active',p.id==='sPanel-'+name));
  if(name==='clients') renderClientsList();
}

/* ─── POPULATE SELECTS ────────────────────────────────────── */
function populateAll() {
  // Resources
  ['incResource','expResource','editResource','filterResource'].forEach(sid=>{
    const el=document.getElementById(sid); if(!el) return;
    const isFilter=sid.startsWith('filter');
    const cur=el.value;
    el.innerHTML=isFilter?'<option value="">הכל</option>':'<option value="">— בחר —</option>';
    resources.forEach(r=>{ const o=document.createElement('option'); o.value=r.id; o.textContent=resourceIcon(r.type)+' '+r.name; el.appendChild(o); });
    if(cur) el.value=cur;
  });
  // Clients
  ['incClient','editClient','filterClient'].forEach(sid=>{
    const el=document.getElementById(sid); if(!el) return;
    const isFilter=sid.startsWith('filter');
    const cur=el.value;
    el.innerHTML=isFilter?'<option value="">הכל</option>':'<option value="">— ללא לקוח —</option>';
    clients.forEach(c=>{ const o=document.createElement('option'); o.value=c.id; o.textContent=c.name; el.appendChild(o); });
    if(cur) el.value=cur;
  });
  // Drivers
  ['incDriver','expDriver','editDriver'].forEach(sid=>{
    const el=document.getElementById(sid); if(!el) return;
    const cur=el.value;
    el.innerHTML='<option value="">— בחר נהג —</option>';
    drivers.forEach(d=>{ const o=document.createElement('option'); o.value=d.name; o.textContent=d.name; el.appendChild(o); });
    const newOpt=document.createElement('option'); newOpt.value='__new__'; newOpt.textContent='➕ הוסף נהג חדש...'; el.appendChild(newOpt);
    if(cur && cur!=='__new__') el.value=cur;
  });
}

/* ─── DRIVER HELPERS ──────────────────────────────────────── */
function pickDriver(selId, wrapId) {
  const isNew = document.getElementById(selId).value === '__new__';
  document.getElementById(wrapId).style.display = isNew ? '' : 'none';
  if (isNew) { const inp=document.getElementById(selId.replace('Driver','DriverNewVal')); if(inp) inp.focus(); }
}
function resolveDriver(selId, newValId) {
  const sel = document.getElementById(selId); if(!sel) return null;
  if (sel.value === '__new__') {
    const newName = document.getElementById(newValId).value.trim();
    if (newName && !drivers.find(d=>d.name===newName)) {
      drivers.push({name:newName}); saveDrivers();
    }
    return newName || null;
  }
  return sel.value || null;
}
function resetDriverField(selId, wrapId, newValId) {
  const el=document.getElementById(selId); if(el) el.value='';
  const wr=document.getElementById(wrapId); if(wr) wr.style.display='none';
  const nv=document.getElementById(newValId); if(nv) nv.value='';
}

/* ─── WORK TYPE ───────────────────────────────────────────── */
function setWorkType(t) {
  document.getElementById('incWorkType').value=t;
  document.getElementById('wbHovla').classList.toggle('active',t==='הובלה');
  document.getElementById('wbHanafa').classList.toggle('active',t==='הנפה');
}
function setEditWorkType(t) {
  document.getElementById('editWorkType').value=t;
  document.getElementById('ewbHovla').classList.toggle('active',t==='הובלה');
  document.getElementById('ewbHanafa').classList.toggle('active',t==='הנפה');
}
function setEditType(t) {
  document.getElementById('editType').value=t;
  document.getElementById('editTypeIncome').classList.toggle('active',t==='income');
  document.getElementById('editTypeExpense').classList.toggle('active',t==='expense');
  document.getElementById('editWorkTypeGroup').style.display=t==='income'?'':'none';
  document.getElementById('editCatGroup').style.display=t==='expense'?'':'none';
}

/* ─── INCOME CLIENT CHANGE ────────────────────────────────── */
function handleIncClientChange() {
  const cid=document.getElementById('incClient').value;
  const client=clientById(cid);
  const origEl=document.getElementById('incOrigin');
  const destGroup=document.getElementById('incDestGroup');
  const destFree=document.getElementById('incDestFreeGroup');
  const destSel=document.getElementById('incDestination');
  const amtEl=document.getElementById('incAmount');
  document.getElementById('incPriceHint').classList.remove('visible');
  amtEl.classList.remove('auto-filled');

  if(client) {
    origEl.value=client.defaultOrigin||'';
    if(client.prices&&client.prices.length) {
      destGroup.style.display='';
      destFree.style.display='none';
      destSel.innerHTML='<option value="">— בחר יעד —</option>';
      client.prices.forEach(p=>{ const o=document.createElement('option'); o.value=p.destination; o.textContent=`${p.destination}  —  ${fmtCurrency(p.price)}`; destSel.appendChild(o); });
    } else {
      destGroup.style.display='none';
      destFree.style.display='';
    }
  } else {
    origEl.value='';
    destGroup.style.display='none';
    destFree.style.display='';
  }
}
function handleIncDestChange() {
  const cid=document.getElementById('incClient').value;
  const dest=document.getElementById('incDestination').value;
  const client=clientById(cid);
  const amtEl=document.getElementById('incAmount');
  const hint=document.getElementById('incPriceHint');
  if(!client||!dest) { amtEl.classList.remove('auto-filled'); hint.classList.remove('visible'); return; }
  const pe=client.prices.find(p=>p.destination===dest);
  if(pe) { amtEl.value=pe.price; amtEl.classList.add('auto-filled'); hint.classList.add('visible'); }
}

/* ─── EDIT CLIENT CHANGE ──────────────────────────────────── */
function handleEditClientChange() {
  const cid=document.getElementById('editClient').value;
  const client=clientById(cid);
  const dg=document.getElementById('editDestGroup');
  const df=document.getElementById('editDestFreeGroup');
  const ds=document.getElementById('editDestination');
  const origEl=document.getElementById('editOrigin');
  if(client) {
    if(!origEl.value) origEl.value=client.defaultOrigin||'';
    if(client.prices&&client.prices.length) {
      dg.style.display=''; df.style.display='none';
      ds.innerHTML='<option value="">— בחר יעד —</option>';
      client.prices.forEach(p=>{ const o=document.createElement('option'); o.value=p.destination; o.textContent=`${p.destination}  —  ${fmtCurrency(p.price)}`; ds.appendChild(o); });
    } else { dg.style.display='none'; df.style.display=''; }
  } else { dg.style.display='none'; df.style.display=''; }
}
function handleEditDestChange() {
  const cid=document.getElementById('editClient').value;
  const dest=document.getElementById('editDestination').value;
  const client=clientById(cid);
  if(!client||!dest) return;
  const pe=client.prices.find(p=>p.destination===dest);
  if(pe) document.getElementById('editAmount').value=pe.price;
}

/* ─── OPEN MODALS ─────────────────────────────────────────── */
function openIncomeModal() {
  populateAll();
  document.getElementById('incDate').value=today();
  document.getElementById('incResource').value='';
  document.getElementById('incClient').value='';
  document.getElementById('incOrigin').value='';
  document.getElementById('incDestination').value='';
  document.getElementById('incDestFree').value='';
  document.getElementById('incAmount').value='';
  document.getElementById('incAmount').classList.remove('auto-filled');
  document.getElementById('incDesc').value='';
  document.getElementById('incPriceHint').classList.remove('visible');
  document.getElementById('incDestGroup').style.display='none';
  document.getElementById('incDestFreeGroup').style.display='';
  setWorkType('הובלה');
  resetDriverField('incDriver','incDriverNewRow','incDriverNewVal');
  document.getElementById('incomeModal').classList.add('open');
}
function openExpenseModal() {
  populateAll();
  document.getElementById('expDate').value=today();
  document.getElementById('expResource').value='';
  document.getElementById('expAmount').value='';
  document.getElementById('expDesc').value='';
  resetDriverField('expDriver','expDriverNewRow','expDriverNewVal');
  document.getElementById('expenseModal').classList.add('open');
}
function openSettingsModal() {
  renderResourcesList();
  renderClientsList();
  switchSettingsTab('resources');
  document.getElementById('settingsModal').classList.add('open');
}
function closeModal(id) { document.getElementById(id).classList.remove('open'); }

/* ─── SAVE INCOME ─────────────────────────────────────────── */
function handleIncome(e) {
  e.preventDefault();
  const clientId=document.getElementById('incClient').value;
  const client=clientById(clientId);
  const hasPriceList=client&&client.prices&&client.prices.length;
  const destination=hasPriceList
    ? document.getElementById('incDestination').value
    : document.getElementById('incDestFree').value.trim();

  const tx={
    id:uid(), date:document.getElementById('incDate').value,
    resourceId:document.getElementById('incResource').value,
    type:'income',
    workType:document.getElementById('incWorkType').value,
    amount:parseFloat(document.getElementById('incAmount').value)||0,
    clientId:clientId||null,
    origin:document.getElementById('incOrigin').value.trim(),
    destination:destination||null,
    desc:document.getElementById('incDesc').value.trim(),
    driverName:resolveDriver('incDriver','incDriverNewVal')||null,
  };
  if(!tx.resourceId){toast('⚠️ יש לבחור משאית/קבלן');return;}
  if(!tx.amount){toast('⚠️ יש להזין סכום');return;}
  transactions.unshift(tx); saveTx();
  closeModal('incomeModal');
  renderTodaySummary();
  toast(`✅ הכנסה נשמרה — ${fmtCurrency(tx.amount)}`);
}

/* ─── SAVE EXPENSE ────────────────────────────────────────── */
function handleExpense(e) {
  e.preventDefault();
  const tx={
    id:uid(), date:document.getElementById('expDate').value,
    resourceId:document.getElementById('expResource').value,
    type:'expense',
    amount:parseFloat(document.getElementById('expAmount').value)||0,
    category:document.getElementById('expCategory').value,
    desc:document.getElementById('expDesc').value.trim(),
    driverName:resolveDriver('expDriver','expDriverNewVal')||null,
  };
  if(!tx.resourceId){toast('⚠️ יש לבחור משאית/קבלן');return;}
  if(!tx.amount){toast('⚠️ יש להזין סכום');return;}
  transactions.unshift(tx); saveTx();
  closeModal('expenseModal');
  renderTodaySummary();
  toast(`✅ הוצאה נשמרה — ${fmtCurrency(tx.amount)}`);
}

/* ─── TODAY SUMMARY ───────────────────────────────────────── */
function renderTodaySummary() {
  const t=today();
  const todayTx=transactions.filter(x=>x.date===t);
  const inc=todayTx.filter(x=>x.type==='income').reduce((s,x)=>s+x.amount,0);
  const exp=todayTx.filter(x=>x.type==='expense').reduce((s,x)=>s+x.amount,0);
  const prf=inc-exp;
  document.getElementById('todayIncome').textContent=fmtCurrency(inc);
  document.getElementById('todayExpense').textContent=fmtCurrency(exp);
  document.getElementById('todayProfit').textContent=fmtCurrency(prf);
  document.getElementById('todayProfitCard').classList.toggle('negative',prf<0);
}

/* ─── JOURNAL ─────────────────────────────────────────────── */
let journalCatFilter = '';  // '' | 'transport' | 'goods'

function setCatFilter(cat) {
  journalCatFilter = cat;
  document.querySelectorAll('.cat-pill').forEach(p => p.classList.toggle('active', p.dataset.cat === cat));
  renderJournal();
}
function resetFilters() {
  ['filterResource','filterClient','filterType'].forEach(id=>document.getElementById(id).value='');
  document.getElementById('filterFrom').value='';
  document.getElementById('filterTo').value='';
  renderJournal();
}
function renderJournal() {
  const fRes=document.getElementById('filterResource').value;
  const fCli=document.getElementById('filterClient').value;
  const fFrom=document.getElementById('filterFrom').value;
  const fTo=document.getElementById('filterTo').value;
  const fType=document.getElementById('filterType').value;
  let list=[...transactions];
  // category filter
  if(journalCatFilter==='transport') list=list.filter(t=>!t.txCategory||t.txCategory==='transport');
  if(journalCatFilter==='goods')     list=list.filter(t=>t.txCategory==='goods');
  if(fRes)  list=list.filter(t=>t.resourceId===fRes);
  if(fCli)  list=list.filter(t=>t.clientId===fCli);
  if(fFrom) list=list.filter(t=>t.date>=fFrom);
  if(fTo)   list=list.filter(t=>t.date<=fTo);
  if(fType) list=list.filter(t=>t.type===fType);
  list.sort((a,b)=>b.date.localeCompare(a.date));

  const c=document.getElementById('journalContainer');

  // Ensure category pills exist above the filters bar
  let pillsEl=document.getElementById('journalCatPills');
  if(!pillsEl){
    pillsEl=document.createElement('div');
    pillsEl.id='journalCatPills';
    pillsEl.className='cat-pills';
    pillsEl.innerHTML=`
      <button class="cat-pill active" data-cat="" onclick="setCatFilter('')">📋 הכל</button>
      <button class="cat-pill" data-cat="transport" onclick="setCatFilter('transport')">🚛 הובלות</button>
      <button class="cat-pill" data-cat="goods"     onclick="setCatFilter('goods')">📦 סחורה</button>`;
    c.parentNode.insertBefore(pillsEl,c);
  }
  // Sync active state
  pillsEl.querySelectorAll('.cat-pill').forEach(p=>p.classList.toggle('active',p.dataset.cat===journalCatFilter));

  if(!list.length){c.innerHTML=`<div class="empty-state"><span class="icon">📭</span>אין פעולות להצגה.</div>`;return;}

  const rows=list.map(t=>{
    const isGoods=(t.txCategory==='goods');
    const isInc=(t.type==='income');

    if(isGoods){
      const payDotHtml=payDot(t.payStatus||'ממתין');
      const docInfo=t.docType&&t.docType!=='ללא'
        ?`<span style="color:var(--txt-muted);font-size:.77rem">${t.docType}${t.docNumber?' #'+t.docNumber:''}</span>`:'';
      const parts=[];
      if(t.goodsParty) parts.push(t.goodsParty);
      if(t.goodsDesc)  parts.push(`<strong>${t.goodsDesc}</strong>`);
      if(t.payStatus)  parts.push(payDotHtml+t.payStatus);
      if(docInfo)      parts.push(docInfo);
      if(t.desc)       parts.push(t.desc);
      return `<tr>
        <td style="white-space:nowrap">${fmtDate(t.date)}</td>
        <td style="font-size:.8rem;color:var(--txt-muted)">—</td>
        <td><span class="badge ${isInc?'goods-inc':'goods-exp'}">${isInc?'💰 מכירה':'🛒 קנייה'}</span></td>
        <td><span class="amount ${isInc?'income':'expense'}">${fmtCurrency(t.amount)}</span></td>
        <td style="font-size:.85rem;line-height:1.5">${parts.join(' · ')}</td>
        <td><div class="action-btns">
          <button class="btn-icon" onclick="openEdit('${t.id}')" title="עריכה">✏️</button>
          <button class="btn-icon del" onclick="deleteTx('${t.id}')" title="מחיקה">🗑️</button>
        </div></td>
      </tr>`;
    }

    // Transport row (existing logic)
    const res=resourceById(t.resourceId);
    const client=clientById(t.clientId);
    const resName=res?resourceIcon(res.type)+' '+res.name:'—';
    const parts=[];
    if(t.workType) parts.push(`<span style="font-weight:700">${t.workType}</span>`);
    if(t.driverName) parts.push(`👤 ${t.driverName}`);
    if(client) parts.push(client.name);
    if(t.origin&&t.destination) parts.push(`${t.origin} → ${t.destination}`);
    else if(t.destination) parts.push(t.destination);
    else if(t.origin) parts.push(t.origin);
    if(!isInc&&t.category) parts.push(t.category);
    if(t.desc) parts.push(t.desc);
    return `<tr>
      <td style="white-space:nowrap">${fmtDate(t.date)}</td>
      <td style="white-space:nowrap">${resName}</td>
      <td><span class="badge ${t.type}">${isInc?'📈 הכנסה':'📉 הוצאה'}</span></td>
      <td><span class="amount ${t.type}">${fmtCurrency(t.amount)}</span></td>
      <td style="font-size:.85rem;line-height:1.4">${parts.join(' · ')}</td>
      <td><div class="action-btns">
        <button class="btn-icon" onclick="openEdit('${t.id}')" title="עריכה">✏️</button>
        <button class="btn-icon del" onclick="deleteTx('${t.id}')" title="מחיקה">🗑️</button>
      </div></td>
    </tr>`;
  }).join('');

  c.innerHTML=`<div class="table-wrap"><table>
    <thead><tr><th>תאריך</th><th>משאית/קבלן</th><th>סוג</th><th>סכום</th><th>פרטים</th><th></th></tr></thead>
    <tbody>${rows}</tbody>
  </table></div>`;
}

function deleteTx(id) {
  if(!confirm('למחוק פעולה זו?')) return;
  transactions=transactions.filter(t=>t.id!==id);
  saveTx(); renderJournal(); renderTodaySummary();
  toast('🗑️ פעולה נמחקה');
}

/* ─── EDIT ────────────────────────────────────────────────── */
let editingId=null;
function openEdit(id) {
  const tx=transactions.find(t=>t.id===id); if(!tx) return;
  if (tx.txCategory === 'goods') { openGoodsEdit(id); return; }
  editingId=id;
  populateAll();
  document.getElementById('editDate').value=tx.date;
  document.getElementById('editResource').value=tx.resourceId||'';
  document.getElementById('editAmount').value=tx.amount;
  document.getElementById('editCategory').value=tx.category||'דלק';
  document.getElementById('editDesc').value=tx.desc||'';
  document.getElementById('editClient').value=tx.clientId||'';
  document.getElementById('editOrigin').value=tx.origin||'';
  document.getElementById('editWorkType').value=tx.workType||'';
  if(tx.workType) setEditWorkType(tx.workType);
  resetDriverField('editDriver','editDriverNewRow','editDriverNewVal');
  if(tx.driverName) document.getElementById('editDriver').value=tx.driverName;
  setEditType(tx.type);
  handleEditClientChange();
  if(tx.destination) {
    const hasPL=clientById(tx.clientId)?.prices?.length;
    if(hasPL) document.getElementById('editDestination').value=tx.destination;
    else document.getElementById('editDestFree').value=tx.destination;
  }
  document.getElementById('editModal').classList.add('open');
}
function saveEdit(e) {
  e.preventDefault();
  const idx=transactions.findIndex(t=>t.id===editingId); if(idx<0) return;
  const clientId=document.getElementById('editClient').value;
  const client=clientById(clientId);
  const hasPL=client?.prices?.length;
  const destination=hasPL
    ? document.getElementById('editDestination').value
    : document.getElementById('editDestFree').value.trim();
  transactions[idx]={
    ...transactions[idx],
    date:document.getElementById('editDate').value,
    resourceId:document.getElementById('editResource').value,
    type:document.getElementById('editType').value,
    workType:document.getElementById('editWorkType').value||null,
    amount:parseFloat(document.getElementById('editAmount').value)||0,
    category:document.getElementById('editCategory').value,
    clientId:clientId||null,
    origin:document.getElementById('editOrigin').value.trim(),
    destination:destination||null,
    desc:document.getElementById('editDesc').value.trim(),
    driverName:resolveDriver('editDriver','editDriverNewVal')||null,
  };
  saveTx(); closeModal('editModal'); renderJournal(); renderTodaySummary();
  toast('✅ שינויים נשמרו');
}

/* ─── REPORT ──────────────────────────────────────────────── */
function initReportSelects() {
  const now=new Date();
  const years=[...new Set([...transactions.map(t=>parseInt(t.date)),now.getFullYear()])].sort((a,b)=>b-a);
  const ys=document.getElementById('reportYear');
  ys.innerHTML=years.map(y=>`<option value="${y}">${y}</option>`).join('');
  document.getElementById('reportMonth').value=now.getMonth()+1;
  ys.value=now.getFullYear();
}
function renderReport() {
  const m=parseInt(document.getElementById('reportMonth').value);
  const y=parseInt(document.getElementById('reportYear').value);
  const filtered=transactions.filter(t=>{ const d=new Date(t.date); return d.getFullYear()===y&&(d.getMonth()+1)===m; });
  const c=document.getElementById('reportContainer');
  if(!filtered.length){c.innerHTML=`<div class="empty-state"><span class="icon">📊</span>אין נתונים לחודש זה.</div>`;return;}

  const transportTx = filtered.filter(t=>!t.txCategory||t.txCategory==='transport');
  const goodsTx     = filtered.filter(t=>t.txCategory==='goods');

  let html='';

  /* ── Transport section ─────────────────────────────────── */
  if(transportTx.length) {
    // Totals
    const tInc=transportTx.filter(t=>t.type==='income').reduce((s,t)=>s+t.amount,0);
    const tExp=transportTx.filter(t=>t.type==='expense').reduce((s,t)=>s+t.amount,0);
    const tPrf=tInc-tExp;
    const tPct=tInc>0?((tPrf/tInc)*100).toFixed(1):'—';

    // Group by resource, sorted by date within each group
    const resOrder=[...resources.map(r=>r.id), '__none__'];
    const byRes={};
    transportTx.forEach(t=>{
      const key=t.resourceId||'__none__';
      if(!byRes[key]) byRes[key]=[];
      byRes[key].push(t);
    });
    // Sort each group by date ascending
    Object.values(byRes).forEach(arr=>arr.sort((a,b)=>a.date.localeCompare(b.date)));

    // Build per-resource blocks
    const resBlocks=resOrder.filter(rid=>byRes[rid]?.length).map(rid=>{
      const txList=byRes[rid];
      const res=rid==='__none__'?null:resourceById(rid);
      const resLabel=res?resourceIcon(res.type)+' '+res.name:'—';
      const rInc=txList.filter(t=>t.type==='income').reduce((s,t)=>s+t.amount,0);
      const rExp=txList.filter(t=>t.type==='expense').reduce((s,t)=>s+t.amount,0);
      const rPrf=rInc-rExp;
      const rows=txList.map(t=>{
        const isInc=t.type==='income';
        const cli=clientById(t.clientId);
        const route=[t.origin,t.destination].filter(Boolean).join(' → ');
        const details=[t.workType,cli?.name,route,!isInc&&t.category?t.category:null,t.desc].filter(Boolean).join(' · ');
        return `<tr>
          <td style="white-space:nowrap;font-size:.85rem">${fmtDate(t.date)}</td>
          <td style="font-size:.85rem">${t.driverName?`<span style="color:var(--txt-sec)">👤 ${t.driverName}</span>`:'—'}</td>
          <td style="font-size:.82rem;color:var(--txt-sec)">${details||'—'}</td>
          <td style="text-align:left"><span class="amount ${t.type}">${isInc?'':'-'}${fmtCurrency(t.amount)}</span></td>
        </tr>`;
      }).join('');
      return `
        <div style="margin-bottom:18px">
          <div style="background:var(--navy-mid);color:rgba(255,255,255,.9);font-weight:800;font-size:.88rem;padding:8px 14px;border-radius:var(--radius) var(--radius) 0 0;display:flex;justify-content:space-between;align-items:center">
            <span>${resLabel}</span>
            <span style="color:${rPrf>=0?'#6EE7A0':'#FCA5A5'};font-size:.82rem">${rPrf>=0?'+':''}${fmtCurrency(rPrf)}</span>
          </div>
          <div class="report-table-wrap" style="margin-top:0;border-radius:0 0 var(--radius) var(--radius);border-top:none">
            <table class="report-table">
              <thead><tr><th>תאריך</th><th>נהג</th><th>פרטים</th><th>סכום</th></tr></thead>
              <tbody>${rows}</tbody>
              <tfoot><tr class="total-row">
                <td colspan="2">סיכום: הכנסות ${fmtCurrency(rInc)} · הוצאות ${fmtCurrency(rExp)}</td>
                <td colspan="2" style="text-align:left"><span class="${rPrf>=0?'profit-pos':'profit-neg'}">${rPrf>=0?'+':''}${fmtCurrency(rPrf)}</span></td>
              </tr></tfoot>
            </table>
          </div>
        </div>`;
    }).join('');

    // Expense category breakdown
    const allCats={};
    transportTx.filter(t=>t.type==='expense').forEach(t=>{const cat=t.category||'אחר'; allCats[cat]=(allCats[cat]||0)+t.amount;});
    const catE=Object.entries(allCats).sort((a,b)=>b[1]-a[1]);
    const maxC=catE.length?catE[0][1]:1;
    const brkHTML=catE.map(([cat,amt])=>`<div class="breakdown-bar-item"><div class="breakdown-bar-label"><span>${cat}</span><span>${fmtCurrency(amt)}</span></div><div class="breakdown-bar-track"><div class="breakdown-bar-fill" style="width:${(amt/maxC*100).toFixed(1)}%"></div></div></div>`).join('');

    html+=`
      <div class="report-cat-divider"><span>🚛 הובלות ומשאיות</span></div>
      <div class="summary-grid">
        <div class="summary-card income-card"><div class="label">הכנסות הובלה</div><div class="value">${fmtCurrency(tInc)}</div></div>
        <div class="summary-card expense-card"><div class="label">הוצאות הובלה</div><div class="value">${fmtCurrency(tExp)}</div></div>
        <div class="summary-card profit-card ${tPrf<0?'negative':''}"><div class="label">רווח הובלות</div><div class="value">${fmtCurrency(tPrf)}<span style="font-size:.75rem;font-weight:600;margin-right:6px">${tPct!=='—'?`(${tPct}%)`:''}  </span></div></div>
      </div>
      ${resBlocks}
      ${catE.length?`<div class="card breakdown-section"><div class="breakdown-title">פירוט הוצאות לפי קטגוריה</div>${brkHTML}</div>`:''}`;
  }

  /* ── Goods section ─────────────────────────────────────── */
  if(goodsTx.length) {
    const gInc=goodsTx.filter(t=>t.type==='income').reduce((s,t)=>s+t.amount,0);
    const gExp=goodsTx.filter(t=>t.type==='expense').reduce((s,t)=>s+t.amount,0);
    const gPrf=gInc-gExp;
    const gPct=gInc>0?((gPrf/gInc)*100).toFixed(1):'—';

    // Pay-status breakdown for income (receivables)
    const payBrk={};
    goodsTx.forEach(t=>{const ps=t.payStatus||'לא ידוע'; payBrk[ps]=(payBrk[ps]||0)+t.amount;});
    const payChips=Object.entries(payBrk).map(([ps,amt])=>`<span class="goods-pay-chip ${PAY_STATUS_CHIP[ps]||'c-pend'}">${payDot(ps)}${ps} ${fmtCurrency(amt)}</span>`).join('');

    // Sales rows
    const gRows=goodsTx.sort((a,b)=>b.date.localeCompare(a.date)).map(t=>{
      const isInc=t.type==='income';
      const docStr=t.docType&&t.docType!=='ללא'?`${t.docType}${t.docNumber?' #'+t.docNumber:''}`:'';
      return `<tr>
        <td style="white-space:nowrap">${fmtDate(t.date)}</td>
        <td><span class="badge ${isInc?'goods-inc':'goods-exp'}">${isInc?'💰 מכירה':'🛒 קנייה'}</span></td>
        <td>${t.goodsParty||'—'}</td>
        <td>${t.goodsDesc||''}</td>
        <td><span class="amount ${isInc?'income':'expense'}">${fmtCurrency(t.amount)}</span></td>
        <td style="font-size:.78rem">${payDot(t.payStatus||'ממתין')}${t.payStatus||''}${docStr?` · ${docStr}`:''}</td>
      </tr>`;
    }).join('');

    html+=`
      <div class="report-cat-divider"><span>📦 סחורה ומסחר</span></div>
      <div class="summary-grid">
        <div class="summary-card income-card"><div class="label">מכירות סחורה</div><div class="value">${fmtCurrency(gInc)}</div></div>
        <div class="summary-card expense-card"><div class="label">קניות סחורה</div><div class="value">${fmtCurrency(gExp)}</div></div>
        <div class="summary-card profit-card ${gPrf<0?'negative':''}"><div class="label">רווח גולמי</div><div class="value">${fmtCurrency(gPrf)}</div></div>
      </div>
      <div class="report-table-wrap">
        <table class="report-table">
          <thead><tr><th>תאריך</th><th>סוג</th><th>לקוח / ספק</th><th>סחורה</th><th>סכום</th><th>תשלום / מסמך</th></tr></thead>
          <tbody>${gRows}</tbody>
          <tfoot><tr class="total-row">
            <td colspan="4">📦 סה"כ סחורה</td>
            <td>${fmtCurrency(gInc-gExp)}</td>
            <td>${gPct!=='—'?`<span class="pct-badge pct-${parseFloat(gPct)>=0?'pos':'neg'}">${gPct}%</span>`:''}</td>
          </tr></tfoot>
        </table>
      </div>
      ${payChips?`<div class="card" style="margin-top:12px"><div class="breakdown-title" style="margin-bottom:10px">סטטוס תשלומים — סחורה</div><div class="goods-pay-row">${payChips}</div></div>`:''}`;
  }

  /* ── Grand total ───────────────────────────────────────── */
  const allInc=filtered.filter(t=>t.type==='income').reduce((s,t)=>s+t.amount,0);
  const allExp=filtered.filter(t=>t.type==='expense').reduce((s,t)=>s+t.amount,0);
  const allPrf=allInc-allExp;

  html+=`
    ${(transportTx.length&&goodsTx.length)?`
    <div class="report-cat-divider"><span>📊 סיכום כולל</span></div>
    <div class="summary-grid">
      <div class="summary-card income-card"><div class="label">סה"כ הכנסות</div><div class="value">${fmtCurrency(allInc)}</div></div>
      <div class="summary-card expense-card"><div class="label">סה"כ הוצאות</div><div class="value">${fmtCurrency(allExp)}</div></div>
      <div class="summary-card profit-card ${allPrf<0?'negative':''}"><div class="label">רווח כולל</div><div class="value">${fmtCurrency(allPrf)}</div></div>
    </div>`:''}
    <button class="btn-export-xl" onclick="exportExcel(${m},${y})">📊 ייצוא ל-Excel — ${MONTHS[m]} ${y}</button>`;

  c.innerHTML=html;
}

/* ─── EXPORT ──────────────────────────────────────────────── */
let _exportHtmlCache = '';
let _exportCsvCache  = '';
let _exportTsvCache  = '';

function exportExcel(m, y) {
  const filtered = transactions.filter(t => {
    const d = new Date(t.date);
    return d.getFullYear() === y && (d.getMonth() + 1) === m;
  });

  const TH = 'background:#0E1C2F;color:rgba(255,255,255,.85);padding:8px 12px;border:1px solid #1C3350;font-weight:700;white-space:nowrap;';
  const TD = 'padding:6px 12px;border:1px solid #D1D9E0;font-size:13px;';
  const TD_INC = TD + 'color:#15803D;font-weight:700;';
  const TD_EXP = TD + 'color:#DC2626;font-weight:700;';
  const TD_SEC = 'background:#1C3350;color:#F5A623;padding:8px 12px;border:1px solid #1C3350;font-weight:800;font-size:14px;';
  const TD_TOT = 'background:#0E1C2F;color:#fff;padding:8px 12px;border:1px solid #1C3350;font-weight:800;font-size:14px;';
  const TD_TOT_POS = TD_TOT + 'color:#6EE7A0;';
  const TD_TOT_NEG = TD_TOT + 'color:#FCA5A5;';

  const transportTx = filtered.filter(t => !t.txCategory || t.txCategory === 'transport');
  const goodsTx     = filtered.filter(t => t.txCategory === 'goods');

  let html = `<table dir="rtl" style="border-collapse:collapse;width:100%;font-family:Arial,sans-serif;font-size:13px;">`;
  let csvRows = ['תאריך,קטגוריה,סוג,משאית/קבלן,עבודה,לקוח/ספק,מוצא,יעד,סחורה,סכום,סטטוס,מסמך,מס׳ מסמך,הערות'];
  const tsv = (cells) => cells.map(v=>String(v).replace(/\t/g,' ')).join('\t');
  let tsvRows = [tsv(['תאריך','קטגוריה','סוג','משאית/קבלן','נהג','עבודה','לקוח/ספק','מוצא','יעד','סחורה','סכום','סטטוס','מסמך','מס׳ מסמך','הערות'])];

  /* ── Transport section ── */
  if (transportTx.length) {
    html += `<tr><td colspan="8" style="${TD_SEC}">🚛 הובלות ומשאיות — ${MONTHS[m]} ${y}</td></tr>`;
    html += `<tr>
      <th style="${TH}">תאריך</th>
      <th style="${TH}">סוג</th>
      <th style="${TH}">משאית/קבלן</th>
      <th style="${TH}">עבודה</th>
      <th style="${TH}">לקוח</th>
      <th style="${TH}">מוצא</th>
      <th style="${TH}">יעד</th>
      <th style="${TH}">סכום ₪</th>
    </tr>`;
    let tInc = 0, tExp = 0;
    transportTx.forEach(t => {
      const res = resourceById(t.resourceId);
      const cli = clientById(t.clientId);
      const isInc = t.type === 'income';
      if (isInc) tInc += t.amount; else tExp += t.amount;
      const bg = isInc ? 'background:#F0FDF4;' : 'background:#FEF2F2;';
      html += `<tr>
        <td style="${TD}${bg}">${t.date}</td>
        <td style="${isInc ? TD_INC : TD_EXP}${bg}">${isInc ? 'הכנסה' : 'הוצאה'}</td>
        <td style="${TD}${bg}">${res ? res.name : ''}</td>
        <td style="${TD}${bg}">${t.workType || ''}</td>
        <td style="${TD}${bg}">${cli ? cli.name : ''}</td>
        <td style="${TD}${bg}">${t.origin || ''}</td>
        <td style="${TD}${bg}">${t.destination || ''}</td>
        <td style="${isInc ? TD_INC : TD_EXP}${bg}">${fmtCurrency(t.amount)}</td>
      </tr>`;
      csvRows.push([t.date,'הובלות',isInc?'הכנסה':'הוצאה',res?res.name:'',t.driverName||'',t.workType||'',cli?cli.name:'',t.origin||'',t.destination||'','',t.amount,'','','',t.desc||''].map(v=>`"${String(v).replace(/"/g,'""')}"`).join(','));
      tsvRows.push(tsv([t.date,'הובלות',isInc?'הכנסה':'הוצאה',res?res.name:'',t.driverName||'',t.workType||'',cli?cli.name:'',t.origin||'',t.destination||'','',t.amount,'','',t.desc||'']));
    });
    const tProfit = tInc - tExp;
    const profStyle = tProfit >= 0 ? TD_TOT_POS : TD_TOT_NEG;
    html += `<tr>
      <td colspan="7" style="${TD_TOT}">סיכום הובלות</td>
      <td style="${profStyle}">${tProfit >= 0 ? '+' : ''}${fmtCurrency(tProfit)}</td>
    </tr>`;
  }

  /* ── Goods section ── */
  if (goodsTx.length) {
    html += `<tr><td colspan="7" style="${TD_SEC}">📦 סחורה ומסחר — ${MONTHS[m]} ${y}</td></tr>`;
    html += `<tr>
      <th style="${TH}">תאריך</th>
      <th style="${TH}">סוג</th>
      <th style="${TH}">לקוח / ספק</th>
      <th style="${TH}">סחורה</th>
      <th style="${TH}">סכום ₪</th>
      <th style="${TH}">תשלום</th>
      <th style="${TH}">מסמך</th>
    </tr>`;
    let gInc = 0, gExp = 0;
    goodsTx.forEach(t => {
      const isInc = t.type === 'income';
      if (isInc) gInc += t.amount; else gExp += t.amount;
      const bg = isInc ? 'background:#F0FDF4;' : 'background:#FEF2F2;';
      const docStr = [t.docType||'', t.docNumber ? `#${t.docNumber}` : ''].filter(Boolean).join(' ');
      html += `<tr>
        <td style="${TD}${bg}">${t.date}</td>
        <td style="${isInc ? TD_INC : TD_EXP}${bg}">${isInc ? 'מכירה' : 'קנייה'}</td>
        <td style="${TD}${bg}">${t.goodsParty || ''}</td>
        <td style="${TD}${bg}">${t.goodsDesc || ''}</td>
        <td style="${isInc ? TD_INC : TD_EXP}${bg}">${fmtCurrency(t.amount)}</td>
        <td style="${TD}${bg}">${t.payStatus || ''}</td>
        <td style="${TD}${bg}">${docStr}</td>
      </tr>`;
      csvRows.push([t.date,'סחורה',isInc?'מכירה':'קנייה','','',t.goodsParty||'','','',t.goodsDesc||'',t.amount,t.payStatus||'',t.docType||'',t.docNumber||'',t.desc||''].map(v=>`"${String(v).replace(/"/g,'""')}"`).join(','));
      tsvRows.push(tsv([t.date,'סחורה',isInc?'מכירה':'קנייה','','','',t.goodsParty||'','','',t.goodsDesc||'',t.amount,t.payStatus||'',t.docType||'',t.docNumber||'',t.desc||'']));
    });
    const gProfit = gInc - gExp;
    const profStyle = gProfit >= 0 ? TD_TOT_POS : TD_TOT_NEG;
    html += `<tr>
      <td colspan="4" style="${TD_TOT}">סיכום סחורה</td>
      <td style="${profStyle}" colspan="3">${gProfit >= 0 ? '+' : ''}${fmtCurrency(gProfit)}</td>
    </tr>`;
  }

  /* ── Grand total ── */
  if (transportTx.length && goodsTx.length) {
    const allInc = filtered.filter(t=>t.type==='income').reduce((s,t)=>s+t.amount,0);
    const allExp = filtered.filter(t=>t.type==='expense').reduce((s,t)=>s+t.amount,0);
    const net = allInc - allExp;
    const profStyle = net >= 0 ? TD_TOT_POS : TD_TOT_NEG;
    html += `<tr>
      <td colspan="7" style="${TD_TOT}">📊 סה"כ — ${MONTHS[m]} ${y}</td>
      <td style="${profStyle}">${net >= 0 ? '+' : ''}${fmtCurrency(net)}</td>
    </tr>`;
  }

  html += `</table>`;

  document.getElementById('excelPreview').innerHTML = html;
  document.getElementById('csvModalTitle').textContent = `${MONTHS[m]} ${y}`;
  document.getElementById('tsvFallbackWrap').style.display = 'none';
  _exportHtmlCache = html;
  _exportCsvCache  = csvRows.join('\n');
  _exportTsvCache  = tsvRows.join('\n');
  document.getElementById('tsvTextarea').value = _exportTsvCache;
  document.getElementById('csvModal').classList.add('open');
}

function copyExcelToClipboard() {
  if (!_exportTsvCache) { toast('⚠️ אין נתונים'); return; }
  const text = _exportTsvCache;

  // Method 1 — hidden textarea + execCommand (works inside iframes)
  const ta = document.createElement('textarea');
  ta.value = text;
  ta.style.cssText = 'position:fixed;top:0;left:0;width:1px;height:1px;opacity:0;';
  document.body.appendChild(ta);
  ta.focus();
  ta.select();
  let ok = false;
  try { ok = document.execCommand('copy'); } catch(e) {}
  document.body.removeChild(ta);

  if (ok) {
    toast('✅ הועתק! פתח Excel והדבק (Ctrl+V)');
    document.getElementById('tsvFallbackWrap').style.display = 'none';
    return;
  }

  // Method 2 — modern clipboard API
  if (navigator.clipboard && navigator.clipboard.writeText) {
    navigator.clipboard.writeText(text)
      .then(() => {
        toast('✅ הועתק! פתח Excel והדבק (Ctrl+V)');
        document.getElementById('tsvFallbackWrap').style.display = 'none';
      })
      .catch(() => showTsvFallback(text));
    return;
  }

  // Method 3 — show textarea
  showTsvFallback(text);
}

function showTsvFallback(text) {
  const wrap = document.getElementById('tsvFallbackWrap');
  const ta   = document.getElementById('tsvTextarea');
  ta.value = text;
  wrap.style.display = '';
  ta.focus(); ta.select();
  toast('⚠️ לחץ Ctrl+A ואז Ctrl+C בתיבה למטה');
}

function selectAllTsv() {
  const ta = document.getElementById('tsvTextarea');
  ta.focus(); ta.select();
  try { document.execCommand('copy'); toast('✅ הועתק!'); } catch(e) {}
}

/* ─── RESOURCES ───────────────────────────────────────────── */
function renderResourcesList() {
  const el=document.getElementById('resourcesList');
  el.innerHTML=resources.length?resources.map(r=>`
    <div class="resource-item">
      <span>${resourceIcon(r.type)}</span>
      <span class="res-name">${r.name}</span>
      <span class="res-type">${resTypeLabel(r.type)}</span>
      <button class="btn-del-small" onclick="deleteResource('${r.id}')">✕</button>
    </div>`).join(''):'<div style="color:var(--txt-muted);font-size:.9rem">אין משאבים.</div>';
}
function addResource() {
  const name=document.getElementById('newResName').value.trim();
  if(!name){toast('⚠️ יש להזין שם');return;}
  resources.push({id:uid(),name,type:document.getElementById('newResType').value});
  saveResources(); renderResourcesList();
  document.getElementById('newResName').value='';
  toast('✅ משאב נוסף');
}
function deleteResource(id) {
  if(transactions.some(t=>t.resourceId===id)&&!confirm('יש עסקאות משויכות. למחוק?')) return;
  resources=resources.filter(r=>r.id!==id);
  saveResources(); renderResourcesList();
  toast('🗑️ משאב הוסר');
}

/* ─── CLIENTS ─────────────────────────────────────────────── */
function renderClientsList() {
  const el=document.getElementById('clientsList');
  if(!clients.length){el.innerHTML='<div style="color:var(--txt-muted);font-size:.9rem">אין לקוחות.</div>';return;}
  el.innerHTML=clients.map(c=>{
    const prRows=(c.prices||[]).map((p,i)=>`<tr>
      <td>${p.destination}</td><td class="price-val">${fmtCurrency(p.price)}</td>
      <td style="text-align:center"><button class="btn-del-price" onclick="deletePrice('${c.id}',${i})">✕</button></td>
    </tr>`).join('');
    const pTable=c.prices&&c.prices.length
      ?`<table class="prices-table"><thead><tr><th>יעד</th><th>מחיר</th><th></th></tr></thead><tbody>${prRows}</tbody></table>`
      :`<p style="font-size:.82rem;color:var(--txt-muted);margin-bottom:10px">אין יעדים.</p>`;
    return `<div class="client-card">
      <div class="client-card-header" onclick="toggleClientCard('${c.id}')">
        <span>👤</span>
        <span class="client-name">${c.name}</span>
        <span class="client-badge">${(c.prices||[]).length} יעדים</span>
        <span class="toggle-icon">▼</span>
      </div>
      <div class="client-card-body" id="cbody-${c.id}">
        ${c.defaultOrigin?`<div class="origin-line">📍 נקודת מוצא: <strong>${c.defaultOrigin}</strong></div>`:''}
        ${pTable}
        <div class="add-price-row">
          <input type="text" id="pDest-${c.id}" placeholder="יעד (עיר)">
          <input type="number" id="pPrice-${c.id}" placeholder="מחיר ₪" min="0">
          <button class="btn-add-price" onclick="addPrice('${c.id}')">+ הוסף</button>
        </div>
        <button class="btn-del-client" onclick="deleteClient('${c.id}')">🗑️ מחק לקוח</button>
      </div>
    </div>`;
  }).join('');
}
function toggleClientCard(id) {
  const body=document.getElementById('cbody-'+id);
  const header=body.previousElementSibling;
  const open=body.classList.toggle('open');
  header.classList.toggle('open',open);
}
function addClient() {
  const name=document.getElementById('newClientName').value.trim();
  if(!name){toast('⚠️ יש להזין שם');return;}
  const origin=document.getElementById('newClientOrigin').value.trim();
  clients.push({id:uid(),name,defaultOrigin:origin,prices:[]});
  saveClients(); populateAll(); renderClientsList();
  document.getElementById('newClientName').value='';
  document.getElementById('newClientOrigin').value='';
  toast('✅ לקוח נוסף');
}
function quickAddClientInline() {
  const row = document.getElementById('quickClientRow');
  row.style.display = row.style.display === 'none' ? '' : 'none';
  if (row.style.display !== 'none') document.getElementById('quickClientName').focus();
}
function confirmQuickClient() {
  const name = document.getElementById('quickClientName').value.trim();
  if (!name) { toast('⚠️ יש להזין שם'); return; }
  const newClient = {id:uid(), name, defaultOrigin:'', prices:[]};
  clients.push(newClient);
  saveClients(); populateAll();
  document.getElementById('incClient').value = newClient.id;
  document.getElementById('quickClientName').value = '';
  document.getElementById('quickClientRow').style.display = 'none';
  handleIncClientChange();
  toast('✅ לקוח נוסף ונבחר');
}
function cancelQuickClient() {
  document.getElementById('quickClientRow').style.display = 'none';
  document.getElementById('quickClientName').value = '';
}
function deleteClient(id) {
  if(!confirm('למחוק לקוח זה?')) return;
  clients=clients.filter(c=>c.id!==id);
  saveClients(); populateAll(); renderClientsList();
  toast('🗑️ לקוח הוסר');
}
function addPrice(clientId) {
  const dest=document.getElementById('pDest-'+clientId).value.trim();
  const price=parseFloat(document.getElementById('pPrice-'+clientId).value);
  if(!dest||isNaN(price)){toast('⚠️ יש למלא יעד ומחיר');return;}
  const c=clientById(clientId); if(!c) return;
  if(!c.prices) c.prices=[];
  c.prices.push({destination:dest,price});
  saveClients(); renderClientsList();
  const body=document.getElementById('cbody-'+clientId);
  if(body){body.classList.add('open');body.previousElementSibling.classList.add('open');}
  toast('✅ יעד נוסף');
}
function deletePrice(clientId,idx) {
  const c=clientById(clientId); if(!c) return;
  c.prices.splice(idx,1); saveClients(); renderClientsList();
  const body=document.getElementById('cbody-'+clientId);
  if(body){body.classList.add('open');body.previousElementSibling.classList.add('open');}
}

/* ─── GOODS — HELPERS ────────────────────────────────────── */
const PAY_STATUS_DOT = {
  'שולם':  's-paid', 'ממתין': 's-pend', 'אשראי': 's-pend', 'בשותף': 's-part'
};
const PAY_STATUS_CHIP = {
  'שולם':  'c-paid', 'ממתין': 'c-pend', 'אשראי': 'c-pend', 'בשותף': 'c-part'
};
function payDot(status) {
  return `<span class="pay-dot ${PAY_STATUS_DOT[status]||'s-pend'}"></span>`;
}
function toggleGoodsDocNum(prefix, val) {
  const el = document.getElementById(prefix + 'DocNumGroup');
  if (el) el.style.display = (val === 'ללא') ? 'none' : '';
}

/* ─── GOODS — PAY TOGGLE ──────────────────────────────────── */
function setGoodsPay(mode, status) {
  const prefix = mode === 'sale' ? 'gsSale' : 'gsBuy';
  document.getElementById(prefix + 'PayVal').value = status;
  const isSale = (mode === 'sale');
  document.querySelectorAll(`#${prefix}PayToggle .pay-btn3`).forEach(btn => {
    const isActive = btn.dataset.v === status;
    btn.classList.remove('active-inc', 'active-exp', 'active-neu');
    if (isActive) {
      if (status === 'שולם')  btn.classList.add(isSale ? 'active-inc' : 'active-inc');
      else if (status === 'בשותף' || status === 'אשראי') btn.classList.add('active-neu');
      else btn.classList.add(isSale ? 'active-exp' : 'active-exp');
    }
  });
}

/* ─── GOODS — OPEN MODALS ─────────────────────────────────── */
function openGoodsSaleModal() {
  document.getElementById('gsSaleDate').value   = today();
  document.getElementById('gsSaleClient').value = '';
  document.getElementById('gsSaleGoods').value  = '';
  document.getElementById('gsSaleAmount').value = '';
  document.getElementById('gsSaleDocType').value= 'חשבונית';
  document.getElementById('gsSaleDocNum').value = '';
  document.getElementById('gsSaleDocNumGroup').style.display = '';
  document.getElementById('gsSaleNote').value   = '';
  setGoodsPay('sale', 'שולם');
  document.getElementById('goodsSaleModal').classList.add('open');
}
function openGoodsBuyModal() {
  document.getElementById('gsBuyDate').value     = today();
  document.getElementById('gsBuySupplier').value = '';
  document.getElementById('gsBuyGoods').value    = '';
  document.getElementById('gsBuyAmount').value   = '';
  document.getElementById('gsBuyDocType').value  = 'חשבונית';
  document.getElementById('gsBuyDocNum').value   = '';
  document.getElementById('gsBuyDocNumGroup').style.display = '';
  document.getElementById('gsBuyNote').value     = '';
  setGoodsPay('buy', 'שולם');
  document.getElementById('goodsBuyModal').classList.add('open');
}

/* ─── GOODS — SAVE ────────────────────────────────────────── */
function handleGoodsSale(e) {
  e.preventDefault();
  const goods  = document.getElementById('gsSaleGoods').value.trim();
  const amount = parseFloat(document.getElementById('gsSaleAmount').value) || 0;
  if (!goods)  { toast('⚠️ יש למלא פרטי סחורה'); return; }
  if (!amount) { toast('⚠️ יש להזין סכום'); return; }
  const docType = document.getElementById('gsSaleDocType').value;
  transactions.unshift({
    id: uid(),
    date:       document.getElementById('gsSaleDate').value,
    resourceId: null,
    type:       'income',
    txCategory: 'goods',
    goodsParty: document.getElementById('gsSaleClient').value.trim(),
    goodsDesc:  goods,
    payStatus:  document.getElementById('gsSalePayVal').value || 'שולם',
    docType,
    docNumber:  docType !== 'ללא' ? document.getElementById('gsSaleDocNum').value.trim() : '',
    amount,
    desc:       document.getElementById('gsSaleNote').value.trim(),
  });
  saveTx(); closeModal('goodsSaleModal'); renderTodaySummary();
  toast(`✅ מכירה נשמרה — ${fmtCurrency(amount)}`);
}
function handleGoodsBuy(e) {
  e.preventDefault();
  const goods  = document.getElementById('gsBuyGoods').value.trim();
  const amount = parseFloat(document.getElementById('gsBuyAmount').value) || 0;
  if (!goods)  { toast('⚠️ יש למלא פרטי סחורה'); return; }
  if (!amount) { toast('⚠️ יש להזין סכום'); return; }
  const docType = document.getElementById('gsBuyDocType').value;
  transactions.unshift({
    id: uid(),
    date:       document.getElementById('gsBuyDate').value,
    resourceId: null,
    type:       'expense',
    txCategory: 'goods',
    goodsParty: document.getElementById('gsBuySupplier').value.trim(),
    goodsDesc:  goods,
    payStatus:  document.getElementById('gsBuyPayVal').value || 'שולם',
    docType,
    docNumber:  docType !== 'ללא' ? document.getElementById('gsBuyDocNum').value.trim() : '',
    amount,
    desc:       document.getElementById('gsBuyNote').value.trim(),
  });
  saveTx(); closeModal('goodsBuyModal'); renderTodaySummary();
  toast(`✅ קנייה נשמרה — ${fmtCurrency(amount)}`);
}

/* ─── GOODS — EDIT ────────────────────────────────────────── */
let editingGoodsId = null;
function openGoodsEdit(id) {
  const tx = transactions.find(t => t.id === id); if (!tx) return;
  editingGoodsId = id;
  document.getElementById('geDate').value    = tx.date;
  document.getElementById('geParty').value   = tx.goodsParty || '';
  document.getElementById('geGoods').value   = tx.goodsDesc  || '';
  document.getElementById('geAmount').value  = tx.amount;
  document.getElementById('gePayStatus').value = tx.payStatus || 'שולם';
  document.getElementById('geDocType').value = tx.docType    || 'חשבונית';
  document.getElementById('geDocNum').value  = tx.docNumber  || '';
  document.getElementById('geNote').value    = tx.desc       || '';
  document.getElementById('geDocNumGroup').style.display = (tx.docType === 'ללא') ? 'none' : '';
  const isInc = tx.type === 'income';
  document.getElementById('geModalTitle').textContent = isInc ? '✏️ עריכת מכירת סחורה' : '✏️ עריכת קנית סחורה';
  document.getElementById('editGoodsModal').classList.add('open');
}
function saveGoodsEdit(e) {
  e.preventDefault();
  const idx = transactions.findIndex(t => t.id === editingGoodsId); if (idx < 0) return;
  const docType = document.getElementById('geDocType').value;
  transactions[idx] = {
    ...transactions[idx],
    date:       document.getElementById('geDate').value,
    goodsParty: document.getElementById('geParty').value.trim(),
    goodsDesc:  document.getElementById('geGoods').value.trim(),
    payStatus:  document.getElementById('gePayStatus').value,
    docType,
    docNumber:  docType !== 'ללא' ? document.getElementById('geDocNum').value.trim() : '',
    amount:     parseFloat(document.getElementById('geAmount').value) || 0,
    desc:       document.getElementById('geNote').value.trim(),
  };
  saveTx(); closeModal('editGoodsModal'); renderJournal(); renderTodaySummary();
  toast('✅ שינויים נשמרו');
}

/* ─── CASH FLOW — BANKS ───────────────────────────────────── */
function openAddBankModal() {
  document.getElementById('bankName').value='';
  document.getElementById('bankBalance').value='';
  document.getElementById('addBankModal').classList.add('open');
}
function addBank() {
  const name=document.getElementById('bankName').value.trim();
  const balance=parseFloat(document.getElementById('bankBalance').value)||0;
  if(!name){toast('⚠️ יש להזין שם בנק');return;}
  banks.push({id:uid(),name,balance,updatedAt:today()});
  saveBanks(); closeModal('addBankModal'); renderCashFlow();
  toast('✅ חשבון נוסף');
}
function openUpdateBankModal(id) {
  const b=banks.find(b=>b.id===id); if(!b) return;
  document.getElementById('updateBankId').value=id;
  document.getElementById('updateBankName').textContent=b.name;
  document.getElementById('updateBankBalance').value=b.balance;
  document.getElementById('updateBankModal').classList.add('open');
}
function confirmUpdateBank() {
  const id=document.getElementById('updateBankId').value;
  const b=banks.find(b=>b.id===id); if(!b) return;
  b.balance=parseFloat(document.getElementById('updateBankBalance').value)||0;
  b.updatedAt=today();
  saveBanks(); closeModal('updateBankModal'); renderCashFlow();
  toast('✅ יתרה עודכנה');
}
function deleteBank(id) {
  if(!confirm('למחוק חשבון זה?')) return;
  banks=banks.filter(b=>b.id!==id);
  saveBanks(); renderCashFlow(); toast('🗑️ חשבון הוסר');
}

/* ─── CASH FLOW — ITEMS (חייבים / הורדות) ────────────────── */
function openAddCashItemModal(type) {
  document.getElementById('cashItemType').value=type;
  document.getElementById('cashItemDesc').value='';
  document.getElementById('cashItemAmount').value='';
  document.getElementById('cashItemDue').value=today();
  document.getElementById('cashItemNote').value='';
  const isRecv=(type==='receivable');
  document.getElementById('cashItemModalTitle').textContent=isRecv?'📥 הוסף חייב':'📤 הוסף הורדה';
  document.getElementById('cashItemModalSub').textContent=isRecv?'כסף שמגיע לך ועדיין לא התקבל':'תשלום / חוב שצריך לשלם';
  document.getElementById('cashItemDescLabel').textContent=isRecv?'שם לקוח / מה החוב':'תיאור ההורדה / ספק';
  document.getElementById('cashItemDesc').placeholder=isRecv?'שם הלקוח...':'שם ספק, סוג תשלום...';
  const btn=document.getElementById('cashItemSaveBtn');
  btn.style.background=isRecv?'var(--amber)':'var(--expense)';
  btn.style.color=isRecv?'var(--navy)':'#fff';
  document.getElementById('addCashItemModal').classList.add('open');
}
function saveCashItem() {
  const type=document.getElementById('cashItemType').value;
  const desc=document.getElementById('cashItemDesc').value.trim();
  const amount=parseFloat(document.getElementById('cashItemAmount').value)||0;
  const dueDate=document.getElementById('cashItemDue').value;
  const note=document.getElementById('cashItemNote').value.trim();
  if(!desc){toast('⚠️ יש להזין תיאור');return;}
  if(!amount){toast('⚠️ יש להזין סכום');return;}
  cashItems.push({id:uid(),type,desc,amount,dueDate,note,paid:false,createdAt:today()});
  saveCashItems(); closeModal('addCashItemModal'); renderCashFlow();
  toast(type==='receivable'?'✅ חייב נוסף':'✅ הורדה נוספה');
}
function toggleCashItemPaid(id) {
  const item=cashItems.find(i=>i.id===id); if(!item) return;
  item.paid=!item.paid;
  saveCashItems(); renderCashFlow();
  toast(item.paid?'✅ סומן כשולם':'↩️ סומן כפתוח');
}
function deleteCashItem(id) {
  if(!confirm('למחוק?')) return;
  cashItems=cashItems.filter(i=>i.id!==id);
  saveCashItems(); renderCashFlow(); toast('🗑️ נמחק');
}

/* ─── RENDER CASH FLOW ────────────────────────────────────── */
function renderCashFlow() {
  renderCfSummary();
  renderBanks();
  renderCfItems('receivable','receivablesContainer');
  renderCfItems('payable','payablesContainer');
}

function renderCfSummary() {
  const totalBank   = banks.reduce((s,b)=>s+b.balance,0);
  const pendingRecv = cashItems.filter(i=>i.type==='receivable'&&!i.paid).reduce((s,i)=>s+i.amount,0);
  const pendingPay  = cashItems.filter(i=>i.type==='payable'&&!i.paid).reduce((s,i)=>s+i.amount,0);
  const net = totalBank + pendingRecv - pendingPay;
  const netColor = net>=0 ? 'var(--income)' : 'var(--expense)';

  // Week label
  const now=new Date();
  const dow=now.getDay();
  const ws=new Date(now); ws.setDate(now.getDate()-dow);
  const we=new Date(ws);  we.setDate(ws.getDate()+6);
  const fmtD=d=>`${d.getDate()}.${d.getMonth()+1}`;

  const overdueRecv=cashItems.filter(i=>i.type==='receivable'&&!i.paid&&i.dueDate&&i.dueDate<today()).length;
  const overduePay =cashItems.filter(i=>i.type==='payable' &&!i.paid&&i.dueDate&&i.dueDate<today()).length;
  const warns=[];
  if(overdueRecv) warns.push(`<span class="overdue-badge">⚠️ ${overdueRecv} חייבים באיחור</span>`);
  if(overduePay)  warns.push(`<span class="overdue-badge">⚠️ ${overduePay} הורדות באיחור</span>`);

  document.getElementById('cfSummaryContainer').innerHTML=`
    <div class="cf-summary-box">
      <div class="cf-sum-title">📊 תזרים שבועי — ${fmtD(ws)} עד ${fmtD(we)}</div>
      <div class="cf-sum-rows">
        <div class="cf-sum-row">
          <span class="cf-sum-label">🏦 יתרת בנקים</span>
          <span class="cf-sum-val">${fmtCurrency(totalBank)}</span>
        </div>
        <div class="cf-sum-row">
          <span class="cf-sum-label">📥 חייבים פתוחים (צפוי להתקבל)</span>
          <span class="cf-sum-val" style="color:var(--income)">+${fmtCurrency(pendingRecv)}</span>
        </div>
        <div class="cf-sum-row">
          <span class="cf-sum-label">📤 הורדות ממתינות</span>
          <span class="cf-sum-val" style="color:var(--expense)">−${fmtCurrency(pendingPay)}</span>
        </div>
        <div class="cf-sum-divider"></div>
        <div class="cf-sum-row total">
          <span class="cf-sum-label">💰 תחזית מזומן נטו</span>
          <span class="cf-sum-val" style="color:${netColor}">${fmtCurrency(net)}</span>
        </div>
      </div>
      ${warns.length?`<div class="cf-warn-strip">${warns.join('')}</div>`:''}
    </div>`;
}

function renderBanks() {
  const c=document.getElementById('banksContainer');
  if(!banks.length){
    c.innerHTML=`<div class="empty-state" style="margin-bottom:0"><span class="icon">🏦</span>הוסף חשבון בנק כדי לעקוב אחר היתרה.</div>`;
    return;
  }
  const total=banks.reduce((s,b)=>s+b.balance,0);
  c.innerHTML=`
    <div class="bank-total-card">
      <div><div class="bt-label">סה"כ בכל הבנקים</div><div class="bt-value">${fmtCurrency(total)}</div></div>
      <span style="font-size:2.2rem">🏦</span>
    </div>
    <div class="banks-grid">
      ${banks.map(b=>`<div class="bank-card">
        <div class="bank-actions">
          <button class="btn-icon" onclick="openUpdateBankModal('${b.id}')" title="עדכן יתרה">✏️</button>
          <button class="btn-icon del" onclick="deleteBank('${b.id}')" title="מחק">🗑️</button>
        </div>
        <div class="bank-name">${b.name}</div>
        <div class="bank-balance">${fmtCurrency(b.balance)}</div>
        <div class="bank-updated">עודכן ${fmtDate(b.updatedAt)}</div>
      </div>`).join('')}
    </div>`;
}

function renderCfItems(type, containerId) {
  const c=document.getElementById(containerId);
  const isRecv=(type==='receivable');
  const items=cashItems.filter(i=>i.type===type).sort((a,b)=>(a.dueDate||'9').localeCompare(b.dueDate||'9'));
  if(!items.length){
    c.innerHTML=`<div class="empty-state" style="margin-bottom:0"><span class="icon">${isRecv?'📥':'📤'}</span>${isRecv?'אין חייבים פתוחים.':'אין הורדות ממתינות.'}</div>`;
    return;
  }
  const t=today();
  const rows=items.map(i=>{
    const overdue=!i.paid&&i.dueDate&&i.dueDate<t;
    const pendingClass=isRecv?'pending-recv':'pending-pay';
    const pendingTxt  =isRecv?'⏳ ממתין לקבלה':'⏳ לא שולם';
    return `<tr class="${i.paid?'paid-row':''}">
      <td style="white-space:nowrap">${i.dueDate?fmtDate(i.dueDate):'—'}${overdue?'<br><span class="overdue-badge">איחור!</span>':''}</td>
      <td>${i.desc}${i.note?`<br><span style="font-size:.77rem;color:var(--txt-muted)">${i.note}</span>`:''}</td>
      <td><span class="amount ${isRecv?'income':'expense'}">${fmtCurrency(i.amount)}</span></td>
      <td><button class="status-badge ${i.paid?'done':pendingClass}" onclick="toggleCashItemPaid('${i.id}')">${i.paid?'✅ הסתיים':pendingTxt}</button></td>
      <td><button class="btn-icon del" onclick="deleteCashItem('${i.id}')">🗑️</button></td>
    </tr>`;
  }).join('');
  c.innerHTML=`<div class="cf-table-wrap"><table class="cf-table">
    <thead><tr><th>מועד</th><th>פרטים</th><th>סכום</th><th>סטטוס</th><th></th></tr></thead>
    <tbody>${rows}</tbody>
  </table></div>`;
}

/* ─── CLOSE ON BACKDROP CLICK ─────────────────────────────── */
document.querySelectorAll('.modal-overlay').forEach(el=>{
  el.addEventListener('click',e=>{if(e.target===el) el.classList.remove('open');});
});

/* ─── TOAST ───────────────────────────────────────────────── */
function toast(msg) {
  const w=document.getElementById('toastWrap');
  const d=document.createElement('div'); d.className='toast'; d.textContent=msg;
  w.appendChild(d); setTimeout(()=>d.remove(),2700);
}

/* ─── LOGIN ───────────────────────────────────────────────── */
const USERS = [
  { user: 'ddhhovalot', pass: '0532379923', role: 'admin',  name: 'דניאל' },
  { user: 'ddhhovalot', pass: 'daniel0500',  role: 'admin',  name: 'מנהלת חשבונות' },
  { user: 'oren',        pass: '4867131',    role: 'driver', name: 'אורן' },
  { user: 'yosef',       pass: '6084857',    role: 'driver', name: 'יוסף' },
  { user: 'driver2',     pass: '6084857',    role: 'driver', name: 'דניאל' },
];
let currentUser = null;

function doLogin() {
  const u = document.getElementById('loginUser').value.trim();
  const p = document.getElementById('loginPass').value;
  const found = USERS.find(x => x.user === u.toLowerCase() && x.pass === p);
  if (found) {
    currentUser = found;
    try { sessionStorage.setItem('ddh_auth', JSON.stringify(found)); } catch(e) {}
    document.getElementById('loginScreen').style.display = 'none';
    if (found.role === 'driver') showDriverView();
  } else {
    document.getElementById('loginErr').textContent = 'שם משתמש או סיסמה שגויים';
    document.getElementById('loginPass').value = '';
    document.getElementById('loginPass').focus();
  }
}
function checkLogin() {
  try {
    const s = sessionStorage.getItem('ddh_auth');
    if (s) {
      currentUser = JSON.parse(s);
      document.getElementById('loginScreen').style.display = 'none';
      if (currentUser.role === 'driver') showDriverView();
      return;
    }
  } catch(e) {}
}
checkLogin();

/* ─── DRIVER VIEW ─────────────────────────────────────────── */
let sigCtx, sigDrawing = false, sigHasContent = false;
let driverPhotoData = null;

let drvDayNight = 'day';
function drvSetDayNight(v) {
  drvDayNight = v;
  document.getElementById('drvBtnDay').className   = 'drv-toggle'+(v==='day'?' active':'');
  document.getElementById('drvBtnNight').className = 'drv-toggle'+(v==='night'?' active':'');
}

function drvNextNoteNum() {
  let notes = []; try { notes = JSON.parse(localStorage.getItem('ddh_notes')||'[]'); } catch {}
  return String(233 + notes.length).padStart(4,'0');
}

function showDriverView() {
  document.getElementById('driverScreen').style.display = 'block';
  document.getElementById('driverNameDisplay').textContent = currentUser ? currentUser.name : '';
  // Note number
  const num = drvNextNoteNum();
  document.getElementById('dnNoteNum').value  = num;
  document.getElementById('drvNoteBadge').textContent = 'מס׳ '+num;
  // Date
  const now = new Date();
  const d = String(now.getDate()).padStart(2,'0');
  const m = String(now.getMonth()+1).padStart(2,'0');
  document.getElementById('dnDate').value = d+'.'+m+'.'+now.getFullYear();
  // Arrival time
  document.getElementById('dnArrival').value = `${String(now.getHours()).padStart(2,'0')}:${String(now.getMinutes()).padStart(2,'0')}`;
  // Driver name
  document.getElementById('dnDriverName').value = currentUser ? currentUser.name : '';
  setTimeout(initSignatureCanvas, 100);
}

function initSignatureCanvas() {
  const canvas = document.getElementById('sigCanvas');
  if (!canvas) return;
  const dpr = window.devicePixelRatio || 1;
  const w = canvas.offsetWidth || 400;
  canvas.width = w * dpr; canvas.height = 110 * dpr;
  canvas.style.width = w+'px'; canvas.style.height = '110px';
  sigCtx = canvas.getContext('2d');
  sigCtx.scale(dpr, dpr);
  sigCtx.strokeStyle = '#14213d';
  sigCtx.lineWidth = 2.4;
  sigCtx.lineCap = 'round';
  sigCtx.lineJoin = 'round';
  const getPos = e => {
    const rect = canvas.getBoundingClientRect();
    const src = e.touches ? e.touches[0] : e;
    return { x: src.clientX - rect.left, y: src.clientY - rect.top };
  };
  const markSig = () => { sigHasContent=true; const o=document.getElementById('sigOverlay'); if(o) o.style.opacity='0'; };
  canvas.addEventListener('mousedown', e => { sigDrawing=true; const p=getPos(e); sigCtx.beginPath(); sigCtx.moveTo(p.x,p.y); });
  canvas.addEventListener('mousemove', e => { if(!sigDrawing) return; const p=getPos(e); sigCtx.lineTo(p.x,p.y); sigCtx.stroke(); markSig(); });
  canvas.addEventListener('mouseup',    () => sigDrawing=false);
  canvas.addEventListener('mouseleave', () => sigDrawing=false);
  canvas.addEventListener('touchstart', e => { e.preventDefault(); sigDrawing=true; const p=getPos(e); sigCtx.beginPath(); sigCtx.moveTo(p.x,p.y); }, {passive:false});
  canvas.addEventListener('touchmove',  e => { e.preventDefault(); if(!sigDrawing) return; const p=getPos(e); sigCtx.lineTo(p.x,p.y); sigCtx.stroke(); markSig(); }, {passive:false});
  canvas.addEventListener('touchend',   () => sigDrawing=false);
}

function clearSignature() {
  if (sigCtx) { const c=document.getElementById('sigCanvas'); sigCtx.clearRect(0,0,c.width,c.height); }
  sigHasContent = false;
  const o=document.getElementById('sigOverlay'); if(o) o.style.opacity='1';
}

function handleDriverPhoto(input) {
  const file = input.files[0]; if (!file) return;
  const reader = new FileReader();
  reader.onload = e => {
    driverPhotoData = e.target.result;
    const p = document.getElementById('dnPhotoPreview');
    p.src = driverPhotoData; p.style.display = 'block';
    const ph = document.getElementById('drvPhotoPlaceholder');
    if (ph) ph.style.display = 'none';
  };
  reader.readAsDataURL(file);
}

function drvPrintNote() {
  const d = {
    num:           document.getElementById('dnNoteNum').value,
    date:          document.getElementById('dnDate').value,
    arriveTime:    document.getElementById('dnArrival').value,
    leaveTime:     document.getElementById('dnDeparture').value,
    custName:      document.getElementById('dnClientName').value,
    custVat:       document.getElementById('dnClientVat').value,
    custPhone:     document.getElementById('dnClientPhone').value,
    ordererName:   document.getElementById('dnOrderer').value,
    driverName:    document.getElementById('dnDriverName').value,
    vehicleNum:    document.getElementById('dnVehicle').value,
    cargoDesc:     document.getElementById('dnItems').value,
    origin1:       document.getElementById('dnOrigin1').value,
    origin2:       document.getElementById('dnOrigin2').value,
    supplierRef:   document.getElementById('dnSupplierRef').value,
    dest1:         document.getElementById('dnDest1').value,
    dest2:         document.getElementById('dnDest2').value,
    craneFrom:     document.getElementById('dnCraneFrom').value,
    craneTo:       document.getElementById('dnCraneTo').value,
    craneTon:      document.getElementById('dnCraneTon').value,
    dayNight:      drvDayNight,
    priceExVat:    document.getElementById('dnPrice').value,
    recipientName: document.getElementById('dnRecipient').value,
    recipientPhone:document.getElementById('dnRecipientPhone').value,
    sig:           sigHasContent ? document.getElementById('sigCanvas').toDataURL() : null,
    photo:         driverPhotoData || null,
  };
  const sigHtml = d.sig ? `<img src="${d.sig}" style="height:55px;display:block;" alt="חתימה">` : '<span style="color:#aaa;font-size:12px">ללא חתימה</span>';
  const photoHtml = d.photo ? `<div style="margin-top:10px"><img src="${d.photo}" style="max-width:220px;max-height:130px;border:1px solid #ccc;border-radius:4px;" alt="תמונה"></div>` : '';
  const html = `<!DOCTYPE html><html dir="rtl" lang="he"><head><meta charset="UTF-8"><title>שטר מטען מס׳ ${d.num}</title>
<style>*{box-sizing:border-box;margin:0;padding:0;}body{font-family:Arial,sans-serif;font-size:13px;color:#111;background:#fff;padding:20px 24px;}
.hdr{display:flex;align-items:flex-start;justify-content:space-between;border-bottom:3px solid #14213d;padding-bottom:12px;margin-bottom:14px;}
.logo{font-size:44px;line-height:1;}.co-name{font-size:19px;font-weight:900;color:#14213d;}.co-tag{font-size:11px;color:#444;line-height:1.7;margin-top:3px;}.co-contact{font-size:11px;color:#14213d;margin-top:4px;font-weight:500;}
.meta{display:flex;align-items:center;justify-content:space-between;background:#14213d;color:#fff;padding:7px 14px;border-radius:6px;margin-bottom:14px;}
.meta-num{font-size:16px;font-weight:900;}.meta-lbl{font-size:10px;opacity:.65;}
.two{display:grid;grid-template-columns:1fr 1fr;gap:14px;margin-bottom:10px;}
.four{display:grid;grid-template-columns:1fr 1fr 70px 70px;gap:10px;margin-bottom:10px;}
.fl{display:flex;flex-direction:column;gap:3px;}.lbl{font-size:10px;font-weight:700;color:#666;letter-spacing:.04em;}.val{border-bottom:1px solid #14213d;padding-bottom:2px;font-size:13px;min-height:20px;color:#1a40a0;font-weight:500;}
.full{margin-bottom:10px;}.fine{background:#f5f7fb;border:1px solid #d0d8ee;border-radius:5px;padding:9px 12px;margin:12px 0;font-size:10.5px;color:#444;line-height:1.8;}
.price{display:flex;align-items:center;justify-content:flex-end;gap:10px;margin:10px 0 14px;padding:8px 14px;border:1.5px solid #14213d;border-radius:6px;background:#f8f9fd;}
.price-lbl{font-size:12px;font-weight:700;color:#14213d;}.price-val{font-size:20px;font-weight:900;color:#14213d;}.price-cur{font-size:13px;font-weight:700;color:#555;}
.sigs{display:grid;grid-template-columns:1fr 1fr 1fr;gap:14px;margin-top:16px;padding-top:12px;border-top:1.5px solid #14213d;}
.sig-b{display:flex;flex-direction:column;align-items:center;gap:6px;text-align:center;}
.sig-line{width:100%;height:55px;border-bottom:1px solid #333;display:flex;align-items:flex-end;justify-content:center;}
.sig-lb{font-size:10px;font-weight:700;color:#555;margin-top:4px;}
.ftr{margin-top:14px;padding-top:8px;border-top:1px solid #dde;text-align:center;font-size:10px;color:#888;}
</style></head><body>
<div class="hdr">
  <div><div class="logo">🚛</div></div>
  <div style="flex:1;text-align:center;">
    <div class="co-name">דניאל דוד הובלות ומסחר</div>
    <div class="co-tag">שירותי מנוף, הובלות קירור, הובלה יבשה<br>יבוא מחו"ל, אחסנה ולוגיסטיקה</div>
    <div class="co-contact">מושב שדה עוזיהו מס׳ 78 &nbsp;|&nbsp; ציון: 053-7780507 &nbsp;|&nbsp; דניאל: 053-2379923 &nbsp;|&nbsp; ע.מ. 207072893</div>
  </div>
  <div style="min-width:60px"></div>
</div>
<div class="meta">
  <div><div class="meta-lbl">שטר מטען מס׳</div><div class="meta-num">${d.num}</div></div>
  <div style="text-align:center"><div class="meta-lbl">תאריך</div><div style="font-size:13px;font-weight:600">${d.date}</div></div>
  <div style="text-align:left"><div class="meta-lbl">שעות</div><div style="font-size:13px;font-weight:600">${d.arriveTime||'--:--'} → ${d.leaveTime||'--:--'}</div></div>
</div>
<div class="two">
  <div class="fl"><span class="lbl">שם הלקוח</span><div class="val">${d.custName}</div></div>
  <div class="fl"><span class="lbl">ע.מ. / ח.פ.</span><div class="val">${d.custVat}</div></div>
</div>
<div class="two">
  <div class="fl"><span class="lbl">שם המזמין</span><div class="val">${d.ordererName}</div></div>
  <div class="fl"><span class="lbl">שם הנהג / מס׳ רכב</span><div class="val">${d.driverName}${d.vehicleNum?' / '+d.vehicleNum:''}</div></div>
</div>
<div class="full" style="margin-top:8px"><span class="lbl">תאור המטען</span><div class="val">${d.cargoDesc}</div></div>
<div class="two"><div class="fl"><span class="lbl">מוצא</span><div class="val">${d.origin1}</div></div><div class="fl"><span class="lbl">מוצא (2)</span><div class="val">${d.origin2}</div></div></div>
<div class="full"><span class="lbl">ת.מ. ספק</span><div class="val">${d.supplierRef}</div></div>
<div class="two"><div class="fl"><span class="lbl">יעד</span><div class="val">${d.dest1}</div></div><div class="fl"><span class="lbl">יעד (2)</span><div class="val">${d.dest2}</div></div></div>
<div class="four" style="margin-top:8px">
  <div class="fl"><span class="lbl">עבודת מנוף משעה</span><div class="val">${d.craneFrom}</div></div>
  <div class="fl"><span class="lbl">עד שעה</span><div class="val">${d.craneTo}</div></div>
  <div class="fl"><span class="lbl">מנוף טון</span><div class="val">${d.craneTon}</div></div>
  <div class="fl"><span class="lbl">יום/לילה</span><div class="val">${d.dayNight==='day'?'יום':'לילה'}</div></div>
</div>
<div class="fine">חיוב שעות מנוף מהגעת המנוף לאתר ועד יציאתו.<br>ביטוח סחורה בהעמסה עד 400,000 להובלה.<br>נזק פיזי ישיר בלבד, השתתפות עצמית ע"ח הלקוח.</div>
<div class="price"><span class="price-lbl">מחיר לא כולל מע"מ:</span><span class="price-val">${d.priceExVat?Number(d.priceExVat).toLocaleString('he-IL'):'______'}</span><span class="price-cur">ש"ח</span></div>
<div class="sigs">
  <div class="sig-b"><div class="sig-line">${sigHtml}</div><div class="sig-lb">חתימת המקבל</div></div>
  <div class="sig-b"><div class="sig-line"><span style="font-size:13px;padding-bottom:4px">${d.recipientPhone}</span></div><div class="sig-lb">טלפון / נייד</div></div>
  <div class="sig-b"><div class="sig-line"><span style="font-size:13px;padding-bottom:4px">${d.recipientName}</span></div><div class="sig-lb">שם המקבל</div></div>
</div>
${photoHtml}
<div class="ftr">מסמך זה הופק אוטומטית — דניאל דוד הובלות ומסחר &nbsp;·&nbsp; ${new Date().toLocaleString('he-IL')}</div>
<script>window.onload=()=>window.print();<\/script>
</body></html>`;
  const w = window.open('','_blank','width=800,height=900');
  w.document.write(html); w.document.close();
}

async function submitDeliveryNote() {
  const clientName = document.getElementById('dnClientName').value.trim();
  if (!clientName) { alert('חובה להכניס שם לקוח'); return; }
  const note = {
    id: uid(),
    num:           document.getElementById('dnNoteNum').value,
    date:          document.getElementById('dnDate').value,
    driverName:    document.getElementById('dnDriverName').value,
    clientName,
    clientVat:     document.getElementById('dnClientVat').value.trim(),
    clientPhone:   document.getElementById('dnClientPhone').value.trim(),
    orderer:       document.getElementById('dnOrderer').value.trim(),
    vehicleNum:    document.getElementById('dnVehicle').value.trim(),
    cargoDesc:     document.getElementById('dnItems').value.trim(),
    origin1:       document.getElementById('dnOrigin1').value.trim(),
    origin2:       document.getElementById('dnOrigin2').value.trim(),
    supplierRef:   document.getElementById('dnSupplierRef').value.trim(),
    dest1:         document.getElementById('dnDest1').value.trim(),
    dest2:         document.getElementById('dnDest2').value.trim(),
    arrivalTime:   document.getElementById('dnArrival').value,
    departureTime: document.getElementById('dnDeparture').value,
    craneFrom:     document.getElementById('dnCraneFrom').value,
    craneTo:       document.getElementById('dnCraneTo').value,
    craneTon:      document.getElementById('dnCraneTon').value,
    dayNight:      drvDayNight,
    priceExVat:    document.getElementById('dnPrice').value,
    recipientName: document.getElementById('dnRecipient').value.trim(),
    recipientPhone:document.getElementById('dnRecipientPhone').value.trim(),
    photo:         driverPhotoData || null,
    signature:     sigHasContent ? document.getElementById('sigCanvas').toDataURL('image/png') : null,
    createdAt:     Date.now()
  };
  let notes = []; try { notes = JSON.parse(localStorage.getItem('ddh_notes')||'[]'); } catch {}
  notes.unshift(note);
  try { localStorage.setItem('ddh_notes', JSON.stringify(notes)); } catch {}
  DB.set('ddh_notes', notes);
  document.getElementById('driverFormView').style.display = 'none';
  document.getElementById('driverSuccessView').style.display = 'block';
}

function startNewDeliveryNote() {
  document.getElementById('driverFormView').style.display = 'block';
  document.getElementById('driverSuccessView').style.display = 'none';
  ['dnClientName','dnClientVat','dnClientPhone','dnOrderer','dnVehicle','dnItems',
   'dnOrigin1','dnOrigin2','dnSupplierRef','dnDest1','dnDest2',
   'dnCraneFrom','dnCraneTo','dnCraneTon','dnPrice','dnRecipient','dnRecipientPhone'].forEach(id => {
    const el = document.getElementById(id); if(el) el.value='';
  });
  document.getElementById('dnPhoto').value='';
  document.getElementById('dnPhotoPreview').style.display='none';
  const ph=document.getElementById('drvPhotoPlaceholder'); if(ph) ph.style.display='flex';
  driverPhotoData = null;
  drvDayNight = 'day';
  drvSetDayNight('day');
  clearSignature();
  const now = new Date();
  const num = drvNextNoteNum();
  document.getElementById('dnNoteNum').value = num;
  document.getElementById('drvNoteBadge').textContent = 'מס׳ '+num;
  document.getElementById('dnArrival').value = `${String(now.getHours()).padStart(2,'0')}:${String(now.getMinutes()).padStart(2,'0')}`;
  document.getElementById('dnDeparture').value = '';
}

/* ─── DELIVERY NOTES (management view) ───────────────────── */
function renderDeliveryNotes() {
  let notes = []; try { notes = JSON.parse(localStorage.getItem('ddh_notes')||'[]'); } catch {}
  const cont = document.getElementById('notesContainer');
  if (!notes.length) { cont.innerHTML='<p style="color:var(--txt-muted);text-align:center;padding:40px 0">אין תעודות עדיין</p>'; return; }
  cont.innerHTML = notes.map((n,i) => `
    <div class="dn-card">
      <div class="dn-card-head">
        <div style="flex:1">
          <div class="dn-driver">🚛 ${n.driverName||'נהג'}</div>
          <div class="dn-date">${n.date}  ${n.arrivalTime||''} – ${n.departureTime||''}</div>
        </div>
        <button onclick="printDeliveryNote('${n.id}')" style="background:var(--amber);color:var(--navy);padding:6px 14px;border-radius:8px;font-weight:700;font-size:.82rem">🖨️ הדפס</button>
      </div>
      <div class="dn-card-body">
        <div><strong>לקוח:</strong> ${n.clientName}</div>
        ${n.fromAddress?`<div><strong>מ:</strong> ${n.fromAddress}</div>`:''}
        ${n.toAddress?`<div><strong>ל:</strong> ${n.toAddress}</div>`:''}
        ${n.items?`<div><strong>סחורה:</strong> ${n.items}</div>`:''}
        ${n.notes?`<div><strong>הערות:</strong> ${n.notes}</div>`:''}
        ${n.signature?`<div style="margin-top:8px"><strong>חתימה:</strong><br><img class="dn-sig-img" src="${n.signature}"></div>`:''}
        ${n.photo?`<div style="margin-top:8px"><strong>תמונה:</strong><br><img class="dn-photo-img" src="${n.photo}"></div>`:''}
      </div>
    </div>
  `).join('');
}

/* ─── INIT ────────────────────────────────────────────────── */
(async function(){
  // 1. Load from localStorage instantly
  loadFromLocalStorage();

  // 2. Render immediately (no waiting)
  initReportSelects();
  populateAll();
  renderTodaySummary();

  // 3. Try to connect to Google Sheets
  if (GS_URL()) {
    setSyncStatus('loading');
    const hadData = await syncFromSheets();
    if (hadData) { populateAll(); refreshCurrentTab(); }
    else {
      // Sheets empty — first-time push
      saveTx(); saveResources(); saveClients(); saveBanks(); saveCashItems(); saveDrivers();
    }
    // Auto-refresh every 60 seconds
    setInterval(async () => {
      const changed = await syncFromSheets();
      if (changed) { populateAll(); refreshCurrentTab(); }
    }, 60000);
  } else {
    setSyncStatus('offline');
  }
})();
</script>
</body>
</html>
