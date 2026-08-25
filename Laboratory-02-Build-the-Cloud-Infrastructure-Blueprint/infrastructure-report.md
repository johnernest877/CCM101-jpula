<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Cloud Infrastructure Report — ubuntu</title>
<style>
  :root{
    --bg: #0b0f0d;
    --panel: #101613;
    --line: #1f2c26;
    --fg: #d7e6dd;
    --dim: #6f8a7c;
    --accent: #5ee6a0;
    --accent-dim: #2f6b4d;
    --amber: #e6c15e;
    --mono: "JetBrains Mono","Fira Code",ui-monospace,"SFMono-Regular",Menlo,Consolas,monospace;
  }
  *{box-sizing:border-box;}
  body{
    margin:0;
    background:
      radial-gradient(ellipse at top left, rgba(94,230,160,0.06), transparent 60%),
      var(--bg);
    color:var(--fg);
    font-family:var(--mono);
    padding:40px 16px 80px;
    line-height:1.5;
  }
  .wrap{max-width:880px;margin:0 auto;}

  /* header */
  .bar{
    display:flex;justify-content:space-between;align-items:baseline;
    border-bottom:1px solid var(--line);
    padding-bottom:14px;margin-bottom:8px;
    font-size:12px;color:var(--dim);letter-spacing:.04em;
  }
  .bar .dot{color:var(--accent);}
  h1{
    font-size:22px;margin:18px 0 2px;color:var(--fg);
    letter-spacing:.01em;
  }
  h1 .caret{color:var(--accent);animation:blink 1.1s steps(1) infinite;}
  @keyframes blink{50%{opacity:0;}}
  .sub{color:var(--dim);font-size:13px;margin-bottom:36px;}
  .sub b{color:var(--amber);font-weight:600;}

  /* section header = shell prompt */
  .prompt{
    display:flex;gap:10px;align-items:center;
    margin:38px 0 14px;
    font-size:13px;
  }
  .prompt .n{color:var(--accent-dim);}
  .prompt .cmd{color:var(--accent);}
  .prompt .path{color:var(--dim);}
  .prompt::after{
    content:"";flex:1;height:1px;background:var(--line);margin-left:8px;
  }

  .panel{
    background:var(--panel);
    border:1px solid var(--line);
    border-radius:6px;
    padding:18px 20px;
  }

  /* key: value rows */
  .kv{display:grid;grid-template-columns:150px 1fr;row-gap:9px;font-size:14px;}
  .kv dt{color:var(--dim);}
  .kv dd{margin:0;color:var(--fg);}
  .kv dd b{color:var(--accent);font-weight:600;}

  /* tables */
  table{width:100%;border-collapse:collapse;font-size:13px;}
  th{
    text-align:left;color:var(--dim);font-weight:500;
    font-size:11px;text-transform:uppercase;letter-spacing:.06em;
    padding:0 10px 8px;border-bottom:1px solid var(--line);
  }
  td{padding:7px 10px;border-bottom:1px solid rgba(255,255,255,0.03);}
  tr:last-child td{border-bottom:none;}
  td.num, th.num{text-align:right;font-variant-numeric:tabular-nums;}
  td.mount{color:var(--accent);}

  /* usage bar */
  .usage{display:flex;align-items:center;gap:8px;}
  .usage .track{
    width:70px;height:6px;background:#152019;border-radius:3px;overflow:hidden;
    border:1px solid var(--line);
  }
  .usage .fill{height:100%;background:linear-gradient(90deg,var(--accent-dim),var(--accent));}
  .usage .pct{font-size:12px;color:var(--dim);width:32px;}

  /* two-col grid for cpu/mem */
  .grid2{display:grid;grid-template-columns:1fr 1fr;gap:16px;}
  @media (max-width:640px){.grid2{grid-template-columns:1fr;}}

  .badge{
    display:inline-block;font-size:11px;padding:2px 8px;border-radius:20px;
    border:1px solid var(--accent-dim);color:var(--accent);letter-spacing:.03em;
  }

  code, .code{
    background:#0e1512;border:1px solid var(--line);border-radius:4px;
    padding:1px 6px;color:var(--amber);font-size:0.92em;
  }

  ul.ips{list-style:none;margin:0;padding:0;font-size:14px;}
  ul.ips li{padding:6px 0;border-bottom:1px dashed var(--line);}
  ul.ips li:last-child{border:none;}
  ul.ips li::before{content:"→ ";color:var(--accent);}

  pre{
    background:#0e1512;border:1px solid var(--line);border-radius:6px;
    padding:16px 18px;font-size:13px;overflow-x:auto;color:var(--fg);
    margin:0;
  }
  pre .c{color:var(--dim);}
  pre .p{color:var(--accent);}

  .summary{
    font-size:14px;color:var(--fg);
    border-left:2px solid var(--accent-dim);
    padding:4px 0 4px 18px;
  }
  .summary b{color:var(--amber);}

  footer{
    margin-top:56px;padding-top:16px;border-top:1px solid var(--line);
    font-size:11px;color:var(--dim);display:flex;justify-content:space-between;
  }
