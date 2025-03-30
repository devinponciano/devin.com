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
    <title>Bee-ware: The Spelling Challenge</title>
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
            border: none;
            padding: 10px 20px;
            cursor: pointer;
            margin-top: 10px;
            border-radius: 10px;
            box-shadow: 3px 3px 0 yellow;
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
        <p>Welcome to the ultimate spelling challenge! Click a button below to generate a word at your chosen difficulty. Think you can spell it? Think again! 🐝</p>
    </div>
    <div class="sections-container">
        <div class="section">
            <h2>Easy</h2>
            <button>Generate Word</button>
        </div>
        <div class="section">
            <h2>Medium</h2>
            <button>Generate Word</button>
        </div>
        <div class="section">
            <h2>Hard</h2>
            <button>Generate Word</button>
        </div>
        <div class="section">
            <h2>Impossible</h2>
            <button>Generate Word</button>
        </div>
    </div>
</body>