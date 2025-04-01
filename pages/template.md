---
layout: default
title: "Комната 234"
description: "Тихое пространство, где время останавливается. Сумеречный свет мягко касается мебели, создавая игру теней на стенах. В этой комнате каждый предмет хранит свою историю, а стены, наполненные молчанием, становятся свидетелями невидимых мыслей и воспоминаний."
image: "/favicons/favicon-96x96.png"
author: "Сюзанна Роттенберг"
year: "2004"
material: "Масло на холсте"
origin: "Частная коллекция"
audio_file: "/sounds/sound.mp3"
work_image: "/images/work.jpg"
gif_1: "/images/at-work-1.gif"
gif_2: "/images/at-work-2.gif"
gif_3: "/images/at-work-3.gif"
caption_1: "Сюзанна работает над 'Комнатой 234'"
caption_2: "Рабочий момент над деталями 'Комнаты 234'"
caption_3: "Крупные мазки маслом"
permalink: template
---

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>{{ page.title }}</title>
    <link rel="stylesheet" href="{{ '/assets/main.css' | relative_url }}">
</head>

<div class="technical-info">
    <h3>{{ page.title }}</h3>
    <p><strong>Автор:</strong> {{ page.author }}</p>
    <p><strong>Год:</strong> {{ page.year }}</p>
    <p><strong>Материал:</strong> {{ page.material }}</p>
    <p><strong>Происхождение:</strong> {{ page.origin }}</p>
</div>

<div class="gif-large">
    <img src="{{ page.gif_1 }}" alt="Гиф 1">
    <div class="caption">{{ page.caption_1 }}</div>
</div>

<div class="gif-stack">
    <div>
        <img src="{{ page.gif_2 }}" alt="Гиф 2">
        <div class="caption">{{ page.caption_2 }}</div>
    </div>
    <div>
        <img src="{{ page.gif_3 }}" alt="Гиф 3">
        <div class="caption">{{ page.caption_3 }}</div>
    </div>
</div>

<button class="player-button" onclick="toggleAudio()"></button>
<audio id="audio" src="{{ page.audio_file }}"></audio>

<script>
    function toggleAudio() {
        var audio = document.getElementById('audio');
        if (audio.paused) {
            audio.play();
        } else {
            audio.pause();
            audio.currentTime = 0;
        }
    }
</script>
