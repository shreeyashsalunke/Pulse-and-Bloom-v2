<h5><i>Pulse and Bloom is a collaberative project done by <b>Saba Ghole, Shilo Shiv Suleman, Rohan Dixit, Heather Stewart, Luke Iseman,</b> and <b>Samuel Clay</b>. I got an opportunity to work with <b>Kavya D</b> and <b>Shilo Shiv Suleman</b> on this Art Installation<br><br>
Thanks to <b>Avijit Michael</b> and <b>Kalyani Ingole</b>.<br>
Special thanks to the amazing <b>Ankit Daftery</b> for his always supporting and helping nature.</i></h5><hr>

<img src="https://raw.githubusercontent.com/shreeyashsalunke/Pulse-and-Bloom-v2/master/images/pulse-and-bloom-burning-man.gif">
<br>
Pulse and Bloom is an interactive and social art installation that visualizes participants’ heartbeats and invites people to share and sync their human heartbeats in a rhythmic pattern. Pulse and Bloom is one of the largest biofeedback installations of its kind, allowing 40 people to visualize their heartbeats simultaneously.

Pulse and Bloom consists of 10 lotuses of varying heights of 10 to 14 feet with pulse sensors mounted on the base of the stem. When a participant places their hand upon the pulse sensor, the stem and the flower in the sky start to beat with their heart. Furthermore, when more than one person places their hand upon the pulse sensor, the stem starts to pulse with both participants’ heartbeats, making it possible to watch how heart rates of different people in intimate spaces start to beat in sync, much like fireflies flashing in patterns.

Arranged in a circular matrix, the 10 lotuses contain LED lights wrapped around their stems and LEDs inside the flowers at the top that are activated when individual participants physically interact with the lotus. Each lotus is equipped with two pulse sensors, each located on a Hamsa Hand, that when pressed by one or two participants translates the participants’ heartbeat into pulsing LED lights within the lotus, visually projecting their heart into the flower in the sky. As more people begin to interact with the different lotuses, visualizing their heartbeats in pulsing lights, we begin to see the effects of each person’s heartbeat on the other and the effect of meditative synchronicity unfold.

<h2>Background by Shilo Shiv Suleman</h2>
Connection is at the core of human experience. All traditional cultures have had their spaces of ‘communion’ - of coming together and sharing. These sacred spaces were intensely personal, yet became a focal point to gather and connect.

Through our art installation Pulse and Bloom, we want to use technology to make our inner invisible worlds more visible. Using visual representations of our inner state, we aim to create group experiences of magical synchronicity that make us more aware as individuals and more connected as a community.

Remembering the ancient philosophers and mystics that spoke of the human heart as the vehicle for union between individual and environment, we wish to recreate this experience through modern heart-quantifying biosensors embedded within public art. Scientific studies show that people who spend a few moments connecting with each other, in time can sync their heartbeats to one another. We’d like to see if having public art as a mirror for this can enable people to connect better and with minimal barriers.

<h2>Interactions</h2>
Each lotus flower is blue until a person or two sits down at its base and places their hand on the pulse sensor. There is a Hamsa hand at the base of the lotus and its embedded pulse sensor. When a pulse is read, the lotus flower shoots the heartbeat up the stem and into the petals, where it blooms in a brilliant display of amber. When two people's hands are being measured, both of their heartbeats are shown as two distinct colors.

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://player.vimeo.com/video/208532071' frameborder='0' webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe></div>
<br>
<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://player.vimeo.com/video/208532049' frameborder='0' webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe></div>


<h2>Building up the Installation</h2>
The installation was divided into 3 major parts:<br>
- <a href="#electronics">The Electronics</a><br>
- <a href="#software">The Software</a><br>
- <a href="#fab">Fabrication of the Lotus Structure and the Aesthetics</a><br>
<hr>

