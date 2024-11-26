# Envy BBS Documentation

## Configuration Files
### envy.ini

`envy.ini` lives in your BBS's working directory, it is used both by servo and envy.

 * Main Section
   * **telnet port** Port to listen for telnet connections on
   * **max nodes** Maximum number of nodes (similtanious connections)
   * **default tagline** Default tagline for networked message bases, can be overridden.
   * **sysop name** The username belonging to the Sysop
   * **bbs name** The name of your bbs
 * Path Section
   * **gfile path** Path to where gfiles are located (Relative to working directory)
   * **data path** Path to where data files are (Relative to working directory)
   * **message path** Path to where message base data is stored (Relative to working directory)
   * **log path** Path where to store log files (Relative to working directory)
   * **temp path** Base path for temporary files eg. Drop files (Relative to working directory)
   * **scripts path** Path to where the JavaScript scripts live (Relative to working directory)
  
### msgbases.toml

Contains an array of `msgbase` lives in the `data path`

Example:
```
[[msgbase]]
name = "FSXNET: General Chat"
file = "fsx_gen"
type = "echomail"
aka = "21:1/999"
write-sec = 25
```

  * **name** The human readable name of the message base
  * **file** The filename (without extension) of the JAM message base containing messages (relative to the `message path` in envy.ini)
  * **type** either local, echomail or netmail
  * **aka** the aka for the network this message base is a part of (only required for netmail / echomail)
  * **write-sec** the minimum security level a user must have to write in the area
  * **read-sec** the minimum security level a user must be for the area to be visible at all

### doors.toml

Contains a array of `door` lives in the `data path`

Example:
```
[[door]]
key = "WORDELLE"
name = "Wordelle"
script = "/home/andrew/doors/wordelle/wordelle.sh"
```

  * **key** a key to use to execute this door via javascript.
  * **name** The human readable name of the door
  * **script** script to run to launch the door, is passed the nodenumber as argument 1

### seclevels.toml

Contains an array of `seclevel` lives in the `data path`

Example:
```
[[seclevel]]
level = 10
name = "New User"
timeout = 15
time = 120
```

  * **level** the security level
  * **name** a name for the security level
  * **timeout** the number of minutes a user of this security can idle before being booted
  * **time** the number of minutes a user of this security level has per day

### trashcan.txt

Each line contains a username that is unavailable to new users

Example:
```
sysop
unknown
guest
nobody
```

## Javascript Reference

  * print
  * getch
  * disconnect
  * gets
  * getpass
  * getattr
  * putattr
  * bgetattro
  * getattro
  * putattro
  * cls
  * gfile
  * exec
  * save
  * load
  * globalsave
  * globalload
  * getusername
  * listmsgs
  * readmsgs
  * writemsg
  * selectarea
  * getarea
  * pause
  * scanbases
  * rundoor
  * getdoors
  * getmsglr
  * getmsgtot
  * listemail
  * enteremail
  * checkuser
  * countemail
  * unreademail
  * timeleft
  * getusers
  * opname
  * getversion
  * setaction
  * getactions
  * getusernameo
  * setpasswordo
  * setpassword
  * checkpassword
  * isvisible
  * readmsg
  * postmsg
