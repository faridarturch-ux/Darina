<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Для Дарины ❤️</title>
<style>
*{box-sizing:border-box}
body{
 margin:0;min-height:100vh;color:#fff;
 font-family:Georgia,serif;text-align:center;
 background:radial-gradient(ellipse at top,#35204f,#100d25 65%,#070711);
 overflow-x:hidden
}
main{max-width:650px;margin:auto;padding:55px 22px}
.heart{font-size:65px;animation:pulse 1.5s infinite}
h1{font-size:clamp(32px,8vw,52px);color:#ffd3e5}
p{font-size:19px;line-height:1.8}
.card{
 margin:24px 0;padding:24px;border:1px solid #ffffff30;
 border-radius:22px;background:#ffffff0d;
 box-shadow:0 0 35px #e04f9a16
}
button{
 border:0;border-radius:30px;padding:14px 23px;margin:8px;
 font-size:16px;font-weight:bold;background:#ff8dbb;color:#271025;
 cursor:pointer
}
button:active{transform:scale(.96)}
#message{min-height:65px;color:#ffd3e5}
footer{margin-top:45px;color:#c4b3d7}
.star{position:fixed;color:#fff;animation:twinkle 3s infinite alternate;pointer-events:none}
@keyframes pulse{50%{transform:scale(1.12)}}
@keyframes twinkle{to{opacity:.25;transform:scale(.7)}}
</style>
</head>
<body>
<main>
<div class="heart">❤️</div>
<h1>Для моей Дарины</h1>
<p>Есть люди, которые делают мир особенным просто тем, что они в нём есть.</p>
<div class="card">
<h2>Наша история ✨</h2>
<p>Дарина, этот маленький уголок интернета создан специально для тебя.</p>
<p>Если бы мне пришлось выбирать снова, я бы снова захотел встретить тебя.</p>
</div>
<div class="card">
<h2>Немного от сердца 💌</h2>
<p id="message">Нажми на кнопку — для тебя есть кое-что особенное.</p>
<button onclick="nextMessage()">Открыть послание 💗</button>
</div>
<div class="card">
<h2>Один вопрос… 🌹</h2>
<p>Ты знаешь, как сильно ты умеешь делать меня счастливым?</p>
<button onclick="answer(true)">Теперь знаю ❤️</button>
<button onclick="answer(false)">Расскажи ещё 🥹</button>
<p id="answer"></p>
</div>
<footer>Создано с любовью. Только для тебя, Дарина ❤️</footer>
</main>
<script>
const messages=[
"Твоя улыбка способна сделать мой день лучше. ❤️",
"Мне нравится, что именно ты — часть моей истории. 💕",
"Даже обычный день становится особенным, когда в нём есть ты. ✨",
"Ты заслуживаешь нежности, заботы и самого искреннего счастья. 🌹",
"Если этот сайт заставил тебя улыбнуться — значит, всё получилось. 💖"
];
let n=0;
function nextMessage(){
 document.getElementById('message').textContent=messages[n%messages.length];
 n++;
}
function answer(yes){
 document.getElementById('answer').textContent=yes
 ?"Тогда обниму тебя крепче. Ты для меня очень важна. ❤️"
 :"Могу рассказывать бесконечно… Главное, что ты у меня есть. 💗";
}
for(let i=0;i<35;i++){
 let s=document.createElement('span');
 s.className='star';s.textContent='✦';
 s.style.left=Math.random()*100+'%';
 s.style.top=Math.random()*100+'%';
 s.style.fontSize=(8+Math.random()*13)+'px';
 s.style.animationDelay=Math.random()*3+'s';
 document.body.appendChild(s);
}
</script>
</body>
</html>
