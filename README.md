[index (3).html](https://github.com/user-attachments/files/26293197/index.3.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta http-equiv="X-UA-Compatible" content="chrome=1">
<meta name="HandheldFriendly" content="True">
<meta name="MobileOptimized" content="width">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
<meta name="mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="apple-mobile-web-app-title" content="Japan-Dash">
<meta name="application-name" content="Japan-Dash">
<meta name="theme-color" content="#0a0a0f">
<meta name="description" content="Japan trip planner — itinerary, budget, packing, phrases, JR Pass">
<title>Japan-Dash 🗾</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=DM+Mono:ital,wght@0,300;0,400;0,500;1,400&family=Syne:wght@400;500;600;700;800&display=swap" rel="stylesheet">

<script>
// ── Open in Chrome on iOS ─────────────────────────────────────
(function() {
  var ua = navigator.userAgent;
  var isIOS = /iP(hone|ad|od)/.test(ua);
  var isChrome = /CriOS/.test(ua) || /Chrome/.test(ua);
  if (isIOS && !isChrome) {
    var url = window.location.href;
    var chromeUrl = url.replace(/^https?:\/\//, function(m) {
      return m === 'https://' ? 'googlechromes://' : 'googlechrome://';
    });
    var banner = document.createElement('div');
    banner.style.cssText = 'position:fixed;top:0;left:0;right:0;z-index:999999;background:#e8354a;color:#fff;font-family:sans-serif;padding:14px 16px;display:flex;align-items:center;gap:12px;box-shadow:0 2px 8px rgba(0,0,0,.3)';
    banner.innerHTML = '<span style="flex:1;font-size:14px;font-weight:600">Japan-Dash works best in Chrome</span>'
      + '<a href="' + chromeUrl + '" style="background:#fff;color:#e8354a;padding:7px 14px;border-radius:6px;font-size:13px;font-weight:700;text-decoration:none;white-space:nowrap">Open in Chrome</a>'
      + '<button onclick="this.parentNode.remove()" style="background:none;border:none;color:#fff;font-size:20px;cursor:pointer;padding:0 4px;line-height:1">×</button>';
    if (document.body) document.body.insertBefore(banner, document.body.firstChild);
    else document.addEventListener('DOMContentLoaded', function() { document.body.insertBefore(banner, document.body.firstChild); });
    try { window.location.href = chromeUrl; } catch(e) {}
  }
})();
</script>

<style>
:root {
  --bg: #0a0a0f;
  --bg2: #111118;
  --bg3: #18181f;
  --bg4: #1f1f28;
  --border: rgba(255,255,255,0.07);
  --border2: rgba(255,255,255,0.13);
  --text: #e8e8f0;
  --text2: #8888a0;
  --text3: #4a4a60;
  --accent: #e8354a;
  --accent2: #c01e31;
  --gold: #f0c040;
  --gold-dim: rgba(240,192,64,0.12);
  --green: #2ecc8a;
  --green-dim: rgba(46,204,138,0.12);
  --red: #ff5566;
  --red-dim: rgba(255,85,102,0.12);
  --amber: #ffb830;
  --amber-dim: rgba(255,184,48,0.12);
  --blue: #4da6ff;
  --blue-dim: rgba(77,166,255,0.1);
  --sakura: #ffb7c5;
  --sakura-dim: rgba(255,183,197,0.1);
  --mono: 'DM Mono', monospace;
  --display: 'Syne', sans-serif;
  --radius: 12px;
  --radius-sm: 8px;
  --safe-bottom: env(safe-area-inset-bottom, 0px);
}

* { margin: 0; padding: 0; box-sizing: border-box; }

body {
  background: var(--bg);
  color: var(--text);
  font-family: var(--mono);
  font-size: 13px;
  min-height: 100vh;
  overflow-x: hidden;
}

/* ── SUBTLE GRID BACKGROUND ── */
body::before {
  content: '';
  position: fixed;
  inset: 0;
  background-image:
    linear-gradient(rgba(232,53,74,0.025) 1px, transparent 1px),
    linear-gradient(90deg, rgba(232,53,74,0.025) 1px, transparent 1px);
  background-size: 40px 40px;
  pointer-events: none;
  z-index: 0;
}

/* ── LAYOUT ── */
.shell { display: flex; min-height: 100vh; position: relative; z-index: 1; }

/* ── SIDEBAR ── */
.sidebar {
  width: 220px;
  flex-shrink: 0;
  background: var(--bg2);
  border-right: 1px solid var(--border);
  display: flex;
  flex-direction: column;
  position: sticky;
  top: 0;
  height: 100vh;
  overflow-y: auto;
}

.logo {
  padding: 24px 20px 20px;
  border-bottom: 1px solid var(--border);
}
.logo-mark {
  font-family: var(--display);
  font-size: 18px;
  font-weight: 800;
  color: var(--text);
  letter-spacing: -0.5px;
}
.logo-mark span { color: var(--accent); }
.logo-sub { font-size: 10px; color: var(--text3); letter-spacing: 0.08em; text-transform: uppercase; margin-top: 2px; }

.nav { padding: 16px 12px; flex: 1; }
.nav-section { margin-bottom: 24px; }
.nav-section-label {
  font-size: 9px;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--text3);
  padding: 0 8px;
  margin-bottom: 6px;
}

.nav-item {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 8px 10px;
  border-radius: var(--radius-sm);
  cursor: pointer;
  color: var(--text2);
  font-size: 12px;
  transition: all 0.15s;
  border: 1px solid transparent;
  position: relative;
  text-decoration: none;
}
.nav-item:hover { background: var(--bg3); color: var(--text); }
.nav-item.active {
  background: rgba(232,53,74,0.12);
  color: var(--accent);
  border-color: rgba(232,53,74,0.2);
}
.nav-item.active::before {
  content: '';
  position: absolute;
  left: -1px; top: 20%; bottom: 20%;
  width: 3px;
  background: var(--accent);
  border-radius: 0 3px 3px 0;
}
.nav-icon { width: 16px; text-align: center; font-size: 14px; flex-shrink: 0; }
.nav-badge {
  margin-left: auto;
  background: var(--bg4);
  color: var(--text3);
  font-size: 9px;
  padding: 2px 6px;
  border-radius: 99px;
}
.nav-item.active .nav-badge {
  background: rgba(232,53,74,0.2);
  color: var(--accent);
}

.sidebar-footer {
  padding: 16px;
  border-top: 1px solid var(--border);
}
.trip-mini {
  background: var(--bg3);
  border: 1px solid var(--border);
  border-radius: var(--radius-sm);
  padding: 12px;
}
.tm-label { font-size: 9px; text-transform: uppercase; letter-spacing: 0.1em; color: var(--text3); margin-bottom: 4px; }
.tm-value { font-family: var(--display); font-size: 18px; font-weight: 700; color: var(--text); }
.tm-sub { font-size: 11px; color: var(--amber); margin-top: 2px; }

/* ── MAIN ── */
.main { flex: 1; overflow-y: auto; }

.page { display: none; padding: 32px; padding-bottom: 32px; }
.page.active { display: block; }

.page-header {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  margin-bottom: 28px;
}
.page-title {
  font-family: var(--display);
  font-size: 26px;
  font-weight: 700;
  letter-spacing: -0.5px;
  color: var(--text);
}
.page-title span { color: var(--accent); }
.page-subtitle { font-size: 12px; color: var(--text2); margin-top: 4px; }

/* ── BUTTONS ── */
.btn {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  padding: 8px 14px;
  border-radius: var(--radius-sm);
  font-family: var(--mono);
  font-size: 12px;
  cursor: pointer;
  transition: all 0.15s;
  border: 1px solid transparent;
  font-weight: 400;
}
.btn-primary { background: var(--accent); color: #fff; border-color: var(--accent); }
.btn-primary:hover { background: var(--accent2); }
.btn-secondary { background: var(--bg3); color: var(--text2); border-color: var(--border2); }
.btn-secondary:hover { color: var(--text); background: var(--bg4); }
.btn-ghost { background: transparent; color: var(--text2); }
.btn-ghost:hover { color: var(--text); background: var(--bg3); }
.btn-danger { background: var(--red-dim); color: var(--red); border-color: rgba(255,85,102,0.2); }
.btn-danger:hover { background: rgba(255,85,102,0.2); }
.btn-sm { padding: 5px 10px; font-size: 11px; }

/* ── KPI CARDS ── */
.kpi-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(150px, 1fr)); gap: 12px; margin-bottom: 24px; }
.kpi-card {
  background: var(--bg2);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 16px;
  position: relative;
  overflow: hidden;
  transition: border-color 0.2s;
}
.kpi-card:hover { border-color: var(--border2); }
.kpi-card::after {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 2px;
  background: var(--accent-color, var(--accent));
  opacity: 0.7;
}
.kpi-label { font-size: 9px; text-transform: uppercase; letter-spacing: 0.1em; color: var(--text3); margin-bottom: 8px; }
.kpi-value { font-family: var(--display); font-size: 22px; font-weight: 700; color: var(--text); }
.kpi-sub { font-size: 11px; margin-top: 4px; }
.kpi-sub.pos { color: var(--green); }
.kpi-sub.neg { color: var(--red); }
.kpi-sub.muted { color: var(--text3); }
.kpi-sub.amber { color: var(--amber); }
.kpi-sub.sakura { color: var(--sakura); }

/* ── SECTION PANELS ── */
.section-panel {
  background: var(--bg2);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  margin-bottom: 20px;
  overflow: hidden;
}
.section-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 16px 20px;
  border-bottom: 1px solid var(--border);
  background: var(--bg3);
}
.section-title {
  font-family: var(--display);
  font-size: 14px;
  font-weight: 600;
  color: var(--text);
  display: flex;
  align-items: center;
  gap: 8px;
}
.section-title .badge {
  font-family: var(--mono);
  font-size: 10px;
  font-weight: 400;
  background: var(--bg4);
  color: var(--text2);
  padding: 2px 8px;
  border-radius: 99px;
  border: 1px solid var(--border);
}

/* ── TABLE ── */
.data-table { width: 100%; border-collapse: collapse; }
.data-table th {
  font-size: 9px;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: var(--text3);
  padding: 10px 16px;
  text-align: left;
  border-bottom: 1px solid var(--border);
  font-weight: 400;
  background: var(--bg3);
}
.data-table th.right { text-align: right; }
.data-table td {
  padding: 12px 16px;
  border-bottom: 1px solid var(--border);
  vertical-align: middle;
}
.data-table tr:last-child td { border-bottom: none; }
.data-table tr:hover td { background: rgba(255,255,255,0.02); }
.data-table td.right { text-align: right; }
.data-table td.mono { font-family: var(--mono); }

/* ── TAGS ── */
.tag {
  display: inline-flex;
  align-items: center;
  gap: 4px;
  padding: 2px 8px;
  border-radius: 99px;
  font-size: 10px;
  border: 1px solid transparent;
}
.tag-green { background: var(--green-dim); color: var(--green); border-color: rgba(46,204,138,0.2); }
.tag-red { background: var(--red-dim); color: var(--red); border-color: rgba(255,85,102,0.2); }
.tag-amber { background: var(--amber-dim); color: var(--amber); border-color: rgba(255,184,48,0.2); }
.tag-blue { background: var(--blue-dim); color: var(--blue); border-color: rgba(77,166,255,0.2); }
.tag-sakura { background: var(--sakura-dim); color: var(--sakura); border-color: rgba(255,183,197,0.2); }
.tag-gold { background: var(--gold-dim); color: var(--gold); border-color: rgba(240,192,64,0.2); }
.tag-muted { background: var(--bg4); color: var(--text3); border-color: var(--border); }

.val-pos { color: var(--green); }
.val-neg { color: var(--red); }
.val-muted { color: var(--text2); }
.val-amber { color: var(--amber); }

/* ── EMPTY STATE ── */
.empty-state { padding: 40px; text-align: center; }
.es-icon { font-size: 28px; margin-bottom: 12px; }
.es-title { font-family: var(--display); font-size: 14px; font-weight: 600; color: var(--text2); margin-bottom: 6px; }
.es-sub { font-size: 12px; color: var(--text3); }

/* ── FORM ELEMENTS ── */
.form-group { margin-bottom: 16px; }
.form-label { font-size: 10px; text-transform: uppercase; letter-spacing: 0.08em; color: var(--text3); margin-bottom: 6px; display: block; }
.form-input {
  width: 100%;
  background: var(--bg3);
  border: 1px solid var(--border2);
  border-radius: var(--radius-sm);
  color: var(--text);
  font-family: var(--mono);
  font-size: 13px;
  padding: 8px 12px;
  outline: none;
  transition: border-color 0.15s;
}
.form-input:focus { border-color: var(--accent); }
.form-input::placeholder { color: var(--text3); }
select.form-input { cursor: pointer; }
.form-row-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
.form-row-3 { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 12px; }