<p><a name="electronics"></a></p>
<h2>The Electronics</h2>
The electronics was further divided into 4 stages:<br>
- <a href="#boards">Making the custom circuit boards</a><br>
- <a href="#pulse-sensors">Making the custom pulse sensors</a><br>
- <a href="#leds">Driving the high current LEDs</a><br>
- <a href="#power">Powering the lotuses</a><br>
- <a href="#power">Endless cycle of Testing and Debugging :P</a><br>

<p><a name="boards"></a></p>
<h3>Making the custom circuit boards</h3>
The main circuit board controls 2 addressable RGB LED Neopixel Strip, 3 sets of 3 (i.e. 9) High Power RGB LEDs and takes input from 2 pulse sensors. The LED Strip and the High Power RGB LEDs runs on 12V supply, the ATMega328p microcontrollers runs on 5V and the Pulse Sensors run 3.3V. To convert 12V to 5V, I used an off-the-shelf voltage regulator. This required a +/- connection for both 12V in and 5V out. To convert 5V to 3.3V I used a SMD linear voltage regulator which was soldered directly on the board. The trace to the LED strip and High Power LEDs were thickened to provide upto 3A of current rating, while they consumed only around 1A current to avoid heat dissipation. Finally, all of the terminations are made using 2.5mm and 3.5mm pitch screw terminals.
<figure><center><img src="https://raw.githubusercontent.com/shreeyashsalunke/Pulse-and-Bloom-v2/master/board/board-schematics.png">
<figcaption align="center"><h5>Board Schematics</h5></figcaption></center></figure>
<figure><center><img src="https://raw.githubusercontent.com/shreeyashsalunke/Pulse-and-Bloom-v2/master/board/board-preview.png"></center>
<figcaption align="center"><h5>Board Layout</h5></figcaption></figure>
<img src="https://raw.githubusercontent.com/shreeyashsalunke/Pulse-and-Bloom-v2/master/images/08.jpg">
<img src="https://raw.githubusercontent.com/shreeyashsalunke/Pulse-and-Bloom-v2/master/images/09.jpg">
<img src="https://raw.githubusercontent.com/shreeyashsalunke/Pulse-and-Bloom-v2/master/images/12.jpg">

<p><a name="pulse-sensors"></a></p>
<h3>Making the custom pulse sensors</h3>
<img src="https://raw.githubusercontent.com/shreeyashsalunke/Pulse-and-Bloom-v2/master/images/13.jpg">
The Pulse Sensor was built by the design made by <i>Samuel Clay</i>. <br>
Link to the schematics and the brd file <a href="https://github.com/samuelclay/pulse-bloom/tree/master/pulse%20eagle">here</a>.<br>
<figure><center><img src="https://raw.githubusercontent.com/shreeyashsalunke/Pulse-and-Bloom-v2/master/images/Pulse & Bloom - sensor schematic.png">
<figcaption align="center"><h5>Pulse Sensor Schematics</h5></figcaption></center></figure>

<figure><center><img src="https://raw.githubusercontent.com/shreeyashsalunke/Pulse-and-Bloom-v2/master/images/Pulse & Bloom - sensor layout.png">
<figcaption align="center"><h5>Pulse Sensor Board Layout</h5></figcaption></center></figure>



<p><a name="leds"></a></p>
<h3>Driving the high current LEDs</h3>
<img src="https://raw.githubusercontent.com/shreeyashsalunke/Pulse-and-Bloom-v2/master/images/10.jpg">
<img src="https://raw.githubusercontent.com/shreeyashsalunke/Pulse-and-Bloom-v2/master/images/11.jpg">

<p><a name="power"></a></p>
<h3>Powering the lotuses</h3>

<h3>Endless cycle of Testing and Debugging :P</h3>
<img src="https://raw.githubusercontent.com/shreeyashsalunke/Pulse-and-Bloom-v2/master/images/14.jpg">
<img src="https://raw.githubusercontent.com/shreeyashsalunke/Pulse-and-Bloom-v2/master/images/15.jpg">

<p><a name="software"></a></p>
<h2>The Software</h2>

<p><a name="fab"></a></p>
<h2>Fabrication of the Lotus Structure and the Aesthetics</h2>
