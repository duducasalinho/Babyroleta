<!DOCTYPE html>

<html lang="pt-BR">
<head>
<meta charset="utf-8"/>
<meta content="width=device-width,initial-scale=1" name="viewport"/>
<title>Roleta CMQ – Números com novas cores</title>
<style>
  :root{
    --azul:#0072BC;
    --azul-bebe:#8DD0F7;
    --laranja:#F47A32;
    --laranja-fraco:#FF9559;
    --linha:#000;
    --aro:#1a1a1a;
    --radpx: 120px;
  }
  *{box-sizing:border-box}
  body{
    margin:0; padding:22px; background:linear-gradient(180deg,#f6f7fb,#eceff5);
    color:#111; font-family: system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, sans-serif;
    display:flex; flex-direction:column; align-items:center; gap:18px;
  }
  .wrap{ position:relative; width:min(88vw,480px); aspect-ratio:1/1; }

  /* Ponteiro no topo apontando para BAIXO */
  .pointer {
        position: absolute;
        top: -35px;
        left: 50%;
        transform: translateX(-50%);
        width: 0; 
        height: 0; 
        border-left: 30px solid transparent;
        border-right: 30px solid transparent;
        border-top: 45px solid red;
        z-index: 10;
    }

  .wheel{
    width:100%; height:100%; border-radius:50%;
    background:
      repeating-conic-gradient(var(--linha) 0deg 1.2deg, transparent 1.2deg 72deg),
      conic-gradient(
        var(--azul)           0deg 72deg,
        var(--laranja)       72deg 144deg,
        var(--azul-bebe)    144deg 216deg,
        var(--laranja-fraco) 216deg 288deg,
        var(--azul)         288deg 360deg
      );
    position:relative; overflow:hidden;
    border:8px solid var(--aro);
    box-shadow: 0 10px 26px rgba(0,0,0,.25), inset 0 0 0 6px rgba(255,255,255,.2), inset 0 0 60px rgba(0,0,0,.15);
    transition: transform 3.4s cubic-bezier(.15,.7,.1,1);
  }

  .labels{ position:absolute; inset:0; z-index:3; }
  .label{
    position:absolute; left:50%; top:50%; transform: translate(-50%,-50%);
    font-weight:900; font-size: clamp(36px, 9.5vw, 64px);
    text-shadow: 0 1px 2px rgba(0,0,0,.25);
  }
  /* 1 verde, 2 vermelho, 3 azul, 4 amarelo, 5 rosa */
  .l1{ transform: translate(-50%,-50%) rotate(36deg)  translateX(var(--radpx)) rotate(-36deg);  color:#3AA63A; } /* verde */
  .l2{ transform: translate(-50%,-50%) rotate(108deg) translateX(var(--radpx)) rotate(-108deg); color:#FF2D2D; } /* vermelho */
  .l3{ transform: translate(-50%,-50%) rotate(180deg) translateX(var(--radpx)) rotate(-180deg); color:#0072BC; } /* azul */
  .l4{ transform: translate(-50%,-50%) rotate(252deg) translateX(var(--radpx)) rotate(-252deg); color:#FFD700; } /* amarelo */
  .l5{ transform: translate(-50%,-50%) rotate(324deg) translateX(var(--radpx)) rotate(-324deg); color:#FF69B4; } /* rosa */

  .center{
    position:absolute; left:50%; top:50%; transform:translate(-50%,-50%);
    width:36%; aspect-ratio:1/1; border-radius:50%;
    background:#fff; border:4px solid rgba(0,0,0,.35);
    display:grid; place-items:center; z-index:4;
    box-shadow: 0 6px 16px rgba(0,0,0,.25);
    overflow:hidden;
  }
  .center img{ width:88%; height:auto; object-fit:contain; }

  .controls{ display:flex; gap:12px; align-items:center; justify-content:center; flex-wrap:wrap; }
  button{
    background: var(--azul); color:#fff; border:none; cursor:pointer;
    padding:12px 18px; border-radius:12px; font-size:16px; font-weight:800;
    box-shadow: 0 6px 16px rgba(0,0,0,.18);
  }
  button:disabled{ opacity:.6; cursor:not-allowed; }
</style>
<style>
.roulette-wrapper {
    position: relative;
    display: inline-block;
}
.pointer-top {
    width: 0;
    height: 0;
    border-left: 20px solid transparent;
    border-right: 20px solid transparent;
    border-top: 30px solid black;
    position: absolute;
    top: -30px;
    left: 50%;
    transform: translateX(-50%);
    z-index: 10;
}
</style>
</head>
<body>
<div class="wrap">
<div aria-hidden="true" class="pointer" style=" top: -10px;"></div>
<div aria-label="Roleta 5 gomos" class="wheel" id="wheel" role="img">
<div class="labels">
<div class="label l1">1</div>
<div class="label l2">2</div>
<div class="label l3">3</div>
<div class="label l4">4</div>
<div class="label l5">5</div>
</div>
<div class="center"><img alt="Logo CMQ" src="data:image/jpeg;base64,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"/></div>
</div>
</div>
<div class="controls">
<button id="btn" type="button">🎯 GIRAR</button>
</div>
<audio id="tick" src="data:audio/wav;base64,VWtsR1JpUUFBQUJYUVZaRlptMTBJQkFBQUFBQkFBRUFFU3NBQUNKV0FBQUNBQkFBWkdGMFlRZ0FBQUFBLy84QUFQLy9BQUQvL3dBQS8vOEFBUC8vQUFELy93QUEvLzhBQVAvL0FBRC8vd0FB"></audio>
<script>
const wheel = document.getElementById('wheel');
const btn = document.getElementById('btn');
const tick = document.getElementById('tick');

function updateRadius(){
  const w = wheel.getBoundingClientRect().width;
  const rad = Math.round(w * 0.33);
  document.documentElement.style.setProperty('--radpx', rad + 'px');
}
updateRadius();
window.addEventListener('resize', updateRadius);

let giroAcumulado = 0;
let girando = false;
let tickInterval;

function sorteiaDelta(){
  const voltas = (Math.floor(Math.random()*3)+3)*360;
  const aleatorio = Math.random()*360;
  return voltas + aleatorio;
}

btn.addEventListener('click', () => {
  if(girando) return;
  girando = true;
  btn.disabled = true;

  const delta = sorteiaDelta();
  giroAcumulado += delta;
  wheel.style.transform = `rotate(${giroAcumulado}deg)`;

  tickInterval = setInterval(() => {
    try { tick.currentTime = 0; tick.play(); } catch(e){}
  }, 100);

  wheel.addEventListener('transitionend', () => {
    clearInterval(tickInterval);
    girando = false;
    btn.disabled = false;
  }, {once:true});
});
</script>
</body>
</html>
