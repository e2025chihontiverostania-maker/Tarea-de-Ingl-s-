
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>The Mexican Revolution - Animated Story</title>

<style>
*{box-sizing:border-box}
body{
 margin:0;
 background:#fff1d9;
 color:#342d27;
 font-family:Georgia,serif;
}
header{
 text-align:center;
 padding:35px 15px;
 background:#a84438;
 color:white;
}
header h1{font-size:clamp(2rem,5vw,3.8rem);margin:10px}
header p{font-family:Arial,sans-serif}
.tag{
 letter-spacing:3px;
 font: bold 12px Arial;
}
main{max-width:1050px;margin:auto;padding:20px}
h2{color:#387052}
button,select{
 border:0;
 border-radius:25px;
 padding:12px 17px;
 font-weight:bold;
 cursor:pointer;
}
button{background:#a84438;color:white}
button:hover{filter:brightness(1.1)}
button:disabled{opacity:.4;cursor:not-allowed}
select{background:#fff;border:1px solid #c8bba7}
.scene{
 position:relative;
 height:410px;
 overflow:hidden;
 border:7px solid white;
 border-radius:20px;
 background:linear-gradient(#8dd0df 0 65%,#b7a06b 65%);
 box-shadow:0 8px 25px #55422b35;
}
.sun{
 position:absolute;right:9%;top:9%;
 width:65px;height:65px;border-radius:50%;
 background:#ffda75;
 box-shadow:0 0 0 15px #ffda7535;
}
.cloud{
 position:absolute;top:17%;left:12%;
 width:100px;height:28px;border-radius:30px;
 background:#fff;
}
.cloud:before,.cloud:after{
 content:"";position:absolute;background:white;border-radius:50%;
}
.cloud:before{width:40px;height:40px;top:-18px;left:15px}
.cloud:after{width:48px;height:45px;top:-20px;right:10px}
.mountains{
 position:absolute;bottom:20%;width:120%;left:-10%;
 height:110px;background:#78956b;
 border-radius:50% 50% 0 0;
}
.floor{
 position:absolute;bottom:0;width:100%;height:23%;
 background:#c9a16a;
}
.house{
 position:absolute;bottom:22%;left:7%;
 width:100px;height:75px;background:#f5d4a0;
 border:4px solid #81543b;
}
.house:before{
 content:"";position:absolute;top:-35px;left:-12px;
 border-left:58px solid transparent;
 border-right:58px solid transparent;
 border-bottom:36px solid #a94b3c;
}
.house:after{
 content:"";position:absolute;bottom:0;left:35px;
 width:24px;height:38px;background:#81543b;
}
.cactus{
 position:absolute;bottom:22%;right:12%;
 width:18px;height:80px;background:#347451;
 border-radius:10px;
}
.cactus:before,.cactus:after{
 content:"";position:absolute;width:25px;height:24px;
 border:9px solid #347451;border-bottom:0;
 border-radius:20px 20px 0 0;
}
.cactus:before{left:-20px;top:25px;transform:rotate(-90deg)}
.cactus:after{right:-20px;top:40px;transform:rotate(90deg)}

.scene-title{
 position:absolute;top:15px;left:15px;
 padding:9px 13px;border-radius:8px;
 background:#fff4df;font:bold 12px Arial;
 color:#7d392f;
}
.cast{
 position:absolute;bottom:16%;left:0;right:0;
 display:flex;justify-content:center;align-items:end;
 gap:35px;height:220px;
}
.character{
 position:relative;width:100px;height:205px;
 animation:float 2s infinite ease-in-out;
}
.character:nth-child(2){animation-delay:.4s}
.character:nth-child(3){animation-delay:.8s}
.head{
 position:absolute;top:12px;left:27px;
 width:52px;height:57px;background:#bd8058;
 border:3px solid #684532;border-radius:45%;
 z-index:3;
}
.hair{
 position:absolute;top:5px;left:23px;
 width:60px;height:25px;background:#30241e;
 border-radius:50% 50% 15% 15%;z-index:4;
}
.hat{
 position:absolute;top:0;left:10px;
 width:82px;height:17px;background:#e9d4a5;
 border:3px solid #654a35;border-radius:50%;z-index:5;
}
.hat:after{
 content:"";position:absolute;top:-18px;left:23px;
 width:28px;height:20px;background:#e9d4a5;
 border:3px solid #654a35;border-radius:8px;
}
.eye{
 position:absolute;top:28px;left:12px;
 width:5px;height:5px;background:#241c17;
 border-radius:50%;box-shadow:18px 0 #241c17;
}
.mustache{
 position:absolute;top:39px;left:9px;
 width:31px;height:9px;
 border-bottom:5px solid #34231c;border-radius:50%;
}
.body{
 position:absolute;top:66px;left:16px;
 width:70px;height:82px;
 background:var(--shirt,#52734d);
 border:3px solid #684532;border-radius:16px 16px 8px 8px;
 z-index:2;
}
.arm{
 position:absolute;top:76px;left:4px;
 width:20px;height:67px;background:#bd8058;
 border:3px solid #684532;border-radius:15px;
 transform:rotate(15deg);z-index:1;
}
.arm.right{
 left:77px;transform:rotate(-15deg);
}
.legs{
 position:absolute;top:145px;left:27px;
 width:20px;height:55px;background:#60452f;
 border:3px solid #392b22;border-radius:8px;
}
.legs:after{
 content:"";position:absolute;left:25px;top:-3px;
 width:20px;height:55px;background:#60452f;
 border:3px solid #392b22;border-radius:8px;
}
.person-name{
 position:absolute;bottom:-15px;left:50%;
 transform:translateX(-50%);
 white-space:nowrap;background:#fff2d9;
 padding:4px 7px;border-radius:5px;
 font:bold 11px Arial;
}
.talking .arm.right{animation:gesture .5s infinite alternate}

@keyframes float{
 0%,100%{transform:translateY(0)}
 50%{transform:translateY(-7px)}
}
@keyframes gesture{
 from{transform:rotate(-15deg)}
 to{transform:rotate(-65deg)}
}

.dialogue{
 background:#fffaf0;
 padding:22px;
 margin-top:15px;
 border-radius:16px;
 box-shadow:0 5px 20px #55422b18;
}
.speaker{
 color:#a84438;
 font:bold 13px Arial;
 letter-spacing:2px;
}
.text{
 font-size:clamp(18px,2.5vw,23px);
 line-height:1.6;
 min-height:65px;
}
.controls{
 display:flex;flex-wrap:wrap;
 justify-content:center;gap:12px;
 margin:20px 0;
}
.progress{
 height:9px;background:#d8cbb8;
 border-radius:20px;overflow:hidden;
}
.progress div{
 height:100%;width:0;background:#a84438;
 transition:width .3s;
}
.section{
 background:#fffaf0;
 border-radius:18px;padding:25px;
 margin:30px 0;
}
.moments{
 display:grid;
 grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
 gap:15px;
}
.moment{
 background:#f5ead7;
 padding:15px;border-radius:12px;
 border-left:5px solid #a84438;
}
.moment small{
 color:#a84438;font:bold 12px Arial;
}
.moment h3{margin:8px 0}
.moment p{font:15px/1.5 Arial}
.voice-settings{
 display:grid;
 grid-template-columns:repeat(auto-fit,minmax(210px,1fr));
 gap:12px;
}
.voice-settings label{
 display:flex;flex-direction:column;
 gap:6px;font:bold 13px Arial;
}
.voice-settings select{width:100%}
.transcript p{
 font:15px/1.8 Arial;
 border-bottom:1px solid #e5dac9;
 padding:8px 0;
}
.transcript strong{color:#a84438}
.transcript u{
 text-decoration-color:#387052;
 text-decoration-thickness:2px;
 text-underline-offset:4px;
}
.note{
 text-align:center;color:#786e60;
 font:13px/1.5 Arial;
 padding:15px;
}
@media(max-width:600px){
 .scene{height:340px}
 .cast{gap:0;transform:scale(.85);transform-origin:bottom center}
 .character{margin:0 -8px}
}
</style>
</head>

<body>

<header>
 <div class="tag">AN EDUCATIONAL ANIMATED STORY</div>
 <h1>THE MEXICAN REVOLUTION</h1>
 <p>A story of courage, freedom and change</p>
</header>

<main>

<section class="scene">
 <div class="sun"></div>
 <div class="cloud"></div>
 <div class="mountains"></div>
 <div class="floor"></div>
 <div class="house"></div>
 <div class="cactus"></div>
 <div class="scene-title" id="sceneTitle">CHAPTER 1</div>
 <div class="cast" id="cast"></div>
</section>

<section class="dialogue">
 <div class="speaker" id="speaker">NARRATOR</div>
 <div class="text" id="dialogue"></div>
</section>

<div class="progress"><div id="progressBar"></div></div>

<div class="controls">
 <button id="previous">← Previous</button>
 <button id="play">▶ Play story</button>
 <button id="next">Next →</button>
 <button id="stop">■ Stop voice</button>
</div>

<section class="section">
 <h2>🎙️ Character voices</h2>
 <p>Choose an English voice for each character. Available voices depend on your device and browser.</p>
 <div class="voice-settings" id="voiceSettings"></div>
</section>

<section class="section">
 <h2>Six important historical moments</h2>
 <div class="moments">

  <article class="moment">
   <small>01 · 1910</small>
   <h3>The beginning of the Revolution</h3>
   <p>Francisco I. Madero called on Mexicans to rise against Porfirio Díaz on November 20, 1910.</p>
  </article>

  <article class="moment">
   <small>02 · 1911</small>
   <h3>Díaz leaves power</h3>
   <p>Porfirio Díaz resigned in May 1911 after the revolutionary movement became stronger.</p>
  </article>

  <article class="moment">
   <small>03 · 1911</small>
   <h3>The Plan of Ayala</h3>
   <p>Emiliano Zapata demanded land for peasants and the return of land to villages.</p>
  </article>

  <article class="moment">
   <small>04 · 1913</small>
   <h3>The Ten Tragic Days</h3>
   <p>A military coup led to the fall of Madero's government. Madero and Pino Suárez were assassinated.</p>
  </article>

  <article class="moment">
   <small>05 · 1914</small>
   <h3>Huerta's defeat</h3>
   <p>Victoriano Huerta left power, BUT revolutionary groups continued to disagree about the future of Mexico.</p>
  </article>

  <article class="moment">
   <small>06 · 1917</small>
   <h3>The Constitution of 1917</h3>
   <p>The new Constitution included important principles about education, land and workers' rights.</p>
  </article>

 </div>
</section>

<section class="section transcript">
 <h2>The complete story</h2>
 <p>Read the complete English narration and character dialogues below.</p>
 <div id="transcript"></div>
</section>

<p class="note">
The story uses your browser's English text-to-speech voices.
For the best experience, use a browser with several English voices installed.
</p>

</main>

<script>

// CHARACTER INFORMATION

const characters={
 "PORFIRIO DÍAZ":{color:"#79503d",hat:true,mustache:true},
 "MADERO":{color:"#416b91",hat:false},
 "ZAPATA":{color:"#386044",hat:true,mustache:true},
 "VILLA":{color:"#94613b",hat:true,mustache:true},
 "HUERTA":{color:"#55516e",hat:true,mustache:true},
 "CARRANZA":{color:"#657c83",hat:true,mustache:true},
 "PEASANT":{color:"#a17a3f",hat:true}
};

const scenes=[
 {
  title:"CHAPTER 1 · MEXICO UNDER PORFIRIO DÍAZ",
  people:["PORFIRIO DÍAZ","PEASANT"],
  lines:[
   ["NARRATOR","At the beginning of the twentieth century, Mexico was ruled by Porfirio Díaz."],
   ["NARRATOR","He had been president for many years. During his government, Mexico developed railroads, factories and industries."],
   ["NARRATOR","HOWEVER, not everyone benefited. Rich people owned large areas of land, while many farmers and workers lived in poverty."],
   ["PEASANT","We work every day, BUT we do not own the land. Our families need a better future!"],
   ["NARRATOR","People were tired of inequality and the lack of political freedom. They wanted a change."]
  ]
 },
 {
  title:"CHAPTER 2 · FRANCISCO I. MADERO",
  people:["MADERO","PEASANT"],
  lines:[
   ["NARRATOR","One man decided to challenge the government. His name was Francisco I. Madero."],
   ["MADERO","Mexico needs democracy! The people deserve free elections and the right to choose their president."],
   ["NARRATOR","IN 1910, Madero published the Plan of San Luis. He called for an uprising ON November 20, 1910."],
   ["MADERO","Mexicans, it is time to stand up and fight for a better country!"],
   ["NARRATOR","AND so, the Mexican Revolution began."]
  ]
 },
 {
  title:"CHAPTER 3 · THE REVOLUTION BEGINS",
  people:["ZAPATA","VILLA","PEASANT"],
  lines:[
   ["NARRATOR","ON November 20, 1910, people in different parts of Mexico began to rise against Díaz."],
   ["NARRATOR","Farmers, workers and revolutionary leaders joined the movement."],
   ["NARRATOR","In the north, Pancho Villa became an important revolutionary leader. In the south, Emiliano Zapata fought for the rights of peasants."],
   ["VILLA","We are fighting for a country where people can have a better life!"],
   ["ZAPATA","The land belongs to the people who work it!"],
   ["NARRATOR","The revolution grew stronger, AND Díaz faced increasing pressure."]
  ]
 },
 {
  title:"CHAPTER 4 · DÍAZ LEAVES POWER",
  people:["PORFIRIO DÍAZ","MADERO"],
  lines:[
   ["NARRATOR","The revolutionary movement continued to grow. Díaz could no longer control the situation."],
   ["NARRATOR","ON May 25, 1911, Porfirio Díaz resigned from the presidency."],
   ["DÍAZ","My time in power has come to an end."],
   ["NARRATOR","A few days later, Díaz left Mexico and went into exile."],
   ["NARRATOR","Madero became president ON November 6, 1911."],
   ["NARRATOR","BUT many people still wanted important social changes."]
  ]
 },
 {
  title:"CHAPTER 5 · ZAPATA AND THE LAND",
  people:["ZAPATA","VILLA"],
  lines:[
   ["NARRATOR","The revolutionaries did not all have the same goals. Madero wanted political democracy, BUT Zapata also wanted land reform."],
   ["ZAPATA","Our communities need their land back. The peasants deserve justice!"],
   ["NARRATOR","ON November 28, 1911, Zapata announced the Plan of Ayala."],
   ["NARRATOR","It demanded the return of land to villages and communities."],
   ["VILLA","The people have different needs, AND the struggle is far from over."]
  ]
 },
 {
  title:"CHAPTER 6 · THE TEN TRAGIC DAYS",
  people:["HUERTA","MADERO"],
  lines:[
   ["NARRATOR","IN February 1913, a military coup began in Mexico City. This event became known as the Ten Tragic Days."],
   ["NARRATOR","Madero was forced out of power. ON February 22, 1913, he and Vice President José María Pino Suárez were assassinated."],
   ["NARRATOR","Victoriano Huerta took control of the government."],
   ["HUERTA","I am now in control of the country!"],
   ["NARRATOR","HOWEVER, many revolutionary leaders rejected his government."],
   ["NARRATOR","The fighting continued, AND Huerta was defeated in 1914."]
  ]
 },
 {
  title:"CHAPTER 7 · A NEW CONSTITUTION",
  people:["CARRANZA","PEASANT"],
  lines:[
   ["NARRATOR","After Huerta left power, revolutionary groups continued fighting because they disagreed about the future of Mexico."],
   ["NARRATOR","Venustiano Carranza became an important leader and supported the creation of a new Constitution."],
   ["NARRATOR","ON February 5, 1917, the Constitution of 1917 was proclaimed."],
   ["NARRATOR","It included important principles about education, land ownership and workers' rights."],
   ["PEASANT","We hope these changes will help future generations!"],
   ["NARRATOR","The Revolution did not end every conflict immediately. HOWEVER, the Constitution became one of its most important results."],
   ["NARRATOR","The Mexican Revolution changed the history of Mexico. It was a struggle for democracy, land, justice and a better future."]
  ]
 }
];

// CREATE CHARACTERS

function drawCharacter(name){
 const p=characters[name];
 return `
 <div class="character" data-name="${name}">
  ${p.hat?'<div class="hat"></div>':''}
  <div class="hair"></div>
  <div class="head">
   <div class="eye"></div>
   ${p.mustache?'<div class="mustache"></div>':''}
  </div>
  <div class="arm"></div>
  <div class="arm right"></div>
  <div class="body" style="--shirt:${p.color}"></div>
  <div class="legs"></div>
  <div class="person-name">${name}</div>
 </div>`;
}

// STORY DATA

let story=[];
scenes.forEach((scene,sceneIndex)=>{
 scene.lines.forEach((line,lineIndex)=>{
  story.push({
   chapter:scene.title,
   people:scene.people,
   speaker:line[0],
   text:line[1],
   sceneIndex,
   lineIndex
  });
 });
});

let current=0;
let playing=false;
let availableVoices=[];
let selectedVoices={};

const $=id=>document.getElementById(id);

// FORMAT THE TEACHER'S REQUIREMENTS

function formatText(text){
 let safe=text
  .replaceAll("&","&amp;")
  .replaceAll("<","&lt;")
  .replaceAll(">","&gt;");

 const connectors=[
  "HOWEVER","THEREFORE","BECAUSE","ALTHOUGH",
  "WHILE","AND","BUT","SO"
 ];

 connectors.forEach(word=>{
  const regex=new RegExp("\\b"+word+"\\b","g");
  safe=safe.replace(regex,"<strong>"+word+"</strong>");
 });

 // Highlight time prepositions only when used with a date or time.
 safe=safe.replace(
  /\b(ON|IN|AT|DURING|AFTER|BEFORE)\b(?=\s+(?:January|February|March|April|May|June|July|August|September|October|November|December|1910|1911|1913|1914|1917|the twentieth century))/gi,
  "<u>$1</u>"
 );

 return safe;
}

// DISPLAY THE CURRENT STORY LINE

function render(){
 const item=story[current];

 $("sceneTitle").textContent=item.chapter;
 $("speaker").textContent=item.speaker;
 $("dialogue").textContent=item.text;

 $("cast").innerHTML=item.people.map(drawCharacter).join("");

 document.querySelectorAll(".character").forEach(el=>{
  if(el.dataset.name===item.speaker){
   el.classList.add("talking");
  }
 });

 $("progressBar").style.width=
  ((current+1)/story.length*100)+"%";

 $("previous").disabled=current===0;
 $("next").disabled=current===story.length-1;
}

// VOICE SETTINGS

function loadVoices(){
 if(!("speechSynthesis" in window))return;

 availableVoices=speechSynthesis.getVoices()
  .filter(v=>v.lang.toLowerCase().startsWith("en"));

 const roles=[
  "NARRATOR","MADERO","DÍAZ","ZAPATA",
  "VILLA","HUERTA","CARRANZA","PEASANT"
 ];

 $("voiceSettings").innerHTML=roles.map(role=>`
  <label>
   ${role}
   <select data-role="${role}">
    <option value="">Automatic voice</option>
    ${availableVoices.map((v,i)=>
     `<option value="${i}">${v.name} (${v.lang})</option>`
    ).join("")}
   </select>
  </label>
 `).join("");

 document.querySelectorAll("[data-role]").forEach(select=>{
  select.addEventListener("change",()=>{
   selectedVoices[select.dataset.role]=select.value;
  });
 });
}

// SPEAK THE CURRENT LINE

function speakLine(item,onEnd){
 if(!("speechSynthesis" in window)){
  alert("Your browser does not support text-to-speech.");
  return;
 }

 speechSynthesis.cancel();

 const utterance=new SpeechSynthesisUtterance(item.text);
 utterance.lang="en-US";

 const selected=selectedVoices[item.speaker];

 if(selected!==undefined && selected!==""){
  utterance.voice=availableVoices[Number(selected)];
 }else{
  const rolePitch={
   "NARRATOR":1,
   "MADERO":1.05,
   "DÍAZ":0.85,
   "ZAPATA":0.9,
   "VILLA":1.1,
   "HUERTA":0.8,
   "CARRANZA":0.9,
   "PEASANT":1.15
  };
  utterance.pitch=rolePitch[item.speaker]||1;
 }

 utterance.rate=item.speaker==="NARRATOR"?.88:.95;
 utterance.onend=()=>{if(onEnd)onEnd()};
 speechSynthesis.speak(utterance);
}

// PLAY THE WHOLE STORY

function playStory(){
 if(playing){
  playing=false;
  speechSynthesis.cancel();
  $("play").textContent="▶ Play story";
  return;
 }

 playing=true;
 $("play").textContent="Ⅱ Pause story";

 function playNext(){
  if(!playing)return;

  const item=story[current];

  render();

  speakLine(item,()=>{
   if(!playing)return;

   if(current<story.length-1){
    current++;
    playNext();
   }else{
    playing=false;
    $("play").textContent="▶ Play story";
   }
  });
 }

 playNext();
}

// BUTTONS

$("play").onclick=playStory;

$("next").onclick=()=>{
 playing=false;
 speechSynthesis.cancel();

 if(current<story.length-1)current++;

 $("play").textContent="▶ Play story";
 render();
};

$("previous").onclick=()=>{
 playing=false;
 speechSynthesis.cancel();

 if(current>0)current--;

 $("play").textContent="▶ Play story";
 render();
};

$("stop").onclick=()=>{
 playing=false;
 speechSynthesis.cancel();
 $("play").textContent="▶ Play story";
};

// COMPLETE WRITTEN SCRIPT

$("transcript").innerHTML=story.map(item=>`
 <p>
  <b>${item.speaker}:</b>
  ${formatText(item.text)}
 </p>
`).join("");

// START

if("speechSynthesis" in window){
 loadVoices();
 speechSynthesis.onvoiceschanged=loadVoices;
}

render();

</script>
</body>
</html>
