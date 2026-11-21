
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>The Mexican Revolution - An Animated Story</title>

<style>
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    font-family: "Trebuchet MS", Arial, sans-serif;
    background: #f5e8cf;
    color: #392b20;
}

header {
    text-align: center;
    padding: 28px 15px;
    background: #783d2b;
    color: white;
}

header h1 {
    margin: 0;
    font-size: clamp(25px, 5vw, 42px);
}

header p {
    margin-bottom: 0;
}

main {
    max-width: 1050px;
    margin: auto;
    padding: 20px;
}

h2 {
    color: #783d2b;
}

.stage {
    position: relative;
    height: 390px;
    overflow: hidden;
    border: 5px solid #783d2b;
    border-radius: 18px;
    background: linear-gradient(#83c9e8 0%, #c8e8e7 65%, #e8cf8c 65%);
}

.sun {
    position: absolute;
    top: 25px;
    right: 65px;
    width: 65px;
    height: 65px;
    border-radius: 50%;
    background: #ffd45d;
}

.cloud {
    position: absolute;
    top: 60px;
    left: 12%;
    width: 100px;
    height: 30px;
    background: white;
    border-radius: 30px;
}

.cloud:before,
.cloud:after {
    content: "";
    position: absolute;
    background: white;
    border-radius: 50%;
}

.cloud:before {
    width: 42px;
    height: 42px;
    top: -20px;
    left: 18px;
}

.cloud:after {
    width: 50px;
    height: 50px;
    top: -25px;
    right: 15px;
}

.mountain {
    position: absolute;
    bottom: 115px;
    width: 0;
    height: 0;
    border-left: 150px solid transparent;
    border-right: 150px solid transparent;
    border-bottom: 170px solid #8e9c63;
}

.mountain.one {
    left: -50px;
}

.mountain.two {
    right: -40px;
    border-bottom-color: #a9a66d;
}

.ground {
    position: absolute;
    bottom: 0;
    width: 100%;
    height: 120px;
    background: #c49a54;
}

.house {
    position: absolute;
    bottom: 95px;
    left: 8%;
    width: 105px;
    height: 75px;
    background: #d7a36b;
    border: 3px solid #71432c;
}

.house:before {
    content: "";
    position: absolute;
    top: -45px;
    left: -10px;
    width: 0;
    height: 0;
    border-left: 60px solid transparent;
    border-right: 60px solid transparent;
    border-bottom: 48px solid #8b4430;
}

.house:after {
    content: "";
    position: absolute;
    bottom: 0;
    left: 38px;
    width: 25px;
    height: 42px;
    background: #68422e;
}

.cactus {
    position: absolute;
    bottom: 90px;
    right: 12%;
    width: 22px;
    height: 90px;
    background: #397b49;
    border-radius: 15px;
}

.cactus:before,
.cactus:after {
    content: "";
    position: absolute;
    width: 22px;
    height: 45px;
    border: 10px solid #397b49;
    border-bottom: 0;
    border-radius: 20px 20px 0 0;
}

.cactus:before {
    left: -22px;
    top: 25px;
}

.cactus:after {
    right: -22px;
    top: 10px;
}

.character {
    position: absolute;
    bottom: 80px;
    left: 50%;
    transform: translateX(-50%);
    width: 105px;
    height: 190px;
    transition: left .5s ease;
    animation: idle 2s infinite ease-in-out;
}

@keyframes idle {
    0%, 100% { transform: translateX(-50%) translateY(0); }
    50% { transform: translateX(-50%) translateY(-5px); }
}

.head {
    position: absolute;
    top: 0;
    left: 25px;
    width: 58px;
    height: 65px;
    border-radius: 45% 45% 48% 48%;
    background: #c98d62;
    border: 2px solid #573b2a;
}

.hair {
    position: absolute;
    top: -5px;
    left: 20px;
    width: 68px;
    height: 24px;
    border-radius: 50% 50% 15% 15%;
    background: #38261c;
}

.hat {
    position: absolute;
    top: -17px;
    left: 10px;
    width: 88px;
    height: 15px;
    background: #d8c49a;
    border: 2px solid #65462b;
    border-radius: 50%;
}

.hat:before {
    content: "";
    position: absolute;
    left: 20px;
    top: -18px;
    width: 44px;
    height: 20px;
    background: #d8c49a;
    border: 2px solid #65462b;
    border-radius: 50% 50% 0 0;
}

.body-character {
    position: absolute;
    top: 62px;
    left: 15px;
    width: 80px;
    height: 105px;
    border-radius: 15px 15px 5px 5px;
    background: #704d3a;
    border: 2px solid #503322;
}

.arm {
    position: absolute;
    top: 78px;
    width: 20px;
    height: 75px;
    background: #c98d62;
    border-radius: 15px;
}

.arm.left {
    left: 2px;
    transform: rotate(15deg);
}

.arm.right {
    right: 2px;
    transform: rotate(-15deg);
}

.legs {
    position: absolute;
    top: 160px;
    left: 25px;
    width: 55px;
    height: 35px;
    background: #49362b;
    border-radius: 5px;
}

.character.speaking {
    animation: speaking .35s infinite alternate;
}

@keyframes speaking {
    from { transform: translateX(-50%) translateY(0) rotate(-2deg); }
    to { transform: translateX(-50%) translateY(-7px) rotate(2deg); }
}

.dialogue {
    background: white;
    padding: 20px;
    margin-top: 15px;
    border-radius: 14px;
    min-height: 125px;
    box-shadow: 0 3px 10px #0002;
}

#speaker {
    font-weight: bold;
    color: #a34c2d;
    margin-bottom: 8px;
}

