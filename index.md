---
title: /
layout: default
permalink: /
---
<style>
.center {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 100%;
}
    .glitch-char {
    display: inline-block;
    position: relative;
    font-family: monospace;
    font-weight: bold;
    color: white;
    background-color: black;
  }

  .glitch-char.glitching::before,
  .glitch-char.glitching::after {
    content: attr(data-char);
    position: absolute;
    left: 0;
    color: red;
    clip: rect(0, 0, 0, 0);
  }

  .glitch-char.glitching::before {
    animation: glitchTop 0.3s linear infinite;
    color: #0ff;
  }

  .glitch-char.glitching::after {
    animation: glitchBottom 0.3s linear infinite;
    color: #f0f;
  }

  @keyframes glitchTop {
    0% { clip: rect(0, 9999px, 0, 0); transform: translate(-2px, -2px); }
    50% { clip: rect(0, 9999px, 100%, 0); transform: translate(2px, -1px); }
    100% { clip: rect(0, 9999px, 0, 0); transform: translate(-1px, 2px); }
  }

  @keyframes glitchBottom {
    0% { clip: rect(100%, 9999px, 0, 0); transform: translate(2px, 2px); }
    50% { clip: rect(0, 9999px, 100%, 0); transform: translate(-2px, 1px); }
    100% { clip: rect(100%, 9999px, 0, 0); transform: translate(1px, -2px); }
  }
</style>

<script>
    document.write('<div style="text-align:center"><div><span style="color: #ff0000"> </span></div><div></div><div><span style="color: #f80000"> </span><span style="color: #f10101"> </span><span style="color: #eb0101"> </span><span style="color: #e40202">█</span><span style="color: #dd0202">█</span><span style="color: #d60202">╗</span><span style="color: #cf0303">█</span><span style="color: #c80303">█</span><span style="color: #c20404">█</span><span style="color: #bb0404">█</span><span style="color: #b40404">█</span><span style="color: #ad0505">█</span><span style="color: #a60505">█</span><span style="color: #9f0606">╗</span></div><div><span style="color: #990606"> </span><span style="color: #920606"> </span><span style="color: #8b0707">█</span><span style="color: #840707">█</span><span style="color: #7d0707">█</span><span style="color: #770808">║</span><span style="color: #700808">╚</span><span style="color: #690909">═</span><span style="color: #620909">═</span><span style="color: #5b0909">═</span><span style="color: #540a0a">═</span><span style="color: #4e0a0a">█</span><span style="color: #470b0b">█</span><span style="color: #400b0b">║</span></div><div><span style="color: #470b0b"> </span><span style="color: #4d0a0a"> </span><span style="color: #84848484">1:<span class="changing-char">A</span>:3:4:5:6:7:8:9:10:<span class="changing-char">A</span><span class="glitch-char">A</span>:12:13:14:15:16:  </span><span style="color: #540a0a">╚</span><span style="color: #5a0909">█</span><span style="color: #610909">█</span><span style="color: #680909">║</span><span style="color: #6e0808"> </span><span style="color: #750808"> </span><span style="color: #7b0808"> </span><span style="color: #820707"> </span><span style="color: #880707">█</span><span style="color: #8f0606">█</span><span style="color: #960606">╔</span><span style="color: #9c0606">╝</span><span style="color: #84848484">  :18:19:<span class="glitch-char">A</span><span class="glitch-char">A</span>:21:22:23:2X:25:26:XX:28:<span class="changing-char">AA</span>:30</span></div><div><span style="color: #a30505"> </span><span style="color: #a90505"> </span><span style="color: #b00505"> </span><span style="color: #b70404">█</span><span style="color: #bd0404">█</span><span style="color: #c40303">║</span><span style="color: #ca0303"> </span><span style="color: #d10303"> </span><span style="color: #d70202"> </span><span style="color: #de0202">█</span><span style="color: #e50202">█</span><span style="color: #eb0101">╔</span><span style="color: #f20101">╝</span><span style="color: #f80000"> </span></div><div><span style="color: #ff0000"> </span><span style="color: #fb0101"> </span><span style="color: #f70202"> </span><span style="color: #f20303">█</span><span style="color: #ee0404">█</span><span style="color: #ea0505">║</span><span style="color: #e60606"> </span><span style="color: #e10707"> </span><span style="color: #dd0808"> </span><span style="color: #d90909">█</span><span style="color: #d50a0a">█</span><span style="color: #d10b0b">║</span><span style="color: #cc0c0c"> </span><span style="color: #c80d0d"> </span></div><div><span style="color: #c40e0e"> </span><span style="color: #c00f0f"> </span><span style="color: #bc1010"> </span><span style="color: #b71111">╚</span><span style="color: #b31212">═</span><span style="color: #af1313">╝</span><span style="color: #ab1414"> </span><span style="color: #a61515"> </span><span style="color: #a21616"> </span><span style="color: #9e1717">╚</span><span style="color: #9a1818">═</span><span style="color: #961919">╝</span><span style="color: #911a1a"> </span><span style="color: #8d1b1b"> </span></div><div></div><div></div><div></div><div></div><div></div><div></div></div>')           
</script>

<script>
  //<span class="changing-char">A</span> 
  const chars = 'RSTUVWXYZghijklz0123456789!@#$%^&*-_<>.,/`~[]{};:"';

  function getRandomChar() {
    const randomIndex = Math.floor(Math.random() * chars.length);
    return chars[randomIndex];
  }

  function getRandomInterval(min = 10, max = 500) {
    return Math.floor(Math.random() * (max - min + 1)) + min;
  }

  function getRandomColor() {
    const choice = Math.random();

    if (choice < 0.33) {
      const red = 200 + Math.floor(Math.random() * 56);
      const green = Math.floor(Math.random() * 30);
      const blue = Math.floor(Math.random() * 30);
      return `rgb(${red},${green},${blue})`;
    } else if (choice < 0.66) {
      const grey = 100 + Math.floor(Math.random() * 100);
      return `rgb(${grey},${grey},${grey})`;
    } else {
      const white = 220 + Math.floor(Math.random() * 36);
      return `rgb(${white},${white},${white})`;
    }
  }

  function changeCharRandomly(span) {
    if (!span) return;

    span.textContent = getRandomChar();
    span.style.color = getRandomColor();

    const nextInterval = getRandomInterval();
    setTimeout(() => changeCharRandomly(span), nextInterval);
  }

  // Initialize for all spans with the class 'changing-char'
  document.addEventListener("DOMContentLoaded", () => {
    const spans = document.querySelectorAll('.changing-char');
    spans.forEach(span => changeCharRandomly(span));
  });
</script>

<script>
  //<span class="glitch-char">A</span>
  document.addEventListener("DOMContentLoaded", function () {
    const glitchChars = document.querySelectorAll('.glitch-char');

    glitchChars.forEach(span => {
      const char = span.textContent.trim();
      span.setAttribute('data-char', char);

      function toggleGlitch() {
        span.classList.add('glitching');
        setTimeout(() => {
          span.classList.remove('glitching');
        }, 300); // duration of the glitch
      }

      // Glitch every 1–3 seconds randomly
      function loop() {
        toggleGlitch();
        setTimeout(loop, 1000 + Math.random() * 2000);
      }

      loop();
    });
  });
</script>

