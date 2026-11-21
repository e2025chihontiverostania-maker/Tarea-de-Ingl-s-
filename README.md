
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>The Mexican Revolution | An Animated Story</title>
<style>
:root{--ink:#24232a;--cream:#fff6e8;--red:#c94c43;--green:#39765b;--gold:#e8b84f;--sky:#9bd0d6}
*{box-sizing:border-box}
body{margin:0;background:#f1e8d9;color:var(--ink);font-family:Georgia,serif}
button{font:700 1rem Arial;cursor:pointer;border:0;border-radius:999px;padding:12px 20px;background:var(--red);color:white;box-shadow:0 4px 0 #87352f}
button:active{transform:translateY(3px);box-shadow:0 1px 0 #87352f}
.wrap{max-width:1100px;margin:auto;padding:20px}
.top{text-align:center;padding:25px 10px}
.eyebrow{font:700 .78rem Arial;letter-spacing:3px;color:var(--green)}
h1{font-size:clamp(2rem,5vw,4rem);margin:8px 0;color:#293b32}
.top p{font:1.05rem Arial;max-width:680px;margin:0 auto;color:#5d5b54}
.stage{position:relative;overflow:hidden;border:8px solid #fff;border-radius:22px;background:#a9d9df;box-shadow:0 12px 35px #55442b30;min-height:390px}
.sky{position:absolute;inset:0;background:linear-gradient(#8ecbd4 0 62%,#e7c77d 62%)}
.sun{position:absolute;right:9%;top:9%;width:70px;height:70px;background:#ffd56d;border-radius:50%;box-shadow:0 0 0 15px #ffd56d35}
.cloud{position:absolute;top:17%;left:12%;width:115px;height:30px;background:#fff9;border-radius:40px}
.cloud:before,.cloud:after{content:"";position:absolute;background:inherit;border-radius:50%}
.cloud:before{width:45px;height:45px;left:20px;top:-20px}
.cloud:after{width:55px;height:50px;right:15px;top:-25px}
.hills{position:absolute;bottom:21%;left:-5%;width:110%;height:100px;background:#73966a;border-radius:50% 50% 0 0}
.ground{position:absolute;bottom:0;height:24%;width:100%;background:#c9a36a}
.town{position:absolute;bottom:22%;left:5%;display:flex;gap:14px;align-items:end}
.house{width:90px;height:75px;background:#f1d8a8;border:4px solid #8d5944;position:relative}
.house:before{content:"";position:absolute;left:-9px;top:-27px;border-left:50px solid transparent;border-right:50px solid transparent;border-bottom:30px solid #9c4b3e}
.house:after{content:"";position:absolute;bottom:0;left:32px;width:20px;height:37px;background:#8a5b43}
.cactus{position:absolute;bottom:22%;right:10%;width:18px;height:75px;background:#39765b;border-radius:10px}
.cactus:before,.cactus:after{content:"";position:absolute;width:28px;height:12px;border:10px solid #39765b;border-bottom:0;border-radius:20px 20px 0 0}
.cactus:before{top:25px;left:-23px;transform:rotate(-90deg)}
.cactus:after{top:42px;right:-23px;transform:rotate(90deg)}
.banner{position:absolute;top:12px;left:15px;padding:8px 13px;background:#fff2dfdd;border-radius:8px;font:700 .78rem Arial;letter-spacing:1px;color:#654637}
.characters{position:absolute;bottom:17%;left:0;right:0;display:flex;justify-content:center;align-items:end;gap:clamp(5px,5vw,55px);height:220px}
.person{position:relative;width:105px;height:205px;animation:bob 2s ease-in-out infinite}
.person:nth-child(2){animation-delay:.3s}
.person:nth-child(3){animation-delay:.6s}
.head{position:absolute;top:8px;left:28px;width:52px;height:58px;background:#bd8058;border:3px solid #633f31;border-radius:45% 45% 48% 48%;z-index:3}
.hair{position:absolute;top:0;left:25px;width:58px;height:23px;background:#30251f;border-radius:50% 50% 15% 15%;z-index:4}
.hat{position:absolute;top:-9px;left:13px;width:82px;height:18px;background:#e7d2a2;border:3px solid #694b36;border-radius:50%;z-index:5}
.hat:after{content:"";position:absolute;left:25px;top:-19px;width:28px;height:22px;background:#e7d2a2;border:3px solid #694b36;border-radius:8px 8px 2px 2px}
.eye{position:absolute;top:28px;left:12px;width:5px;height:5px;background:#28201c;border-radius:50%;box-shadow:18px 0 #28201c}
.moustache{position:absolute;top:39px;left:11px;width:29px;height:8px;border-bottom:5px solid #33231d;border-radius:50%}
.body{position:absolute;top:62px;left:20px;width:70px;height:88px;background:var(--shirt,#426c55);border:3px solid #573c2d;border-radius:18px 18px 8px 8px;z-index:2}
.belt{position:absolute;top:118px;left:20px;width:70px;height:9px;background:#4a3325;z-index:3}
.arm{position:absolute;top:72px;left:8px;width:19px;height:75px;background:#bd8058;border:3px solid #633f31;border-radius:15px;transform:rotate(18deg);transform-origin:top;z-index:1}
.arm.right{left:79px;transform:rotate(-20deg)}
.legs{position:absolute;top:145px;left:30px;width:20px;height:53px;background:#594535;border:3px solid #382c25;border-radius:8px}
.legs:after{content:"";position:absolute;left:24px;top:0;width:20px;height:53px;background:inherit;border:inherit;border-radius:8px}
.label{position:absolute;bottom:-17px;left:50%;transform:translateX(-50%);white-space:nowrap;background:#fff1d7;padding:4px 8px;border-radius:6px;font:700 .72rem Arial}
.speech{position:relative;background:var(--cream);border-radius:18px;padding:20px 24px;margin:-4px auto 0;max-width:900px;box-shadow:0 8px 22px #594b3520}
.speaker{font:700 .78rem Arial;letter-spacing:2px;color:var(--red);margin-bottom:7px}
.line{font-size:clamp(1.05rem,2.2vw,1.35rem);line-height:1.55;min-height:55px}
.controls{display:flex;justify-content:center;flex-wrap:wrap;gap:12px;margin:18px 0}
.controls .secondary{background:var(--green);box-shadow:0 4px 0 #24513d}
.controls .light{background:#e5bd65;color:#302719;box-shadow:0 4px 0 #a47d34}
.progress{height:8px;background:#d7cbb9;border-radius:20px;overflow:hidden;margin:15px 0}
.progress>div{height:100%;width:0;background:var(--red);transition:width .3s}
.section{background:#fffaf1;border-radius:20px;padding:25px;margin:28px 0;box-shadow:0 5px 20px #594b3512}
.section h2{margin-top:0;color:#315e49;font-size:1.8rem}
.moments{display:grid;grid-template-columns:repeat(auto-fit,minmax(230px,1fr));gap:14px}
.moment{background:#f4ead8;border-left:5px solid var(--red);padding:15px;border-radius:10px}
.moment b{font:700 .82rem Arial;color:#a13f37;letter-spacing:1px}
.moment h3{margin:8px 0}
.moment p{font:.98rem/1.5 Arial;margin:0}
.transcript p{font:1rem/1.7 Arial;border-bottom:1px solid #e7ddce;padding:8px 0;margin:0}
.transcript strong{color:#a13f37}
.transcript u{text-decoration-thickness:2px;text-decoration-color:#39765b;text-underline-offset:3px}
.note{font:.85rem/1.5 Arial;color:#71695d;text-align:center;margin:20px}
.hide{display:none!important}
.person.talk .arm.right{animation:talk .35s ease-in-out infinite alternate}
@keyframes bob{0%,100%{translate:0 0}50%{translate:0 -5px}}
@keyframes talk{from{transform:rotate(-20deg)}to{transform:rotate(-65deg)}}
@media(max-width:600px){
.stage{min-height:330px}
.characters{height:180px;bottom:18%;gap:0}
.person{transform:scale(.8);transform-origin:bottom center;margin:0 -8px}
.town{transform:scale(.75);transform-origin:bottom left}
.speech{padding:17px}
.section{padding:18px}
}
</style>
</head>
<body>
<main class="wrap">

<header class="top">
<div class="eyebrow">A HISTORY STORY IN ENGLISH</div>
<h1>The Mexican Revolution</h1>
<p>A story about power, courage, inequality and the fight for a new Mexico.</p>
</header>

<section class="stage" aria-label="Animated story scene">
<div class="sky"></div>
<div class="sun"></div>
<div class="cloud"></div>
<div class="hills"></div>
<div class="ground"></div>
<div class="town"><div class="house"></div><div class="house" style="transform:scale(.7)"></div></div>
<div class="cactus"></div>
<div class="banner" id="sceneTitle">CHAPTER 1 · A COUNTRY OF CONTRASTS</div>
<div class="characters" id="characters"></div>
</section>

<section class="speech">
<div class="speaker" id="speaker">NARRATOR</div>
<div class="line" id="line">At the beginning of the twentieth century, Mexico was changing.</div>
</section>

<div class="progress"><div id="bar"></div></div>

<div class="controls">
<button class="secondary" id="prev">← Previous</button>
<button id="play">▶ Play story</button>
<button class="light" id="next">Next →</button>
<button class="secondary" id="stop">■ Stop voice</button>
</div>

<section class="section">
<h2>Six key historical moments</h2>
<div class="moments">

<article class="moment">
<b>01 · 1910</b>
<h3>The call to revolt</h3>
<p>Francisco I. Madero challenged Porfirio Díaz and called on Mexicans to rise up on November 20, 1910.</p>
</article>

<article class="moment">
<b>02 · 1911</b>
<h3>Díaz leaves power</h3>
<p>After the uprising spread, Porfirio Díaz resigned in May 1911 and went into exile.</p>
</article>

<article class="moment">
<b>03 · 1911</b>
<h3>The Plan of Ayala</h3>
<p>Emiliano Zapata demanded land reform because many peasants had lost their lands.</p>
</article>

<article class="moment">
<b>04 · 1913</b>
<h3>The Ten Tragic Days</h3>
<p>A military coup in Mexico City ended with President Madero and Vice President Pino Suárez being assassinated.</p>
</article>

<article class="moment">
<b>05 · 1914</b>
<h3>Huerta is defeated</h3>
<p>Revolutionary forces defeated Victoriano Huerta's government, but different revolutionary groups continued to disagree.</p>
</article>

<article class="moment">
<b>06 · 1917</b>
<h3>A new Constitution</h3>
<p>The Constitution of 1917 included important principles about education, land and workers' rights.</p>
</article>

</div>
</section>

<section class="section transcript">
<h2>The complete story · English script</h2>
<div id="transcript"></div>
</section>

<p class="note">The narration uses your browser's English text-to-speech voice. If the voice sounds different on another device, the written script remains the same.</p>

</main>

<script>
const story=[

{
chapter:'CHAPTER 1 · A COUNTRY OF CONTRASTS',
scene:'porfirio',
parts:[
['NARRATOR','At the beginning of the twentieth century, Mexico was ruled by Porfirio Díaz.'],
['NARRATOR','He had been in power for many years. The country built railroads and factories.'],
['NARRATOR','BUT wealth was not shared equally. Many farmers and workers lived in poverty, AND they had very few rights.'],
['PEASANT','We work hard, BUT we do not own the land we cultivate.'],
['NARRATOR','People wanted change.']
]
},

{
chapter:'CHAPTER 2 · THE CALL FOR CHANGE',
scene:'madero',
parts:[
['NARRATOR','Francisco I. Madero believed that Mexico needed free elections.'],
['MADERO','Mexico needs democracy! The people must choose their president.'],
['NARRATOR','IN 1910, Madero published the Plan of San Luis. He called for an uprising ON November 20, 1910.'],
['NARRATOR','AND the Mexican Revolution began.']
]
},

{
chapter:'CHAPTER 3 · THE REVOLUTION BEGINS',
scene:'revolt',
parts:[
['NARRATOR','ON November 20, 1910, groups of people began to rise against Díaz.'],
['NARRATOR','Farmers, workers and revolutionary leaders joined the struggle.'],
['NARRATOR','In the north, leaders such as Pancho Villa became important. IN the south, Emiliano Zapata fought for land and justice.'],
['ZAPATA','The land belongs to the people who work it!'],
['VILLA','We are fighting for a country with a better future!']
]
},

{
chapter:'CHAPTER 4 · DÍAZ LEAVES POWER',
scene:'exile',
parts:[
['NARRATOR','The movement grew stronger, AND Díaz could no longer remain in power.'],
['NARRATOR','ON May 25, 1911, Porfirio Díaz resigned. A few days later, he left Mexico for exile.'],
['DIAZ','My long government has come to an end.'],
['NARRATOR','Madero became president IN November 1911. BUT the revolution was not over.']
]
},

{
chapter:'CHAPTER 5 · DIFFERENT IDEAS',
scene:'zapata',
parts:[
['NARRATOR','Many revolutionaries wanted different things. Madero wanted political democracy, while Zapata demanded land for peasants.'],
['ZAPATA','We need land reform. The promises must become real.'],
['NARRATOR','ON November 28, 1911, Zapata announced the Plan of Ayala. It demanded the return of land to villages.'],
['NARRATOR','Meanwhile, Pancho Villa and other leaders continued fighting in the north.']
]
},

{
chapter:'CHAPTER 6 · A NEW CRISIS',
scene:'huerta',
parts:[
['NARRATOR','IN February 1913, a military coup began in Mexico City. It became known as the Ten Tragic Days.'],
['NARRATOR','Madero was forced from power. He and Vice President José María Pino Suárez were assassinated ON February 22, 1913.'],
['NARRATOR','Victoriano Huerta took control, BUT many revolutionaries refused to accept his government.'],
['NARRATOR','The fight continued, AND Huerta was defeated in 1914.']
]
},

{
chapter:'CHAPTER 7 · A NEW CONSTITUTION',
scene:'constitution',
parts:[
['NARRATOR','After Huerta fell, revolutionary groups continued to fight because they disagreed about the future of Mexico.'],
['NARRATOR','Venustiano Carranza became a leading figure in the movement that created a new Constitution.'],
['NARRATOR','ON February 5, 1917, the Constitution was proclaimed. It included important principles about education, land and workers’ rights.'],
['NARRATOR','The Revolution did not end all conflicts immediately. HOWEVER, the Constitution became a major result of the struggle.'],
['NARRATOR','The Mexican Revolution changed the country and shaped its modern history.']
]
}

];

const people={
'PORFIRIO DÍAZ':{shirt:'#7b4c3c',hat:true,moustache:true},
'PEASANT':{shirt:'#9a6b37',hat:true},
'FRANCISCO I. MADERO':{shirt:'#315c80',hat:false},
'EMILIANO ZAPATA':{shirt:'#315d43',hat:true,moustache:true},
'PANCHO VILLA':{shirt:'#8a5136',hat:true,moustache:true},
'DÍAZ':{shirt:'#7b4c3c',hat:true,moustache:true},
'VICTORIANO HUERTA':{shirt:'#554f70',hat:true,moustache:true},
'VENUSTIANO CARRANZA':{shirt:'#4c6572',hat:true,moustache:true}
};

const cast={
porfirio:['PORFIRIO DÍAZ','PEASANT'],
madero:['FRANCISCO I. MADERO','PEASANT'],
revolt:['EMILIANO ZAPATA','PANCHO VILLA','PEASANT'],
exile:['DÍAZ','FRANCISCO I. MADERO'],
zapata:['EMILIANO ZAPATA','PANCHO VILLA'],
huerta:['VICTORIANO HUERTA','EMILIANO ZAPATA','PANCHO VILLA'],
constitution:['VENUSTIANO CARRANZA','PEASANT']
};

function person(name){
const p=people[name]||{};
return `<div class="person">
<div class="hat ${p.hat?'':'hide'}"></div>
<div class="hair"></div>
<div class="head">
<i class="eye"></i>
<i class="moustache ${p.moustache?'':'hide'}"></i>
</div>
<div class="arm"></div>
<div class="arm right"></div>
<div class="body" style="--shirt:${p.shirt||'#52745a'}"></div>
<div class="belt"></div>
<div class="legs"></div>
<div class="label">${name}</div>
</div>`;
}

const flat=[];
story.forEach((s,si)=>s.parts.forEach((p,pi)=>flat.push({
chapter:s.chapter,
scene:s.scene,
speaker:p[0],
text:p[1],
si,
pi
})));

let index=0,playing=false;
const $=id=>document.getElementById(id);

function esc(s){
return s.replaceAll('&','&amp;').replaceAll('<','&lt;').replaceAll('>','&gt;');
}

function format(s){
let t=esc(s);
const connectors=['BUT','AND','BECAUSE','HOWEVER','WHILE','ALTHOUGH','THEREFORE','MEANWHILE'];
connectors.forEach(w=>{
t=t.replace(new RegExp('\\b'+w+'\\b','g'),'<strong>'+w+'</strong>');
});
const times=['AT','ON','IN','DURING','AFTER','BEFORE'];
times.forEach(w=>{
t=t.replace(new RegExp('\\b'+w+'\\b','g'),'<u>'+w+'</u>');
});
return t;
}

function render(){
const item=flat[index];
const scene=story[item.si];

$('sceneTitle').textContent=scene.chapter;
$('speaker').textContent=item.speaker;
$('line').textContent=item.text;
$('characters').innerHTML=cast[item.scene].map(person).join('');
$('bar').style.width=((index+1)/flat.length*100)+'%';
$('prev').disabled=index===0;
$('next').disabled=index===flat.length-1;

document.querySelectorAll('.person').forEach((el,i)=>{
if(item.speaker!=='NARRATOR'&&cast[item.scene][i]===item.speaker){
el.classList.add('talk');
}
});
}

function speakCurrent(){
if(!('speechSynthesis'in window)){
alert('Text-to-speech is not supported in this browser.');
return;
}
speechSynthesis.cancel();
const item=flat[index];
const u=new SpeechSynthesisUtterance(item.text);
u.lang='en-US';
u.rate=.88;
u.pitch=1;
const voices=speechSynthesis.getVoices();
const english=voices.find(v=>v.lang&&v.lang.toLowerCase().startsWith('en'));
if(english)u.voice=english;
speechSynthesis.speak(u);
}

function next(){
if(index<flat.length-1){
index++;
render();
if(playing)speakCurrent();
}else{
playing=false;
$('play').textContent='▶ Play story';
}
}

function play(){
if(playing){
playing=false;
speechSynthesis.cancel();
$('play').textContent='▶ Play story';
return;
}

playing=true;
$('play').textContent='Ⅱ Pause story';

const run=()=>{
if(!playing)return;
const item=flat[index];
const u=new SpeechSynthesisUtterance(item.text);
u.lang='en-US';
u.rate=.88;

const v=speechSynthesis.getVoices().find(v=>v.lang&&v.lang.toLowerCase().startsWith('en'));
if(v)u.voice=v;

u.onend=()=>{
if(!playing)return;
if(index<flat.length-1){
index++;
render();
run();
}else{
playing=false;
$('play').textContent='▶ Play story';
}
};

speechSynthesis.cancel();
speechSynthesis.speak(u);
};

run();
}

$('prev').onclick=()=>{
playing=false;
speechSynthesis.cancel();
index=Math.max(0,index-1);
$('play').textContent='▶ Play story';
render();
};

$('next').onclick=()=>{
playing=false;
speechSynthesis.cancel();
$('play').textContent='▶ Play story';
next();
};

$('play').onclick=play;

$('stop').onclick=()=>{
playing=false;
speechSynthesis.cancel();
$('play').textContent='▶ Play story';
};

$('transcript').innerHTML=flat.map(x=>
`<p><b>${x.speaker}:</b> ${format(x.text)}</p>`
).join('');

render();
</script>
</body>
</html>