/* ── MODAL ── */
.modal-overlay {
  display: none;
  position: fixed; inset: 0; z-index: 9000;
  background: rgba(0,0,0,0.7);
  backdrop-filter: blur(4px);
  align-items: center;
  justify-content: center;
}
.modal-overlay.open { display: flex; }
.modal {
  background: var(--bg2);
  border: 1px solid var(--border2);
  border-radius: 16px;
  padding: 28px;
  width: 480px;
  max-width: 95vw;
  max-height: 90vh;
  overflow-y: auto;
  box-shadow: 0 40px 80px rgba(0,0,0,0.7);
}
.modal-title {
  font-family: var(--display);
  font-size: 18px;
  font-weight: 700;
  color: var(--text);
  margin-bottom: 20px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.modal-close {
  background: none;
  border: none;
  color: var(--text3);
  font-size: 20px;
  cursor: pointer;
  padding: 0 4px;
  line-height: 1;
  transition: color 0.15s;
}
.modal-close:hover { color: var(--text); }
.modal-footer { display: flex; gap: 8px; justify-content: flex-end; margin-top: 20px; padding-top: 16px; border-top: 1px solid var(--border); }

/* ── TOAST ── */
#toast-container { position: fixed; bottom: 88px; right: 20px; z-index: 99999; display: flex; flex-direction: column; gap: 8px; pointer-events: none; }
.toast {
  background: var(--bg3);
  border: 1px solid var(--border2);
  border-radius: 10px;
  padding: 10px 16px;
  font-size: 12px;
  color: var(--text);
  box-shadow: 0 8px 24px rgba(0,0,0,0.5);
  animation: toastIn 0.25s ease-out, toastOut 0.25s ease-in 2.75s forwards;
  max-width: 280px;
}
.toast.success { border-left: 3px solid var(--green); }
.toast.error { border-left: 3px solid var(--red); }
.toast.info { border-left: 3px solid var(--blue); }
@keyframes toastIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
@keyframes toastOut { from { opacity: 1; } to { opacity: 0; transform: translateY(-4px); } }

/* ── ITINERARY ── */
.day-card {
  background: var(--bg2);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  margin-bottom: 14px;
  overflow: hidden;
  transition: border-color 0.2s;
}
.day-card:hover { border-color: var(--border2); }
.day-header {
  display: flex;
  align-items: center;
  gap: 14px;
  padding: 14px 18px;
  background: var(--bg3);
  border-bottom: 1px solid var(--border);
  cursor: pointer;
}
.day-num {
  font-family: var(--display);
  font-size: 11px;
  font-weight: 700;
  width: 28px;
  height: 28px;
  border-radius: 7px;
  background: rgba(232,53,74,0.15);
  color: var(--accent);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}
.day-title { font-family: var(--display); font-size: 14px; font-weight: 600; color: var(--text); flex: 1; }
.day-city { font-size: 10px; color: var(--text3); letter-spacing: 0.06em; text-transform: uppercase; }
.day-date { font-size: 11px; color: var(--text2); font-family: var(--mono); }
.day-body { padding: 4px 0; }

.event-row {
  display: flex;
  align-items: flex-start;
  gap: 12px;
  padding: 10px 18px;
  border-bottom: 1px solid var(--border);
  transition: background 0.15s;
}
.event-row:last-child { border-bottom: none; }
.event-row:hover { background: rgba(255,255,255,0.02); }
.event-time { font-family: var(--mono); font-size: 10px; color: var(--text3); width: 44px; flex-shrink: 0; padding-top: 2px; }
.event-icon { font-size: 14px; flex-shrink: 0; width: 22px; text-align: center; }
.event-info { flex: 1; }
.event-name { font-size: 13px; color: var(--text); margin-bottom: 2px; }
.event-note { font-size: 11px; color: var(--text3); }
.event-cost { font-family: var(--mono); font-size: 12px; color: var(--text2); flex-shrink: 0; }
.event-done { width: 20px; height: 20px; border-radius: 5px; border: 2px solid var(--border2); flex-shrink: 0; cursor: pointer; display: flex; align-items: center; justify-content: center; font-size: 10px; transition: all 0.15s; }
.event-done:hover { border-color: var(--green); }
.event-done.checked { background: var(--green); border-color: var(--green); color: #fff; }

/* ── BUDGET ── */
.budget-bar { height: 8px; background: var(--bg4); border-radius: 99px; overflow: hidden; margin: 6px 0; }
.budget-fill { height: 100%; border-radius: 99px; transition: width 0.5s ease; }
.budget-row {
  display: flex;
  align-items: center;
  gap: 14px;
  padding: 13px 20px;
  border-bottom: 1px solid var(--border);
  transition: background 0.15s;
}
.budget-row:last-child { border-bottom: none; }
.budget-row:hover { background: rgba(255,255,255,0.02); }
.budget-cat { flex: 1; }
.budget-cat-name { font-size: 13px; color: var(--text); margin-bottom: 2px; }
.budget-cat-sub { font-size: 11px; color: var(--text3); }
.budget-amounts { text-align: right; flex-shrink: 0; }
.budget-spent { font-family: var(--mono); font-size: 13px; color: var(--text); }
.budget-limit { font-size: 11px; color: var(--text3); }

/* ── PACKING LIST ── */
.pack-category { margin-bottom: 4px; }
.pack-cat-header { display: flex; align-items: center; justify-content: space-between; padding: 10px 20px; border-bottom: 1px solid var(--border); background: var(--bg3); cursor: pointer; }
.pack-cat-name { font-family: var(--display); font-size: 13px; font-weight: 600; color: var(--text); display: flex; align-items: center; gap: 8px; }
.pack-cat-prog { font-size: 11px; color: var(--text2); font-family: var(--mono); }
.pack-item-row { display: flex; align-items: center; gap: 12px; padding: 9px 20px; border-bottom: 1px solid var(--border); transition: background 0.15s; }
.pack-item-row:last-child { border-bottom: none; }
.pack-item-row:hover { background: rgba(255,255,255,0.02); }
.pack-check { width: 20px; height: 20px; border-radius: 5px; border: 2px solid var(--border2); flex-shrink: 0; cursor: pointer; display: flex; align-items: center; justify-content: center; font-size: 10px; transition: all 0.15s; }
.pack-check:hover { border-color: var(--accent); }
.pack-check.packed { background: var(--accent); border-color: var(--accent); color: #fff; }
.pack-item-name { flex: 1; font-size: 13px; color: var(--text); }
.pack-item-name.done { text-decoration: line-through; color: var(--text3); }
.pack-item-note { font-size: 11px; color: var(--text3); }
.pack-priority { font-size: 10px; padding: 1px 6px; border-radius: 99px; flex-shrink: 0; }
@keyframes packPop { 0%{transform:scale(1)} 40%{transform:scale(1.3)} 100%{transform:scale(1)} }
.pack-pop { animation: packPop 0.2s ease-out; }

/* ── PHRASES ── */
.phrase-row { display: flex; align-items: flex-start; gap: 14px; padding: 14px 20px; border-bottom: 1px solid var(--border); transition: background 0.15s; }
.phrase-row:last-child { border-bottom: none; }
.phrase-row:hover { background: rgba(255,255,255,0.02); }
.phrase-jp { font-size: 18px; color: var(--text); line-height: 1.3; flex: 1; }
.phrase-romaji { font-size: 11px; color: var(--accent); font-family: var(--mono); margin-top: 2px; }
.phrase-en { font-size: 12px; color: var(--text2); margin-top: 4px; }
.phrase-copy { background: none; border: 1px solid var(--border2); border-radius: 6px; color: var(--text3); font-size: 10px; padding: 4px 8px; cursor: pointer; transition: all 0.15s; flex-shrink: 0; margin-top: 4px; font-family: var(--mono); }
.phrase-copy:hover { border-color: var(--accent); color: var(--accent); }
.phrase-cat-header { padding: 8px 20px; background: var(--bg3); border-bottom: 1px solid var(--border); font-size: 9px; text-transform: uppercase; letter-spacing: 0.12em; color: var(--text3); }

/* ── CHECKLIST ── */
.check-row {
  display: flex;
  align-items: flex-start;
  gap: 12px;
  padding: 12px 20px;
  border-bottom: 1px solid var(--border);
  transition: background 0.15s;
}
.check-row:last-child { border-bottom: none; }
.check-row:hover { background: rgba(255,255,255,0.02); }
.check-box { width: 22px; height: 22px; border-radius: 6px; border: 2px solid var(--border2); flex-shrink: 0; cursor: pointer; display: flex; align-items: center; justify-content: center; font-size: 12px; transition: all 0.15s; margin-top: 1px; }
.check-box:hover { border-color: var(--green); }
.check-box.done { background: var(--green); border-color: var(--green); color: #fff; }
.check-info { flex: 1; }
.check-title { font-size: 13px; color: var(--text); }
.check-title.done { text-decoration: line-through; color: var(--text3); }
.check-note { font-size: 11px; color: var(--text3); margin-top: 2px; }

/* ── JR PASS / RAIL ── */
.rail-route { display: flex; align-items: center; gap: 12px; padding: 14px 20px; border-bottom: 1px solid var(--border); }
.rail-route:last-child { border-bottom: none; }
.rail-from-to { flex: 1; }
.rail-cities { font-size: 13px; color: var(--text); }
.rail-train { font-size: 11px; color: var(--text3); margin-top: 2px; }
.rail-duration { font-family: var(--mono); font-size: 12px; color: var(--text2); width: 55px; text-align: center; }
.rail-cost { font-family: var(--mono); font-size: 13px; color: var(--text); width: 80px; text-align: right; }
.rail-covered { font-size: 10px; padding: 2px 7px; border-radius: 99px; flex-shrink: 0; }

/* ── DASHBOARD TICKER ── */
.dash-ticker { display: flex; gap: 32px; padding: 12px 20px; border-bottom: 1px solid var(--border); overflow-x: auto; background: var(--bg3); }
.ticker-item { display: flex; flex-direction: column; gap: 2px; flex-shrink: 0; }
.ticker-label { font-size: 9px; text-transform: uppercase; letter-spacing: 0.1em; color: var(--text3); }
.ticker-val { font-family: var(--display); font-size: 16px; font-weight: 700; color: var(--text); }
.ticker-sub { font-size: 10px; }

/* ── SCROLLBAR ── */
::-webkit-scrollbar { width: 6px; height: 6px; }
::-webkit-scrollbar-track { background: transparent; }
::-webkit-scrollbar-thumb { background: var(--bg4); border-radius: 3px; }
::-webkit-scrollbar-thumb:hover { background: var(--border2); }

/* ── HIGHLIGHT ── */
@keyframes rowHighlight {
  0% { background: rgba(232,53,74,0.12); }
  100% { background: transparent; }
}
.row-new td { animation: rowHighlight 1.5s ease-out forwards; }

/* ── OVERVIEW GRID ── */
.overview-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-bottom: 20px; }
.overview-full { grid-column: 1 / -1; }

/* ── COUNTDOWN ── */
.countdown-widget {
  background: linear-gradient(135deg, rgba(232,53,74,0.12), rgba(240,192,64,0.06));
  border: 1px solid rgba(232,53,74,0.2);
  border-radius: var(--radius);
  padding: 24px;
  text-align: center;
  position: relative;
  overflow: hidden;
}
.countdown-widget::before {
  content: '🗾';
  position: absolute;
  right: 20px;
  top: 50%;
  transform: translateY(-50%);
  font-size: 48px;
  opacity: 0.15;
}
.countdown-days { font-family: var(--display); font-size: 52px; font-weight: 800; color: var(--accent); line-height: 1; }
.countdown-label { font-size: 11px; color: var(--text3); text-transform: uppercase; letter-spacing: 0.1em; margin-top: 6px; }
.countdown-date { font-size: 12px; color: var(--text2); margin-top: 8px; font-family: var(--mono); }

/* ── WEATHER STRIP ── */
.weather-strip { display: flex; gap: 8px; overflow-x: auto; padding: 14px 20px; }
.weather-day { background: var(--bg3); border: 1px solid var(--border); border-radius: 10px; padding: 10px 14px; text-align: center; flex-shrink: 0; min-width: 72px; }
.weather-dow { font-size: 9px; text-transform: uppercase; letter-spacing: 0.1em; color: var(--text3); }
.weather-icon { font-size: 20px; margin: 6px 0; }
.weather-hi { font-family: var(--display); font-size: 16px; font-weight: 700; color: var(--text); }
.weather-lo { font-size: 11px; color: var(--text3); }

/* ── EXCHANGE RATE CARD ── */
.rate-display {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 16px 20px;
  border-bottom: 1px solid var(--border);
}
.rate-big { font-family: var(--display); font-size: 28px; font-weight: 800; color: var(--text); }
.rate-label { font-size: 10px; color: var(--text3); margin-top: 2px; }
.rate-calc { padding: 16px 20px; display: flex; align-items: center; gap: 12px; }

/* ── MOBILE BOTTOM NAV ── */
#mobile-nav {
  display: none;
  position: fixed;
  bottom: 0; left: 0; right: 0;
  z-index: 9000;
  background: var(--bg2);
  border-top: 1px solid var(--border2);
  padding-bottom: var(--safe-bottom);
}
.mnav-items { display: flex; }
.mnav-btn {
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 3px;
  padding: 10px 4px 10px;
  font-family: var(--mono);
  font-size: 9px;
  color: var(--text3);
  background: none;
  border: none;
  cursor: pointer;
  transition: color 0.15s;
  letter-spacing: 0.02em;
}
.mnav-btn:hover { color: var(--text2); }
.mnav-btn.active { color: var(--accent); }
.mnav-icon { font-size: 16px; line-height: 1; }

/* ── SYNC STATUS ── */
.sync-pill {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  font-size: 10px;
  color: var(--text3);
  background: var(--bg3);
  border: 1px solid var(--border);
  border-radius: 99px;
  padding: 4px 10px;
}

/* ── RESPONSIVE ── */
@media (max-width: 768px) {
  .sidebar { display: none; }
  #mobile-nav { display: flex; }
  .page { padding: 20px 16px; padding-bottom: 100px; }
  .overview-grid { grid-template-columns: 1fr; }
  .form-row-2 { grid-template-columns: 1fr; }
  .form-row-3 { grid-template-columns: 1fr 1fr; }
  .kpi-grid { grid-template-columns: repeat(2, 1fr); }
}

@keyframes spin { from{transform:rotate(0deg)} to{transform:rotate(360deg)} }
@keyframes fadeIn { from{opacity:0;transform:translateY(6px)} to{opacity:1;transform:translateY(0)} }
.page.active { animation: fadeIn 0.2s ease-out; }
</style>
</head>
<body>

<div id="toast-container"></div>

<!-- ═══════════════ SHELL ═══════════════ -->
<div class="shell">

<!-- ═══════════════ SIDEBAR ═══════════════ -->
<aside class="sidebar">
  <div class="logo">
    <div class="logo-mark">Japan<span>-Dash</span></div>
    <div class="logo-sub">Trip Planner · 日本</div>
  </div>

  <nav class="nav">
    <div class="nav-section">
      <div class="nav-section-label">Overview</div>
      <div class="nav-item active" onclick="goPage('overview',this)">
        <span class="nav-icon">◈</span> Dashboard
      </div>
      <div class="nav-item" onclick="goPage('itinerary',this)">
        <span class="nav-icon">📅</span> Itinerary
        <span class="nav-badge" id="badge-itinerary">0</span>
      </div>
      <div class="nav-item" onclick="goPage('pricing',this)">
        <span class="nav-icon">🎟</span> Activity Pricing
      </div>
    </div>

    <div class="nav-section">
      <div class="nav-section-label">Money</div>
      <div class="nav-item" onclick="goPage('budget',this)">
        <span class="nav-icon">💴</span> Budget
      </div>
      <div class="nav-item" onclick="goPage('exchange',this)">
        <span class="nav-icon">↔</span> Exchange
      </div>
      <div class="nav-item" onclick="goPage('rail',this)">
        <span class="nav-icon">🚄</span> JR Pass
      </div>
    </div>

    <div class="nav-section">
      <div class="nav-section-label">Prep</div>
      <div class="nav-item" onclick="goPage('packing',this)">
        <span class="nav-icon">🧳</span> Packing
        <span class="nav-badge" id="badge-packing">0</span>
      </div>
      <div class="nav-item" onclick="goPage('checklist',this)">
        <span class="nav-icon">☑</span> Pre-Trip
        <span class="nav-badge" id="badge-checklist">0</span>
      </div>
      <div class="nav-item" onclick="goPage('phrases',this)">
        <span class="nav-icon">🗣</span> Phrases
      </div>
    </div>

    <div class="nav-section">
      <div class="nav-section-label">Settings</div>
      <div class="nav-item" onclick="goPage('settings',this)">
        <span class="nav-icon">⚙</span> Trip Settings
      </div>
    </div>
  </nav>

  <div class="sidebar-footer">
    <div class="trip-mini">
      <div class="tm-label">Days Until Departure</div>
      <div class="tm-value" id="sb-countdown">—</div>
      <div class="tm-sub" id="sb-trip-dates">Set dates in Settings</div>
    </div>
    <div style="margin-top:10px;display:flex;align-items:center;justify-content:space-between">
      <span class="sync-pill" id="sync-status-pill">◌ Local</span>
      <button class="btn btn-ghost btn-sm" onclick="goPage('settings',null)">⚙</button>
    </div>
  </div>
</aside>

<!-- ═══════════════ MAIN ═══════════════ -->
<main class="main" id="main">

<!-- ─── OVERVIEW / DASHBOARD ─── -->
<div class="page active" id="page-overview">
  <div class="page-header">
    <div>
      <div class="page-title">Trip <span>Overview</span></div>
      <div class="page-subtitle" id="overview-subtitle">Your Japan adventure at a glance</div>
    </div>
    <div style="display:flex;gap:8px;align-items:center">
      <button class="btn btn-primary" onclick="goPage('itinerary',null)">View Itinerary →</button>
    </div>
  </div>

  <!-- Countdown hero -->
  <div class="countdown-widget overview-full" style="margin-bottom:20px" id="countdown-widget">
    <div class="countdown-days" id="countdown-days">—</div>
    <div class="countdown-label">Days Until Japan</div>
    <div class="countdown-date" id="countdown-date">Set your departure date in Settings</div>
  </div>

  <!-- KPIs -->
  <div class="kpi-grid" id="overview-kpis">
    <div class="kpi-card" style="--accent-color:var(--accent)">
      <div class="kpi-label">Trip Duration</div>
      <div class="kpi-value" id="kpi-days">0 days</div>
      <div class="kpi-sub muted" id="kpi-dates">No dates set</div>
    </div>
    <div class="kpi-card" style="--accent-color:var(--gold)">
      <div class="kpi-label">Total Budget</div>
      <div class="kpi-value" id="kpi-budget">¥0</div>
      <div class="kpi-sub muted" id="kpi-budget-sub">Set in Budget page</div>
    </div>
    <div class="kpi-card" style="--accent-color:var(--green)">
      <div class="kpi-label">Packing Progress</div>
      <div class="kpi-value" id="kpi-packing">0%</div>
      <div class="kpi-sub muted" id="kpi-packing-sub">0 / 0 items</div>
    </div>
    <div class="kpi-card" style="--accent-color:var(--amber)">
      <div class="kpi-label">Pre-Trip Tasks</div>
      <div class="kpi-value" id="kpi-tasks">0%</div>
      <div class="kpi-sub muted" id="kpi-tasks-sub">0 / 0 done</div>
    </div>
    <div class="kpi-card" style="--accent-color:var(--sakura)">
      <div class="kpi-label">Cities</div>
      <div class="kpi-value" id="kpi-cities">0</div>
      <div class="kpi-sub sakura" id="kpi-cities-sub">—</div>
    </div>
    <div class="kpi-card" style="--accent-color:var(--blue)">
      <div class="kpi-label">Exchange Rate</div>
      <div class="kpi-value" id="kpi-rate">¥0</div>
      <div class="kpi-sub muted">per 1 USD</div>
    </div>
  </div>

  <!-- City plan + budget split -->
  <div class="overview-grid">
    <div class="section-panel">
      <div class="section-header">
        <div class="section-title">📍 City Schedule</div>
      </div>
      <div id="city-schedule-list">
        <div class="empty-state">
          <div class="es-icon">🗾</div>
          <div class="es-title">No cities added yet</div>
          <div class="es-sub">Add days in the Itinerary page</div>
        </div>
      </div>
    </div>

    <div class="section-panel">
      <div class="section-header">
        <div class="section-title">💴 Budget Snapshot</div>
        <button class="btn btn-ghost btn-sm" onclick="goPage('budget',null)">Details →</button>
      </div>
      <div id="budget-snapshot">
        <div class="empty-state">
          <div class="es-icon">💴</div>
          <div class="es-title">Budget not set</div>
          <div class="es-sub">Add categories in Budget page</div>
        </div>
      </div>
    </div>
  </div>

  <!-- Upcoming events -->
  <div class="section-panel">
    <div class="section-header">
      <div class="section-title">📅 Next Up</div>
      <button class="btn btn-ghost btn-sm" onclick="goPage('itinerary',null)">Full itinerary →</button>
    </div>
    <div id="next-up-list">
      <div class="empty-state">
        <div class="es-icon">📅</div>
        <div class="es-title">Itinerary empty</div>
        <div class="es-sub">Start planning in the Itinerary section</div>
      </div>
    </div>
  </div>
</div>

<!-- ─── ITINERARY ─── -->
<div class="page" id="page-itinerary">
  <div class="page-header">
    <div>
      <div class="page-title">Trip <span>Itinerary</span></div>
      <div class="page-subtitle">Day-by-day plan with events, costs, and notes</div>
    </div>
    <div style="display:flex;gap:8px">
      <button class="btn btn-secondary" onclick="openModal('add-day')">+ Day</button>
      <button class="btn btn-primary" onclick="openModal('add-event')">+ Event</button>
    </div>
  </div>
  <div id="itinerary-list">
    <div class="empty-state">
      <div class="es-icon">📅</div>
      <div class="es-title">No days planned yet</div>
      <div class="es-sub">Click "+ Day" to add your first day</div>
    </div>
  </div>
</div>

<!-- ─── BUDGET ─── -->
<div class="page" id="page-budget">
  <div class="page-header">
    <div>
      <div class="page-title">Trip <span>Budget</span></div>
      <div class="page-subtitle">Track spending by category · JPY & USD</div>
    </div>
    <div style="display:flex;gap:8px">
      <button class="btn btn-secondary btn-sm" onclick="toggleBudgetCurrency()">¥ / $</button>
      <button class="btn btn-primary" onclick="openModal('add-budget')">+ Category</button>
    </div>
  </div>

  <div class="kpi-grid" style="grid-template-columns:repeat(3,1fr)">
    <div class="kpi-card" style="--accent-color:var(--gold)">
      <div class="kpi-label">Total Budget</div>
      <div class="kpi-value" id="bgt-total">¥0</div>
      <div class="kpi-sub muted">allocated</div>
    </div>
    <div class="kpi-card" style="--accent-color:var(--amber)">
      <div class="kpi-label">Spent</div>
      <div class="kpi-value" id="bgt-spent">¥0</div>
      <div class="kpi-sub muted" id="bgt-spent-pct">0%</div>
    </div>
    <div class="kpi-card" style="--accent-color:var(--green)">
      <div class="kpi-label">Remaining</div>
      <div class="kpi-value" id="bgt-remaining">¥0</div>
      <div class="kpi-sub pos" id="bgt-remaining-sub">Available</div>
    </div>
  </div>

  <div class="section-panel">
    <div class="section-header">
      <div class="section-title">Budget Categories</div>
    </div>
    <div id="budget-list">
      <div class="empty-state">
        <div class="es-icon">💴</div>
        <div class="es-title">No budget set up</div>
        <div class="es-sub">Add categories like Accommodation, Food, Transport…</div>
      </div>
    </div>
  </div>

  <div class="section-panel">
    <div class="section-header">
      <div class="section-title">Expense Log</div>
      <button class="btn btn-primary btn-sm" onclick="openModal('add-expense')">+ Expense</button>
    </div>
    <table class="data-table">
      <thead>
        <tr>
          <th>Description</th>
          <th>Category</th>
          <th>Date</th>
          <th class="right">Amount (¥)</th>
          <th class="right">Actions</th>
        </tr>
      </thead>
      <tbody id="expense-table"></tbody>
    </table>
  </div>
</div>

<!-- ─── EXCHANGE ─── -->
<div class="page" id="page-exchange">
  <div class="page-header">
    <div>
      <div class="page-title">Currency <span>Exchange</span></div>
      <div class="page-subtitle">USD ↔ JPY converter · ATM tips · cash planning</div>
    </div>
  </div>

  <!-- Rate display -->
  <div class="section-panel" style="margin-bottom:20px">
    <div class="section-header">
      <div class="section-title">Live Rate (Manual)</div>
    </div>
    <div class="rate-display">
      <div>
        <div class="rate-big"><span id="rate-display">155.00</span> <span style="font-size:16px;color:var(--text3)">¥</span></div>
        <div class="rate-label">per 1 USD — update below</div>
      </div>
      <div style="display:flex;gap:8px;align-items:center">
        <input type="number" id="rate-input" class="form-input" style="width:100px" step="0.01" placeholder="155.00">
        <button class="btn btn-primary btn-sm" onclick="saveRate()">Update</button>
      </div>
    </div>
    <div class="rate-calc">
      <input type="number" id="conv-usd" class="form-input" style="width:120px" placeholder="USD" oninput="convertUSD()">
      <span style="color:var(--text3)">USD =</span>
      <div style="font-family:var(--display);font-size:20px;font-weight:700;color:var(--gold)" id="conv-jpy">¥0</div>
      <span style="color:var(--text3);margin-left:auto">or</span>
      <input type="number" id="conv-jpy-in" class="form-input" style="width:120px" placeholder="JPY" oninput="convertJPY()">
      <span style="color:var(--text3)">JPY =</span>
      <div style="font-family:var(--display);font-size:20px;font-weight:700;color:var(--green)" id="conv-usd-out">$0</div>
    </div>
  </div>

  <!-- Quick reference grid -->
  <div class="kpi-grid">
    <div class="kpi-card" style="--accent-color:var(--gold)">
      <div class="kpi-label">¥1,000</div>
      <div class="kpi-value" id="ref-1k">$—</div>
      <div class="kpi-sub muted">convenience store run</div>
    </div>
    <div class="kpi-card" style="--accent-color:var(--gold)">
      <div class="kpi-label">¥10,000</div>
      <div class="kpi-value" id="ref-10k">$—</div>
      <div class="kpi-sub muted">daily spending</div>
    </div>
    <div class="kpi-card" style="--accent-color:var(--amber)">
      <div class="kpi-label">¥50,000</div>
      <div class="kpi-value" id="ref-50k">$—</div>
      <div class="kpi-sub muted">week of cash</div>
    </div>
    <div class="kpi-card" style="--accent-color:var(--amber)">
      <div class="kpi-label">¥100,000</div>
      <div class="kpi-value" id="ref-100k">$—</div>
      <div class="kpi-sub muted">budget baseline</div>
    </div>
  </div>

  <!-- Cash tips -->
  <div class="section-panel">
    <div class="section-header"><div class="section-title">💡 Cash & ATM Tips</div></div>
    <div style="padding:0">
      <div class="phrase-row">
        <div class="phrase-jp" style="font-size:13px">🏧 7-Eleven & Japan Post ATMs</div>
        <div style="flex:1">
          <div class="phrase-en">Best international card acceptance. Available 24/7 at convenience stores nationwide.</div>
        </div>
      </div>
      <div class="phrase-row">
        <div class="phrase-jp" style="font-size:13px">💳 Notify your bank</div>
        <div style="flex:1">
          <div class="phrase-en">Call your bank before departure to whitelist Japan transactions. Avoid card blocks.</div>
        </div>
      </div>
      <div class="phrase-row">
        <div class="phrase-jp" style="font-size:13px">💴 Cash-heavy culture</div>
        <div style="flex:1">
          <div class="phrase-en">Many small restaurants, shrines, and markets are cash-only. Carry ¥10,000–¥30,000 daily.</div>
        </div>
      </div>
      <div class="phrase-row">
        <div class="phrase-jp" style="font-size:13px">🏦 Wise / Revolut cards</div>
        <div style="flex:1">
          <div class="phrase-en">Near-interbank rates for ATM withdrawals. Low or no foreign transaction fees.</div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- ─── JR PASS ─── -->
<div class="page" id="page-rail">
  <div class="page-header">
    <div>
      <div class="page-title">JR Pass & <span>Rail</span></div>
      <div class="page-subtitle">Shinkansen routes, pass coverage, and booking notes</div>
    </div>
    <button class="btn btn-primary btn-sm" onclick="openModal('add-route')">+ Route</button>
  </div>

  <!-- JR Pass KPIs -->
  <div class="kpi-grid">
    <div class="kpi-card" style="--accent-color:var(--amber)">
      <div class="kpi-label">JR Pass Cost</div>
      <div class="kpi-value" id="jr-pass-cost">¥50,000</div>
      <div class="kpi-sub muted">14-day ordinary</div>
    </div>
    <div class="kpi-card" style="--accent-color:var(--green)">
      <div class="kpi-label">Covered Value</div>
      <div class="kpi-value" id="jr-covered-val">¥0</div>
      <div class="kpi-sub pos" id="jr-savings">+¥0 savings</div>
    </div>
    <div class="kpi-card" style="--accent-color:var(--blue)">
      <div class="kpi-label">Routes Planned</div>
      <div class="kpi-value" id="jr-routes-count">0</div>
      <div class="kpi-sub muted" id="jr-covered-count">0 JR covered</div>
    </div>
    <div class="kpi-card" style="--accent-color:var(--red)">
      <div class="kpi-label">Not Covered</div>
      <div class="kpi-value" id="jr-uncovered-val">¥0</div>
      <div class="kpi-sub neg">pay separately</div>
    </div>
  </div>

  <!-- Rail settings -->
  <div class="section-panel" style="margin-bottom:20px">
    <div class="section-header">
      <div class="section-title">⚙ Pass Settings</div>
    </div>
    <div style="padding:16px 20px;display:grid;grid-template-columns:1fr 1fr;gap:16px">
      <div class="form-group" style="margin:0">
        <label class="form-label">JR Pass Type</label>
        <select class="form-input" id="jr-pass-type" onchange="updateJRPassCost()">
          <option value="50000">7-day Ordinary — ¥50,000</option>
          <option value="79600">14-day Ordinary — ¥79,600</option>
          <option value="101200">21-day Ordinary — ¥101,200</option>
          <option value="no">No JR Pass</option>
        </select>
      </div>
      <div class="form-group" style="margin:0">
        <label class="form-label">Pass Start Date</label>
        <input type="date" class="form-input" id="jr-start-date" onchange="saveJRSettings()">
      </div>
    </div>
  </div>

  <!-- Route list -->
  <div class="section-panel">
    <div class="section-header">
      <div class="section-title">Routes <span class="badge" id="jr-badge">0</span></div>
    </div>
    <div id="rail-route-list">
      <div class="empty-state">
        <div class="es-icon">🚄</div>
        <div class="es-title">No routes added</div>
        <div class="es-sub">Add shinkansen and local train legs to calculate JR Pass value</div>
      </div>
    </div>
  </div>

  <!-- Reference fares -->
  <div class="section-panel">
    <div class="section-header"><div class="section-title">📊 Reference Fares (2024)</div></div>
    <table class="data-table">
      <thead>
        <tr><th>Route</th><th>Train</th><th class="right">Duration</th><th class="right">Unreserved ¥</th><th class="right">JR Covered</th></tr>
      </thead>
      <tbody>
        <tr><td>Tokyo → Kyoto</td><td>Nozomi / Hikari</td><td class="right mono">~2h15m</td><td class="right mono">¥13,320</td><td class="right"><span class="tag tag-green">✓ Hikari</span></td></tr>
        <tr><td>Kyoto → Osaka</td><td>Shinkansen / Local</td><td class="right mono">~15m</td><td class="right mono">¥570</td><td class="right"><span class="tag tag-green">✓ Yes</span></td></tr>
        <tr><td>Osaka → Hiroshima</td><td>Sakura / Kodama</td><td class="right mono">~1h40m</td><td class="right mono">¥10,490</td><td class="right"><span class="tag tag-green">✓ Yes</span></td></tr>
        <tr><td>Tokyo → Nikko</td><td>Tobu / JR Nikko</td><td class="right mono">~2h</td><td class="right mono">¥1,360</td><td class="right"><span class="tag tag-amber">Partial</span></td></tr>
        <tr><td>Osaka → Nara</td><td>Kintetsu / JR</td><td class="right mono">~45m</td><td class="right mono">¥720</td><td class="right"><span class="tag tag-amber">JR only</span></td></tr>
        <tr><td>Tokyo → Hakone</td><td>Romancecar / JR</td><td class="right mono">~1h30m</td><td class="right mono">¥1,520</td><td class="right"><span class="tag tag-red">✗ No</span></td></tr>
        <tr><td>Airport → Tokyo (Narita)</td><td>N'EX</td><td class="right mono">~1h</td><td class="right mono">¥3,070</td><td class="right"><span class="tag tag-green">✓ Yes</span></td></tr>
        <tr><td>Airport → Osaka (KIX)</td><td>Haruka</td><td class="right mono">~75m</td><td class="right mono">¥2,860</td><td class="right"><span class="tag tag-green">✓ Yes</span></td></tr>
      </tbody>
    </table>
  </div>
</div>

<!-- ─── PACKING LIST ─── -->
<div class="page" id="page-packing">
  <div class="page-header">
    <div>
      <div class="page-title">Packing <span>List</span></div>
      <div class="page-subtitle">Everything you need for Japan — check as you pack</div>
    </div>
    <div style="display:flex;gap:8px">
      <button class="btn btn-ghost btn-sm" onclick="resetPacking()">Reset</button>
      <button class="btn btn-primary" onclick="openModal('add-pack-item')">+ Item</button>
    </div>
  </div>

  <!-- Progress -->
  <div class="section-panel" style="margin-bottom:20px">
    <div style="padding:16px 20px;display:flex;align-items:center;gap:20px">
      <div style="flex:1">
        <div style="display:flex;justify-content:space-between;margin-bottom:6px">
          <span style="font-size:12px;color:var(--text2)">Overall Progress</span>
          <span style="font-family:var(--mono);font-size:12px;color:var(--text)" id="pack-progress-pct">0%</span>
        </div>
        <div class="budget-bar"><div class="budget-fill" id="pack-progress-bar" style="background:var(--green);width:0%"></div></div>
      </div>
      <div style="text-align:center;flex-shrink:0">
        <div style="font-family:var(--display);font-size:22px;font-weight:700;color:var(--text)" id="pack-count">0/0</div>
        <div style="font-size:10px;color:var(--text3)">items packed</div>
      </div>
    </div>
  </div>

  <div id="packing-list"></div>
</div>

<!-- ─── PRE-TRIP CHECKLIST ─── -->
<div class="page" id="page-checklist">
  <div class="page-header">
    <div>
      <div class="page-title">Pre-Trip <span>Checklist</span></div>
      <div class="page-subtitle">Visa, bookings, documents, prep tasks</div>
    </div>
    <button class="btn btn-primary btn-sm" onclick="openModal('add-check-item')">+ Task</button>
  </div>

  <!-- Progress strip -->
  <div class="section-panel" style="margin-bottom:20px">
    <div style="display:grid;grid-template-columns:repeat(4,1fr);border-bottom:1px solid var(--border)">
      <div style="padding:14px 20px;border-right:1px solid var(--border)">
        <div style="font-size:9px;text-transform:uppercase;letter-spacing:.1em;color:var(--text3);margin-bottom:4px">Done</div>
        <div style="font-family:var(--display);font-size:20px;font-weight:700;color:var(--green)" id="ck-done">0</div>
      </div>
      <div style="padding:14px 20px;border-right:1px solid var(--border)">
        <div style="font-size:9px;text-transform:uppercase;letter-spacing:.1em;color:var(--text3);margin-bottom:4px">Remaining</div>
        <div style="font-family:var(--display);font-size:20px;font-weight:700;color:var(--amber)" id="ck-remaining">0</div>
      </div>
      <div style="padding:14px 20px;border-right:1px solid var(--border)">
        <div style="font-size:9px;text-transform:uppercase;letter-spacing:.1em;color:var(--text3);margin-bottom:4px">Total</div>
        <div style="font-family:var(--display);font-size:20px;font-weight:700;color:var(--text)" id="ck-total">0</div>
      </div>
      <div style="padding:14px 20px">
        <div style="font-size:9px;text-transform:uppercase;letter-spacing:.1em;color:var(--text3);margin-bottom:4px">Progress</div>
        <div style="font-family:var(--display);font-size:20px;font-weight:700;color:var(--accent)" id="ck-pct">0%</div>
      </div>
    </div>
    <div style="padding:12px 20px">
      <div class="budget-bar" style="height:10px"><div class="budget-fill" id="ck-progress-bar" style="background:linear-gradient(90deg,var(--accent),var(--amber));width:0%"></div></div>
    </div>
  </div>

  <div id="checklist-list"></div>
</div>

<!-- ─── PHRASES ─── -->
<div class="page" id="page-phrases">
  <div class="page-header">
    <div>
      <div class="page-title">Japanese <span>Phrases</span></div>
      <div class="page-subtitle">Essential phrases for your trip — tap to copy</div>
    </div>
    <div style="display:flex;gap:6px">
      <button class="btn btn-secondary btn-sm" id="phrase-filter-all" onclick="filterPhrases('all',this)" style="background:rgba(232,53,74,0.12);color:var(--accent);border-color:rgba(232,53,74,0.2)">All</button>
      <button class="btn btn-ghost btn-sm" id="phrase-filter-essentials" onclick="filterPhrases('essentials',this)">Essentials</button>
      <button class="btn btn-ghost btn-sm" id="phrase-filter-food" onclick="filterPhrases('food',this)">Food</button>
      <button class="btn btn-ghost btn-sm" id="phrase-filter-transport" onclick="filterPhrases('transport',this)">Transport</button>
      <button class="btn btn-ghost btn-sm" id="phrase-filter-shopping" onclick="filterPhrases('shopping',this)">Shopping</button>
    </div>
  </div>
  <div id="phrases-container"></div>
</div>

<!-- ─── SETTINGS ─── -->
<div class="page" id="page-settings">
  <div class="page-header">
    <div>
      <div class="page-title">Trip <span>Settings</span></div>
      <div class="page-subtitle">Dates, exchange rate, and app data</div>
    </div>
  </div>

  <div class="section-panel" style="margin-bottom:20px">
    <div class="section-header"><div class="section-title">📅 Trip Dates</div></div>
    <div style="padding:20px;display:grid;grid-template-columns:1fr 1fr;gap:16px">
      <div class="form-group" style="margin:0">
        <label class="form-label">Departure Date</label>
        <input type="date" class="form-input" id="setting-depart" onchange="saveSettings()">
      </div>
      <div class="form-group" style="margin:0">
        <label class="form-label">Return Date</label>
        <input type="date" class="form-input" id="setting-return" onchange="saveSettings()">
      </div>
    </div>
  </div>

  <div class="section-panel" style="margin-bottom:20px">
    <div class="section-header"><div class="section-title">💴 Exchange Rate</div></div>
    <div style="padding:20px;display:flex;align-items:center;gap:12px">
      <div class="form-group" style="margin:0;flex:1">
        <label class="form-label">1 USD = ? JPY</label>
        <input type="number" class="form-input" id="setting-rate" step="0.01" placeholder="155.00" onchange="saveSettings()">
      </div>
      <button class="btn btn-primary" onclick="saveSettings();showToast('Rate saved','success')">Save Rate</button>
    </div>
  </div>

  <div class="section-panel" style="margin-bottom:20px">
    <div class="section-header"><div class="section-title">🗑 Data Management</div></div>
    <div style="padding:20px;display:flex;flex-wrap:wrap;gap:10px">
      <button class="btn btn-secondary btn-sm" onclick="exportData()">↓ Export JSON</button>
      <button class="btn btn-secondary btn-sm" onclick="importDataPrompt()">↑ Import JSON</button>
      <button class="btn btn-danger btn-sm" onclick="confirmClearAll()">⚠ Clear All Data</button>
    </div>
    <div style="padding:0 20px 20px;font-size:11px;color:var(--text3)">Data is stored locally in your browser. Export regularly to back up your trip data.</div>
  </div>
</div>

<!-- ─── ACTIVITY PRICING ─── -->
<div class="page" id="page-pricing">
  <div class="page-header">
    <div>
      <div class="page-title">Activity <span>Pricing</span></div>
      <div class="page-subtitle">Per-person USD estimates · Klook sourced · Apr 28 – May 10</div>
    </div>
    <div style="display:flex;gap:6px;flex-wrap:wrap">
      <button class="btn btn-sm" id="pf-all"     onclick="filterPricing('all',this)"     style="background:rgba(232,53,74,0.12);color:var(--accent);border-color:rgba(232,53,74,0.2);border:1px solid">All</button>
      <button class="btn btn-ghost btn-sm" id="pf-free"    onclick="filterPricing('free',this)">Free</button>
      <button class="btn btn-ghost btn-sm" id="pf-paid"    onclick="filterPricing('paid',this)">Paid</button>
      <button class="btn btn-ghost btn-sm" id="pf-tokyo"   onclick="filterPricing('Tokyo',this)">Tokyo</button>
      <button class="btn btn-ghost btn-sm" id="pf-osaka"   onclick="filterPricing('Osaka',this)">Osaka</button>
      <button class="btn btn-ghost btn-sm" id="pf-kyoto"   onclick="filterPricing('Kyoto',this)">Kyoto</button>
      <button class="btn btn-ghost btn-sm" id="pf-okinawa" onclick="filterPricing('Okinawa',this)">Okinawa</button>
    </div>
  </div>

  <div class="kpi-grid" style="grid-template-columns:repeat(4,1fr);margin-bottom:20px">
    <div class="kpi-card" style="--accent-color:var(--accent)">
      <div class="kpi-label">Total Activities</div>
      <div class="kpi-value" id="pr-total-count">0</div>
      <div class="kpi-sub muted">across all days</div>
    </div>
    <div class="kpi-card" style="--accent-color:var(--green)">
      <div class="kpi-label">Free</div>
      <div class="kpi-value" id="pr-free-count">0</div>
      <div class="kpi-sub pos">no cost</div>
    </div>
    <div class="kpi-card" style="--accent-color:var(--gold)">
      <div class="kpi-label">Est. Min Spend</div>
      <div class="kpi-value" id="pr-min-total">$0</div>
      <div class="kpi-sub muted">per person</div>
    </div>
    <div class="kpi-card" style="--accent-color:var(--amber)">
      <div class="kpi-label">Est. Max Spend</div>
      <div class="kpi-value" id="pr-max-total">$0</div>
      <div class="kpi-sub amber">per person</div>
    </div>
  </div>

  <div id="pricing-container"></div>
</div>

</main>
</div>

<!-- ═══════════════ MOBILE BOTTOM NAV ═══════════════ -->
<nav id="mobile-nav">
  <div class="mnav-items">
    <button class="mnav-btn active" id="mnav-overview" onclick="mnavGo('overview',this)">
      <span class="mnav-icon">◈</span>Plan
    </button>
    <button class="mnav-btn" id="mnav-itinerary" onclick="mnavGo('itinerary',this)">
      <span class="mnav-icon">📅</span>Days
    </button>
    <button class="mnav-btn" id="mnav-budget" onclick="mnavGo('budget',this)">
      <span class="mnav-icon">💴</span>Budget
    </button>
    <button class="mnav-btn" id="mnav-packing" onclick="mnavGo('packing',this)">
      <span class="mnav-icon">🧳</span>Pack
    </button>
    <button class="mnav-btn" id="mnav-more" onclick="mnavShowMore()">
      <span class="mnav-icon">⋯</span>More
    </button>
  </div>
</nav>
<div id="mnav-more-drawer" style="display:none;position:fixed;bottom:0;left:0;right:0;z-index:8999;background:var(--bg2);border-top:1px solid var(--border2);padding:16px 16px calc(72px + var(--safe-bottom));grid-template-columns:repeat(3,1fr);gap:8px"></div>
<div id="mnav-more-backdrop" onclick="mnavCloseMore()" style="display:none;position:fixed;inset:0;z-index:8998;background:rgba(0,0,0,.5)"></div>

<!-- ═══════════════ MODALS ═══════════════ -->

<!-- Add Day Modal -->
<div class="modal-overlay" id="modal-add-day">
  <div class="modal">
    <div class="modal-title">Add Itinerary Day <button class="modal-close" onclick="closeModal('add-day')">×</button></div>
    <div class="form-group">
      <label class="form-label">Day Title</label>
      <input type="text" class="form-input" id="day-title-input" placeholder="e.g. Tokyo Exploration">
    </div>
    <div class="form-row-2">
      <div class="form-group">
        <label class="form-label">Date</label>
        <input type="date" class="form-input" id="day-date-input">
      </div>
      <div class="form-group">
        <label class="form-label">City</label>
        <input type="text" class="form-input" id="day-city-input" placeholder="e.g. Tokyo">
      </div>
    </div>
    <div class="form-group">
      <label class="form-label">Notes</label>
      <input type="text" class="form-input" id="day-notes-input" placeholder="Optional notes…">
    </div>
    <div class="modal-footer">
      <button class="btn btn-secondary" onclick="closeModal('add-day')">Cancel</button>
      <button class="btn btn-primary" onclick="addDay()">Add Day</button>
    </div>
  </div>
</div>

<!-- Add Event Modal -->
<div class="modal-overlay" id="modal-add-event">
  <div class="modal">
    <div class="modal-title">Add Event <button class="modal-close" onclick="closeModal('add-event')">×</button></div>
    <div class="form-group">
      <label class="form-label">Day</label>
      <select class="form-input" id="event-day-select"></select>
    </div>
    <div class="form-row-2">
      <div class="form-group">
        <label class="form-label">Time</label>
        <input type="time" class="form-input" id="event-time-input">
      </div>
      <div class="form-group">
        <label class="form-label">Type</label>
        <select class="form-input" id="event-type-input">
          <option value="🏛">🏛 Sightseeing</option>
          <option value="🍜">🍜 Food</option>
          <option value="🚄">🚄 Transport</option>
          <option value="🏨">🏨 Hotel</option>
          <option value="🛍">🛍 Shopping</option>
          <option value="⛩">⛩ Shrine/Temple</option>
          <option value="🎌">🎌 Activity</option>
          <option value="✈">✈ Flight</option>
          <option value="📝">📝 Other</option>
        </select>
      </div>
    </div>
    <div class="form-group">
      <label class="form-label">Event Name</label>
      <input type="text" class="form-input" id="event-name-input" placeholder="e.g. Senso-ji Temple">
    </div>
    <div class="form-row-2">
      <div class="form-group">
        <label class="form-label">Cost (¥)</label>
        <input type="number" class="form-input" id="event-cost-input" placeholder="0" min="0">
      </div>
      <div class="form-group">
        <label class="form-label">Note</label>
        <input type="text" class="form-input" id="event-note-input" placeholder="Optional note…">
      </div>
    </div>
    <div class="modal-footer">
      <button class="btn btn-secondary" onclick="closeModal('add-event')">Cancel</button>
      <button class="btn btn-primary" onclick="addEvent()">Add Event</button>
    </div>
  </div>
</div>

<!-- Add Budget Category Modal -->
<div class="modal-overlay" id="modal-add-budget">
  <div class="modal">
    <div class="modal-title">Add Budget Category <button class="modal-close" onclick="closeModal('add-budget')">×</button></div>
    <div class="form-group">
      <label class="form-label">Category Name</label>
      <input type="text" class="form-input" id="bcat-name-input" placeholder="e.g. Accommodation">
    </div>
    <div class="form-row-2">
      <div class="form-group">
        <label class="form-label">Budget (¥)</label>
        <input type="number" class="form-input" id="bcat-budget-input" placeholder="50000" min="0">
      </div>
      <div class="form-group">
        <label class="form-label">Color</label>
        <select class="form-input" id="bcat-color-input">
          <option value="var(--accent)">🔴 Red</option>
          <option value="var(--gold)">🟡 Gold</option>
          <option value="var(--green)">🟢 Green</option>
          <option value="var(--blue)">🔵 Blue</option>
          <option value="var(--amber)">🟠 Amber</option>
          <option value="var(--sakura)">🌸 Sakura</option>
        </select>
      </div>
    </div>
    <div class="modal-footer">
      <button class="btn btn-secondary" onclick="closeModal('add-budget')">Cancel</button>
      <button class="btn btn-primary" onclick="addBudgetCat()">Add Category</button>
    </div>
  </div>
</div>

<!-- Add Expense Modal -->
<div class="modal-overlay" id="modal-add-expense">
  <div class="modal">
    <div class="modal-title">Log Expense <button class="modal-close" onclick="closeModal('add-expense')">×</button></div>
    <div class="form-group">
      <label class="form-label">Description</label>
      <input type="text" class="form-input" id="exp-desc-input" placeholder="e.g. Ramen at Ichiran">
    </div>
    <div class="form-row-3">
      <div class="form-group">
        <label class="form-label">Amount (¥)</label>
        <input type="number" class="form-input" id="exp-amount-input" placeholder="1500" min="0">
      </div>
      <div class="form-group">
        <label class="form-label">Category</label>
        <select class="form-input" id="exp-cat-select"></select>
      </div>
      <div class="form-group">
        <label class="form-label">Date</label>
        <input type="date" class="form-input" id="exp-date-input">
      </div>
    </div>
    <div class="modal-footer">
      <button class="btn btn-secondary" onclick="closeModal('add-expense')">Cancel</button>
      <button class="btn btn-primary" onclick="addExpense()">Log Expense</button>
    </div>
  </div>
</div>

<!-- Add Route Modal -->
<div class="modal-overlay" id="modal-add-route">
  <div class="modal">
    <div class="modal-title">Add Rail Route <button class="modal-close" onclick="closeModal('add-route')">×</button></div>
    <div class="form-row-2">
      <div class="form-group">
        <label class="form-label">From</label>
        <input type="text" class="form-input" id="route-from-input" placeholder="e.g. Tokyo">
      </div>
      <div class="form-group">
        <label class="form-label">To</label>
        <input type="text" class="form-input" id="route-to-input" placeholder="e.g. Kyoto">
      </div>
    </div>
    <div class="form-row-3">
      <div class="form-group">
        <label class="form-label">Train</label>
        <input type="text" class="form-input" id="route-train-input" placeholder="e.g. Hikari">
      </div>
      <div class="form-group">
        <label class="form-label">Duration</label>
        <input type="text" class="form-input" id="route-duration-input" placeholder="2h 15m">
      </div>
      <div class="form-group">
        <label class="form-label">Cost (¥)</label>
        <input type="number" class="form-input" id="route-cost-input" placeholder="13320" min="0">
      </div>
    </div>
    <div class="form-group">
      <label class="form-label">JR Pass Coverage</label>
      <select class="form-input" id="route-jr-input">
        <option value="yes">✓ Fully Covered</option>
        <option value="partial">Partial Coverage</option>
        <option value="no">✗ Not Covered</option>
      </select>
    </div>
    <div class="modal-footer">
      <button class="btn btn-secondary" onclick="closeModal('add-route')">Cancel</button>
      <button class="btn btn-primary" onclick="addRoute()">Add Route</button>
    </div>
  </div>
</div>

<!-- Add Pack Item Modal -->
<div class="modal-overlay" id="modal-add-pack-item">
  <div class="modal">
    <div class="modal-title">Add Packing Item <button class="modal-close" onclick="closeModal('add-pack-item')">×</button></div>
    <div class="form-row-2">
      <div class="form-group">
        <label class="form-label">Item Name</label>
        <input type="text" class="form-input" id="pack-name-input" placeholder="e.g. Passport">
      </div>
      <div class="form-group">
        <label class="form-label">Category</label>
        <select class="form-input" id="pack-cat-select">
          <option>Documents</option>
          <option>Electronics</option>
          <option>Clothing</option>
          <option>Toiletries</option>
          <option>Health</option>
          <option>Money</option>
          <option>Japan Essentials</option>
          <option>Misc</option>
        </select>
      </div>
    </div>
    <div class="form-row-2">
      <div class="form-group">
        <label class="form-label">Priority</label>
        <select class="form-input" id="pack-priority-select">
          <option value="essential">🔴 Essential</option>
          <option value="important">🟡 Important</option>
          <option value="nice">🟢 Nice to Have</option>
        </select>
      </div>
      <div class="form-group">
        <label class="form-label">Note</label>
        <input type="text" class="form-input" id="pack-note-input" placeholder="Optional tip…">
      </div>
    </div>
    <div class="modal-footer">
      <button class="btn btn-secondary" onclick="closeModal('add-pack-item')">Cancel</button>
      <button class="btn btn-primary" onclick="addPackItem()">Add Item</button>
    </div>
  </div>
</div>

<!-- Add Checklist Item Modal -->
<div class="modal-overlay" id="modal-add-check-item">
  <div class="modal">
    <div class="modal-title">Add Pre-Trip Task <button class="modal-close" onclick="closeModal('add-check-item')">×</button></div>
    <div class="form-group">
      <label class="form-label">Task</label>
      <input type="text" class="form-input" id="check-title-input" placeholder="e.g. Book Shinkansen tickets">
    </div>
    <div class="form-row-2">
      <div class="form-group">
        <label class="form-label">Category</label>
        <select class="form-input" id="check-cat-select">
          <option>Bookings</option>
          <option>Documents</option>
          <option>Money</option>
          <option>Health</option>
          <option>Packing</option>
          <option>Research</option>
          <option>Other</option>
        </select>
      </div>
      <div class="form-group">
        <label class="form-label">Note</label>
        <input type="text" class="form-input" id="check-note-input" placeholder="Optional note…">
      </div>
    </div>
    <div class="modal-footer">
      <button class="btn btn-secondary" onclick="closeModal('add-check-item')">Cancel</button>
      <button class="btn btn-primary" onclick="addCheckItem()">Add Task</button>
    </div>
  </div>
</div>

<script>
// ══════════════════════════════════════════════════════════
//  DB — localStorage wrapper
// ══════════════════════════════════════════════════════════
var DB = {
  get: function(key, def) {
    try { var v = localStorage.getItem('jd_' + key); return v !== null ? JSON.parse(v) : def; } catch(e) { return def; }
  },
  set: function(key, val) {
    try { localStorage.setItem('jd_' + key, JSON.stringify(val)); } catch(e) {}
  },
  remove: function(key) {
    try { localStorage.removeItem('jd_' + key); } catch(e) {}
  }
};

// ══════════════════════════════════════════════════════════
//  STATE — load from localStorage
// ══════════════════════════════════════════════════════════
var State = {
  settings: DB.get('settings', { depart: '', returnDate: '', rate: 155 }),
  days: DB.get('days', []),
  events: DB.get('events', []),
  budgetCats: DB.get('budgetCats', []),
  expenses: DB.get('expenses', []),
  routes: DB.get('routes', []),
  packItems: DB.get('packItems', null),   // null = use defaults
  checkItems: DB.get('checkItems', null), // null = use defaults
  jr: DB.get('jr', { type: '79600', startDate: '' }),
  budgetCurrency: 'jpy'
};

function saveState() {
  DB.set('settings', State.settings);
  DB.set('days', State.days);
  DB.set('events', State.events);
  DB.set('budgetCats', State.budgetCats);
  DB.set('expenses', State.expenses);
  DB.set('routes', State.routes);
  DB.set('packItems', State.packItems);
  DB.set('checkItems', State.checkItems);
  DB.set('jr', State.jr);
}

// ══════════════════════════════════════════════════════════
//  DEFAULT DATA
// ══════════════════════════════════════════════════════════
var DEFAULT_PACK_ITEMS = [
  // Documents
  { id: uid(), cat: 'Documents', name: 'Passport', note: 'Valid 6+ months from entry', priority: 'essential', packed: false },
  { id: uid(), cat: 'Documents', name: 'Copy of passport', note: 'Digital + physical copy', priority: 'essential', packed: false },
  { id: uid(), cat: 'Documents', name: 'Flight confirmation', note: 'Printed or screenshot', priority: 'essential', packed: false },
  { id: uid(), cat: 'Documents', name: 'Hotel reservations', note: 'All printed/saved offline', priority: 'essential', packed: false },
  { id: uid(), cat: 'Documents', name: 'Travel insurance', note: 'Policy number handy', priority: 'essential', packed: false },
  { id: uid(), cat: 'Documents', name: 'JR Pass voucher', note: 'Exchange at arrival airport', priority: 'important', packed: false },
  // Electronics
  { id: uid(), cat: 'Electronics', name: 'Phone + charger', note: '', priority: 'essential', packed: false },
  { id: uid(), cat: 'Electronics', name: 'Universal adapter (Type A)', note: 'Japan uses 100V Type A flat plugs', priority: 'essential', packed: false },
  { id: uid(), cat: 'Electronics', name: 'Portable battery bank', note: 'Walking all day drains phones', priority: 'important', packed: false },
  { id: uid(), cat: 'Electronics', name: 'Camera', note: '', priority: 'nice', packed: false },
  { id: uid(), cat: 'Electronics', name: 'IC Card (Suica/Pasmo)', note: 'Buy at airport on arrival', priority: 'important', packed: false },
  // Clothing
  { id: uid(), cat: 'Clothing', name: 'Comfortable walking shoes', note: 'You\'ll walk 20,000+ steps/day', priority: 'essential', packed: false },
  { id: uid(), cat: 'Clothing', name: 'Slip-on shoes', note: 'Easy on/off for temples', priority: 'important', packed: false },
  { id: uid(), cat: 'Clothing', name: 'Light layers / jacket', note: 'Weather varies by region', priority: 'important', packed: false },
  { id: uid(), cat: 'Clothing', name: 'Modest outfit for temples', note: 'Cover shoulders / no shorts at some temples', priority: 'important', packed: false },
  // Toiletries
  { id: uid(), cat: 'Toiletries', name: 'Toothbrush + paste', note: 'Basic toiletries at konbini', priority: 'essential', packed: false },
  { id: uid(), cat: 'Toiletries', name: 'Deodorant', note: 'Harder to find Western brands', priority: 'important', packed: false },
  { id: uid(), cat: 'Toiletries', name: 'Sunscreen SPF 50+', note: 'Intense UV especially in summer', priority: 'important', packed: false },
  // Japan Essentials
  { id: uid(), cat: 'Japan Essentials', name: 'Pocket WiFi / SIM card', note: 'Book pocket WiFi ahead — available at airport', priority: 'essential', packed: false },
  { id: uid(), cat: 'Japan Essentials', name: 'Google Translate (offline JP)', note: 'Download Japanese language pack', priority: 'essential', packed: false },
  { id: uid(), cat: 'Japan Essentials', name: 'Small towel / handkerchief', note: 'Public restrooms often have no dryers', priority: 'important', packed: false },
  { id: uid(), cat: 'Japan Essentials', name: 'Cash (¥30,000–50,000)', note: 'Withdraw at 7-Eleven ATM on arrival', priority: 'essential', packed: false },
  { id: uid(), cat: 'Japan Essentials', name: 'Coin purse', note: 'Lots of ¥500 and ¥100 coins', priority: 'nice', packed: false },
  { id: uid(), cat: 'Japan Essentials', name: 'Reusable tote bag', note: 'Stores charge for plastic bags', priority: 'nice', packed: false },
  // Money
  { id: uid(), cat: 'Money', name: 'Credit card (no foreign fees)', note: 'Visa/Mastercard widely accepted now', priority: 'essential', packed: false },
  { id: uid(), cat: 'Money', name: 'Wise or Revolut card', note: 'Best ATM rates', priority: 'important', packed: false },
];

var DEFAULT_CHECK_ITEMS = [
  // Bookings
  { id: uid(), cat: 'Bookings', title: 'Book flights', note: 'International + any domestic', done: false },
  { id: uid(), cat: 'Bookings', title: 'Book accommodations', note: 'All hotels / hostels for each city', done: false },
  { id: uid(), cat: 'Bookings', title: 'Purchase JR Pass', note: 'Buy online before departure — cheaper', done: false },
  { id: uid(), cat: 'Bookings', title: 'Book popular restaurants', note: 'Sushi counters, ramen, omakase — book weeks ahead', done: false },
  { id: uid(), cat: 'Bookings', title: 'Book TeamLab / popular attractions', note: 'Sells out months in advance', done: false },
  // Documents
  { id: uid(), cat: 'Documents', title: 'Check passport expiry', note: 'Must be valid 6+ months from arrival', done: false },
  { id: uid(), cat: 'Documents', title: 'Fill out Visit Japan Web', note: 'Pre-register customs & immigration online', done: false },
  { id: uid(), cat: 'Documents', title: 'Print/save all reservations', note: 'Hotels, flights, attractions', done: false },
  // Money
  { id: uid(), cat: 'Money', title: 'Notify bank of Japan travel', note: 'Prevent card blocks abroad', done: false },
  { id: uid(), cat: 'Money', title: 'Get Wise / Revolut card', note: 'Best exchange rates at ATMs', done: false },
  { id: uid(), cat: 'Money', title: 'Set trip budget', note: 'Use Budget page', done: false },
  // Health
  { id: uid(), cat: 'Health', title: 'Get travel insurance', note: 'Medical coverage important abroad', done: false },
  { id: uid(), cat: 'Health', title: 'Pack any prescription medications', note: 'Bring supply + doctor\'s note', done: false },
  // Research
  { id: uid(), cat: 'Research', title: 'Download offline maps (Maps.me)', note: 'Works without internet', done: false },
  { id: uid(), cat: 'Research', title: 'Download Google Translate (JP offline)', note: 'Camera translation very useful', done: false },
  { id: uid(), cat: 'Research', title: 'Learn basic Japanese phrases', note: 'Use Phrases page', done: false },
  { id: uid(), cat: 'Research', title: 'Research IC card (Suica/Pasmo)', note: 'Load at airport vending machine', done: false },
];

var PHRASES_DATA = [
  // Essentials
  { cat: 'essentials', jp: 'すみません', romaji: 'Sumimasen', en: 'Excuse me / Sorry (to get attention)' },
  { cat: 'essentials', jp: 'ありがとうございます', romaji: 'Arigatou gozaimasu', en: 'Thank you very much' },
  { cat: 'essentials', jp: 'はい / いいえ', romaji: 'Hai / Iie', en: 'Yes / No' },
  { cat: 'essentials', jp: 'わかりません', romaji: 'Wakarimasen', en: 'I don\'t understand' },
  { cat: 'essentials', jp: '英語を話せますか？', romaji: 'Eigo o hanasemasu ka?', en: 'Do you speak English?' },
  { cat: 'essentials', jp: 'トイレはどこですか？', romaji: 'Toire wa doko desu ka?', en: 'Where is the restroom?' },
  { cat: 'essentials', jp: 'いくらですか？', romaji: 'Ikura desu ka?', en: 'How much does this cost?' },
  { cat: 'essentials', jp: 'ください', romaji: 'Kudasai', en: 'Please give me… / I\'ll have…' },
  { cat: 'essentials', jp: 'これをください', romaji: 'Kore o kudasai', en: 'I\'ll take this one' },
  // Food
  { cat: 'food', jp: '一人です', romaji: 'Hitori desu', en: 'Just one person (for seating)' },
  { cat: 'food', jp: 'ふたりです', romaji: 'Futari desu', en: 'Two people (for seating)' },
  { cat: 'food', jp: 'おすすめは何ですか？', romaji: 'Osusume wa nan desu ka?', en: 'What do you recommend?' },
  { cat: 'food', jp: 'おいしいです！', romaji: 'Oishii desu!', en: 'This is delicious!' },
  { cat: 'food', jp: 'お会計をお願いします', romaji: 'Okaikei o onegaishimasu', en: 'Check/bill, please' },
  { cat: 'food', jp: 'アレルギーがあります', romaji: 'Arerugii ga arimasu', en: 'I have an allergy' },
  { cat: 'food', jp: '辛くしないでください', romaji: 'Karakunshinai de kudasai', en: 'Please make it not spicy' },
  { cat: 'food', jp: 'ビールをください', romaji: 'Biiru o kudasai', en: 'A beer, please' },
  // Transport
  { cat: 'transport', jp: '〜はどこですか？', romaji: '〜 wa doko desu ka?', en: 'Where is [place]?' },
  { cat: 'transport', jp: '〜に行きたいです', romaji: '〜 ni ikitai desu', en: 'I want to go to [place]' },
  { cat: 'transport', jp: 'このバスは〜に止まりますか？', romaji: 'Kono basu wa ~ ni tomarimasu ka?', en: 'Does this bus stop at [place]?' },
  { cat: 'transport', jp: '乗り換えはどこですか？', romaji: 'Norikae wa doko desu ka?', en: 'Where do I transfer?' },
  { cat: 'transport', jp: '自由席はありますか？', romaji: 'Jiyu-seki wa arimasu ka?', en: 'Are there unreserved seats?' },
  { cat: 'transport', jp: 'タクシーをお願いします', romaji: 'Takushii o onegaishimasu', en: 'Please call a taxi' },
  // Shopping
  { cat: 'shopping', jp: '試着してもいいですか？', romaji: 'Shichaku shite mo ii desu ka?', en: 'May I try this on?' },
  { cat: 'shopping', jp: '別々に包んでください', romaji: 'Betsubetsu ni tsutsunde kudasai', en: 'Please wrap them separately (gifts)' },
  { cat: 'shopping', jp: '免税できますか？', romaji: 'Menzei dekimasu ka?', en: 'Can I get tax-free shopping?' },
  { cat: 'shopping', jp: 'カードで払えますか？', romaji: 'Kaado de haraemasu ka?', en: 'Can I pay by card?' },
  { cat: 'shopping', jp: '袋はいりません', romaji: 'Fukuro wa irimasen', en: 'I don\'t need a bag' },
  { cat: 'shopping', jp: '値引きできますか？', romaji: 'Nebiki dekimasu ka?', en: 'Can you give a discount?' },
];

// ══════════════════════════════════════════════════════════
//  UTILS
// ══════════════════════════════════════════════════════════
function uid() { return Math.random().toString(36).substr(2,9); }

function fmt(n) {
  if (State.budgetCurrency === 'usd') {
    return '$' + (n / State.settings.rate).toFixed(0);
  }
  return '¥' + Math.round(n).toLocaleString();
}

function fmtJPY(n) { return '¥' + Math.round(n).toLocaleString(); }
function fmtUSD(n) { return '$' + (n / State.settings.rate).toFixed(0); }

function el(id) { return document.getElementById(id); }

function showToast(msg, type) {
  var c = el('toast-container');
  var t = document.createElement('div');
  t.className = 'toast ' + (type || 'info');
  t.textContent = msg;
  c.appendChild(t);
  setTimeout(function() { if (t.parentNode) t.parentNode.removeChild(t); }, 3100);
}

function daysUntil(dateStr) {
  if (!dateStr) return null;
  var now = new Date(); now.setHours(0,0,0,0);
  var d = new Date(dateStr + 'T00:00:00');
  return Math.ceil((d - now) / 86400000);
}

function daysBetween(a, b) {
  if (!a || !b) return 0;
  var d1 = new Date(a + 'T00:00:00'), d2 = new Date(b + 'T00:00:00');
  return Math.ceil((d2 - d1) / 86400000);
}

function formatDate(dateStr) {
  if (!dateStr) return '';
  var d = new Date(dateStr + 'T00:00:00');
  return d.toLocaleDateString('en-US', { month: 'short', day: 'numeric', year: 'numeric' });
}

// ══════════════════════════════════════════════════════════
//  NAVIGATION
// ══════════════════════════════════════════════════════════
function goPage(pageId, navEl) {
  document.querySelectorAll('.page').forEach(function(p) { p.classList.remove('active'); });
  document.querySelectorAll('.nav-item').forEach(function(n) { n.classList.remove('active'); });
  var page = el('page-' + pageId);
  if (page) page.classList.add('active');
  if (navEl) navEl.classList.add('active');
  else {
    var match = document.querySelector('.nav-item[onclick*="\'' + pageId + '\'"]');
    if (match) match.classList.add('active');
  }
  renderPage(pageId);
  mnavCloseMore();
  // sync mobile nav
  document.querySelectorAll('.mnav-btn').forEach(function(b) { b.classList.remove('active'); });
  var mnav = el('mnav-' + pageId);
  if (mnav) mnav.classList.add('active');
}

function mnavGo(pageId, btn) {
  goPage(pageId, null);
  document.querySelectorAll('.mnav-btn').forEach(function(b) { b.classList.remove('active'); });
  if (btn) btn.classList.add('active');
}

function mnavShowMore() {
  var drawer = el('mnav-more-drawer');
  var backdrop = el('mnav-more-backdrop');
  var pages = [
    { id:'pricing',   icon:'🎟', label:'Pricing' },
    { id:'exchange',  icon:'↔',  label:'Exchange' },
    { id:'rail',      icon:'🚄', label:'JR Pass' },
    { id:'checklist', icon:'☑',  label:'Pre-Trip' },
    { id:'phrases',   icon:'🗣', label:'Phrases' },
    { id:'settings',  icon:'⚙',  label:'Settings' },
  ];
  drawer.innerHTML = pages.map(function(p) {
    return '<button class="nav-item" style="flex-direction:column;gap:4px;height:72px;justify-content:center" onclick="mnavGo(\'' + p.id + '\',null);mnavCloseMore()">'
      + '<span style="font-size:20px">' + p.icon + '</span>'
      + '<span style="font-size:10px">' + p.label + '</span>'
      + '</button>';
  }).join('');
  drawer.style.display = 'grid';
  backdrop.style.display = 'block';
}

function mnavCloseMore() {
  var d = el('mnav-more-drawer'), b = el('mnav-more-backdrop');
  if(d) d.style.display = 'none';
  if(b) b.style.display = 'none';
}

// ══════════════════════════════════════════════════════════
//  MODALS
// ══════════════════════════════════════════════════════════
function openModal(id) {
  var overlay = el('modal-' + id);
  if (!overlay) return;
  // Pre-populate selects
  if (id === 'add-event') {
    var sel = el('event-day-select');
    sel.innerHTML = State.days.map(function(d) {
      return '<option value="' + d.id + '">' + (d.date ? formatDate(d.date) + ' — ' : '') + d.title + '</option>';
    }).join('');
    if (!State.days.length) { showToast('Add a day first', 'error'); return; }
  }
  if (id === 'add-expense') {
    var cs = el('exp-cat-select');
    cs.innerHTML = State.budgetCats.map(function(c) {
      return '<option value="' + c.id + '">' + c.name + '</option>';
    }).join('');
    el('exp-date-input').value = new Date().toISOString().split('T')[0];
  }
  overlay.classList.add('open');
}

function closeModal(id) {
  var overlay = el('modal-' + id);
  if (overlay) overlay.classList.remove('open');
}

// ══════════════════════════════════════════════════════════
//  SETTINGS
// ══════════════════════════════════════════════════════════
function saveSettings() {
  State.settings.depart = el('setting-depart').value;
  State.settings.returnDate = el('setting-return').value;
  var r = parseFloat(el('setting-rate').value);
  if (r > 0) State.settings.rate = r;
  saveState();
  renderAll();
  showToast('Settings saved', 'success');
}

function loadSettingsForm() {
  el('setting-depart').value = State.settings.depart || '';
  el('setting-return').value = State.settings.returnDate || '';
  el('setting-rate').value = State.settings.rate || 155;
}

// ══════════════════════════════════════════════════════════
//  ITINERARY
// ══════════════════════════════════════════════════════════
function addDay() {
  var title = el('day-title-input').value.trim();
  var date = el('day-date-input').value;
  var city = el('day-city-input').value.trim();
  var notes = el('day-notes-input').value.trim();
  if (!title) { showToast('Enter a day title', 'error'); return; }
  State.days.push({ id: uid(), title: title, date: date, city: city, notes: notes });
  State.days.sort(function(a,b) { return (a.date||'').localeCompare(b.date||''); });
  saveState();
  closeModal('add-day');
  renderPage('itinerary');
  renderOverview();
  showToast('Day added', 'success');
  // clear
  el('day-title-input').value = '';
  el('day-date-input').value = '';
  el('day-city-input').value = '';
  el('day-notes-input').value = '';
}

function addEvent() {
  var dayId = el('event-day-select').value;
  var time = el('event-time-input').value;
  var type = el('event-type-input').value;
  var name = el('event-name-input').value.trim();
  var cost = parseInt(el('event-cost-input').value) || 0;
  var note = el('event-note-input').value.trim();
  if (!name) { showToast('Enter an event name', 'error'); return; }
  State.events.push({ id: uid(), dayId: dayId, time: time, type: type, name: name, cost: cost, note: note, done: false });
  State.events.sort(function(a,b) { return (a.time||'').localeCompare(b.time||''); });
  saveState();
  closeModal('add-event');
  renderPage('itinerary');
  renderOverview();
  showToast('Event added', 'success');
  el('event-name-input').value = '';
  el('event-time-input').value = '';
  el('event-cost-input').value = '';
  el('event-note-input').value = '';
}

function toggleEventDone(evtId) {
  var ev = State.events.find(function(e) { return e.id === evtId; });
  if (ev) { ev.done = !ev.done; saveState(); renderPage('itinerary'); }
}

function deleteDay(dayId) {
  if (!confirm('Delete this day and all its events?')) return;
  State.days = State.days.filter(function(d) { return d.id !== dayId; });
  State.events = State.events.filter(function(e) { return e.dayId !== dayId; });
  saveState();
  renderPage('itinerary');
  renderOverview();
  showToast('Day deleted', 'info');
}

function deleteEvent(evtId) {
  State.events = State.events.filter(function(e) { return e.id !== evtId; });
  saveState();
  renderPage('itinerary');
  showToast('Event removed', 'info');
}

function renderItinerary() {
  var container = el('itinerary-list');
  if (!State.days.length) {
    container.innerHTML = '<div class="empty-state"><div class="es-icon">📅</div><div class="es-title">No days planned yet</div><div class="es-sub">Click "+ Day" to add your first day</div></div>';
    el('badge-itinerary').textContent = '0';
    return;
  }
  el('badge-itinerary').textContent = State.days.length;
  container.innerHTML = State.days.map(function(day, idx) {
    var evts = State.events.filter(function(e) { return e.dayId === day.id; });
    var doneEvts = evts.filter(function(e) { return e.done; }).length;
    var dayTotal = evts.reduce(function(s,e) { return s + (e.cost||0); }, 0);
    return '<div class="day-card">'
      + '<div class="day-header">'
      + '<div class="day-num">D' + (idx+1) + '</div>'
      + '<div style="flex:1">'
      + '<div class="day-title">' + day.title + '</div>'
      + '<div style="display:flex;gap:10px;margin-top:2px">'
      + (day.city ? '<span class="day-city">📍 ' + day.city + '</span>' : '')
      + (day.date ? '<span class="day-date">' + formatDate(day.date) + '</span>' : '')
      + '</div>'
      + '</div>'
      + '<div style="display:flex;align-items:center;gap:8px">'
      + (dayTotal ? '<span style="font-family:var(--mono);font-size:11px;color:var(--text3)">' + fmtJPY(dayTotal) + '</span>' : '')
      + (evts.length ? '<span class="tag tag-muted">' + doneEvts + '/' + evts.length + '</span>' : '')
      + '<button class="btn btn-ghost btn-sm" onclick="deleteDay(\'' + day.id + '\')" style="padding:4px 6px;font-size:12px;color:var(--text3)">✕</button>'
      + '</div>'
      + '</div>'
      + '<div class="day-body">'
      + (evts.length ? evts.map(function(ev) {
          return '<div class="event-row">'
            + '<div class="event-time">' + (ev.time || '—') + '</div>'
            + '<div class="event-icon">' + ev.type + '</div>'
            + '<div class="event-info">'
            + '<div class="event-name" style="' + (ev.done ? 'text-decoration:line-through;color:var(--text3)' : '') + '">' + ev.name + '</div>'
            + (ev.note ? '<div class="event-note">' + ev.note + '</div>' : '')
            + '</div>'
            + (ev.cost ? '<div class="event-cost">' + fmtJPY(ev.cost) + '</div>' : '')
            + '<div class="event-done' + (ev.done ? ' checked' : '') + '" onclick="toggleEventDone(\'' + ev.id + '\')">' + (ev.done ? '✓' : '') + '</div>'
            + '<button onclick="deleteEvent(\'' + ev.id + '\')" style="background:none;border:none;color:var(--text3);cursor:pointer;font-size:12px;padding:0 2px;flex-shrink:0">✕</button>'
            + '</div>';
        }).join('')
        : '<div style="padding:12px 18px;font-size:12px;color:var(--text3)">No events yet — click "+ Event" to add</div>')
      + '</div>'
      + (day.notes ? '<div style="padding:10px 18px;border-top:1px solid var(--border);font-size:11px;color:var(--text3);font-style:italic">📝 ' + day.notes + '</div>' : '')
      + '</div>';
  }).join('');
}

// ══════════════════════════════════════════════════════════
//  BUDGET
// ══════════════════════════════════════════════════════════
function toggleBudgetCurrency() {
  State.budgetCurrency = State.budgetCurrency === 'jpy' ? 'usd' : 'jpy';
  renderPage('budget');
}

function addBudgetCat() {
  var name = el('bcat-name-input').value.trim();
  var budget = parseInt(el('bcat-budget-input').value) || 0;
  var color = el('bcat-color-input').value;
  if (!name) { showToast('Enter a category name', 'error'); return; }
  State.budgetCats.push({ id: uid(), name: name, budget: budget, color: color });
  saveState();
  closeModal('add-budget');
  renderPage('budget');
  renderOverview();
  showToast('Category added', 'success');
  el('bcat-name-input').value = '';
  el('bcat-budget-input').value = '';
}

function deleteBudgetCat(catId) {
  if (!confirm('Delete this category and its expenses?')) return;
  State.budgetCats = State.budgetCats.filter(function(c) { return c.id !== catId; });
  State.expenses = State.expenses.filter(function(e) { return e.catId !== catId; });
  saveState();
  renderPage('budget');
  showToast('Category deleted', 'info');
}

function addExpense() {
  var desc = el('exp-desc-input').value.trim();
  var amount = parseInt(el('exp-amount-input').value) || 0;
  var catId = el('exp-cat-select').value;
  var date = el('exp-date-input').value;
  if (!desc || !amount) { showToast('Fill in description and amount', 'error'); return; }
  State.expenses.push({ id: uid(), desc: desc, amount: amount, catId: catId, date: date });
  saveState();
  closeModal('add-expense');
  renderPage('budget');
  showToast('Expense logged', 'success');
  el('exp-desc-input').value = '';
  el('exp-amount-input').value = '';
}

function deleteExpense(expId) {
  State.expenses = State.expenses.filter(function(e) { return e.id !== expId; });
  saveState();
  renderPage('budget');
  showToast('Expense removed', 'info');
}

function renderBudget() {
  var totalBudget = State.budgetCats.reduce(function(s,c) { return s + c.budget; }, 0);
  var totalSpent = State.expenses.reduce(function(s,e) { return s + e.amount; }, 0);
  var remaining = totalBudget - totalSpent;

  el('bgt-total').textContent = fmt(totalBudget);
  el('bgt-spent').textContent = fmt(totalSpent);
  el('bgt-spent-pct').textContent = totalBudget ? Math.round(totalSpent/totalBudget*100) + '%' : '0%';
  el('bgt-remaining').textContent = fmt(remaining);
  el('bgt-remaining-sub').textContent = remaining >= 0 ? 'Available' : 'Over budget!';
  el('bgt-remaining-sub').className = 'kpi-sub ' + (remaining >= 0 ? 'pos' : 'neg');

  var listEl = el('budget-list');
  if (!State.budgetCats.length) {
    listEl.innerHTML = '<div class="empty-state"><div class="es-icon">💴</div><div class="es-title">No categories</div><div class="es-sub">Add categories like Accommodation, Food, Transport…</div></div>';
  } else {
    listEl.innerHTML = State.budgetCats.map(function(cat) {
      var spent = State.expenses.filter(function(e) { return e.catId === cat.id; }).reduce(function(s,e) { return s + e.amount; }, 0);
      var pct = cat.budget ? Math.min(100, Math.round(spent / cat.budget * 100)) : 0;
      var over = cat.budget && spent > cat.budget;
      return '<div class="budget-row">'
        + '<div class="budget-cat">'
        + '<div class="budget-cat-name">' + cat.name + '</div>'
        + '<div style="margin-top:4px">'
        + '<div class="budget-bar"><div class="budget-fill" style="width:' + pct + '%;background:' + (over ? 'var(--red)' : cat.color) + '"></div></div>'
        + '<div style="font-size:10px;color:var(--text3)">' + pct + '% used</div>'
        + '</div>'
        + '</div>'
        + '<div class="budget-amounts">'
        + '<div class="budget-spent">' + fmt(spent) + '</div>'
        + '<div class="budget-limit">of ' + fmt(cat.budget) + '</div>'
        + '</div>'
        + '<button onclick="deleteBudgetCat(\'' + cat.id + '\')" class="btn btn-ghost btn-sm" style="padding:4px 6px;color:var(--text3)">✕</button>'
        + '</div>';
    }).join('');
  }

  // Expense table
  var tbody = el('expense-table');
  if (!State.expenses.length) {
    tbody.innerHTML = '<tr><td colspan="5" style="text-align:center;padding:24px;color:var(--text3)">No expenses logged yet</td></tr>';
  } else {
    var sortedExp = State.expenses.slice().sort(function(a,b) { return (b.date||'').localeCompare(a.date||''); });
    tbody.innerHTML = sortedExp.map(function(exp) {
      var cat = State.budgetCats.find(function(c) { return c.id === exp.catId; });
      return '<tr>'
        + '<td>' + exp.desc + '</td>'
        + '<td>' + (cat ? '<span class="tag" style="background:rgba(0,0,0,0.2);color:' + (cat.color) + ';border-color:rgba(0,0,0,0.1)">' + cat.name + '</span>' : '—') + '</td>'
        + '<td class="val-muted">' + (exp.date ? formatDate(exp.date) : '—') + '</td>'
        + '<td class="right mono">' + fmtJPY(exp.amount) + '</td>'
        + '<td class="right"><button onclick="deleteExpense(\'' + exp.id + '\')" class="btn btn-ghost btn-sm" style="padding:3px 6px;color:var(--text3)">✕</button></td>'
        + '</tr>';
    }).join('');
  }
}

// ══════════════════════════════════════════════════════════
//  EXCHANGE
// ══════════════════════════════════════════════════════════
function saveRate() {
  var r = parseFloat(el('rate-input').value);
  if (r > 0) {
    State.settings.rate = r;
    saveState();
    renderExchange();
    renderOverview();
    showToast('Rate updated', 'success');
  }
}

function convertUSD() {
  var v = parseFloat(el('conv-usd').value) || 0;
  el('conv-jpy').textContent = '¥' + Math.round(v * State.settings.rate).toLocaleString();
}

function convertJPY() {
  var v = parseFloat(el('conv-jpy-in').value) || 0;
  el('conv-usd-out').textContent = '$' + (v / State.settings.rate).toFixed(2);
}

function renderExchange() {
  var rate = State.settings.rate || 155;
  el('rate-display').textContent = rate.toFixed(2);
  el('rate-input').value = rate;
  el('ref-1k').textContent = '$' + (1000/rate).toFixed(2);
  el('ref-10k').textContent = '$' + (10000/rate).toFixed(0);
  el('ref-50k').textContent = '$' + (50000/rate).toFixed(0);
  el('ref-100k').textContent = '$' + (100000/rate).toFixed(0);
}

// ══════════════════════════════════════════════════════════
//  JR PASS / RAIL
// ══════════════════════════════════════════════════════════
function updateJRPassCost() {
  State.jr.type = el('jr-pass-type').value;
  saveState();
  renderRail();
}

function saveJRSettings() {
  State.jr.startDate = el('jr-start-date').value;
  saveState();
}

function addRoute() {
  var from = el('route-from-input').value.trim();
  var to = el('route-to-input').value.trim();
  var train = el('route-train-input').value.trim();
  var duration = el('route-duration-input').value.trim();
  var cost = parseInt(el('route-cost-input').value) || 0;
  var jr = el('route-jr-input').value;
  if (!from || !to) { showToast('Enter origin and destination', 'error'); return; }
  State.routes.push({ id: uid(), from: from, to: to, train: train, duration: duration, cost: cost, jr: jr });
  saveState();
  closeModal('add-route');
  renderPage('rail');
  showToast('Route added', 'success');
  el('route-from-input').value = '';
  el('route-to-input').value = '';
  el('route-train-input').value = '';
  el('route-duration-input').value = '';
  el('route-cost-input').value = '';
}

function deleteRoute(routeId) {
  State.routes = State.routes.filter(function(r) { return r.id !== routeId; });
  saveState();
  renderPage('rail');
}

function renderRail() {
  var passCost = parseInt(State.jr.type) || 0;
  var coveredVal = State.routes.filter(function(r) { return r.jr === 'yes'; }).reduce(function(s,r) { return s + r.cost; }, 0);
  var partialVal = State.routes.filter(function(r) { return r.jr === 'partial'; }).reduce(function(s,r) { return s + r.cost * 0.5; }, 0);
  var notCoveredVal = State.routes.filter(function(r) { return r.jr === 'no'; }).reduce(function(s,r) { return s + r.cost; }, 0);
  var savings = coveredVal + partialVal - passCost;

  el('jr-pass-cost').textContent = passCost > 0 ? fmtJPY(passCost) : 'No Pass';
  el('jr-covered-val').textContent = fmtJPY(coveredVal + partialVal);
  el('jr-savings').textContent = savings >= 0 ? '+' + fmtJPY(savings) + ' savings' : fmtJPY(Math.abs(savings)) + ' short';
  el('jr-savings').className = 'kpi-sub ' + (savings >= 0 ? 'pos' : 'neg');
  el('jr-routes-count').textContent = State.routes.length;
  el('jr-covered-count').textContent = State.routes.filter(function(r) { return r.jr === 'yes' || r.jr === 'partial'; }).length + ' JR covered';
  el('jr-uncovered-val').textContent = fmtJPY(notCoveredVal);
  el('jr-badge').textContent = State.routes.length;
  el('jr-pass-type').value = State.jr.type || '79600';
  el('jr-start-date').value = State.jr.startDate || '';

  var container = el('rail-route-list');
  if (!State.routes.length) {
    container.innerHTML = '<div class="empty-state"><div class="es-icon">🚄</div><div class="es-title">No routes added</div><div class="es-sub">Add your planned train journeys to see JR Pass value</div></div>';
    return;
  }
  container.innerHTML = State.routes.map(function(r) {
    var jrTag = r.jr === 'yes' ? '<span class="tag tag-green">✓ Covered</span>'
      : r.jr === 'partial' ? '<span class="tag tag-amber">Partial</span>'
      : '<span class="tag tag-red">✗ Not Covered</span>';
    return '<div class="rail-route">'
      + '<div class="rail-from-to">'
      + '<div class="rail-cities">' + r.from + ' → ' + r.to + '</div>'
      + '<div class="rail-train">' + (r.train || '') + '</div>'
      + '</div>'
      + '<div class="rail-duration">' + (r.duration || '—') + '</div>'
      + '<div class="rail-cost">' + (r.cost ? fmtJPY(r.cost) : '—') + '</div>'
      + '<div style="width:90px;text-align:right">' + jrTag + '</div>'
      + '<button onclick="deleteRoute(\'' + r.id + '\')" class="btn btn-ghost btn-sm" style="padding:4px 6px;color:var(--text3)">✕</button>'
      + '</div>';
  }).join('');
}

// ══════════════════════════════════════════════════════════
//  PACKING
// ══════════════════════════════════════════════════════════
function getPackItems() {
  if (!State.packItems) {
    State.packItems = DEFAULT_PACK_ITEMS.map(function(i) { return Object.assign({}, i, {id:uid()}); });
    saveState();
  }
  return State.packItems;
}

function togglePacked(itemId) {
  var items = getPackItems();
  var item = items.find(function(i) { return i.id === itemId; });
  if (item) { item.packed = !item.packed; saveState(); renderPage('packing'); renderOverview(); }
}

function addPackItem() {
  var name = el('pack-name-input').value.trim();
  var cat = el('pack-cat-select').value;
  var priority = el('pack-priority-select').value;
  var note = el('pack-note-input').value.trim();
  if (!name) { showToast('Enter item name', 'error'); return; }
  var items = getPackItems();
  items.push({ id: uid(), cat: cat, name: name, note: note, priority: priority, packed: false });
  saveState();
  closeModal('add-pack-item');
  renderPage('packing');
  showToast('Item added', 'success');
  el('pack-name-input').value = '';
  el('pack-note-input').value = '';
}

function deletePackItem(itemId) {
  State.packItems = getPackItems().filter(function(i) { return i.id !== itemId; });
  saveState();
  renderPage('packing');
}

function resetPacking() {
  if (!confirm('Reset all packing checkmarks?')) return;
  getPackItems().forEach(function(i) { i.packed = false; });
  saveState();
  renderPage('packing');
  showToast('Packing list reset', 'info');
}

function renderPacking() {
  var items = getPackItems();
  var packed = items.filter(function(i) { return i.packed; }).length;
  var pct = items.length ? Math.round(packed/items.length*100) : 0;
  el('pack-progress-pct').textContent = pct + '%';
  el('pack-progress-bar').style.width = pct + '%';
  el('pack-count').textContent = packed + '/' + items.length;
  el('badge-packing').textContent = packed + '/' + items.length;

  var cats = {};
  items.forEach(function(i) { if (!cats[i.cat]) cats[i.cat] = []; cats[i.cat].push(i); });

  var priColor = { essential:'var(--red)', important:'var(--amber)', nice:'var(--green)' };
  var priLabel = { essential:'Essential', important:'Important', nice:'Nice' };

  var container = el('packing-list');
  container.innerHTML = Object.keys(cats).map(function(cat) {
    var catItems = cats[cat];
    var catPacked = catItems.filter(function(i) { return i.packed; }).length;
    return '<div class="section-panel" style="margin-bottom:14px">'
      + '<div class="pack-cat-header">'
      + '<div class="pack-cat-name">' + cat + '<span class="badge">' + catPacked + '/' + catItems.length + '</span></div>'
      + '<span class="pack-cat-prog">' + Math.round(catPacked/catItems.length*100) + '%</span>'
      + '</div>'
      + catItems.map(function(item) {
          return '<div class="pack-item-row">'
            + '<div class="pack-check' + (item.packed ? ' packed' : '') + '" onclick="togglePacked(\'' + item.id + '\')">' + (item.packed ? '✓' : '') + '</div>'
            + '<div style="flex:1">'
            + '<div class="pack-item-name' + (item.packed ? ' done' : '') + '">' + item.name + '</div>'
            + (item.note ? '<div class="pack-item-note">' + item.note + '</div>' : '')
            + '</div>'
            + '<span class="pack-priority tag" style="background:rgba(0,0,0,0.2);color:' + (priColor[item.priority]||'var(--text3)') + ';border-color:transparent;font-size:9px">' + (priLabel[item.priority]||item.priority) + '</span>'
            + '<button onclick="deletePackItem(\'' + item.id + '\')" class="btn btn-ghost btn-sm" style="padding:3px 5px;color:var(--text3);font-size:11px">✕</button>'
            + '</div>';
        }).join('')
      + '</div>';
  }).join('');
}

// ══════════════════════════════════════════════════════════
//  CHECKLIST
// ══════════════════════════════════════════════════════════
function getCheckItems() {
  if (!State.checkItems) {
    State.checkItems = DEFAULT_CHECK_ITEMS.map(function(i) { return Object.assign({}, i, {id:uid()}); });
    saveState();
  }
  return State.checkItems;
}

function toggleCheck(itemId) {
  var items = getCheckItems();
  var item = items.find(function(i) { return i.id === itemId; });
  if (item) { item.done = !item.done; saveState(); renderPage('checklist'); renderOverview(); }
}

function addCheckItem() {
  var title = el('check-title-input').value.trim();
  var cat = el('check-cat-select').value;
  var note = el('check-note-input').value.trim();
  if (!title) { showToast('Enter task title', 'error'); return; }
  var items = getCheckItems();
  items.push({ id: uid(), cat: cat, title: title, note: note, done: false });
  saveState();
  closeModal('add-check-item');
  renderPage('checklist');
  showToast('Task added', 'success');
  el('check-title-input').value = '';
  el('check-note-input').value = '';
}

function deleteCheckItem(itemId) {
  State.checkItems = getCheckItems().filter(function(i) { return i.id !== itemId; });
  saveState();
  renderPage('checklist');
}

function renderChecklist() {
  var items = getCheckItems();
  var done = items.filter(function(i) { return i.done; }).length;
  var remaining = items.length - done;
  var pct = items.length ? Math.round(done/items.length*100) : 0;
  el('ck-done').textContent = done;
  el('ck-remaining').textContent = remaining;
  el('ck-total').textContent = items.length;
  el('ck-pct').textContent = pct + '%';
  el('ck-progress-bar').style.width = pct + '%';
  el('badge-checklist').textContent = done + '/' + items.length;

  var catIcons = { Bookings:'📋', Documents:'📄', Money:'💴', Health:'🏥', Packing:'🧳', Research:'🔍', Other:'📝' };
  var cats = {};
  items.forEach(function(i) { if (!cats[i.cat]) cats[i.cat] = []; cats[i.cat].push(i); });

  el('checklist-list').innerHTML = Object.keys(cats).map(function(cat) {
    var catItems = cats[cat];
    var catDone = catItems.filter(function(i) { return i.done; }).length;
    return '<div class="section-panel" style="margin-bottom:14px">'
      + '<div class="section-header">'
      + '<div class="section-title">' + (catIcons[cat]||'📝') + ' ' + cat + '<span class="badge">' + catDone + '/' + catItems.length + '</span></div>'
      + '</div>'
      + catItems.map(function(item) {
          return '<div class="check-row">'
            + '<div class="check-box' + (item.done ? ' done' : '') + '" onclick="toggleCheck(\'' + item.id + '\')">' + (item.done ? '✓' : '') + '</div>'
            + '<div class="check-info">'
            + '<div class="check-title' + (item.done ? ' done' : '') + '">' + item.title + '</div>'
            + (item.note ? '<div class="check-note">' + item.note + '</div>' : '')
            + '</div>'
            + '<button onclick="deleteCheckItem(\'' + item.id + '\')" class="btn btn-ghost btn-sm" style="padding:3px 5px;color:var(--text3);font-size:11px">✕</button>'
            + '</div>';
        }).join('')
      + '</div>';
  }).join('');
}

// ══════════════════════════════════════════════════════════
//  PHRASES
// ══════════════════════════════════════════════════════════
var currentPhraseFilter = 'all';

function filterPhrases(filter, btn) {
  currentPhraseFilter = filter;
  document.querySelectorAll('[id^="phrase-filter-"]').forEach(function(b) {
    b.className = 'btn btn-ghost btn-sm';
  });
  if (btn) {
    btn.style.background = 'rgba(232,53,74,0.12)';
    btn.style.color = 'var(--accent)';
    btn.style.borderColor = 'rgba(232,53,74,0.2)';
  }
  renderPhrases();
}

function copyPhrase(text) {
  navigator.clipboard && navigator.clipboard.writeText(text).then(function() {
    showToast('Copied: ' + text, 'success');
  }).catch(function() {
    showToast('Copied!', 'success');
  });
}

function renderPhrases() {
  var filtered = currentPhraseFilter === 'all' ? PHRASES_DATA : PHRASES_DATA.filter(function(p) { return p.cat === currentPhraseFilter; });
  var cats = {};
  filtered.forEach(function(p) { if (!cats[p.cat]) cats[p.cat] = []; cats[p.cat].push(p); });
  var catLabels = { essentials:'🗣 Essentials', food:'🍜 Food & Dining', transport:'🚄 Transport', shopping:'🛍 Shopping' };

  el('phrases-container').innerHTML = Object.keys(cats).map(function(cat) {
    return '<div class="section-panel" style="margin-bottom:14px">'
      + '<div class="section-header"><div class="section-title">' + (catLabels[cat]||cat) + '</div></div>'
      + cats[cat].map(function(p) {
          return '<div class="phrase-row">'
            + '<div style="flex:1">'
            + '<div class="phrase-jp">' + p.jp + '</div>'
            + '<div class="phrase-romaji">' + p.romaji + '</div>'
            + '<div class="phrase-en">' + p.en + '</div>'
            + '</div>'
            + '<button class="phrase-copy" onclick="copyPhrase(\'' + p.jp.replace(/'/g, "\\'") + '\')">copy</button>'
            + '</div>';
        }).join('')
      + '</div>';
  }).join('');
}

// ══════════════════════════════════════════════════════════
//  OVERVIEW
// ══════════════════════════════════════════════════════════
function renderOverview() {
  var dep = State.settings.depart;
  var ret = State.settings.returnDate;
  var rate = State.settings.rate || 155;
  var daysUntilDep = dep ? daysUntil(dep) : null;
  var tripDuration = dep && ret ? daysBetween(dep, ret) : 0;

  // Countdown
  if (daysUntilDep !== null) {
    if (daysUntilDep > 0) {
      el('countdown-days').textContent = daysUntilDep;
      el('countdown-label') && (el('countdown-label').textContent = 'Days Until Japan');
      el('countdown-date').textContent = 'Departing ' + formatDate(dep) + (ret ? ' · Returning ' + formatDate(ret) : '');
    } else if (daysUntilDep === 0) {
      el('countdown-days').textContent = '今日';
      el('countdown-date').textContent = 'Today is the day! Have an amazing trip! 🎉';
    } else {
      el('countdown-days').textContent = Math.abs(daysUntilDep);
      el('countdown-label') && (el('countdown-label').textContent = 'Days In Japan');
      el('countdown-date').textContent = 'You\'re there! Enjoying Japan right now 🗾';
    }
    el('sb-countdown').textContent = daysUntilDep > 0 ? daysUntilDep : (daysUntilDep === 0 ? 'Today!' : 'In Japan!');
    el('sb-trip-dates').textContent = dep + (ret ? ' – ' + ret : '');
  } else {
    el('countdown-days').textContent = '—';
    el('sb-countdown').textContent = '—';
    el('sb-trip-dates').textContent = 'Set dates in Settings';
  }

  // KPIs
  el('kpi-days').textContent = tripDuration ? tripDuration + ' days' : '—';
  el('kpi-dates').textContent = dep && ret ? formatDate(dep) + ' – ' + formatDate(ret) : 'No dates set';

  var totalBudget = State.budgetCats.reduce(function(s,c) { return s + c.budget; }, 0);
  var totalSpent = State.expenses.reduce(function(s,e) { return s + e.amount; }, 0);
  el('kpi-budget').textContent = fmtJPY(totalBudget);
  el('kpi-budget-sub').textContent = fmtJPY(totalSpent) + ' spent';

  var packItems = State.packItems || DEFAULT_PACK_ITEMS;
  var packed = packItems.filter(function(i) { return i.packed; }).length;
  var packPct = packItems.length ? Math.round(packed/packItems.length*100) : 0;
  el('kpi-packing').textContent = packPct + '%';
  el('kpi-packing-sub').textContent = packed + ' / ' + packItems.length + ' items';

  var checkItems = State.checkItems || DEFAULT_CHECK_ITEMS;
  var checkDone = checkItems.filter(function(i) { return i.done; }).length;
  var checkPct = checkItems.length ? Math.round(checkDone/checkItems.length*100) : 0;
  el('kpi-tasks').textContent = checkPct + '%';
  el('kpi-tasks-sub').textContent = checkDone + ' / ' + checkItems.length + ' done';

  var cities = {};
  State.days.forEach(function(d) { if (d.city) cities[d.city] = true; });
  var cityNames = Object.keys(cities);
  el('kpi-cities').textContent = cityNames.length || '0';
  el('kpi-cities-sub').textContent = cityNames.length ? cityNames.join(' · ') : 'No cities yet';

  el('kpi-rate').textContent = '¥' + rate.toFixed(0);

  // City schedule
  var scheduleEl = el('city-schedule-list');
  if (!cityNames.length) {
    scheduleEl.innerHTML = '<div class="empty-state"><div class="es-icon">🗾</div><div class="es-title">No cities added yet</div><div class="es-sub">Add days with city names in Itinerary</div></div>';
  } else {
    var cityDays = {};
    State.days.forEach(function(d) {
      if (d.city) {
        if (!cityDays[d.city]) cityDays[d.city] = 0;
        cityDays[d.city]++;
      }
    });
    scheduleEl.innerHTML = Object.keys(cityDays).map(function(city) {
      return '<div class="budget-row">'
        + '<div class="budget-cat"><div class="budget-cat-name">📍 ' + city + '</div></div>'
        + '<span class="tag tag-muted">' + cityDays[city] + ' day' + (cityDays[city]>1?'s':'') + '</span>'
        + '</div>';
    }).join('');
  }

  // Budget snapshot
  var bsEl = el('budget-snapshot');
  if (!State.budgetCats.length) {
    bsEl.innerHTML = '<div class="empty-state"><div class="es-icon">💴</div><div class="es-title">Budget not set</div><div class="es-sub">Add categories in Budget page</div></div>';
  } else {
    bsEl.innerHTML = State.budgetCats.slice(0,4).map(function(cat) {
      var spent = State.expenses.filter(function(e) { return e.catId === cat.id; }).reduce(function(s,e) { return s + e.amount; }, 0);
      var pct = cat.budget ? Math.min(100, Math.round(spent/cat.budget*100)) : 0;
      return '<div class="budget-row">'
        + '<div class="budget-cat">'
        + '<div class="budget-cat-name">' + cat.name + '</div>'
        + '<div class="budget-bar" style="margin-top:4px"><div class="budget-fill" style="width:' + pct + '%;background:' + cat.color + '"></div></div>'
        + '</div>'
        + '<div class="budget-amounts"><div class="budget-spent">' + fmtJPY(spent) + '</div><div class="budget-limit">of ' + fmtJPY(cat.budget) + '</div></div>'
        + '</div>';
    }).join('');
  }

  // Next Up
  var today = new Date(); today.setHours(0,0,0,0);
  var upcomingDays = State.days.filter(function(d) {
    if (!d.date) return false;
    var dd = new Date(d.date + 'T00:00:00');
    return dd >= today;
  }).slice(0,3);

  var nextUpEl = el('next-up-list');
  if (!upcomingDays.length) {
    nextUpEl.innerHTML = '<div class="empty-state"><div class="es-icon">📅</div><div class="es-title">No upcoming days</div><div class="es-sub">Add dated days in Itinerary</div></div>';
  } else {
    nextUpEl.innerHTML = upcomingDays.map(function(day) {
      var evts = State.events.filter(function(e) { return e.dayId === day.id; }).slice(0,3);
      return '<div class="event-row" style="align-items:flex-start;padding:14px 18px">'
        + '<div style="flex-shrink:0;margin-right:4px">'
        + '<div class="day-num" style="width:36px;height:36px;font-size:10px">' + formatDate(day.date).split(' ')[0].substr(0,3).toUpperCase() + '<br>' + new Date(day.date+'T00:00:00').getDate() + '</div>'
        + '</div>'
        + '<div style="flex:1">'
        + '<div style="font-family:var(--display);font-size:14px;font-weight:600;color:var(--text)">' + day.title + '</div>'
        + (day.city ? '<div style="font-size:11px;color:var(--text3);margin-bottom:6px">📍 ' + day.city + '</div>' : '')
        + evts.map(function(e) {
            return '<div style="font-size:12px;color:var(--text2);margin-bottom:2px">' + e.type + ' ' + e.name + (e.time ? ' <span style="color:var(--text3)">' + e.time + '</span>' : '') + '</div>';
          }).join('')
        + (State.events.filter(function(e) { return e.dayId === day.id; }).length > 3 ? '<div style="font-size:11px;color:var(--text3)">+' + (State.events.filter(function(e){return e.dayId===day.id;}).length-3) + ' more…</div>' : '')
        + '</div>'
        + '</div>';
    }).join('');
  }

  el('overview-subtitle').textContent = dep
    ? 'Trip to Japan' + (tripDuration ? ' · ' + tripDuration + ' days' : '') + (daysUntilDep > 0 ? ' · Departing in ' + daysUntilDep + ' days' : '')
    : 'Your Japan adventure at a glance';
}

// ══════════════════════════════════════════════════════════
//  DATA MANAGEMENT
// ══════════════════════════════════════════════════════════
function exportData() {
  var data = { settings: State.settings, days: State.days, events: State.events, budgetCats: State.budgetCats, expenses: State.expenses, routes: State.routes, packItems: State.packItems, checkItems: State.checkItems, jr: State.jr };
  var blob = new Blob([JSON.stringify(data, null, 2)], {type:'application/json'});
  var a = document.createElement('a');
  a.href = URL.createObjectURL(blob);
  a.download = 'japan-dash-backup-' + new Date().toISOString().split('T')[0] + '.json';
  a.click();
  showToast('Data exported!', 'success');
}

function importDataPrompt() {
  var input = document.createElement('input');
  input.type = 'file';
  input.accept = '.json';
  input.onchange = function(e) {
    var file = e.target.files[0];
    if (!file) return;
    var reader = new FileReader();
    reader.onload = function(ev) {
      try {
        var data = JSON.parse(ev.target.result);
        if (data.settings) State.settings = data.settings;
        if (data.days) State.days = data.days;
        if (data.events) State.events = data.events;
        if (data.budgetCats) State.budgetCats = data.budgetCats;
        if (data.expenses) State.expenses = data.expenses;
        if (data.routes) State.routes = data.routes;
        if (data.packItems) State.packItems = data.packItems;
        if (data.checkItems) State.checkItems = data.checkItems;
        if (data.jr) State.jr = data.jr;
        saveState();
        loadSettingsForm();
        renderAll();
        showToast('Data imported!', 'success');
      } catch(err) {
        showToast('Invalid JSON file', 'error');
      }
    };
    reader.readAsText(file);
  };
  input.click();
}

function confirmClearAll() {
  if (!confirm('Clear ALL trip data? This cannot be undone.')) return;
  State.days = []; State.events = []; State.budgetCats = []; State.expenses = []; State.routes = [];
  State.packItems = null; State.checkItems = null;
  State.settings = { depart: '', returnDate: '', rate: 155 };
  State.jr = { type: '79600', startDate: '' };
  saveState();
  loadSettingsForm();
  renderAll();
  showToast('All data cleared', 'info');
}

// ══════════════════════════════════════════════════════════
//  ACTIVITY PRICING DATA
// ══════════════════════════════════════════════════════════
var PRICING_DATA = [
  // Pre-Trip
  { day: 'Pre-Trip', date: '', city: 'Pre-Trip', label: '📱 WiFi / Data', activities: [
    { name: 'Pocket WiFi (airport pickup)', min: 26, max: 26, note: '~$1.85/day × 14 days', free: false, klook: true },
    { name: 'eSIM (Softbank/Docomo, unlimited)', min: 5.35, max: 5.35, note: '💡 Best value — no pickup required', free: false, klook: true },
  ]},
  // Apr 28
  { day: 'Tuesday, April 28', date: '2025-04-28', city: 'Tokyo', label: '📅 Tuesday Apr 28', activities: [
    { name: 'Sensō-ji Temple', min: 0, max: 0, note: 'Asakusa — always open', free: true },
  ]},
  // Apr 29
  { day: 'Wednesday, April 29', date: '2025-04-29', city: 'Tokyo', label: '📅 Wednesday Apr 29', activities: [
    { name: 'Asakusa Mameshiba Cafe', min: 7, max: 15, note: 'Entry + interaction fee', free: false, klook: true },
    { name: 'Cinnamoroll Cafe', min: 3, max: 5, note: 'Reservation fee + food extra', free: false },
    { name: 'Meiji Jingu', min: 0, max: 7, note: 'Free entry · Inner Hall ~$7 optional', free: false },
    { name: 'Takeshita Street / Shibuya Crossing / Hachiko', min: 0, max: 0, note: 'Free exploration', free: true },
    { name: 'HARRY Otter Cafe', min: 25, max: 35, note: 'Reservation required', free: false, klook: true },
    { name: 'Street Go-Kart (Shibuya)', min: 65.25, max: 65.25, note: 'Klook price', free: false, klook: true },
  ]},
  // Apr 30
  { day: 'Thursday, April 30', date: '2025-04-30', city: 'Tokyo', label: '📅 Thursday Apr 30', activities: [
    { name: 'Sanrio Puroland', min: 4.19, max: 4.19, note: 'Varies by date — check Klook', free: false, klook: true },
    { name: 'ICHIRAN Ramen', min: 10, max: 15, note: 'Solo booth ramen experience', free: false },
    { name: 'Omoide Yokocho', min: 0, max: 0, note: 'Free entry · food extra', free: true },
    { name: 'Sumo Show (Shinjuku)', min: 70.75, max: 70.75, note: 'Klook price', free: false, klook: true },
  ]},
  // May 1 — Fuji
  { day: 'Friday, May 1 — Mt. Fuji', date: '2025-05-01', city: 'Mt. Fuji', label: '📅 Friday May 1 · Mt. Fuji Day', activities: [
    { name: 'Mount Fuji 5th Station', min: 0, max: 0, note: 'Free · bus ~$25–30 round trip', free: true },
    { name: 'Arakurayama Sengen Park', min: 0, max: 0, note: 'Iconic pagoda view — free', free: true },
    { name: 'Oshino Hakkai', min: 1, max: 1, note: '~$1 donation', free: false },
    { name: 'Oishi Park', min: 0, max: 0, note: 'Lake Kawaguchi lakeside — free', free: true },
  ]},
  // May 2
  { day: 'Saturday, May 2', date: '2025-05-02', city: 'Tokyo', label: '📅 Saturday May 2', activities: [
    { name: 'Arcades (TAITO / GiGO / etc.)', min: 10, max: 30, note: 'Depends how much you play', free: false },
    { name: 'Wagyu Yakiniku Ushihachi', min: 30, max: 60, note: 'Per person estimate', free: false },
    { name: 'teamLab Planets', min: 28.19, max: 28.19, note: 'Klook — book ahead!', free: false, klook: true },
    { name: 'Kirby Café', min: 3, max: 3, note: 'Reservation fee + food extra', free: false },
  ]},
  // May 3 — Tokyo → Osaka
  { day: 'Sunday, May 3 — Tokyo → Osaka', date: '2025-05-03', city: 'Osaka', label: '📅 Sunday May 3 · Tokyo → Osaka', activities: [
    { name: 'Shinkansen (Bullet Train)', min: 87.95, max: 87.95, note: 'Klook · or use JR Pass', free: false, klook: true },
    { name: 'Osaka Amazing Pass (1-day)', min: 21.99, max: 21.99, note: 'Includes subway + many attractions', free: false, klook: true },
    { name: 'Katsuoji Temple', min: 3, max: 3, note: 'Daruma temple — small entry fee', free: false },
    { name: 'Dotonbori / Don Quijote', min: 0, max: 0, note: 'Free to explore · food extra', free: true },
    { name: 'Round 1 (Osaka)', min: 5, max: 15, note: 'Bowling, arcade, sports', free: false },
  ]},
  // May 4 — Nara + Osaka
  { day: 'Monday, May 4 — Nara + Osaka', date: '2025-05-04', city: 'Nara', label: '📅 Monday May 4 · Nara + Osaka', activities: [
    { name: 'Nara Park (deer)', min: 0, max: 0, note: 'Free · deer crackers ~$1.50', free: true },
    { name: 'Tōdai-ji (Great Buddha)', min: 7, max: 7, note: 'Admission fee', free: false },
    { name: 'Pokémon Café (Osaka)', min: 3, max: 5, note: 'Reservation fee + food extra', free: false },
    { name: 'Kushikatsu Ittoku', min: 15, max: 25, note: 'Per person for kushikatsu dinner', free: false },
    { name: 'Tsutenkaku Tower', min: 7, max: 7, note: 'Shinsekai tower admission', free: false },
  ]},
  // May 5 — Kyoto
  { day: 'Tuesday, May 5 — Kyoto', date: '2025-05-05', city: 'Kyoto', label: '📅 Tuesday May 5 · Kyoto', activities: [
    { name: 'Arashiyama Bamboo Forest', min: 0, max: 0, note: 'Free — morning for fewer crowds', free: true },
    { name: 'Fushimi Inari Taisha', min: 0, max: 0, note: 'Free — thousands of torii gates', free: true },
    { name: 'Kiyomizu-dera', min: 3.50, max: 3.50, note: 'Admission fee', free: false },
    { name: 'Higashiyama / Gion District', min: 0, max: 0, note: 'Free to walk · shops/food extra', free: true },
    { name: 'glänta Kyoto (Scandinavian restaurant)', min: 15, max: 30, note: 'Dinner estimate', free: false },
  ]},
  // May 6 — USJ
  { day: 'Wednesday, May 6 — USJ', date: '2025-05-06', city: 'Osaka', label: '📅 Wednesday May 6 · Universal Studios Japan', activities: [
    { name: 'Universal Studios Japan', min: 56.10, max: 85, note: 'From $56.10 · peak dates $75–85 · Klook', free: false, klook: true },
  ]},
  // May 7 — Okinawa
  { day: 'Thursday, May 7 — Okinawa', date: '2025-05-07', city: 'Okinawa', label: '📅 Thursday May 7 · Okinawa', activities: [
    { name: 'Car Rental (Okinawa)', min: 19, max: 19, note: '~$19/day — needed for north island', free: false },
    { name: 'Churaumi Aquarium', min: 14.10, max: 14.10, note: 'One of the world\'s largest', free: false, klook: true },
    { name: 'Kouri Bridge / Cape Manzamo', min: 0, max: 0, note: 'Scenic coastal spots — free', free: true },
    { name: 'Emerald Beach', min: 0.50, max: 0.50, note: 'Inside Ocean Expo Park', free: false },
  ]},
  // May 8 — Kerama
  { day: 'Friday, May 8', date: '2025-05-08', city: 'Okinawa', label: '📅 Friday May 8', activities: [
    { name: 'Kerama Islands Snorkeling Day Trip', min: 56.59, max: 56.59, note: 'Klook — includes boat + gear', free: false, klook: true },
  ]},
  // May 9 — Blue Cave
  { day: 'Saturday, May 9', date: '2025-05-09', city: 'Okinawa', label: '📅 Saturday May 9', activities: [
    { name: 'Blue Cave Snorkeling', min: 29.95, max: 29.95, note: 'Klook — famous sea cave', free: false, klook: true },
    { name: 'American Village', min: 0, max: 0, note: 'Free to explore · shopping/food extra', free: true },
  ]},
  // May 10
  { day: 'Sunday, May 10', date: '2025-05-10', city: 'Okinawa', label: '📅 Sunday May 10', activities: [
    { name: 'Shuri Castle', min: 3, max: 3, note: 'UNESCO World Heritage Site', free: false },
    { name: 'Kokusai Street', min: 0, max: 0, note: 'Main shopping street — free to walk', free: true },
    { name: 'Amigo Tacos / Yunangi (dinner)', min: 15, max: 30, note: 'Okinawan cuisine estimate', free: false },
  ]},
];

var currentPricingFilter = 'all';

function filterPricing(filter, btn) {
  currentPricingFilter = filter;
  document.querySelectorAll('[id^="pf-"]').forEach(function(b) {
    b.style.background = '';
    b.style.color = '';
    b.style.borderColor = '';
    b.className = 'btn btn-ghost btn-sm';
  });
  if (btn) {
    btn.className = 'btn btn-sm';
    btn.style.background = 'rgba(232,53,74,0.12)';
    btn.style.color = 'var(--accent)';
    btn.style.border = '1px solid rgba(232,53,74,0.2)';
  }
  renderPricing();
}

function renderPricing() {
  // Flatten all activities for KPI calculation
  var allActs = [];
  PRICING_DATA.forEach(function(day) { day.activities.forEach(function(a) { allActs.push(a); }); });

  var freeCount = allActs.filter(function(a) { return a.free; }).length;
  var minTotal = allActs.reduce(function(s, a) { return s + (a.min || 0); }, 0);
  var maxTotal = allActs.reduce(function(s, a) { return s + (a.max || 0); }, 0);

  el('pr-total-count').textContent = allActs.length;
  el('pr-free-count').textContent = freeCount;
  el('pr-min-total').textContent = '$' + minTotal.toFixed(0);
  el('pr-max-total').textContent = '$' + maxTotal.toFixed(0);

  // Filter days
  var filtered = PRICING_DATA.map(function(day) {
    var acts = day.activities.filter(function(a) {
      if (currentPricingFilter === 'all') return true;
      if (currentPricingFilter === 'free') return a.free;
      if (currentPricingFilter === 'paid') return !a.free;
      return day.city === currentPricingFilter;
    });
    return { day: day, activities: acts };
  }).filter(function(d) { return d.activities.length > 0; });

  var container = el('pricing-container');
  if (!filtered.length) {
    container.innerHTML = '<div class="empty-state"><div class="es-icon">🎟</div><div class="es-title">No activities match filter</div></div>';
    return;
  }

  var cityColors = {
    'Tokyo': 'var(--accent)', 'Mt. Fuji': 'var(--blue)', 'Osaka': 'var(--amber)',
    'Nara': 'var(--green)', 'Kyoto': 'var(--sakura)', 'Okinawa': 'var(--teal, #2eccc8)',
    'Pre-Trip': 'var(--text3)'
  };

  container.innerHTML = filtered.map(function(d) {
    var day = d.day;
    var acts = d.activities;
    var dayMin = acts.reduce(function(s,a) { return s + a.min; }, 0);
    var dayMax = acts.reduce(function(s,a) { return s + a.max; }, 0);
    var cityColor = cityColors[day.city] || 'var(--accent)';
    var cityTag = '<span class="tag" style="background:rgba(0,0,0,0.2);color:' + cityColor + ';border-color:rgba(0,0,0,0.1)">' + day.city + '</span>';

    return '<div class="section-panel" style="margin-bottom:16px">'
      + '<div class="section-header">'
      + '<div class="section-title">' + day.label + ' ' + cityTag + '</div>'
      + (dayMin > 0 || dayMax > 0
          ? '<div style="font-family:var(--mono);font-size:12px;color:var(--text2)">'
            + (dayMin === dayMax ? '$' + dayMin.toFixed(2) : '$' + dayMin.toFixed(0) + '–$' + dayMax.toFixed(0))
            + ' <span style="color:var(--text3);font-size:10px">est/person</span></div>'
          : '<span class="tag tag-green">All Free</span>')
      + '</div>'
      + '<table class="data-table">'
      + '<thead><tr>'
      + '<th>Activity</th>'
      + '<th>Note</th>'
      + '<th class="right" style="width:110px">Cost (USD)</th>'
      + '<th class="right" style="width:60px">Source</th>'
      + '</tr></thead>'
      + '<tbody>'
      + acts.map(function(a) {
          var costCell;
          if (a.free) {
            costCell = '<span class="tag tag-green">FREE</span>';
          } else if (a.min === a.max) {
            costCell = '<span style="font-family:var(--mono);color:var(--gold)">$' + a.min.toFixed(2) + '</span>';
          } else {
            costCell = '<span style="font-family:var(--mono);color:var(--amber)">$' + a.min.toFixed(0) + '–$' + a.max.toFixed(0) + '</span>';
          }
          var sourceCell = a.klook
            ? '<span class="tag tag-blue" style="font-size:9px">Klook</span>'
            : '<span class="tag tag-muted" style="font-size:9px">Est.</span>';
          return '<tr>'
            + '<td style="font-size:13px;color:var(--text)">' + a.name + '</td>'
            + '<td style="font-size:11px;color:var(--text3)">' + (a.note || '') + '</td>'
            + '<td class="right">' + costCell + '</td>'
            + '<td class="right">' + sourceCell + '</td>'
            + '</tr>';
        }).join('')
      + '</tbody></table>'
      + (acts.length > 1 && (dayMin > 0 || dayMax > 0)
          ? '<div style="padding:10px 20px;border-top:1px solid var(--border);display:flex;justify-content:flex-end;gap:6px;font-size:11px;color:var(--text3)">'
            + 'Day total estimate: <span style="font-family:var(--mono);color:var(--text)">'
            + (dayMin === dayMax ? '$' + dayMin.toFixed(2) : '$' + dayMin.toFixed(0) + ' – $' + dayMax.toFixed(0))
            + '</span></div>'
          : '')
      + '</div>';
  }).join('');
}

// ══════════════════════════════════════════════════════════
//  RENDER ROUTER
// ══════════════════════════════════════════════════════════
function renderPage(pageId) {
  switch(pageId) {
    case 'overview': renderOverview(); break;
    case 'itinerary': renderItinerary(); break;
    case 'budget': renderBudget(); break;
    case 'exchange': renderExchange(); break;
    case 'rail': renderRail(); break;
    case 'packing': renderPacking(); break;
    case 'checklist': renderChecklist(); break;
    case 'phrases': renderPhrases(); break;
    case 'pricing': renderPricing(); break;
    case 'settings': loadSettingsForm(); break;
  }
}

function renderAll() {
  renderOverview();
  renderItinerary();
  renderBudget();
  renderExchange();
  renderRail();
  renderPacking();
  renderChecklist();
  renderPhrases();
  renderPricing();
  loadSettingsForm();
}

// ══════════════════════════════════════════════════════════
//  BOOT
// ══════════════════════════════════════════════════════════
document.addEventListener('DOMContentLoaded', function() {
  // Init defaults
  getPackItems();
  getCheckItems();
  loadSettingsForm();
  renderAll();
});
</script>
</body>
</html>
