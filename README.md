<!doctype html>
<html lang="tr">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1.0,viewport-fit=cover"/>
<title>Pro Camera Demo — Analog Presets + Grain</title>
<style>
  :root{
    --bg:#0f1115; --card:#111217; --muted:#9aa0a6; --accent:#e6a85e;
    --glass: rgba(255,255,255,0.03);
  }
  *{box-sizing:border-box}
  body{margin:0;font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,"Helvetica Neue",Arial;color:#eef2f3;background:linear-gradient(180deg,#0b0c0e 0%, #0f1115 100%);display:flex;flex-direction:column;height:100vh}
  header{display:flex;align-items:center;justify-content:space-between;padding:12px 16px;background:transparent}
  .brand{display:flex;align-items:center;gap:10px}
  .logo{width:36px;height:36px;border-radius:8px;background:linear-gradient(135deg,#f6d9b0,#e6a85e);display:flex;align-items:center;justify-content:center;font-weight:700;color:#1b1b1b}
  h1{font-size:16px;margin:0;font-weight:600}
  .muted{color:var(--muted);font-size:12px}

  main{flex:1;display:flex;gap:14px;padding:12px}
  /* Left: camera preview area */
  .stage{flex:1;min-width:240px;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:8px}
  .camera-wrap{position:relative;width:100%;max-width:720px;background:#000;border-radius:14px;overflow:hidden;box-shadow:0 6px 30px rgba(0,0,0,0.6)}
  video{width:100%;height:auto;display:block;object-fit:cover; background:#000}
  canvas{width:100%;height:auto;display:block}

  /* controls overlay */
  .overlay-controls{position:absolute;left:12px;right:12px;bottom:12px;display:flex;align-items:center;justify-content:space-between;gap:8px;pointer-events:none}
  .control-left, .control-right{display:flex;gap:8px;align-items:center;pointer-events:auto}
  .btn{background:var(--glass);border:1px solid rgba(255,255,255,0.03);padding:8px 12px;border-radius:10px;color:#fff;font-weight:600;backdrop-filter: blur(6px);cursor:pointer}
  .btn-ghost{background:transparent;border:1px solid rgba(255,255,255,0.0