#dialogueText {
    font-size: 18px;
    line-height: 1.6;
}

.controls {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 10px;
    margin: 18px 0;
}

button {
    border: none;
    padding: 12px 19px;
    border-radius: 9px;
    cursor: pointer;
    background: #783d2b;
    color: white;
    font-size: 15px;
    font-weight: bold;
}

button:hover {
    background: #a85a38;
}

button:disabled {
    opacity: .45;
    cursor: not-allowed;
}

.voice-panel,
.moments,
.transcript {
    background: white;
    padding: 20px;
    margin-top: 25px;
    border-radius: 14px;
    box-shadow: 0 3px 10px #0001;
}

.voice-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 12px;
}

.voice-grid label {
    display: block;
    font-weight: bold;
    font-size: 14px;
}

.voice-grid select {
    width: 100%;
    margin-top: 6px;
    padding: 8px;
    border-radius: 7px;
    border: 1px solid #c9b49a;
}

.moments-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 15px;
}

.moment {
    background: #f7ead5;
    border-left: 5px solid #a34c2d;
    padding: 15px;
    border-radius: 9px;
}

.moment h3 {
    margin-top: 0;
    color: #783d2b;
}

.transcript p {
    line-height: 1.7;
    border-bottom: 1px solid #eee;
    padding-bottom: 10px;
}

footer {
    text-align: center;
    padding: 20px;
    color: #765c48;
}

@media(max-width:600px) {
    .stage {
        height: 330px;
    }

    .character {
        transform: translateX(-50%) scale(.85);
        transform-origin: bottom center;
    }

    #dialogueText {
        font-size: 16px;
    }
}
</style>
</head>

<body>

<header>
    <h1>The Mexican Revolution</h1>
    <p>An animated historical story</p>
</header>

<main>

<section>
    <h2>🎬 The Story</h2>

    <div class="stage">
        <div class="sun"></div>
        <div class="cloud"></div>
        <div class="mountain one"></div>
        <div class="mountain two"></div>
        <div class="house"></div>
        <div class="cactus"></div>
        <div class="ground"></div>

        <div class="character" id="character">
            <div class="hat" id="hat"></div>
            <div class="head"></div>
            <div class="hair"></div>
            <div class="body-character"></div>
            <div class="arm left"></div>
            <div class="arm right"></div>
            <div class="legs"></div>
        </div>
    </div>

    <div class="dialogue">
        <div id="speaker">NARRATOR</div>
        <div id="dialogueText">
            Welcome to the story of the Mexican Revolution.
        </div>
    </div>

    <div class="controls">
        <button id="previousButton" onclick="previousLine()">⏮ Previous</button>
        <button onclick="speakCurrentLine()">🔊 Speak this line</button>
        <button id="nextButton" onclick="nextLine()">Next ⏭</button>
        <button onclick="playStory()">▶ Play story</button>
        <button onclick="stopStory()">■ Stop</button>
    </div>
</section>

<section class="voice-panel">
    <h2>🎙 Character voices</h2>
    <p>
        The narrator uses a female English voice. All the historical
        characters use male English voices.
    </p>
    <div id="voiceStatus">Loading English voices...</div>
    <div class="voice-grid" id="voiceSettings"></div>
</section>

