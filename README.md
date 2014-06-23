OSG Connect Quickstart
======================

Login to OSG Connect
--------------------
If not already registered to OSG Connect, go to the registration site and follow instructions there.
Once registered you are authorized to use login.osgconnect.net (the Condor submit host) and stash.osgconnect.net (the data host), in each case authenticating with your network ID (netid) and password

Set up the tutorial
-------------------
You may perform the examples in the tutorial by typing them in from the text below, or by using tutorial files already on login.osgconnect.net. It's your choice; the tutorial is the same either way. 


### Pretyped setup
To save some typing, you can install the tutorial into your home directory from login.osgconnect.net. This is highly recommended to ensure that you don't encounter transcription errors during the tutorials. 

````bash
$ tutorial 
usage: tutorial name-of-tutorial 
       tutorial info name-of-tutorial

Available tutorials: 
quickstart     Basic HTCondor job submission tutorial
````

Now, run the quickstart tutorial:
````bash
$ tutorial quickstart 
$ cd ~/osg-quickstart 
````

### Manual setup 
Alternatively, if you want the full manual experience, create a new directory for the tutorial work: 
````bash
$ mkdir osg-quickstart 
$ cd osg-quickstart
````

Tutorial jobs
-------------
### Job 1: A simple, nonparallel job

Inside the tutorial directory that you created or installed previously, let's create a test script to execute as your job: 

````bash
#!/bin/bash
# short.sh: a short discovery job
printf "Start time: "; /bin/date
printf "Job is running on node: "; /bin/hostname
printf "Job running as user: "; /usr/bin/id
printf "Job is running in directory: "; /bin/pwd
echo
echo "Working hard..."
sleep ${1-15}
echo "Science complete!"
````


