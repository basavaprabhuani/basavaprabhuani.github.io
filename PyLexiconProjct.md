---
layout: page
title: PyLexicon
permalink: /projects/pylexicon
---
<p>This is a Python Program, which takes in a list/series of words as inputs, then processes the words/runs the program to fetch the Definition, Part of Speech, & Example sentence (if any) for the word. This then gathers these pieces of information for all the entered words, finally compiling all of them into an excel sheet.</p>
<p>Here is a video showing the working of this program:</p>
<figure>
    <video controls>
        <source src="/media/PyLexicon_Demo.mp4" type="video/mp4">
        Error with browser: Does not support video.
    </video>
    <figcaption>Video (at 3x) showing the working of PyLexicon </figcaption>
</figure>
<p>Watch on YouTube <a href="https://www.youtube.com/watch?v=1SiDIR2XgSQ" class="content-link">here</a></p>

<p>As seen in the video, the basic function of this program is to <br>1. take in a list of words, <br>2. Take each of those words and fetch information about those words from Merriam Webster, then finally, <br>3. Organize the info for all those words, and export that into an excel file.</p>
<br><hr><br><h3>GitHub Repo</h3>
<p>View the GitHub repository for the program on  <a href="https://github.com/basavaprabhuani/PyLexicon" class="content-link">here</a></p>
<br>
<figure>
    <img src="/media/PyLexicon_GitHub.png">
    <figcaption>Image of GitHub Repo</figcaption>
</figure>
<p>The entire code, along with detailed steps and explanations of its functions, has been provided to ensure comprehensive coverage.</p>
<br><hr><br><h3>Why I built It</h3>
<p>I wrote this program to automate one of my academic tasks-listing down difficult words from prose/poetry in English Literature. Though there weren't many words for each chapter, it was pretty tedious to manually search up this info for alll the words and copy them down into excel. <br>This project was not entirely my idea: I started doing this (manually) when I was of around 11 years old, and at the same time, my brother, too had been learning VBA. Given the angelic soul of his, he wrote a program using VBA to automate this task. <p>Then why did I write all over again? Well, the website from which my brother's code was fetching the info from, had kinda shut down. Therefore, there were only two options - Either copy all that down manually, or, automate it. And you know which option I chose 😉.</p> <p>I had already learnt Python by the time this happened, so I could write this program to do the same job which my brother's code did. 
Nevertheless, I wrote this Python code all by myself, only referring google for syntax of the modules.</p>
<br><hr><br><h3>How I built It</h3>
<p>I wrote the code for this using the Python Libraries: <br><span class="reference-text">BeautifulSoup<br></span><span class="reference-text">openpyxl</span><br><span class="reference-text">os</span><br><span class="reference-text">requests</span></p>

The first part after taking the inputs of all words, was to identify the parts of HTML for a word in the MW Website. I had to identify the sections of HTML which provided the definitions, examples, part of speech, etc. After extracting this, I made use of bs4 to fetch the relevant info for a word. Finally, I used <span class="reference-text">openpyxl</span> to export all this data into a excel sheet. I initially thought of using <span class="reference-text">pandas</span> for this, but then it has a limitation - It cannot add sheets to the same excel file; it can create only new excel files. This meant each time I added words, it would create a new excel file, which wouldn't be so user-friendly. The formatting of the excel file had been customized using the features of <span class="reference-text">openpyxl</span>.

<br><hr><br><h3>What I learned</h3>
<p>Throughout the building of this project, I learned:</p>
<ul>
    <li>How to use <span class="reference-text">openpyxl</span> effectively, customizing attributes of the excel file</li>
    <li>How to quickly recognize sections of HTML code, using tools like <a href="https://codebeautify.org/htmlviewer" class="content-link">Code Beautify</a>, and in-built functions of <span class="reference-text">BeautifulSoup</span>.</li>
</ul>
<br><hr><br><h3>Review & Reflect</h3>
<p>This project turned out to be more than just code on a screen. It gave me the chance to practice combining multiple Python libraries, debugging messy parts of HTML, and formatting data into something polished and usable. As I move forward, I see this as one of the first stepping stones that will help me take on larger and more complex projects with confidence.</p><p> It showed me how even a simple idea can grow into a tool that actually saves time and effort.  It also taught me that the “hardest” part is often just figuring out how to start, after which things slowly fall into place. Beyond just technical lessons, it reminded me that every project — no matter how small — adds up to a bigger journey of growth. With this experience, I’m excited to push further into automation and data-driven projects, exploring ways to make my tools smarter and more versatile.  </p><p>I’m looking forward to building on this foundation as I take on new challenges in STEM and programming.</p>
<br><hr>

