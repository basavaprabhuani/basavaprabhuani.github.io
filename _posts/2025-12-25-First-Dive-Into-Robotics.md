---
layout: post
title: My First Dive Into Robotics
date: 2025-12-29 00:00:00 +0530
categories: Robotics Arduino
---

<p>Yessir, I got my Arduino a month ago, and I am having a lot of fun with it! I still don't have any impressive projects or anything impressive at all, but still, I am having fun integrating coding with hardware (or electronics). </p><p>The first two days felt absolutely brutal — no proper program, being clumsy at everything, and being unable to remember the simplest of syntax. But here I am now, having fun with everything that I'm doing — connecting hardware to breadboards, writing programs to control them, taking inputs using that hardware, and whatnot.</p>
<hr><br>
<p>The real challenge began on the day my desire for learning robotics started — choosing between Raspberry Pi and Arduino. Raspberry Pi was a whole computer; Arduino is just a processor. <br>But after deep research using AI and the internet, I found Arduino most suitable for my stage right now — an introduction to robotics and electronics. Raspberry Pi seemed to be more useful for advanced robotics programmers.</p>
<p>The next challenge, as humorous as it sounds, was choosing which Arduino board to buy — again, many options. So I went through each board, asked AI and YouTube, and found that <b>Arduino UNO R4 Minima</b> was most suitable — both for my introductory phase and my pocket (my brother's pocket, in fact). </p><p>I faced yet another challenge — which starter kit to buy. The official kit is unreal-level expensive, so I had to go for generic kits. And thus began my least-liked chore — searching for stuff. Then I managed to find a starter kit worth the money, with the official R4 Minima board. Luckily, third time’s a charm, so this was the final challenge — until my Arduino arrived.</p>
<hr><br><p>The first day I got my Arduino, I was baffled — where to start, what the proper way to learn it was, and all. I watched many YouTube videos on how to start, and the official documentation of the board is pretty vast too, so you don’t really know where exactly to begin. For the first two days, the progress I achieved was close to nothing, because I read unnecessary (though informative) stuff in the documentation. But then I just couldn't wait to connect things and code them to do whatever and that’s when real, noticeable progress started.</p>
<p>First off, before I could even code ANYTHING on the Arduino at all, I still had more to learn: <span class="reference-text">C++</span>. But thanks to my big brain, I could think of starting to learn <span class="reference-text">C++</span> on the day I ordered the board, so that as soon as I get it delivered, I can start  building "projects" with it. (not to mention the first two days trying to figure out the details and basics). </p>
<p>And learning <span class="reference-text">C++</span> was kinda easy, to be frank. This might have been because of my already strong programming background with <span class="reference-text">Python</span>. Nevertheless, I learnt only basic <span class="reference-text">C++</span>, enough for me to use Arduino - because Arduino uses only the basic outline of <span class="reference-text">C++</span> and the rest is its own documentation (like <span class="reference-text">pinMode</span>, <span class="reference-text">digitalWrite</span>, <span class="reference-text">analogWrite</span>, etc.), which can be accessed here: <a href="https://docs.arduino.cc/language-reference/" class="content-link">Language Reference for Arduino</a><url for the programming documentation> </p>
<hr><br><p>On a lighter note, the more I learnt <span class="reference-text">C++</span>, the more did my abhorrence for it grow as well 😤. </p><p>And here's a short list, stating why: 
<ul>
<li>Having to enter a semi-colon <span class="reference-text">(;)</span> at end of every line. Python doesn't require you to do it. </li>
<li>Having to specify datatype. Python's a smart kid - It knows which datatype a piece of data is. </li>
<li>Having to use <span class="reference-text">std::....</span>for the simplest of commands (I find this so petty that I cannot even describe it.) </li>
<li>Having to use <span class="reference-text">#include <...> </span>for everything - So irritating. </li>
<li>Unnecessary complication for <span class="reference-text">for/while loops </span> and <span class="reference-text"> if/else if statements </span>: using '<span class="reference-text">&&</span>' instead of 'and', using '<span class="reference-text">||</span>' instead of 'or' - Python is more user-friendly ('and', 'or').</li>
</ul>
</p>

<p>These are just a few points which I noticed when I was learning basic <span class="reference-text">C++</span>. It would not be hyperbolic to assume many more complications in more advanced <span class="reference-text">C++</span> (at this point, I think the 'C' in <span class="reference-text">C++</span> stands for 'crappy' 😂). Call me whiny, but Python's way better. </p>
<hr><br><p>
Now back to Arduino; So yes, I was now ready to start learning Arduino (boy, does this sound like a lot of hard work just to begin learning Arduino 💦). <br> I'll be honest, I spent the first two days just connecting LEDs, pretending I'm doing development in cutting-edge tech and writing code to just light it up, and blinking the LEDs. But as time went on, I started going through each part in my kit and the documentation to use the part. As of now (28th Dec 2025), I have learnt using these parts: 
<ul>
<li>LED</li>
<li>Potentiometer</li>
<li>Button</li>
<li>Buzzer (same as using LED) </li>
</ul>
</p>
<p>This seems very little, but I utilised most of my free time learning this and could learn this much. 
</p>
<p>
Here's a tiny clip showing a very tiny I-Don't-Know-What-To-Call-It I built, using LEDs, Button and very basic coding:
<p>Get the context by watching the video: </p><br>
<figure>
    <video controls>
        <source src="/media/Arduino_fun_1.mp4" type="video/mp4">
        Error with browser: Does not support video.
    </video>
    <!-- <figcaption></figcaption> -->
</figure>

</p>
<br>
<p>Code for the I-Don't-Know-What-To-Call-It:
<br>
<pre><code>
int button_reading = 2;
int led_blue = 7;
int led_red = 10;<br>
void setup() {
  pinMode(button_reading, INPUT);
  Serial.begin(9600);
  pinMode(led_blue, OUTPUT);
  pinMode(led_red, OUTPUT);
}<br>
void loop() {
  int reading = digitalRead(button_reading);
  Serial.println(reading);
  if(reading == 1) {
    digitalWrite(led_blue, HIGH);
    digitalWrite(led_red, LOW);
  }
  else if (reading != 1) {
    digitalWrite(led_blue, LOW);
    digitalWrite(led_red, HIGH);
  }<br>
}
</code></pre>
</p>
<hr><br>
<p>
The next goal, after learning to use these parts, was to build a real application, or a project, if I may say so. The idea was to build a reaction game (two players), where each player has to be more reflexive than the other and press the button quicker than the other person in order to win the game. <br>
I could make this after the second attempt, because the first time, I kinda messed up the circuit (hardware part) and the components couldnt function properly, and there might have been silly but important programming mistakes in the software part too. However, after careful speculation and reflection, along with utilising the experience from the first build, I could figure it out -- after working with it for 1.5 Hours. But I guess this is fine, because I'm still a beginner and am not well-conversed with the components and code. 
</p><p>
I aspire to build a more advanced version of this using Liquid Crystal Display (LCD) and a score-board (second LCD), to make this more player-friendly and attractive, after learning to use the particular modules. This version will be posted in the Projects section of the website. </p>
<hr><br><p>
Lately, I’ve been so deeply interested that I end up spending hours with the board and components, needing an alarm to remind me to stop and go to sleep <lol>. Of all the stuff, the thing that is most interesting to me right now, is me discovering new kinds of outputs from different components, and just imagining their uses/applications in my future projects. 
Once I understand at least 50% of all the components in the kit, I'll seriously start building real, useful and meaningful projects (and that includes mini-games 😜). 
</p>

<hr><br>

<h3>Links 🔗 </h3>
<p>Arduino kit that I purchased: <a href=https://www.amazon.in/dp/B0FVXW6K2T class="content-link">Kit</a> <br><br>
Documentation to get started with electronics and uses via examples: <a href=https://docs.arduino.cc/built-in-examples/ class="content-link">Arduino Docs</a><br><br>
Information about the board and technical details: <a href=https://docs.arduino.cc/learn/ class=content-link>About the Board</a> </p>
<hr>




