
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>The Mexican Revolution - Animated Cartoon</title>
<style>
*{box-sizing:border-box}
body{margin:0;background:#f4e5c9;color:#39291f;font-family:Arial,sans-serif}
header{background:#873329;color:white;text-align:center;padding:20px}
header h1{font-family:Georgia;font-size:30px}
main{max-width:900px;margin:auto;padding:15px}
.stage{background:#fff;border:5px solid #493326;border-radius:16px;overflow:hidden}
.top{text-align:center;background:#493326;color:white;padding:10px}
svg{display:block;width:100%;height:auto;background:#a9dcec}
.character{transform-box:fill-box;transform-origin:center bottom}
.walk{animation:walk 3s ease-in-out infinite}
.walk2{animation:walk2 3.5s ease-in-out infinite}
.horse{animation:horse 1s ease-in-out infinite}
.talk{animation:talk .25s infinite alternate}
.wave{animation:wave .6s infinite alternate;transform-box:fill-box;transform-origin:bottom}
.sun{animation:sun 5s infinite alternate;transform-box:fill-box;transform-origin:center}
.cloud{animation:cloud 18s linear infinite}
@keyframes walk{0%,100%{transform:translateX(0)}50%{transform:translateX(65px)}}
@keyframes walk2{0%,100%{transform:translateX(0)}50%{transform:translateX(-65px)}}
@keyframes horse{0%,100%{transform:translateY(0)}50%{transform:translateY(-9px)}}
@keyframes talk{from{transform:rotate(-2deg)}to{transform:rotate(2deg)}}
@keyframes wave{from{transform:rotate(-15deg)}to{transform:rotate(30deg)}}
@keyframes sun{to{transform:rotate(25deg)}}
@keyframes cloud{from{transform:translateX(-40px)}to{transform:translateX(100px)}}
.dialogue{padding:17px;min-height:145px;background:#fffaf0;line-height:1.7}
.dialogue p{margin:0}
.speaker{font-weight:bold;color:#a33d2d;margin-bottom:8px}
strong{color:#b32d22}
u{text-decoration-color:#2584a3;text-decoration-thickness:2px}
.controls{display:flex;flex-wrap:wrap;justify-content:center;gap:9px;margin:18px 0}
button{background:#963b2d;color:white;border:0;border-radius:10px;padding:12px 16px;font-weight:bold;cursor:pointer}
button:hover{background:#60251e}
.section{background:white;border-radius:14px;padding:20px;margin:25px 0;line-height:1.7}
.section h2{color:#963b2d;text-align:center}
.card{border:2px solid #ead9c0;border-radius:12px;padding:13px;margin:12px 0}
.card h3{color:#963b2d}
#highlights,#transcript{display:none}
#status{text-align:center;color:#765c49;padding:8px}
</style>
</head>
<body>

<header>
<h1>THE MEXICAN REVOLUTION</h1>
<p>An Animated Historical Story</p>
<p>November 20th, 1910</p>
</header>

<main>
<div class="stage">
<div class="top">
<h2 id="title">Mexico Before the Revolution</h2>
<p id="chapter">Chapter 1</p>
</div>

<!-- ANIMATED CARTOON STAGE -->
<svg viewBox="0 0 800 390" role="img" aria-label="Animated Mexican village and historical characters">
<defs>
<g id="farmer">
<!-- body -->
<path d="M-24 160 L-30 240 L-45 310 L-12 310 L0 245 L15 310 L48 310 L28 230 L25 160Z" fill="#a94d2c" stroke="#442b20" stroke-width="4"/>
<path d="M-23 170 L-45 215 L-63 238 L-50 250 L-20 225 L0 195 L22 225 L50 250 L64 238 L42 205 L25 165Z" fill="#d59a54" stroke="#442b20" stroke-width="4"/>
<!-- face -->
<circle cx="0" cy="120" r="42" fill="#bd805b" stroke="#442b20" stroke-width="4"/>
<path d="M-48 112 Q0 65 48 112 L35 119 L-35 119Z" fill="#7d4329" stroke="#442b20" stroke-width="4"/>
<ellipse cx="0" cy="105" rx="75" ry="13" fill="#d3a45b" stroke="#442b20" stroke-width="5"/>
<path d="M-18 135 Q0 155 18 135" fill="none" stroke="#542e24" stroke-width="4"/>
<circle cx="-14" cy="119" r="4" fill="#241b16"/>
<circle cx="14" cy="119" r="4" fill="#241b16"/>
<path d="M-10 150 Q0 160 10 150" fill="none" stroke="#542e24" stroke-width="3"/>
</g>

<g id="madero">
<path d="M-25 165 L-30 240 L-45 310 L-10 310 L0 245 L15 310 L48 310 L27 230 L25 165Z" fill="#263f61" stroke="#29221d" stroke-width="4"/>
<path d="M-25 170 L-48 220 L-62 240 L-49 251 L-15 215 L0 195 L20 220 L48 250 L62 240 L40 205 L25 165Z" fill="#e0d1b2" stroke="#29221d" stroke-width="4"/>
<circle cx="0" cy="120" r="42" fill="#bd805b" stroke="#442b20" stroke-width="4"/>
<path d="M-43 103 Q0 65 43 103 L35 112 L-35 112Z" fill="#493020" stroke="#29221d" stroke-width="4"/>
<path d="M-35 91 Q0 60 35 91 L24 84 L-24 84Z" fill="#d2a65b" stroke="#29221d" stroke-width="3"/>
<ellipse cx="0" cy="91" rx="55" ry="9" fill="#493020" stroke="#29221d" stroke-width="3"/>
<circle cx="-14" cy="119" r="4" fill="#241b16"/>
<circle cx="14" cy="119" r="4" fill="#241b16"/>
<path d="M-12 144 Q0 151 12 144" fill="none" stroke="#542e24" stroke-width="3"/>
<path d="M-24 132 Q0 145 24 132" fill="none" stroke="#493020" stroke-width="5"/>
</g>

<g id="diaz">
<path d="M-25 160 L-30 240 L-45 310 L-10 310 L0 245 L15 310 L48 310 L27 230 L25 160Z" fill="#30394b" stroke="#29221d" stroke-width="4"/>
<path d="M-24 165 L-40 210 L-10 225 L0 185 L15 225 L43 210 L25 165Z" fill="#eee0c5" stroke="#29221d" stroke-width="3"/>
<circle cx="0" cy="120" r="42" fill="#c28b69" stroke="#442b20" stroke-width="4"/>
<path d="M-42 105 Q0 72 42 105 L35 114 L-35 114Z" fill="#77716c" stroke="#29221d" stroke-width="3"/>
<circle cx="-14" cy="119" r="4" fill="#241b16"/>
<circle cx="14" cy="119" r="4" fill="#241b16"/>
<path d="M-18 140 Q0 151 18 140" fill="none" stroke="#77716c" stroke-width="7"/>
<path d="M-16 128 L-4 132 M4 132 L16 128" stroke="#77716c" stroke-width="5"/>
</g>

<g id="horse">
<ellipse cx="0" cy="205" rx="70" ry="38" fill="#8c4b2c" stroke="#3f291d" stroke-width="4"/>
<path d="M35 190 Q45 115 78 120 L103 160 L75 184Z" fill="#8c4b2c" stroke="#3f291d" stroke-width="4"/>
<path d="M82 127 Q115 100 126 130 L105 153 L78 151Z" fill="#8c4b2c" stroke="#3f291d" stroke-width="4"/>
<path d="M-48 230 L-55 300 L-42 300 L-23 230 M20 230 L10 300 L25 300 L42 225" fill="#563322" stroke="#3f291d" stroke-width="6"/>
<path d="M-60 180 Q-100 150 -85 130" fill="none" stroke="#3f291d" stroke-width="9"/>
<circle cx="107" cy="135" r="4" fill="black"/>
</g>

<g id="house">
<rect x="0" y="100" width="140" height="110" fill="#d9a66f" stroke="#77452b" stroke-width="5"/>
<path d="M-15 105 L70 35 L155 105Z" fill="#9c4730" stroke="#77452b" stroke-width="5"/>
<rect x="53" y="145" width="35" height="65" fill="#69402a"/>
<rect x="12" y="125" width="30" height="30" fill="#a9dcec" stroke="#77452b" stroke-width="4"/>
</g>
</defs>

<!-- SKY AND LAND -->
<rect width="800" height="390" fill="#9cdaed"/>
<circle class="sun" cx="700" cy="65" r="36" fill="#ffd66d"/>
<g class="cloud" fill="white">
<ellipse cx="180" cy="65" rx="65" ry="20"/>
<circle cx="145" cy="57" r="23"/>
<circle cx="185" cy="45" r="28"/>
</g>
<path d="M0 260 L130 155 L255 260 L410 145 L570 260 L690 160 L800 255 L800 390 L0 390Z" fill="#86a76b"/>
<path d="M0 295 Q180 255 380 305 T800 285 L800 390 L0 390Z" fill="#789c4c"/>

<!-- HOUSES -->
<use href="#house" x="40" y="150"/>
<use href="#house" x="600" y="155" transform="translate(600 155) scale(.8) translate(-600 -155)"/>

<!-- DIALOGUE CHARACTERS -->
<g id="characterA" class="character">
<use href="#diaz" transform="translate(210 0)"/>
</g>
<g id="characterB" class="character">
<use href="#farmer" transform="translate(450 0)"/>
</g>
<g id="characterC" class="character">
<use href="#madero" transform="translate(660 0) scale(.8) translate(-660 0)"/>
</g>
<g id="horseGroup" class="character horse" style="display:none">
<use href="#horse" transform="translate(120 0) scale(.8)"/>
</g>
</svg>

<div class="dialogue" id="dialogue">
<div class="speaker" id="speaker">NARRATOR</div>
<p id="text">Mexico, in 1910...</p>
</div>
</div>

<div id="status">Ready to begin!</div>

<div class="controls">
<button onclick="play()">▶ Play</button>
<button onclick="pause()">Ⅱ Pause</button>
<button onclick="stop()">■ Stop</button>
<button onclick="previous()">← Back</button>
<button onclick="next()">Next →</button>
</div>

<section class="section">
<h2>Historical Highlights</h2>
<p>The six most important moments of the Mexican Revolution.</p>
<div id="highlights"></div>
</section>

<section class="section">
<h2>The Complete Story</h2>
<p id="student"></p>
<div id="transcript"></div>
</section>
</main>

<script>
const chapters=[
{
title:"Mexico Before the Revolution",
action:"village",
people:["Porfirio Díaz","Farmer","Worker"],
lines:[
["NARRATOR","Mexico, <u>in</u> 1910, was a country with great differences between rich and poor. Porfirio Díaz had governed Mexico for more than thirty years."],
["FARMER","We work every day, <strong>but</strong> we do not own the land. Our families need help!"],
["WORKER","Our working conditions are unfair, <strong>and</strong> we have very few rights."],
["NARRATOR","<strong>However</strong>, the government focused on economic development while many people continued to suffer."],
["FARMER","We want a better future for our children!"]
]},
{
title:"Madero Arrives",
action:"madero",
people:["Francisco I. Madero","Farmer","Citizen"],
lines:[
["NARRATOR","A political leader named Francisco I. Madero began to challenge Díaz's government."],
["MADERO","Mexico needs democracy! The people deserve free elections!"],
["FARMER","Can you help us get our land back?"],
["MADERO","I believe in a fair government. <strong>Therefore</strong>, we must work together."],
["NARRATOR","<u>On</u> October 5th, 1910, Madero published the Plan of San Luis. He called for an uprising <u>on</u> November 20th."]
]},
{
title:"The Revolution Begins",
action:"revolution",
people:["Revolutionary","Horse","Farmer"],
lines:[
["NARRATOR","<u>On</u> November 20th, 1910, the Mexican Revolution began. People rose up in different parts of the country."],
["REVOLUTIONARY","It is time for change! We want freedom!"],
["FARMER","<strong>And</strong> we want our land back!"],
["NARRATOR","Leaders like Emiliano Zapata and Pancho Villa joined the struggle. <strong>Then</strong>, the movement became stronger."],
["REVOLUTIONARY","Let's move forward!"]
]},
{
title:"Díaz Leaves Mexico",
action:"departure",
people:["Porfirio Díaz","Citizen","Farmer"],
lines:[
["NARRATOR","After months of fighting, Díaz's government became weaker."],
["DÍAZ","I am resigning from the presidency."],
["NARRATOR","<u>On</u> May 25th, 1911, Porfirio Díaz resigned. <u>On</u> May 31st, he left Mexico for France."],
["CITIZEN","A new chapter is beginning!"],
["NARRATOR","<strong>Finally</strong>, the country had an opportunity for political change."]
]},
{
title:"Madero and Zapata",
action:"meeting",
people:["Madero","Zapata","Farmer"],
lines:[
["NARRATOR","<u>On</u> November 6th, 1911, Francisco I. Madero became president."],
["MADERO","I want a democratic country!"],
["ZAPATA","We need land reform. Farmers cannot wait any longer!"],
["NARRATOR","<u>On</u> November 28th, 1911, Zapata proclaimed the Plan of Ayala."],
["ZAPATA","<strong>However</strong>, the struggle for land is not over!"]
]},
{
title:"The Ten Tragic Days",
action:"conflict",
people:["Citizen","Madero","Huerta"],
lines:[
["NARRATOR","<u>During</u> February 1913, a coup took place in Mexico City. It became known as the Ten Tragic Days."],
["CITIZEN","There is fighting in the capital! What will happen?"],
["NARRATOR","General Victoriano Huerta took power. Madero was forced from office."],
["NARRATOR","<u>On</u> February 22nd, 1913, Madero and Vice President Pino Suárez were assassinated."],
["CITIZEN","Mexico is facing another difficult time."]
]},
{
title:"The Constitution of 1917",
action:"constitution",
people:["Carranza","Citizen","Farmer"],
lines:[
["NARRATOR","After more fighting and political changes, a new Constitution was adopted <u>on</u> February 5th, 1917."],
["CARRANZA","Mexico needs new laws and a stronger constitutional government!"],
["NARRATOR","The Constitution included important rights related to education, land and workers."],
["FARMER","Our demands for a better life must be heard!"],
["NARRATOR","<strong>Finally</strong>, the Constitution of 1917 became one of the most important results of the Revolution."]
]}
];

const highlights=[
["The Porfiriato","Before 1910","Porfirio Díaz governed for more than thirty years. Inequality and limited political freedom caused growing discontent."],
["The Plan of San Luis","October 5th, 1910","Madero called for an uprising against Díaz and demanded free elections."],
["The Revolution Begins","November 20th, 1910","Armed uprisings began in different parts of Mexico."],
["Díaz Resigns","May 25th, 1911","Porfirio Díaz resigned from the presidency and later left Mexico."],
["The Ten Tragic Days","February 1913","A coup led to Huerta taking power. Madero and Pino Suárez were assassinated."],
["The Constitution","February 5th, 1917","Mexico adopted a new Constitution with important social rights."]
];

let s=0,l=0,playing=false,timer=null;
let englishVoices=[];

function getVoices(){
 if(!("speechSynthesis" in window))return;
 englishVoices=speechSynthesis.getVoices().filter(v=>v.lang.startsWith("en"));
}
getVoices();
if("speechSynthesis" in window)speechSynthesis.onvoiceschanged=getVoices;

function render(){
 const c=chapters[s];
 document.getElementById("title").textContent=c.title;
 document.getElementById("chapter").textContent="Chapter "+(s+1)+" of "+chapters.length;

 const A=document.getElementById("characterA");
 const B=document.getElementById("characterB");
 const C=document.getElementById("characterC");
 const H=document.getElementById("horseGroup");

 [A,B,C].forEach(x=>x.setAttribute("class","character"));
 H.style.display="none";

 if(c.action==="village"){
 A.style.display="block";B.style.display="block";C.style.display="none";
 A.classList.add("wave");B.classList.add("walk");
 }
 if(c.action==="madero"){
 A.style.display="none";B.style.display="block";C.style.display="block";
 B.classList.add("walk2");C.classList.add("walk");
 }
 if(c.action==="revolution"){
 A.style.display="none";B.style.display="block";C.style.display="block";
 B.classList.add("walk");C.classList.add("wave");H.style.display="block";
 }
 if(c.action==="departure"){
 A.style.display="block";B.style.display="block";C.style.display="none";
 A.classList.add("walk2");B.classList.add("wave");
 }
 if(c.action==="meeting"){
 A.style.display="block";B.style.display="block";C.style.display="none";
 A.classList.add("talk");B.classList.add("wave");
 }
 if(c.action==="conflict"){
 A.style.display="block";B.style.display="block";C.style.display="block";
 A.classList.add("walk");B.classList.add("wave");C.classList.add("walk2");
 }
 if(c.action==="constitution"){
 A.style.display="block";B.style.display="block";C.style.display="none";
 A.classList.add("wave");B.classList.add("walk");
 }
 showLine();
}

function showLine(){
 let line=chapters[s].lines[l];
 document.getElementById("speaker").textContent=line[0];
 document.getElementById("text").innerHTML=line[1];
 document.getElementById("status").textContent=
 "Chapter "+(s+1)+" | Dialogue "+(l+1)+" of "+chapters[s].lines.length;
}

function speak(){
 if(!("speechSynthesis" in window))return;
 speechSynthesis.cancel();
 let temp=document.createElement("div");
 temp.innerHTML=chapters[s].lines[l][1];
 let spoken=temp.textContent;
 let utter=new SpeechSynthesisUtterance(spoken);
 utter.lang="en-US";utter.rate=.9;
 let index=(s+l)%Math.max(1,englishVoices.length);
 if(englishVoices.length)utter.voice=englishVoices[index];
 utter.onend=()=>{if(playing)nextAuto()};
 speechSynthesis.speak(utter);
}

function nextAuto(){
 if(l<chapters[s].lines.length-1)l++;
 else if(s<chapters.length-1){s++;l=0;render();}
 else{
 playing=false;
 document.getElementById("status").textContent="The story is complete!";
 document.getElementById("highlights").style.display="block";
 document.getElementById("highlights").scrollIntoView({behavior:"smooth"});
 return;
 }
 showLine();speak();
}
function play(){
 if(playing)return;
 playing=true;
 speak();
}
function pause(){
 playing=false;
 speechSynthesis.pause();
 document.getElementById("status").textContent="Paused";
}
function stop(){
 playing=false;speechSynthesis.cancel();l=0;s=0;render();
}
function next(){
 playing=false;speechSynthesis.cancel();
 if(l<chapters[s].lines.length-1)l++;
 else if(s<chapters.length-1){s++;l=0;render();}
 showLine();
}
function previous(){
 playing=false;speechSynthesis.cancel();
 if(l>0)l--;
 else if(s>0){s--;l=chapters[s].lines.length-1;render();}
 showLine();
}

highlights.forEach((h,i)=>{
 let d=document.createElement("div");
 d.className="card";
 d.innerHTML="<h3>"+(i+1)+". "+h[0]+"</h3><strong>"+h[1]+"</strong><p>"+h[2]+"</p>";
 document.getElementById("highlights").appendChild(d);
});

chapters.forEach((c,i)=>{
 let d=document.createElement("div");
 d.className="card";
 let content="<h3>Chapter "+(i+1)+": "+c.title+"</h3>";
 c.lines.forEach(line=>{
 content+="<p><strong>"+line[0]+":</strong> "+line[1]+"</p>";
 });
 d.innerHTML=content;
 document.getElementById("transcript").appendChild(d);
});

document.getElementById("highlights").style.display="block";
document.getElementById("transcript").style.display="block";
render();
</script>
</body>
</html>
