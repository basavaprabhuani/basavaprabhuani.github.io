---
layout: page
title: Proximity Sensor (Arduino)
permalink: /projects/proximity_sensor
---
<p>The proximity sensor, built with Arduino... senses proximity? 🫣 Hehe, well yeah, it is a distance-measuring module. Along with distance-measurement, I also added the feature of an LED blinking and a buzzer beeping if the distance gets too close. That way, I also used many components and addition of these two features was a real upgrade to my coding skills, as I shall share it in the below section.</p>
<p>Watch the working demo of the Proximity Sensor below:</p>
<figure>
    <video controls>
        <source src="/media/proximity_sensor_demo.mp4" type="video/mp4">
        Error with browser: Does not support video.
    </video>
    <figcaption>Video showing the demo of Proximity Sensor </figcaption>
</figure>
<p>Watch on YouTube <a href="https://www.youtube.com/watch?v=eT85A3h6H-w" class="content-link">here</a></p>

<br><hr><br><h3>GitHub Repo</h3>
<p>View the GitHub repository for the program <a href="https://github.com/basavaprabhuani/Proximity-Sensor-Arduino-" class="content-link">here</a></p>
<br>
<figure>
    <img src="/media/Proximity Sensor GitHub.png">
    <figcaption>Image of GitHub Repo</figcaption>
</figure>
<p>The entire code for the project can be accessed in the GitHub Repo above.</p>

<br><hr><br><h3>How I built It</h3>
<p>The code was written, entirely in C++ of Arduino (with its own functions, and stuff for the components).</p>
<ul>
<li>The first part (version) was the simplest one. All I had to do was calculate the distance, and display it in the LCD. <br>The ultrasonic sensor sends out pulses, and measures the time it took for it to receive it back after echoing. Using this time, I could calculate the distance The formula is $$
\text{Distance} = \frac{\text{Time} \times \text{Speed of Sound}}{2}
$$ </li>
</ul>

