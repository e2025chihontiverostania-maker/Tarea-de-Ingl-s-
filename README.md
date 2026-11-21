
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>The Mexican Revolution - Animated Story</title>

<style>
*{box-sizing:border-box}

body{
 margin:0;
 background:#f4ead9;
 color:#332b25;
 font-family:Georgia,serif;
}

header{
 background:#963f35;
 color:white;
 text-align:center;
 padding:32px 15px;
}

header h1{
 font-size:clamp(2rem,5vw,3.7rem);
 margin:12px 0;
}

header p{
 font-family:Arial,sans-serif;
}

.eyebrow{
 font:bold 12px Arial;
 letter-spacing:3px;
}

main{
 max-width:1100px;
 margin:auto;
 padding:20px;
}

h2{color:#376c50}

.scene{
 position:relative;
 height:410px;
 overflow:hidden;
 border:7px solid white;
 border-radius:20px;
 background:linear-gradient(#8ed0dc 0 65%,#c5a06c 65%);
 box-shadow:0 8px 25px #0002;
}

.sun{
 position:absolute;
 top:9%;
 right:10%;
 width:65px;
 height:65px;
 border-radius:50%;
 background:#ffdc79;
 box-shadow:0 0 0 15px #ffdc7935;
}

.cloud{
 position:absolute;
 top:18%;
 left:13%;
 width:100px;
 height:28px;
 background:white;
 border-radius:30px;
}

.cloud:before,.cloud:after{
 content:"";
 position:absolute;
 background:white;
 border-radius:50%;
}

.cloud:before{
 width:40px;
 height:40px;
 top:-18px;
 left:15px;
}

.cloud:after{
 width:48px;
 height:45px;
 top:-20px;
 right:10px;
}

.mountains{
 position:absolute;
 bottom:20%;
 left:-10%;
 width:120%;
 height:110px;
 background:#78976d;
 border-radius:50% 50% 0 0;
}

.floor{
 position:absolute;
 bottom:0;
 width:100%;
 height:23%;
 background:#c8a16b;
}

.house{
 position:absolute;
 bottom:22%;
 left:7%;
 width:100px;
 height:75px;
 background:#f2d5a5;
 border:4px solid #81543b;
}

.house:before{
 content:"";
 position:absolute;
 top:-35px;
 left:-12px;
 border-left:58px solid transparent;
 border-right:58px solid transparent;
 border-bottom:36px solid #a94b3c;
}

.house:after{
 content:"";
 position:absolute;
 bottom:0;
 left:35px;
 width:24px;
 height:38px;
 background:#81543b;
}

.cactus{
 position:absolute;
 bottom:22%;
 right:12%;
 width:18px;
 height:80px;
 background:#397653;
 border-radius:10px;
}

.cactus:before,.cactus:after{
 content:"";
 position:absolute;
 width:25px;
 height:24px;
 border:9px solid #397653;
 border-bottom:0;
 border-radius:20px 20px 0 0;
}

.cactus:before{
 left:-20px;
 top:25px;
 transform:rotate(-90deg);
}

.cactus:after{
 right:-20px;
 top:40px;
 transform:rotate(90deg);
}

.scene-title{
 position:absolute;
 top:15px;
 left:15px;
 padding:9px 13px;
 border-radius:8px;
 background:#fff3dc;
 color:#813a31;
 font:bold 12px Arial;
 z-index:5;
}

.cast{
 position:absolute;
 bottom:16%;
 left:0;
 right:0;
 display:flex;
 justify-content:center;
 align-items:end;
 gap:30px;
 height:220px;
}

.character{
 position:relative;
 width:100px;
 height:205px;
 animation:float 2s infinite ease-in-out;
}

.character:nth-child(2){animation-delay:.4s}
.character:nth-child(3){animation-delay:.8s}

.head{
 position:absolute;
 top:12px;
 left:27px;
 width:52px;
 height:57px;
 background:#bd8058;
 border:3px solid #684532;
 border-radius:45%;
 z-index:3;
}

.hair{
 position:absolute;
 top:5px;
 left:23px;
 width:60px;
 height:25px;
 background:#30241e;
 border-radius:50% 50% 15% 15%;
 z-index:4;
}

.hat{
 position:absolute;
 top:0;
 left:10px;
 width:82px;
 height:17px;
 background:#e9d4a5;
 border:3px solid #654a35;
 border-radius:50%;
 z-index:5;
}

.hat:after{
 content:"";
 position:absolute;
 top:-18px;
 left:23px;
 width:28px;
 height:20px;
 background:#e9d4a5;
 border:3px solid #654a35;
 border-radius:8px;
}

.eye{
 position:absolute;
 top:28px;
 left:12px;
 width:5px;
 height:5px;
 background:#241c17;
 border-radius:50%;
 box-shadow:18px 0 #241c17;
}

.mustache{
 position:absolute;
 top:39px;
 left:9px;
 width:31px;
 height:9px;
 border-bottom:5px solid #34231c;
 border-radius:50%;
}

.body{
 position:absolute;
 top:66px;
 left:16px;
 width:70px;
 height:82px;
 background:var(--shirt,#52734d);
 border:3px solid #684532;
 border-radius:16px 16px 8px 8px;
 z-index:2;
}

.arm{
 position:absolute;
 top:76px;
 left:4px;
 width:20px;
 height:67px;
 background:#bd8058;
 border:3px solid #684532;
 border-radius:15px;
 transform:rotate(15deg);
 z-index:1;
}

.arm.right{
 left:77px;
 transform:rotate(-15deg);
}

.legs{
 position:absolute;
 top:145px;
 left:27px;
 width:20px;
 height:55px;
 background:#60452f;
 border:3px solid #392b22;
 border-radius:8px;
}

.legs:after{
 content:"";
 position:absolute;
 left:25px;
 top:-3px;
 width:20px;
 height:55px;
 background:#60452f;
 border:3px solid #392b22;
 border-radius:8px;
}

.person-name{
 position:absolute;
 bottom:-15px;
 left:50%;
 transform:translateX(-50%);
 white-space:nowrap;
 background:#fff2d9;
 padding:4px 7px;
 border-radius:5px;
 font:bold 11px Arial;
}

.talking .arm.right{
 animation:gesture .5s infinite alternate;
}

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
 line-height:1.7;
 min-height:65px;
}

.text strong,.transcript strong{
 font-weight:900;
 color:#a33128;
}

.text u,.transcript u{
 text-decoration-thickness:2px;
 text-decoration-color:#387052;
 text-underline-offset:4px;
}

.controls{
 display:flex;
 flex-wrap:wrap;
 justify-content:center;
 gap:12px;
 margin:20px 0;
}

button,select{
 border:0;
 border-radius:25px;
 padding:12px 17px;
 font-weight:bold;
 cursor:pointer;
}

button{
 background:#a84438;
 color:white;
}

button.secondary{
 background:#397052;
}

button:disabled{
 opacity:.4;
 cursor:not-allowed;
}

.progress{
 height:9px;
 background:#d8cbb8;
 border-radius:20px;
 overflow:hidden;
}

.progress div{
 height:100%;
 width:0;
 background:#a84438;
 transition:width .3s;
}

.section{
 background:#fffaf0;
 border-radius:18px;
 padding:25px;
 margin:30px 0;
}

.moments{
 display:grid;
 grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
 gap:15px;
}

.moment{
 background:#f5ead7;
 padding:15px;
 border-radius:12px;
 border-left:5px solid #a84438;
}

.moment small{
 color:#a84438;
 font:bold 12px Arial;
}

.moment h3{margin:8px 0}

.moment p{
 font:15px/1.5 Arial;
}

.voice-settings{
 display:grid;
 grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
 gap:14px;
}

.voice-settings label{
 display:flex;
 flex-direction:column;
 gap:7px;
 font:bold 13px Arial;
}

.voice-settings select{
 width:100%;
 background:white;
 border:1px solid #d0c1ad;
}

.voice-status{
 font:14px/1.5 Arial;
 color:#397052;
}

.transcript p{
 font:15px/1.8 Arial;
 border-bottom:1px solid #e5dac9;
 padding:8px 0;
}

.note{
 text-align:center;
 color:#786e60;
 font:13px/1.5 Arial;
 padding:15px;
}

@media(max-width:600px){
 .scene{height:340px}
 .cast{
  gap:0;
  transform:scale(.85);
  transform-origin:bottom center;
 }
 .character{margin:0 -8px}
}
</style>
</head>

<body>

<header>
 <div class="eyebrow">AN EDUCATIONAL ANIMATED STORY</div>
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

<div class="progress">
 <div id="progressBar"></div>
</div>

<div class="controls">
 <button id="previous">← Previous</button>
 <button id="play">▶ Play story</button>
 <button id="next">Next →</button>
 <button class="secondary" id="speak">🔊 Speak this line</button>
 <button class="secondary" id="stop">■ Stop voice</button>
</div>

<section class="section">
 <h2>🎙️ Character voices</h2>
 <p>Each character has a preselected English voice. You can change the voice if you want.</p>
 <div id="voiceStatus" class="voice-status">Loading English voices...</div>
 <div class="voice-settings" id="voiceSettings"></div>
</section>

<section class="section">
 <h2>Six Important Historical Moments</h2>

 <div class="moments">

  <article class="moment">
   <small>01 · 1910</small>
   <h3>The Beginning of the Revolution</h3>
   <p>Francisco I. Madero called on Mexicans to rise against Porfirio Díaz on November 20, 1910.</p>
  </article>

  <article class="moment">
   <small>02 · 1911</small>
   <h3>Díaz Leaves Power</h3>
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
   <h3>Huerta's Defeat</h3>
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
 <h2>The Complete Story</h2>
 <p>Read the complete English narration and character dialogues below.</p>
 <div id="transcript"></div>
</section>

<p class="note">
The voices are generated by your browser. Available English voices depend on the device.
</p>

</main>

<script>

// CHARACTER INFORMATION

const characters={
 "PORFIRIO DÍAZ":{
  color:"#79503d",hat:true,mustache:true
 },
 "MADERO":{
  color:"#416b91",hat:false,mustache:false
 },
 "ZAPATA":{
  color:"#386044",hat:true,mustache:true
 },
 "VILLA":{
  color:"#94613b",hat:true,mustache:true
 },
 "HUERTA":{
  color:"#55516e",hat:true,mustache:true
 },
 "CARRANZA":{
  color:"#657c83",hat:true,mustache:true
 },
 "PEASANT":{
  color:"#a17a3f",hat:true,mustache:false
 }
};

// STORY

const scenes=[

{
 title:"CHAPTER 1 · MEXICO UNDER PORFIRIO DÍAZ",
 people:["PORFIRIO DÍAZ","PEASANT"],
 lines:[
  ["NARRATOR","At the beginning of the twentieth century, Mexico was ruled by Porfirio Díaz."],
  ["NARRATOR","He had been president for many years. During his government, Mexico developed railroads, factories and industries."],
  ["NARRATOR","HOWEVER, not everyone benefited. Rich people owned large areas of land, while many farmers and workers lived in poverty."],
  ["PEASANT","We work every day, BUT we do not own the land. Our families need a better future!"],
  ["NARRATOR","People were tired of inequality and the lack of political freedom. They wanted change."]
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
  ["PEASANT","We want land, justice and a better future for our families!"],
  ["NARRATOR","The revolution grew stronger, AND Díaz faced increasing pressure."]
 ]
},

{
 title:"CHAPTER 4 · DÍAZ LEAVES POWER",
 people:["PORFIRIO DÍAZ","MADERO"],
 lines:[
  ["NARRATOR","The revolutionary movement continued to grow. Díaz could no longer control the situation."],
  ["NARRATOR","ON May 25, 1911, Porfirio Díaz resigned from the presidency."],
  ["PORFIRIO DÍAZ","My time in power has come to an end."],
  ["NARRATOR","A few days later, Díaz left Mexico and went into exile."],
  ["NARRATOR","Madero became president ON November 6, 1911."],
  ["NARRATOR","BUT many people still wanted important social changes."]
 ]
},

{
 title:"CHAPTER 5 · ZAPATA AND THE LAND",
 people:["ZAPATA","VILLA","PEASANT"],
 lines:[
  ["NARRATOR","The revolutionaries did not all have the same goals. Madero wanted political democracy, BUT Zapata also wanted land reform."],
  ["ZAPATA","Our communities need their land back. The peasants deserve justice!"],
  ["NARRATOR","ON November 28, 1911, Zapata announced the Plan of Ayala."],
  ["NARRATOR","It demanded the return of land to villages and communities."],
  ["PEASANT","We need our land to grow food and support our families!"],
  ["VILLA","The people have different needs, AND the struggle is far from over."]
 ]
},

{
 title:"CHAPTER 6 · THE TEN TRAGIC DAYS",
 people:["HUERTA","MADERO","PEASANT"],
 lines:[
  ["NARRATOR","IN February 1913, a military coup began in Mexico City. This event became known as the Ten Tragic Days."],
  ["NARRATOR","Madero was forced out of power. ON February 22, 1913, he and Vice President José María Pino Suárez were assassinated."],
  ["NARRATOR","Victoriano Huerta took control of the government."],
  ["HUERTA","I am now in control of the country!"],
  ["NARRATOR","HOWEVER, many revolutionary leaders rejected his government."],
  ["PEASANT","We still want justice and a better future!"],
  ["NARRATOR","The fighting continued, AND Huerta was defeated in 1914."]
 ]
},

{
 title:"CHAPTER 7 · A NEW CONSTITUTION",
 people:["CARRANZA","PEASANT","ZAPATA"],
 lines:[
  ["NARRATOR","After Huerta left power, revolutionary groups continued fighting because they disagreed about the future of Mexico."],
  ["NARRATOR","Venustiano Carranza became an important leader and supported the creation of a new Constitution."],
  ["NARRATOR","ON February 5, 1917, the Constitution of 1917 was proclaimed."],
  ["NARRATOR","It included important principles about education, land ownership and workers' rights."],
  ["CARRANZA","A new Constitution can help establish important rights for the country."],
  ["PEASANT","We hope these changes will help future generations!"],
  ["NARRATOR","The Revolution did not end every conflict immediately. HOWEVER, the Constitution became one of its most important results."],
  ["NARRATOR","The Mexican Revolution changed the history of Mexico. It was a struggle for democracy, land, justice and a better future."]
 ]
}

];

// FLATTEN THE STORY

const story=[];

scenes.forEach((scene,sceneIndex)=>{
 scene.lines.forEach(line=>{
  story.push({
   chapter:scene.title,
   people:scene.people,
   speaker:line[0],
   text:line[1],
   sceneIndex
  });
 });
});

let current=0;
let playing=false;
let availableVoices=[];
let selectedVoices={};
let playbackToken=0;

const $=id=>document.getElementById(id);

// CHARACTER DRAWING

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

// TEXT FORMATTING
// The audio reads the original text.
// HTML formatting is only used for the written version.

function formatText(text){

 let safe=text
  .replaceAll("&","&amp;")
  .replaceAll("<","&lt;")
  .replaceAll(">","&gt;");

 // CONNECTORS: BOLD AND UPPERCASE

 const connectors=[
  "HOWEVER",
  "THEREFORE",
  "BECAUSE",
  "ALTHOUGH",
  "WHILE",
  "AND",
  "BUT",
  "SO"
 ];

 connectors.forEach(word=>{
  const regex=new RegExp("\\b"+word+"\\b","gi");

  safe=safe.replace(regex,match=>
   "<strong>"+match.toUpperCase()+"</strong>"
  );
 });

 // TIME PREPOSITIONS

 const timeWords=[
  "ON","IN","AT","DURING","AFTER","BEFORE"
 ];

 timeWords.forEach(word=>{
  const regex=new RegExp(
   "\\b"+word+"\\b(?=\\s+(?:January|February|March|April|May|June|July|August|September|October|November|December|1910|1911|1913|1914|1917|the twentieth century|the beginning))",
   "gi"
  );

  safe=safe.replace(regex,match=>"<u>"+match+"</u>");
 });

 return safe;
}

// RENDER SCENE

function render(){

 const item=story[current];

 $("sceneTitle").textContent=item.chapter;
 $("speaker").textContent=item.speaker;

 // FORMATTED WRITTEN TEXT
 $("dialogue").innerHTML=formatText(item.text);

 $("cast").innerHTML=item.people
  .map(drawCharacter)
  .join("");

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

// VOICE ASSIGNMENT

function loadVoices(){

 if(!("speechSynthesis" in window))return;

 availableVoices=speechSynthesis.getVoices()
  .filter(v=>v.lang.toLowerCase().startsWith("en"));

 const roles=[
  "NARRATOR",
  "MADERO",
  "PORFIRIO DÍAZ",
  "ZAPATA",
  "VILLA",
  "HUERTA",
  "CARRANZA",
  "PEASANT"
 ];

 if(availableVoices.length===0){
  $("voiceStatus").textContent=
   "English voices are not available yet. Please wait or check your browser settings.";
  return;
 }

 // Assign a voice to EVERY character.
 // If the device has fewer voices than characters,
 // some characters will share a voice.

 const voicePreferences={
  "NARRATOR":0,
  "MADERO":1,
  "PORFIRIO DÍAZ":2,
  "ZAPATA":3,
  "VILLA":4,
  "HUERTA":5,
  "CARRANZA":6,
  "PEASANT":7
 };

 roles.forEach(role=>{
  const preferred=voicePreferences[role];
  const voiceIndex=preferred%availableVoices.length;
  selectedVoices[role]=String(voiceIndex);
 });

 $("voiceSettings").innerHTML=roles.map(role=>{

  const selected=selectedVoices[role];

  return `
   <label>
    ${role}
    <select data-role="${role}">
     ${availableVoices.map((voice,index)=>`
      <option value="${index}" ${String(index)===selected?"selected":""}>
       ${voice.name} (${voice.lang})
      </option>
     `).join("")}
    </select>
   </label>
  `;
 }).join("");

 document.querySelectorAll("[data-role]").forEach(select=>{
  select.addEventListener("change",()=>{
   selectedVoices[select.dataset.role]=select.value;
  });
 });

 $("voiceStatus").textContent=
  availableVoices.length+" English voices detected. Voices have been assigned to all characters.";
}

// SPEAK ONE LINE

function speakLine(item,onEnd,token){

 if(!("speechSynthesis" in window))return;

 const utterance=new SpeechSynthesisUtterance(item.text);

 utterance.lang="en-US";

 const voiceIndex=Number(selectedVoices[item.speaker]);
 const chosenVoice=availableVoices[voiceIndex];

 if(chosenVoice){
  utterance.voice=chosenVoice;
 }

 const pitch={
  "NARRATOR":1,
  "MADERO":1.08,
  "PORFIRIO DÍAZ":0.85,
  "ZAPATA":0.9,
  "VILLA":1.15,
  "HUERTA":0.82,
  "CARRANZA":0.95,
  "PEASANT":1.2
 };

 utterance.pitch=pitch[item.speaker]||1;
 utterance.rate=item.speaker==="NARRATOR"?.88:.95;

 utterance.onend=()=>{
  if(token!==playbackToken)return;
  if(onEnd)onEnd();
 };

 utterance.onerror=(event)=>{
  if(token!==playbackToken)return;

  console.error("Speech error:",event.error);

  if(onEnd)onEnd();
 };

 speechSynthesis.speak(utterance);
}

// PLAY THE COMPLETE STORY

function playStory(){

 if(playing){
  playing=false;
  playbackToken++;
  speechSynthesis.cancel();
  $("play").textContent="▶ Play story";
  return;
 }

 playing=true;
 playbackToken++;

 const token=playbackToken;

 $("play").textContent="Ⅱ Pause story";

 function playNext(){

  if(!playing||token!==playbackToken)return;

  render();

  const item=story[current];

  speakLine(item,()=>{

   if(!playing||token!==playbackToken)return;

   if(current<story.length-1){
    current++;
    playNext();
   }else{
    playing=false;
    $("play").textContent="▶ Play story";
   }

  },token);
 }

 playNext();
}

// STOP PLAYBACK

function stopPlayback(){

 playing=false;
 playbackToken++;

 speechSynthesis.cancel();

 $("play").textContent="▶ Play story";
}

// BUTTONS

$("play").onclick=playStory;

$("stop").onclick=stopPlayback;

$("next").onclick=()=>{
 stopPlayback();

 if(current<story.length-1){
  current++;
 }

 render();
};

$("previous").onclick=()=>{
 stopPlayback();

 if(current>0){
  current--;
 }

 render();
};

// SPEAK THE CURRENT LINE

$("speak").onclick=()=>{
 stopPlayback();

 const token=playbackToken;
 const item=story[current];

 speakLine(item,null,token);
};

// COMPLETE TRANSCRIPT

$("transcript").innerHTML=story.map(item=>`
 <p>
  <b>${item.speaker}:</b>
  ${formatText(item.text)}
 </p>
`).join("");

// INITIALIZE VOICES

function initialize(){

 render();

 if(!("speechSynthesis" in window)){
  $("voiceStatus").textContent=
   "This browser does not support speech synthesis.";
  return;
 }

 loadVoices();

 speechSynthesis.onvoiceschanged=loadVoices;

 // Try again because some browsers load voices asynchronously.
 setTimeout(()=>{
  if(availableVoices.length===0){
   loadVoices();
  }
 },1000);
}

initialize();

</script>
</body>
</html>
