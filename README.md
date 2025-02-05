## Pretty self explanitory


### Boating off course alarm  NOT ready for use yet still debugging
Single file application that runs in your browser. 
Ideally you should be able to run from the local file system, however I suspect that there may be an issue with browser security alowing access to the location services. 

#### DEMO_MODE
It currently runs in **DEMO_MODE**  you can change this by editing the head of the file. A few other parameters such as the audio to play on alarm, though I think that the one used is pretty good. 

Demo mode will run for 10 iterations on course then veer through 45 degrees. The alarm should then trigger. You can change the alarm parameters ( increase the alowed deviation ) and cointinue running. Eventually it will trigger again. 
Demo mode asumes you are stationary, it gets gps coordinates then adds a demo offse that varies over time. You can adjust these also at the head of the file for your amusement and to get to see what happens using the app.


#### testOffCourse.html user instructions
- Press **Stby** to capture an initial position.
- Get your vessel on to the desired heading, trim etc.
 review **Settings** for desired checking interval and off-course bearing and xte limit.
- press **Run** to capture the current position. A heading will be calculated and a timer started.
- When the timer expires  the current position will be updated and the course checked against the heading from earlier.
-  If am alarm condition exists, the screen will flash and the klaxon will sound.
**Reset** the alarm will stop the noise BUT if the alarm condition still exists it will trigger again next check.
- You can either change **Settings**, go to **Stby** or turn **OFF**

### Where to run it from
That's the 64M$ question. you can't run from the repo, but you can dowload the file. 
#### local filesystem
On a computer you can point your browser at the file and it should load. Make sure you download the audio file as well to the same location. 
file:///home/<xxxx>/Downloads/testOffcourse.html
#### webserver
I'm launching the simple python webserver to serve it up as localhost. This seems to be OK for the case where running from the local filesystem does not work.
`<xxxx>@fedora:~/Downloads$ python3 -m http.server 9000`
then http://localhost:9000/testOffcourse.html

##### rawgit.com
rawgit alows you to runfiles in a git repo, This is how I am testing on a phone. 
https://raw.githack.com/dna0xff/recipes/master/testOffcourse.html

or perhaps for production related use, this does rely on content being pushed to the cdn bit if so you get a local copy rather than back to git centeral. 
https://cdn.raw.githack.com/dna0xff/recipes/master/testOffcourse.html
