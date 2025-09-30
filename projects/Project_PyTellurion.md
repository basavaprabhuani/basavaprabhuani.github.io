---
layout: page
title: PyTellurion
permalink: /projects/pytellurion
---
<p>PyTellurion is a project I built, which is a digital simulation of an actual <i>tellurion</i>. What is a tellurion? Well, A tellurion is a mechanical or digital model that demonstrates the relationship between the Earth, Moon, and Sun. A physical/actual tellurion is in fact more advanced than my simulation, in the sense that it can show the phases of the moon, day & night, changing seasons and eclipses. </p><p>Let's not allow a tellurion to steal the show; coming back to my project, this shows the orbit of the moon, traced, as it revolves around the sun while revolving around the Earth. (A note: The celestial bodies here are definitely not to scale, they are just to visualize the motion of the Earth and Moon)</p>
<p>Here's a video showing the simulation: </p>
<figure>
    <video controls>
        <source src="/media/PyTellurion.mp4" type="video/mp4">
        Error with browser: Does not support video.
    </video>
    <figcaption>Video showing the simulation of PyTellurion </figcaption>
</figure>
<p>Watch on YouTube <a href="https://youtu.be/L3vc5SPEmqg" class="content-link">here</a></p>

<br><hr><br><h3>GitHub Repo</h3>
<p>View the GitHub repository for the program <a href="https://github.com/basavaprabhuani/PyTellurion" class="content-link">here</a></p>
<br>
<figure>
    <img src="/media/PyTellurion_GitHub.png">
    <figcaption>Image of GitHub Repo</figcaption>
</figure>
<p>The entire code, along with detailed steps and explanations of its functions, has been provided to ensure comprehensive coverage. </p>

<br><hr><br><h3>Why I built It</h3>
<p>The idea to build such a project struck me on the day of the Blood Moon (lunar eclipse in India, around September 7, 2025. I could have said 'during the lunar eclipse' but 'The day of the Blood Moon' sounds more histrionic and cool, 😁). At the same time, I too was thinking of building a new project, which was nowhere similar to what I had done earlier. There wasn't a particular goal of WHY I built it - It just seemed fun.</p>
<p>What made me build <i>this</i> project was the fact that this wasn't just 'going around the circle' animation or something (which, too, was completely new for me). Sure, the part of making the Earth go around the Sun is simple and all, but I actually had to make use of those brain cells in my head (obviously) to get the moon to go around the Earth, that too, while it orbits around the sun.</p>
<p>And ooh, I gotta tell you, this wasn't just some fancy copy-the-code stuff-It involved actual mathematics (i.e., coordinate geometry), and that's what makes me feel proud about this. This was actually the first program that I built, of this kind. One would have to be clear with the equations of ellipses, circles and angles, in order to make this (you don't need to be Elon Musk or Einstein, don't worry).</p>

<br><hr><br><h3>How I built It</h3>
<p>I wrote the code for this using the Python Libraries <span class="reference-text">MatPlotLib</span> and <span class="reference-text">numpy</span>
<p>Firstly, I had to set up the location of the Sun, which I did by plotting a large circle (almost the same as plotting a point) at the centre of THE ANIMATION, using <span class="reference-text">MatPlotLib</span>. 
<br>&nbsp;&nbsp;&nbsp;Following this, I added the orbit Earth had to follow, by plotting an ellipse around the sun (using the equation of an ellipse, through <span class='reference-text'>numpy</span>). 
<br>&nbsp;&nbsp;&nbsp;The next step was to code the Earth to go around the Sun, which I did using the <i>animations</i> feature of <span class="reference-text">MatPlotLib</span>, by making the Earth follow the laid out orbit in the previous steps, by simply updating the Point (the representation of Earth) to the next coordinate, by the frames. 
<br>&nbsp;&nbsp;&nbsp;The trickiest part was making the moon go around the Earth; animations was used here as well, and the central idea to make this work, was to make the moon to keep on going in circles, but use the Earth's coordinates as the centre, to ensure that the moon revolves around the Earth, rather than it going in circles randomly. The ever-moving property of the Earth made this tricky (I had to write down some stuff on paper to get this right!). </p>

<p>The comprehensive source code for the program has been made public in my GitHub Repository, which you can go to, using the above link ☝️. Meticulous instructions and details of each line of code have been given in the source code itself.</p>

<br><hr><br><h3>What I learned</h3>
<p>Throughout the building of this project, I learned:</p>
<ul>
    <li>Thoroughly drawing graphs using <span class="reference-text">MatPlotLib</span> (this is not visible in the video, but graphs or at least a part of them is necessary to do this)</li>
    <li>Some geometric/mathematical features of <span class="reference-text">numpy</span></li>
    <li>Making animations using <span class="reference-text">MatPlotLib</span></li>
    <li>Efficiently using documentations of modules - Not skipping to <i>only</i> necessary parts, but <i>understanding</i> the basic boilerplate code, and integrating the necessary part into the project. This way, it helps me truly have a sense of what I am doing, rather than being in obscurity by just copying code.</li> 
    <li>Not exactly a learning, but I had fun integrating Maths with Coding (like when I animated the Earth using the coordinates (Math) of some frame (Coding) to make it go around the sun)</li>
</ul>

<p>I did learn several other non-coding and non-mathematical stuff throughout the building, but now I realize I should've taken notes as I learnt something 😭.</p>

<br><hr><br><h3>Review & Reflect</h3>
<p>An exciting thing about building this project was that the final product made my laptop’s fans blow fast — meaning the code was actually process-heavy and required capable laptops, which means I created something truly worthy of a computer’s power! I don't know if this is actually something to be happy about, but was exhilarating to me this time, for sure, haha.<p>
<p>Working on PyTellurion turned out to be more challenging than it might look at first glance. On the surface, it’s just the Sun, Earth, and Moon moving around—but making the Moon orbit the Earth while the Earth orbits the Sun required careful use of math, coordinate transformations, and timing. It wasn’t only about writing code; it was about thinking through how to model orbital motion in a way that feels natural and accurate. I also realized how much of the “intelligence” in a project like this comes from balancing simplicity and detail—for example, deciding how fast the Moon should move compared to the Earth, or how to represent the Sun’s glow visually. </p><p>In the end, PyTellurion became more than a coding exercise—it’s a reminder of how math, physics, and programming can come together to build something both educational and beautiful.</p>
<p><b>I want to end this snapshot of the project by saying that if NASA or ISRO ever needs a backup simulator, they know where to find me (hint: in my den, with snacks). 🚀🍕</p></b>
<br><hr>