---
toc: false
layout: none
title: Presentation Night Spelling Bee
description: A page for the spelling bee section of my presentation.
type: hacks
permalink: /spelling_bee
---

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PRESENTATION SPELLING BEE</title>
    <style>
        body {
            background-color: #ffeb3b;
            color: black;
            font-family: 'Comic Sans MS', cursive, sans-serif;
            text-align: center;
        }
        h1 {
            background-color: black;
            color: yellow;
            padding: 20px;
            margin: 0;
            font-size: 2.5em;
        }
        .instructions {
            background: white;
            border: 5px dashed black;
            padding: 15px;
            margin: 20px auto;
            width: 60%;
            font-size: 1.2em;
            box-shadow: 5px 5px 0 black;
        }
        .sections-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        .section {
            background: white;
            border: 5px solid black;
            padding: 20px;
            width: 200px;
            text-align: center;
            box-shadow: 5px 5px 0 black;
        }
        .word-content-container {
            align-items: center;
            text-align: center;
            display: none; /* otherwise inline-block */
        }
        .spelling-word {
            color: #d46a00;
            font-family: "Times New Roman", serif;
            font-size: 1.5em;
        }
        .hint-sentence {
            color: black;
            font-family: "Times New Roman", serif;
            font-size: 1.3em;
            display: none; /* otherwise inline-block */
        }
        button {
            background-color: black;
            color: yellow;
            font-size: 1.2em;
            font-family: 'Comic Sans MS', cursive, sans-serif;
            border: none;
            padding: 10px 20px;
            cursor: pointer;
            margin-top: 10px;
            border-radius: 10px;
            box-shadow: 3px 3px 0 yellow;
            transition: background-color 0.3s ease, color 0.3s ease, box-shadow 0.3s ease;
        }
        button:hover {
            background-color: yellow;
            color: black;
            box-shadow: 3px 3px 0 black;
        }
    </style>
</head>
<body>
    <h1>🐝 I CAN SPELL REALY WELL ACTUALLY 🐝</h1>
    <div class="instructions">
        <div id="instructions-container">
            <u>HOW THIS WORKS</u>:
            <ol style="text-align: left;">
                <li>I cover my eyes and face away from the screen</li>
                <li>One of you clicks the generate button and reads out the word that was generated from the bank of words</li>
                <li>If I need help, I can ask for the word to be used in a sentance by pressing an additional button</li>
                <li>I spell the word out loud (AND GET IT RIGHT MUAHAHAHASGSASG)</li>
                <li>Repeat until I spell <b>3 words</b> from every difficulty</li>
            </ol>
            <br>
            For each word taht I spell wrong, <em>I will not play League for one day</em>. So if I spell 7 words wrong, <em>I cannot play for a week</em>.
        </div>
        <button id="instructions-toggler" onclick="toggleInstructions()">Hide Instructions</button>
    </div>
    <div class="sections-container">
        <div class="section">
            <h2>Easy</h2>
            <div id="easy-word-content-container" class="word-content-container">
                <div id="easy-spelling-word" class="spelling-word"></div>
                <button id="easy-generate-sentence-button">Gimme Sentence</button>
                <div id="easy-hint-sentence" class="hint-sentence"></div>
            </div>
            <button id="easy-word-button">Gimme Word</button>
        </div>
        <div class="section">
            <h2>Medium</h2>
            <div id="medium-word-content-container" class="word-content-container">
                <div id="medium-spelling-word" class="spelling-word"></div>
                <button id="medium-generate-sentence-button">Give Me Sentence</button>
                <div id="medium-hint-sentence" class="hint-sentence"></div>
            </div>
            <button id="medium-word-button">Give Me Word</button>
        </div>
        <div class="section">
            <h2>Hard</h2>
            <div id="hard-word-content-container" class="word-content-container">
                <div id="hard-spelling-word" class="spelling-word"></div>
                <button id="hard-generate-sentence-button">Sentence Please</button>
                <div id="hard-hint-sentence" class="hint-sentence"></div>
            </div>
            <button id="hard-word-button">Word Please</button>
        </div>
    </div>
</body>

<script>
    // initializing word data
    let WORD_DATA;

    // getting the word data
    fetch("{{site.baseurl}}/assets/json/word_data.json")
    .then(response => response.json()) // converting the response to JSON
    .then(data => {
        console.log(data);
        WORD_DATA = data;
    })


    // page globals for tracking states
    let instructionsShown = true

    // function to toggle the instructions
    function toggleInstructions() {
        if (instructionsShown) {
            document.getElementById("instructions-container").style.display = 'none';
            document.getElementById("instructions-toggler").innerHTML = "Show Instructions";
            instructionsShown = false;
        } else {
            document.getElementById("instructions-container").style.display = 'block';
            document.getElementById("instructions-toggler").innerHTML = "Hide Instructions";
            instructionsShown = true;
        }
    }
</script>