<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Para Ti ❤️</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial,sans-serif;
}

body{
height:100vh;
display:flex;
justify-content:center;
align-items:center;
background:linear-gradient(135deg,#000,#1d001d,#ff4fa3);
overflow:hidden;
color:white;
text-align:center;
}

.card{
background:rgba(255,255,255,.08);
backdrop-filter:blur(10px);
padding:40px;
border-radius:25px;
box-shadow:0 0 30px rgba(255,105,180,.5);
animation:fade 2s;
}

h1{
font-size:38px;
animation:pulse 2s infinite;
}

p{
margin-top:15px;
font-size:18px;
}

button{
margin-top:25px;
padding:14px 28px;
border:none;
border-radius:50px;
background:#ff4fa3;
color:white;
font-size:18px;
cursor:pointer;
transition:.3s;
}

button:hover{
transform:scale(1.08);
background:#ff77bb;
}

.heart{
position:absolute;
color:#ff4fa3;
font-size:20px;
animation:float 8s linear infinite;
}

@keyframes fade{
from{opacity:0;transform:translateY(40px);}
to{opacity:1;transform:translateY(0);}
}

@keyframes pulse{
50%{transform:scale(1.05);}
}

@keyframes float{
0%{
transform:translateY(100vh);
opacity:0;
}
20%{opacity:1;}
100%{
transform:translateY(-100px);
opacity:0;
}
}
</style>
</head>

<body>

<div class="card">
<h1>💖 ¿QUIERES ACEPTAR ANDAR CONMIGO? 💖</h1>

<p>
Desde que llegaste, haces mis días más bonitos.
Me encantaría compartir muchos momentos contigo. ❤️
</p>

<button onclick="acepto()">Sí, acepto ❤️</button>

</div>

<script>

function acepto(){
document.body.innerHTML=
"<div style='display:flex;justify-content:center;align-items:center;height:100vh;background:black;color:white;font-size:35px;text-align:center;padding:20px;'>💖 Gracias por aceptar. Prometo hacerte muy feliz. Te quiero muchísimo. 🌹❤️</div>";
}

setInterval(()=>{
let h=document.createElement("div");
h.className="heart";
h.innerHTML="❤";
h.style.left=Math.random()*100+"vw";
h.style.fontSize=(20+Math.random()*30)+"px";
document.body.appendChild(h);

setTimeout(()=>{
h.remove();
},8000);

},300);

</script>

</body>
</html>
