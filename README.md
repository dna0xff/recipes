## Pretty self explanitory


### Boating off course alarm
Single file application that runs in your browser. 
Ideally you should be able to run from the local file system, however I suspect that there may be an issue with browser security alowing access to the location services. 
It currently runs in *DEMO_MODE*  you can change this by editing the head of the file. A few other parameters such as the audio to play on alarm, though I think that the one used is pretty good. 

Demo mode will run for 10 ityterations on course then verr through 45 degrees. The alarm should then trigger. You can change the alarm parameters ( increase the alowed deviation ) and cointinue running. Eventually it will trigger again. 
Demo mode asumes you are stationary, it gets gps coordinates then adds a demo offse that varies over time. You can adjust these also at the head of the file for your amusement and to get to see what happens using the app.


#### testOffCourse.html use instructions
<li>Press <b>Stby</b> to capture an initial position.</li>
  <li>Get your vessel on to the desired heading, trim etc.</li>
  <li>review <b>Settings</b> for desired checking interval and off-course bearing and xte limit.</li>
  <li>press <b>Run</b> to capture the current position. A heading will be calculated and a timer started.</li>
  <li>When the timer expires  the current position will be updated and the course checked against the heading from earlier.</li>
  <li>If am alarm condition exists, the screen will flash and the klaxon will sound.</li>
  <li><b>Reset</b> the alarm will stop the noise BUT if the alarm condition still exists it will trigger again next check.</li>
  <li>You can either change <b>Settings</b>, go to <b>Stby</b> or turn <b>OFF</b></li>