<section class="moments">
    <h2>📜 Six Key Historical Moments</h2>

    <div class="moments-grid">
        <div class="moment">
            <h3>1. The Porfiriato</h3>
            <p>
                Porfirio Díaz ruled Mexico for many years.
                Economic growth occurred, but wealth and land
                were distributed unequally.
            </p>
        </div>

        <div class="moment">
            <h3>2. The Plan of San Luis</h3>
            <p>
                In 1910, Francisco I. Madero called on the Mexican
                people to rise up against Díaz on November 20.
            </p>
        </div>

        <div class="moment">
            <h3>3. Díaz Leaves Power</h3>
            <p>
                Porfirio Díaz resigned on May 25, 1911.
                Madero became president on November 6, 1911.
            </p>
        </div>

        <div class="moment">
            <h3>4. The Plan of Ayala</h3>
            <p>
                On November 28, 1911, Emiliano Zapata
                demanded land reform and justice for peasants.
            </p>
        </div>

        <div class="moment">
            <h3>5. The Ten Tragic Days</h3>
            <p>
                In February 1913, a coup took place.
                Madero and Pino Suárez were assassinated
                on February 22.
            </p>
        </div>

        <div class="moment">
            <h3>6. The Constitution of 1917</h3>
            <p>
                On February 5, 1917, a new Constitution was
                promulgated, including important social rights.
            </p>
        </div>
    </div>
</section>

<section class="transcript">
    <h2>📖 Complete Story Transcript</h2>
    <div id="fullTranscript"></div>
</section>

</main>

<footer>
    The Mexican Revolution | English History Project
</footer>

<script>
const story = [
    {
        speaker: "NARRATOR",
        text: "At the beginning of the twentieth century, Mexico was a country full of contrasts. For many years, Porfirio Díaz had ruled the nation. This period was known as the Porfiriato."
    },
    {
        speaker: "NARRATOR",
        text: "During his government, railways, industries, and cities grew. HOWEVER, not everyone benefited. Many peasants lost their land, workers had difficult conditions, and wealth was concentrated in the hands of a few people."
    },
    {
        speaker: "PEASANT",
        text: "We work hard every day, BUT we do not have enough land or fair opportunities. We want justice!"
    },
    {
        speaker: "PORFIRIO DÍAZ",
        text: "Mexico needs order and progress. I believe my government has brought stability to the country."
    },
    {
        speaker: "NARRATOR",
        text: "As the years passed, more people began to demand political change. One of them was Francisco I. Madero, who wanted democracy and free elections."
    },
    {
        speaker: "MADERO",
        text: "The people deserve the right to choose their leaders. Mexico needs democracy, not a government that stays in power forever!"
    },
    {
        speaker: "NARRATOR",
        text: "In 1910, Madero published the Plan of San Luis. He called on the Mexican people to rise up against Díaz on November 20, 1910."
    },
    {
        speaker: "MADERO",
        text: "I invite the Mexican people to fight for democracy and a better future. Our country needs change!"
    },
    {
        speaker: "NARRATOR",
        text: "The Mexican Revolution began. Different groups joined the movement, including peasants, workers, and revolutionary leaders."
    },
    {
        speaker: "VILLA",
        text: "We will fight for a country where people have more opportunities. The people must be heard!"
    },
    {
        speaker: "ZAPATA",
        text: "Land and freedom are essential. The peasants deserve the land they work!"
    },
    {
        speaker: "NARRATOR",
        text: "The movement grew stronger. THEREFORE, Porfirio Díaz resigned on May 25, 1911, and left Mexico. Later, Francisco I. Madero became president on November 6, 1911."
    },
    {
        speaker: "MADERO",
        text: "This is a new opportunity for Mexico. We must build a government that respects the people."
    },
    {
        speaker: "NARRATOR",
        text: "HOWEVER, not everyone agreed with Madero's government. Emiliano Zapata believed that the promises about land reform were not being fulfilled."
    },
    {
        speaker: "ZAPATA",
        text: "We need real changes. The peasants cannot continue waiting for the land they deserve!"
    },
    {
        speaker: "NARRATOR",
        text: "On November 28, 1911, Zapata presented the Plan of Ayala. It demanded land reform and defended the rights of peasants."
    },
    {
        speaker: "NARRATOR",
        text: "In February 1913, another conflict began in Mexico City. It became known as the Ten Tragic Days. General Victoriano Huerta participated in the coup against Madero."
    },
    {
        speaker: "HUERTA",
        text: "I will take control of the government. The political situation is changing."
    },
    {
        speaker: "NARRATOR",
        text: "Madero and Vice President José María Pino Suárez were assassinated on February 22, 1913. Their deaths caused even more conflict."
    },
    {
        speaker: "NARRATOR",
        text: "Venustiano Carranza opposed Huerta and organized a movement to restore constitutional order."
    },
    {
        speaker: "CARRANZA",
        text: "We must defend the Constitution and establish a legitimate government. Mexico needs laws that protect its people."
    },
    {
        speaker: "NARRATOR",
        text: "During 1914, Huerta's government was defeated. Nevertheless, different revolutionary groups continued to disagree about the future of Mexico."
    },
    {
        speaker: "VILLA",
        text: "We have fought for change. Now we must decide what kind of country we want to build."
    },
    {
        speaker: "ZAPATA",
        text: "A better Mexico must include justice and land for the peasants."
    },
    {
        speaker: "NARRATOR",
        text: "Finally, on February 5, 1917, a new Constitution was promulgated. It included important rights related to education, land, and workers."
    },
    {
        speaker: "CARRANZA",
        text: "This Constitution is an important step toward a new Mexico. The country needs laws that recognize social rights."
    },
    {
        speaker: "NARRATOR",
        text: "The Mexican Revolution transformed the country's political and social life. Although conflicts did not end immediately in 1917, the Revolution changed the future of Mexico."
    },
    {
        speaker: "NARRATOR",
        text: "And that is how the Mexican Revolution became one of the most important events in Mexican history."
    }
];

