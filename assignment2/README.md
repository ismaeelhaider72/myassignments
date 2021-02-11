#  Question
Accepts a filename on the command line. The file is a Linux-like log file
from a system you are debugging. Mixed in among the various statements are
messages indicating the state of the device. They look like this:<br/>
   Jul 11 16:11:51:490 [139681125603136] dut: Device State: ON<br/>
The device state message has many possible values, but this program cares
about only three: ON, OFF, and ERR.<br/>
Your program will parse the given log file and print out a report giving
how long the device was ON and the timestamp of any ERR conditions.<br/>
<br />
_**output:**_<br />
Device was on for 7 seconds<br/>
Timestamps of error events:<br/>
   Jul 11 16:11:54:661<br/>
   Jul 11 16:11:56:067

---

###  Answer:

Modules used:

``` python
import datetime   
import sys

```

used `sys.argv[1]` to Accepts a filename on the command line<br/><br />
used `strptime()` method creates a datetime object from the given string <br/>
The `strptime()` class method takes two arguments:

* string (that be converted to datetime)<br/>	
* format code<br />

**In last:**<br/>
Getting Result:<br/>

Method `result=(offevent - onevent).total_seconds()` to get output in Seconds <br/>

_**Execution**_<br/>

Save this python file and log file (e.g D:\\assignment\sample.log) ,(e.g D:\\assignment\parsing.py) and open the console and <br/> run it by just typing below command<br/> `py  D:\\assignment\parsing.py  D:\\assignment\sample.log`



---




