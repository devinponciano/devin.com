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
                <li>One of you clicks the generate button and reads out the word</li>
                <li>I spell the word out loud (AND GET IT RIGHT MUAHAHAHASGSASG)</li>
                <li>Repeat until I spell a word from every category</li>
            </ol>
            <br>
            For each word taht I spell wrong, <em>I will not play League for one day</em>. So if I spell 7 words wrong, <em>I cannot play for a week</em>.
        </div>
        <button id="instructions-toggler" onclick="toggleInstructions()">Hide Instructions</button>
    </div>
    <div class="sections-container">
        <div class="section">
            <h2>Easy</h2>
            <button>Gimme Word</button>
        </div>
        <div class="section">
            <h2>Medium</h2>
            <button>Gimme a Word</button>
        </div>
        <div class="section">
            <h2>Hard</h2>
            <button>Give Me Word</button>
        </div>
        <div class="section">
            <h2>Impossible</h2>
            <button>Word Please</button>
        </div>
    </div>
</body>

<script>
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