const roles = [
    "NARRATOR",
    "MADERO",
    "PORFIRIO DÍAZ",
    "ZAPATA",
    "VILLA",
    "HUERTA",
    "CARRANZA",
    "PEASANT"
];

const femaleNames = [
    "samantha", "victoria", "zira", "jenny", "aria",
    "sara", "hazel", "libby", "susan", "karen",
    "eva", "female", "woman", "ava", "natasha"
];

const maleNames = [
    "david", "mark", "guy", "james", "ryan",
    "christopher", "eric", "george", "male",
    "man", "daniel", "alex", "thomas", "fred",
    "aaron", "brian"
];

let availableVoices = [];
let voiceAssignments = {};
let currentIndex = 0;
let playbackToken = 0;
let isPlaying = false;

const normalRate = 1.0;

function voiceGenderScore(voice, gender) {
    const name = (voice.name + " " + voice.voiceURI).toLowerCase();
    const terms = gender === "female" ? femaleNames : maleNames;

    let score = 0;

    terms.forEach(term => {
        if (name.includes(term)) score += 3;
    });

    return score;
}

function getEnglishVoices() {
    return availableVoices.filter(voice =>
        voice.lang && voice.lang.toLowerCase().startsWith("en")
    );
}

function chooseVoice(gender, usedVoices) {
    const englishVoices = getEnglishVoices();

    if (!englishVoices.length) return null;

    const candidates = englishVoices
        .map(voice => ({
            voice,
            score: voiceGenderScore(voice, gender)
        }))
        .sort((a, b) => b.score - a.score);

    const unused = candidates.find(item =>
        !usedVoices.has(item.voice.name)
    );

    if (unused) {
        usedVoices.add(unused.voice.name);
        return unused.voice;
    }

    return candidates[0].voice;
}

function loadVoices() {
    availableVoices = speechSynthesis.getVoices();

    const englishVoices = getEnglishVoices();

    const status = document.getElementById("voiceStatus");

    if (!englishVoices.length) {
        status.textContent =
            "No English voices were found. Your browser may need English voices installed.";
        return;
    }

    const previousAssignments = { ...voiceAssignments };
    const usedVoices = new Set();

    roles.forEach(role => {
        const gender = role === "NARRATOR" ? "female" : "male";
        const previousName = previousAssignments[role];

        let selected = englishVoices.find(voice =>
            voice.name === previousName
        );

        if (!selected) {
            selected = chooseVoice(gender, usedVoices);
        }

        if (!selected) selected = englishVoices[0];

        voiceAssignments[role] = selected.name;
        usedVoices.add(selected.name);
    });

    status.textContent =
        "English voices loaded. Female narrator and male character voices selected when available.";

    renderVoiceSettings();
}

function renderVoiceSettings() {
    const settings = document.getElementById("voiceSettings");
    const englishVoices = getEnglishVoices();

    settings.innerHTML = "";

    roles.forEach(role => {
        const label = document.createElement("label");
        const gender = role === "NARRATOR" ? "Female voice" : "Male voice";

        label.textContent = role + " — " + gender;

        const select = document.createElement("select");

        englishVoices.forEach(voice => {
            const option = document.createElement("option");
            option.value = voice.name;
            option.textContent = voice.name + " (" + voice.lang + ")";
            select.appendChild(option);
        });

        select.value = voiceAssignments[role];

        select.addEventListener("change", () => {
            voiceAssignments[role] = select.value;
        });

        label.appendChild(select);
        settings.appendChild(label);
    });
}

