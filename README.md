**DarkSky - Take a Talk Into the Art of Dark Sky Photography With a Splunk Ninja**

This is the app used for my .conf2017 talk
**IOT121001 - Take a Talk Into the Art of Dark Sky Photography With a Splunk Ninja**
https://conf.splunk.com/conf-online.html?search=IOT121001#/

For your own sake, don't install this on a production system or Splunk Cloud!

**What this app does?**

This app will help you finding the closest, most darkest location to get an awesome
night sky photo. For more details read the slides
`take-a-talk-into-the-art-of-dark-sky-photography-with-a-splunk-ninja.pdf`
included in the app `install` folder.

All the astronomy related research was done on Google, therefore please assume
anything is wrong ;)


**Install:**

Get the app from https://github.com/M-u-S/DarkSky2017 and install as any other
Splunk app.
To get the moon, Mapbox API data you need to install the following
app: https://splunkbase.splunk.com/app/3880 (v1.2.2 or later)

There are two additional apps in the `install` folder that must be
installed as well. They were slightly modified to work with the DarkSky app.

You then need to download 5Gb of map tiles and light pollution data from
https://mega.nz/#!byQTQQLa!TfMcjUn58gQoFCVUGl2AhjJZa-1eSt2YnKnOPmDrd4Q
and manually unpack it into the already installed `DarkSky2017` app folder.


**Configure:**

The app will create an index called `darksky` and an accelerated DM with the
same name. The DM root search is using an eventtype called `darksky`. If you
have changed any of the input options, please adapt this eventtype to reflect
the changes made.

The app contains one input to index the light pollution data, you must enable
the input. The light pollution data contains 90 millions lines of data and the
index, DM and accelerated data will be around 11Gb in total!

All map tiles are configured to use a host called `crux` (A constellation called
Southern Cross https://en.wikipedia.org/wiki/Crux ). If you are not using
this hostname, than you need to change the following dashboard:

- DarkSky-Start.xml (or use the UI)

**Debug:**

Nothing to see here, move along.


**Support**

This is an open source project, no support provided, but you can ask questions
on answers.splunk.com and I will most likely answer it.
Github repository: https://github.com/M-u-S/DarkSky2017

I validate all my apps with appinspect and the log can be found in the README
folder of each app.

Running Splunk on Windows? Good Luck, not my problem.

**Things to-do / Future ideas**

-  `¯\_(ツ)_/¯`  


**Versions**

0.1.0 : Somewhen in 2015 | Initial idea  
1.0.0 : June 2017 | Ready for .conf  
1.0.1 : 26. September 2017 | Last minute panic changes just before the talk  
1.0.1 : Oct 2017 - Feb 2019 | ....  
1.1.0 : 8. February 2019 | Finally ready to be published
