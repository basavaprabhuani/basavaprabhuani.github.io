---
layout: post
title: Rayla vs. Probability
date: 2025-11-02 00:00:00 +0530
categories: Mathematics Combinatorics 
---

<p>Get the context by watching the video: </p><br>
<figure>
    <video controls>
        <source src="/media/rayla_lucky_vid.mp4" type="video/mp4">
        Error with browser: Does not support video.
    </video>
    <figcaption>A scene from The Dragon Prince</figcaption>
</figure>
<br>

<p>As seen in the video, Ezran (the little kid) presses a bunch of stones on a wall, while calling it a Stone or a Rock (what's the difference anyway, though?). Don't call me acerbic, but I must say, it is amusing to watch him be intelligent enough to remember that combination along with stone/rock, but not smart or hygienic enough to wipe off or AT LEAST lick off the jelly on his hands. UGH! <br>Coming back to the story, we see Rayla (the elf) effortlessly cracking the combination, allegedly by "pressing all the stones with jelly handprints". If that's so, then there are only two explanations: <b>(i) The security to that secret chamber is compromised </b>as hell, which is unlikely, or <b>(ii) Rayla got handsomely lucky</b> (or beautifully lucky, in her case).</p>

<br>
<p>Here's why: </p>
<p>The lock consisted of pressing <text class="number">9</text> rocks, in a specific series, while calling it with a specific name: Rock or Stone. Since Rayla was very clear that she pressed the stones with jelly handprints, she knew the rocks to be pressed. All she had to do was get the order right. Also, for the sake of proving Rayla's luck, let us assume that each rock had to be pressed only once.</p>

<p>This is similar to a situation where you know the digits of a number lock but do not know the order. Consider this keypad: </p>
<div style="text-align: center;">
    <figure>
        <img src="/media/keypad.png">
        <figcaption>(Consider the password to this lock to be <b><text class="number">8461</text></b>)</figcaption>
    </figure>
</div>

<p>The circumstances allow for us to know the digits of the lock. <br>  
These are the digits required to open the lock: <text class="number">1</text>, <text class="number">4</text>, <text class="number">6</text>, and <text class="number">8</text>. We arrive at a point to prove Rayla's insane luck already: Just knowing the digits is not enough. We need the specific order of the digits in the lock.<br><br> For instance, these are the different numbers we can get using these digits (once) alone: </p>

<table>
    <tbody>
      <tr><td>1468</td><td>4168</td><td>6148</td><td>8146</td></tr>
      <tr><td>1486</td><td>4186</td><td>6184</td><td>8164</td></tr>
      <tr><td>1648</td><td>4618</td><td>6418</td><td>8416</td></tr>
      <tr><td>1684</td><td>4681</td><td>6481</td><td><font color="green"><b>8461</b></font></td></tr>
      <tr><td>1846</td><td>4816</td><td>6814</td><td>8614</td></tr>
      <tr><td>1864</td><td>4861</td><td>6841</td><td>8641</td></tr>
    </tbody>
</table>

<p>From the table, it can be observed that the <text class="number">8461</text> is <text class="number">1</text> of the <text class="number">24</text> different combinations that can be obtained by shuffling the digits – and Rayla got it in under <text class="number">20</text> seconds. This example is enough to prove that she was lucky. </p>

<p>All good. But how lucky was she, numerically? </p>

<p>According to the data we have, we know that <text class="number">9</text> rocks had to be pressed, in a specific sequence. We could label each of those rocks with a letter, say <text class="number">A, B, C, D, ... , I</text>. Then, we could work out all the possible sequences the rocks could be pressed, to find out the total number of possibilities. Let's gooo: </p>

<p>ABCDEFG<font color="orange">HI</font>, ABCDEFG<font color="orange">IH</font>, ABCDEF<font color="orange">HGI</font>, ...</p>

<p>Oof, I'm tired and this thing feels so time-consuming and boring... Any way we could find out the number of such sequences possible instantly? </p>

<p>Heck yeah, boy, that's where Permutations come in! <br>A permutation means a specific sequence or order in which a list of things occur, be it digits, or letters, or just about any group of things. So, the various sequences of the letters A to I that can possibly occur, they are permutations. For example, ABCDEFG<font color="orange">HI</font>, and ABCDEFG<font color="orange">IH</font> are two permutations of the group of letters from A to I. </p>

<p>There is a very simple and logical (of course) way to calculate the total number of all possible permutations. </p>

<p>To understand this, consider a simple example. Take just three letters, <text class="number">A, B</text> and <text class="number">C</text>. </p>

<p>To begin with, you have <text class="number">3</text> letters to choose from. For the next digit, you have <text class="number">2</text> letters to choose from. Therefore, you can represent this possible number of permutations mathematically: </p>

<p class="formula">3 × 2 × 1 = 6</p>

<p>When you work the permutations out manually, you find that you get <text class="number">6</text> different permutations even then! </p>

<table>
    <tbody>
      <tr><td>ABC</td><td>ACB</td><td>BAC</td></tr>
      <tr><td>BCA</td><td>CAB</td><td>CBA</td></tr>
    </tbody>
</table>

<p>Also for the keypad-password example above, you could use the same logic: </p>

<p>1<sup>st</sup> digit → <text class="number">4</text> numbers to choose from<br>
2<sup>nd</sup> digit → <text class="number">3</text> numbers to choose from<br>
3<sup>rd</sup> digit → <text class="number">2</text> digits to choose from<br>
4<sup>th</sup> digit → <text class="number">1</text> digit to choose from.<br><br>
Mathematically:</p>

<p class="formula">4 × 3 × 2 × 1 = 24</p>

<p>Lookie what we've got: <text class="number">24</text>. Which is exactly equal to the number of permutations we got when we worked them out manually.</p>

<p>There's a simpler way to express this pattern of multiplying numbers with their preceding numbers till <text class="number">1</text>: Factorials.</p>

<p>This is how factorials are expressed mathematically: </p>

<p class="formula">n! = n × (n − 1) × (n − 2) × ... × 1</p>

<p>For example, </p>

<p class="formula">3! = 3 × 2 × 1 = 6<br>4! = 4 × 3 × 2 × 1 = 24</p>

<p><br>Coming back to our original question, to work out the number of permutations we can obtain using the rocks, i.e., the letters <text class="number">A</text> to <text class="number">I</text>, we could use factorials. Since there are <text class="number">9</text> rocks, the total number of permutations is:</p>

<p class="formula">9! = 9 × 8 × 7 × 6 × 5 × 4 × 3 × 2 × 1 = 362,880</p>

<p>This is a neat trick to find out the number of permutations possible, but <b>note, this is valid only for non-recurring digits in a sequence</b>. If all digits could repeat themselves, it would be exponential. For example, if you could use the digits <text class="number">1</text>, <text class="number">2</text> and <text class="number">3</text> any number of times to get a <text class="number">3</text>-digit number, not necessarily all digits have to be present, then, by the same logic, there would be <text class="number">3</text> digits to choose from for the first digit, for the second digit too there would be <text class="number">3</text> digits, because the digits can repeat in this case! <br><br>So, to obtain a <text class="number">3</text>-digit number from the <text class="number">3</text> digits, mathematically, we would do:</p>

<p class="formula">3 × 3 × 3 = 3³ = 27</p>

<p>In such recurrable cases, we use exponents. If we have <text class="number">n</text> digits and have to make an <text class="number">m</text>-digit number, under the condition that we can use any digit any number of times and not all digits must be present in a number, then the number of permutations possible would be <text class="formula">n<sup>m</sup></text>, since we don't <i>lose</i> a digit with each place. </p>

<p>Now to the original question (again): We're not done yet; remember that there was a specific Rock/Stone keyword attached with each stone pressed? This only magnifies the elf's luck now; using the above information, and the fact that there could be a Stone or Rock for each stone pressed, the number of permutations, now including both the sequence of rocks pressed AND Stone/Rock for each stone, increases. Calculating the new permutation again, we get: </p>

<figure>
    <img src="/media/permutations_2.png">
</figure>

<p>There we go! A total of <text class="number">185,794,560</text> possible permutations, and Rayla unlocked the secret opening within a matter of <text class="number">15</text> seconds. If this is not lucky, I don't know what is. And in addition to my two theories above, here's a third one, based on this: <b>(iii) Rayla had a time machine which she used to rewind time over and over again until she opened the lock.</b> </p>

<br>
<hr><br>

<p>So, to sum it up: either Rayla is impossibly lucky, or probability decided to take a personal day. In any case, I’ll stick to math (and science)— it’s the only thing that doesn’t depend on jelly consistency. And I'm second-guessing: Rayla didn’t just get lucky—she looked Probability dead in the eye and said, “Move.” And Probability did. Somewhere, a statistician just screamed into a pillow.</p>

<br>
<hr>