function formatText(text) {
    const connectors = [
        "HOWEVER", "THEREFORE", "BECAUSE",
        "ALTHOUGH", "WHILE", "AND", "BUT", "SO"
    ];

    let formatted = text;

    connectors.forEach(word => {
        const regex = new RegExp("\\b" + word + "\\b", "gi");
        formatted = formatted.replace(regex, match =>
            "<strong>" + match.toUpperCase() + "</strong>"
        );
    });

    const timeWords = [
        "ON", "IN", "AT", "DURING", "AFTER", "BEFORE"
    ];

    timeWords.forEach(word => {
        const regex = new RegExp(
            "\\b(" + word + ")\\b(?=\\s+(?:the\\s+)?(?:[A-Z][a-z]+|\\d{1,2}|the beginning))",
            "gi"
        );

        formatted = formatted.replace(regex, "<u>$1</u>");
    });

    return formatted;
}

function renderLine() {
    const item = story[currentIndex];

    document.getElementById("speaker").textContent = item.speaker;
    document.getElementById("dialogueText").innerHTML =
        formatText(item.text);

    const character = document.getElementById("character");
    const hat = document.getElementById("hat");

    const positions = {
        "NARRATOR": "50%",
        "MADERO": "42%",
        "PORFIRIO DÍAZ": "60%",
        "ZAPATA": "43%",
        "VILLA": "58%",
        "HUERTA": "45%",
        "CARRANZA": "58%",
        "PEASANT": "38%"
    };

    character.style.left = positions[item.speaker] || "50%";
    hat.style.display = item.speaker === "NARRATOR" ? "none" : "block";

    document.getElementById("previousButton").disabled =
        currentIndex === 0;

    document.getElementById("nextButton").disabled =
        currentIndex === story.length - 1;
}

function createUtterance(item) {
    const utterance = new SpeechSynthesisUtterance(item.text);

    const voiceName = voiceAssignments[item.speaker];
    const voice = availableVoices.find(v => v.name === voiceName);

    if (voice) {
        utterance.voice = voice;
        utterance.lang = voice.lang;
    } else {
        utterance.lang = "en-US";
    }

    // Normal speaking speed: no acceleration.
    utterance.rate = normalRate;
    utterance.pitch = item.speaker === "NARRATOR" ? 1.08 : 0.95;

    return utterance;
}

function speakCurrentLine() {
    stopStory();

    const item = story[currentIndex];
    const utterance = createUtterance(item);
    const character = document.getElementById("character");

    utterance.onstart = () => character.classList.add("speaking");
    utterance.onend = () => character.classList.remove("speaking");
    utterance.onerror = () => character.classList.remove("speaking");

    speechSynthesis.speak(utterance);
}

function nextLine() {
    stopStory();

    if (currentIndex < story.length - 1) {
        currentIndex++;
        renderLine();
    }
}

function previousLine() {
    stopStory();

    if (currentIndex > 0) {
        currentIndex--;
        renderLine();
    }
}

function stopStory() {
    playbackToken++;
    isPlaying = false;
    speechSynthesis.cancel();
    document.getElementById("character").classList.remove("speaking");
}

function playStory() {
    stopStory();

    isPlaying = true;
    const token = playbackToken;

    playFromCurrent(token);
}

function playFromCurrent(token) {
    if (token !== playbackToken || !isPlaying) return;

    if (currentIndex >= story.length) {
        isPlaying = false;
        currentIndex = story.length - 1;
        renderLine();
        return;
    }

    renderLine();

    const item = story[currentIndex];
    const utterance = createUtterance(item);
    const character = document.getElementById("character");

    utterance.onstart = () => {
        if (token === playbackToken) {
            character.classList.add("speaking");
        }
    };

    utterance.onend = () => {
        if (token !== playbackToken || !isPlaying) return;

        character.classList.remove("speaking");

        currentIndex++;

        // Start the next speaker immediately after the previous line ends.
        playFromCurrent(token);
    };

    utterance.onerror = () => {
        if (token === playbackToken) {
            character.classList.remove("speaking");
            isPlaying = false;
        }
    };

    speechSynthesis.speak(utterance);
}

function renderTranscript() {
    const transcript = document.getElementById("fullTranscript");

    transcript.innerHTML = story.map(item =>
        "<p><strong>" + item.speaker + ":</strong> " +
        formatText(item.text) + "</p>"
    ).join("");
}

speechSynthesis.onvoiceschanged = loadVoices;

loadVoices();
renderLine();
renderTranscript();
</script>

</body>
</html>
