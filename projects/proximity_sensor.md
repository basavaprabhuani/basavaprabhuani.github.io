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
<li>The first part (version) was the simplest one. All I had to do was calculate the distance, and display it in the LCD. <br>The ultrasonic sensor sends out pulses, and measures the time it took for it to receive it back after echoing. Using this time, I could calculate the distance using the speed-distance formula. <br>The formula for speed is: <br>$$\text{Speed}=\frac{\text{Distance}}{\text{Time}}$$
So, $$\text{Distance}=\text{Speed}\times \text{Time} $$
Since the pulse has to travel <b>twice</b> the distance (first traveling once, then twice to come back after echo), 
$$\text{Distance}\times 2=\text{Speed}\times \text{Time}$$
$$\text{Distance}=\frac{\text{Speed}\times \text{Time}}{2} $$
And voila! That's the equation I used to calculate the distance. 

I used the speed of sound to be $343ms^{-1}$, and the time it took was obtained using the ultrasonic sensor's reading, given by this part of the code: 
{% highlight arduino %}
void loop() {
  // Ultrasonic trigger
  digitalWrite(TRIG, LOW);
  delayMicroseconds(2);
  digitalWrite(TRIG, HIGH);
  delayMicroseconds(10);
  digitalWrite(TRIG, LOW);

  float time_twice = pulseIn(ECHO, HIGH, 100000);
{% endhighlight %}

The distance is then calculated using:
{% highlight arduino %}
float distance = time_twice * 0.0343 / 2;
{% endhighlight %}

This reading is printed on the LCD using this code: 
{% highlight arduino %}
// LCD DISPLAY

  // Row 0 → Distance
  display.setCursor(0, 0);
  display.print("Dist.: ");
  display.print(distance);
  display.print("   "); // clear leftover digits
{% endhighlight %}

</li>

</ul>