</style>
</head>
<body>
<div class="wrap">

  <div class="bar">
    <span><span class="dot">●</span> SYSTEM REPORT / live snapshot</span>
    <span>host: ubuntu · env: killercoda</span>
  </div>

  <h1>Cloud Infrastructure Report<span class="caret">_</span></h1>
  <div class="sub">Diagnostic snapshot of the provisioned KillerCoda cloud instance — collected via <b>8</b> shell commands.</div>

  <!-- OS / KERNEL -->
  <div class="prompt"><span class="n">01</span><span class="cmd">lsb_release -a && uname -r</span></div>
  <div class="panel">
    <dl class="kv">
      <dt>OS</dt><dd><b>Ubuntu 24.04.4 LTS</b></dd>
      <dt>Codename</dt><dd>Noble <span class="badge">LTS</span></dd>
      <dt>Kernel</dt><dd><span class="code">6.8.0-138-generic</span></dd>
    </dl>
  </div>

  <!-- CPU / MEM -->
  <div class="prompt"><span class="n">02</span><span class="cmd">lscpu | grep "Model name" && nproc && free -h</span></div>
  <div class="grid2">
    <div class="panel">
      <dl class="kv">
        <dt>CPU model</dt><dd><b>Intel Xeon E312xx</b></dd>
        <dt>Platform</dt><dd>Sandy Bridge, IBRS update</dd>
        <dt>Cores</dt><dd><b>1</b> vCPU</dd>
      </dl>
    </div>
    <div class="panel">
      <dl class="kv">
        <dt>Total RAM</dt><dd><b>1.9 GiB</b></dd>
        <dt>Used</dt><dd>453 MiB</dd>
        <dt>Free</dt><dd>747 MiB</dd>
        <dt>Available</dt><dd>1.4 GiB</dd>
        <dt>Swap</dt><dd>1.0 GiB</dd>
      </dl>
    </div>
  </div>

  <!-- DISK -->
  <div class="prompt"><span class="n">03</span><span class="cmd">df -h</span></div>
  <div class="panel">
    <table>
      <thead><tr><th>Filesystem</th><th class="num">Size</th><th class="num">Used</th><th class="num">Avail</th><th>Usage</th><th>Mount</th></tr></thead>
      <tbody>
        <tr>
          <td><span class="code">/dev/vda1</span></td>
          <td class="num">19G</td><td class="num">5.4G</td><td class="num">13G</td>
          <td><div class="usage"><div class="track"><div class="fill" style="width:30%"></div></div><span class="pct">30%</span></div></td>
          <td class="mount">/</td>
        </tr>
      </tbody>
    </table>
  </div>

  <!-- MOUNTS -->
  <div class="prompt"><span class="n">04</span><span class="cmd">df -h</span><span class="path">&nbsp;(all)</span></div>
  <div class="panel">
    <table>
      <thead><tr><th>Filesystem</th><th class="num">Size</th><th class="num">Used</th><th class="num">Avail</th><th>Usage</th><th>Mount</th></tr></thead>
      <tbody>
        <tr><td>tmpfs</td><td class="num">191M</td><td class="num">996K</td><td class="num">190M</td>
          <td><div class="usage"><div class="track"><div class="fill" style="width:1%"></div></div><span class="pct">1%</span></div></td><td class="mount">/run</td></tr>
        <tr><td><span class="code">/dev/vda1</span></td><td class="num">19G</td><td class="num">5.4G</td><td class="num">13G</td>
          <td><div class="usage"><div class="track"><div class="fill" style="width:30%"></div></div><span class="pct">30%</span></div></td><td class="mount">/</td></tr>
        <tr><td>tmpfs</td><td class="num">952M</td><td class="num">84K</td><td class="num">952M</td>
          <td><div class="usage"><div class="track"><div class="fill" style="width:1%"></div></div><span class="pct">1%</span></div></td><td class="mount">/dev/shm</td></tr>
        <tr><td>tmpfs</td><td class="num">5.0M</td><td class="num">0</td><td class="num">5.0M</td>
          <td><div class="usage"><div class="track"><div class="fill" style="width:0%"></div></div><span class="pct">0%</span></div></td><td class="mount">/run/lock</td></tr>
        <tr><td><span class="code">/dev/vda16</span></td><td class="num">881M</td><td class="num">117M</td><td class="num">703M</td>
          <td><div class="usage"><div class="track"><div class="fill" style="width:15%"></div></div><span class="pct">15%</span></div></td><td class="mount">/boot</td></tr>
        <tr><td><span class="code">/dev/vda15</span></td><td class="num">105M</td><td class="num">6.2M</td><td class="num">99M</td>
          <td><div class="usage"><div class="track"><div class="fill" style="width:6%"></div></div><span class="pct">6%</span></div></td><td class="mount">/boot/efi</td></tr>
      </tbody>
    </table>
  </div>

  <!-- NETWORK -->
  <div class="prompt"><span class="n">05</span><span class="cmd">hostname && hostname -I</span></div>
  <div class="grid2">
    <div class="panel">
      <dl class="kv">
        <dt>Hostname</dt><dd><b>ubuntu</b></dd>
      </dl>
    </div>
    <div class="panel">
      <ul class="ips">
        <li><span class="code">172.30.1.2</span></li>
        <li><span class="code">172.17.0.1</span></li>
      </ul>
    </div>
  </div>

  <!-- COMMANDS -->
  <div class="prompt"><span class="n">06</span><span class="cmd">history</span><span class="path">&nbsp;— commands executed</span></div>
  <pre><span class="c">01</span>  <span class="p">$</span> lsb_release -a
