 [![Build Status](https://secure.travis-ci.org/jh3y/sike.png)](http://travis-ci.org/jh3y/sike)

sike 
===
![alt tag](https://raw.githubusercontent.com/jh3y/sike/page-dev/src/files/images/sike.png)

a cli tool that reminds you to move around every once in a while!

```bash
	sike -i 2h -m "Go grab a coffee! You've earnt it."
```
##what is sike?
sike is a cli tool that alerts you at set intervals, a set duration or a set time to get up and be active for a few minutes with command line messages and the triggering of system sounds. 

##why sike?
 Sometimes, you find yourself getting stuck into some issue or feature implementation or any other thing really and before you know it hours have passed. You may have lost track of time and actually wanted to get something else done but now you've lost that time etc.

Also if you spend a lot of time rooted to one position it's not particularly good for your body, you need to get up a move every once in a while. A little reminder could help you out.

It's something that I personally find useful and maybe somebody else will.

##who is it for?
sike is for those that spend a long time behind a screen or at a workstation and get stuck in the _zone_. It's a handy scheduling/reminder tool for those that spend a lot of time in the command line and don't want to burden themselves with flashy UIs to do such a simple thing.

##example uses

* setting sike to tell you to get up and be active every hour or whatever interval you define.
* setting sike to remind you to get up and move about at a certain time of day.
* setting sike to tell you to get up and walk away in a certain amount of time.

##usage
###prerequisites
It's assumed that you have `node` already installed.
###install
Simply run,
```bash
	npm install -g sike
```
###options

#### `-i, --interval [interval]`
Sets alert interval. Accepts a string input defining hours, minutes and seconds or a combination. For example, `sike -i 1h10m` would set sike to alert you every one hour and ten minutes.
#### `-d, --duration [duration]`
Sets duration until alert. Similarly to __interval__ accepts a time string. For example, `sike -d 45m` would set sike to alert you in forty five minutes one time. This is handy if you set yourself a task to complete in a certain amount of time.
#### `-t, --time [time]`
Sets alert time. This is used when you want sike to go off at a certain time and works on a 24 hour clock system. For example, `sike -t 18:30` would set sike to go off at six thirty pm.
#### `-m, --message [message]`
Sets interval message. Allows you to customise the interval message accepting a string message to be displayed at every interval. The default is "Get up and move around!" but you could for example use `sike -i 30m -m "Go grab a coffee!". But that's a lot of coffee in a day!
#### `--timeMessage [timeMessage]`
Sets time message. This is similiar to message but allows you to customise the message being displayed when using the `time` or `duration` options. For example, `sike -d 1h30m --timeMessage "Go get some lunch now!".
#### --dontShowTimestamp`
Defines whether timestamp message is shown with alerts. By default this is set to `false` and timestamps are shown for alerts.
#### `-b, --bells [bells]`
Set number of bells on alert. Accepts a number that defines the amount of bell chimes that should be played at each alert message. The default is `2`. But for example you may want `5` using `sike -i 2h -m "Go grab a coffee" -b 5`.
#### `-h, --help`
Show help.

###examples
```bash	
	sike --interval 1h30m
	sike -i 1h30m
	sike --duration 1h
	sike -d 1h
	sike --time 18:20
	sike -t 18:20
	sike --time 18:20 --timeMessage "Get ready to go grab that flight now!"
	sike --interval 2h --message "Go grab a coffee"
	sike -i 2h -m "Go grab a coffee"
	sike --interval 45m --bells 2
	sike -i 45m -b 2
```
##under the hood
sike is very lightweight and uses commander, colors and moment to provide its service.

##contributing
As sike is in its infancy, any input and suggestions are much appreciated. If this is a tool you think you could find useful, please let me know how it could be improved. For me personally, the interval option is the most useful but others might want a different option or more logging provided. So, please post an issue if you have anything!

Any suggestions, improvements or issues are welcome. :)

@jh3y


##license

MIT

Copyright (c) 2014 [@jh3y](https://github.com/jh3y)
