---
layout: default
title: Teaching
permalink: /teaching/
---

# Teachings

<div class="tabs">
    <button class="tab-button" onclick="openTab(event, '26-27')">2026-2027</button>
    <button class="tab-button active" onclick="openTab(event, '25-26')">2025-2026</button>
    <button class="tab-button" onclick="openTab(event, '24-25')">2024-2025</button>
    <button class="tab-button" onclick="openTab(event, '23-24')">2023-2024</button>
    <button class="tab-button" onclick="openTab(event, '22-23')">2022-2023</button>
    <button class="tab-button" onclick="openTab(event, '21-22')">2021-2022</button>
</div>


<div id="25-26" class="tab-content" style="display:block;">
    <ul>
        <li>C programming</li>
        <li>Algorithmic in Python</li>
        <li>Numerical algorithms</li>
        <li>Graphs</li>
        <li>Game theory</li>
        <li>Operational research</li>
        <li>Systems modeling and optimization</li>
        <li>Mathematical and computational writing (Git, LaTeX)</li>
    </ul>
</div>

<div id="24-25" class="tab-content">
    <ul>
        <li>Mathematical and computational writing (Git, LaTeX)</li>
        <li>C programming</li>
        <li>Databases (SQL, relational algebra)</li>
        <li>Operational research</li>
        <li>Numerical algorithms</li>
        <li>Graphs</li>
    </ul>
</div>

<div id="23-24" class="tab-content">
    <ul>
        <li>C programming</li>
        <li>Numerical algorithms</li>
        <li>Operational research</li>
        <li>Systems modeling and optimization</li>
    </ul>
</div>

<div id="22-23" class="tab-content">
    <ul>
        <li>C programming</li>
        <li>Numerical algorithms</li>
        <li>Operational research</li>
    </ul>
</div>

<div id="21-22" class="tab-content">
    <ul>
        <li>Computing project (Python, Git, LaTeX)</li>
        <li>Object-oriented programming (Java)</li>
        <li>Operational research</li>
    </ul>
</div>


<script>
function openTab(evt, tabName) {
  const contents = document.getElementsByClassName("tab-content");
  for (let c of contents) c.style.display = "none";

  const buttons = document.getElementsByClassName("tab-button");
  for (let b of buttons) b.classList.remove("active");

  document.getElementById(tabName).style.display = "block";
  evt.currentTarget.classList.add("active");
}
</script>