<span class="c">02</span>  <span class="p">$</span> uname -r
<span class="c">03</span>  <span class="p">$</span> lscpu | grep "Model name"
<span class="c">04</span>  <span class="p">$</span> nproc
<span class="c">05</span>  <span class="p">$</span> free -h
<span class="c">06</span>  <span class="p">$</span> df -h
<span class="c">07</span>  <span class="p">$</span> hostname
<span class="c">08</span>  <span class="p">$</span> hostname -I</pre>

  <!-- SUMMARY -->
  <div class="prompt"><span class="n">07</span><span class="cmd">cat SUMMARY.md</span></div>
  <div class="panel">
    <p class="summary">
      The KillerCoda environment provides a virtualized <b>Ubuntu 24.04.4 LTS</b> cloud server, hostname <b>ubuntu</b>,
      reachable at <b>172.30.1.2</b> and <b>172.17.0.1</b>. It runs on an <b>Intel Xeon E312xx</b> processor with a single core,
      roughly <b>1.9&nbsp;GiB</b> of RAM, and a <b>19&nbsp;GB</b> main disk partition (<span class="code">/dev/vda1</span>) at 30% utilization.
      Additional mounted file systems support the OS, boot, EFI, and temporary in-memory data.
    </p>
  </div>

  <footer>
    <span>generated report · static snapshot</span>
    <span>ubuntu@killercoda:~$</span>
  </footer>

</div>
</body>
</html>
