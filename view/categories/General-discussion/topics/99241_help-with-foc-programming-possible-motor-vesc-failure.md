# Help with FOC programming ( possible motor/vesc failure )

### Replies: 8 Views: 119

## \#1 Posted by: GoofyRider89 Posted at: 2019-07-28T04:44:53.988Z Reads: 34

```
I used the FOC wizard in Vesc-tool 1.16, I selected the 700g outrunner option as I figured this was closest to what I have. Set the series number to 5 and the battery capacity ah to 15.00ah. The motors spin up smoothly, stop then jiggle a bit with some electronic buzzing then I get these results.![20190727_211504|374x500](upload://gDwF988izb3TSBL07DC8KNwLmCo.jpeg)  One motor says sensorless when they both have hall sensors and one is running really low current compared to the other. 

Then I get to the direction spin section where I can spin each motor individually and see if they are spinning the correct way. One spins up just fine ( I'm assuming it's the one that detected the hall sensors ) the other one makes a god awful loud noise kinda skreetchy and buzzy at the same time and the motor does not move. 

I wanted to see if it was the vesc doing this or the motor so I unplugged everything and swapped the phase wires from one vesc to the other then tried again. The symptom has moved from one motor to the other. Did I fry one of my vescs or did one of my motors get fried? I don't understand how it worked when I used it last (sometime in March/may) and now it's giving me this. 

My Build: 
2 x 4.12 vesc software 3.58 connected via can
10s5p 30q 
V4 torque drives

Any help would be appreciated, not sure where to go from here. Thanks in advance.
```

---
## \#2 Posted by: Darkie02 Posted at: 2019-07-28T07:46:09.098Z Reads: 26

```
Had 1\2 of you issues with new VESC software had to manually go in after the auto detect and tell it to use hall senceres on one of the vesc.

Read motor config Click on the sensor tab, tell it hall sensors run sensor detection on that vesc apply, Wright motor configuration

It also cam up with my battery max at 200a when I said I was using 10s 7ah.

By the looks of it your other vesc is having issues the one seeing the sensors reading a massive resistance. That’s why it’s giving such a bad values 

You could use the values generated by the good vesc then swop the motor to the bad detection one an manually add the values.
```

---
## \#3 Posted by: GoofyRider89 Posted at: 2019-07-28T22:55:29.005Z Reads: 19

```
Thanks for the advice, I decided to switch my vescs back to their original side before trying it out. Unplugged the three phase and the suspected bad vesc and this happened lol![Screenshot_20190728-155249|281x500](upload://htAvvcb9dNjUCdTLLhiXHAH3jhc.jpeg)   Going to re-solder tommorow and retest. I'll post my results. Thanks again.
```

---
## \#4 Posted by: GoofyRider89 Posted at: 2019-07-30T01:51:04.713Z Reads: 11

```
Ok so I fixed the phase wire, then hooked everything back up. I used the previous version of the vesc tool v1.05 and I downgraded my vescs back to 3.51. Went through the FOC wizard and SUCCESS! ![20190729_183608|374x500](upload://rGgGcfdg7YUrCZKrKKB1D4iVeQl.jpeg)  hall sensors are now being read on both motors with proper reading and no horrible noise. 

Now that I have that all figured out I have one more question. Anyone know the ID name for an HM-10 BT module? I have it plugged in to my master vesc and set the baud rate to 9600. I purchased the vesc tool app but I when I go to connect to the BT module I get a list of about 10 ID's I have tried all of them and none of them successfully connect. Any ideas?
```

---
## \#5 Posted by: Santino Posted at: 2019-07-30T02:08:02.611Z Reads: 10

```
vesctool .........set it to  PPM and UART ...
```

---
## \#6 Posted by: GoofyRider89 Posted at: 2019-07-30T02:42:24.366Z Reads: 9

```
Tried to start fresh and do it again, ![20190729_192908|374x500](upload://5vvnq5QD6zNFkbo80xyZW17tNCQ.jpeg) ![20190729_192954|374x500](upload://8DQVkIsXchajw7zAGojafOpqxhx.jpeg) ![20190729_193119|374x500](upload://zpM7UHg4k8QHNMh0w17tPlE9Deh.jpeg) ![20190729_193143|374x500](upload://tiTcmXUgDFlLwxXqR3KQcUBW6E.jpeg) still no luck, am I missing something?
```

---
## \#9 Posted by: Santino Posted at: 2019-07-30T05:44:05.545Z Reads: 7

```
![blue2|690x388](upload://hOQfq48vpLHIGBWvYjGOOL9u10m.jpeg)

APP SETTINGS....GENERAL....APP TO USE select PPM and UART
```

---
## \#10 Posted by: GoofyRider89 Posted at: 2019-07-30T06:12:30.500Z Reads: 5

```
That is what I have it on, I clicked on the read current setting and it says ppm and UART. I clicked the drop down then reselected ppm and UART and clicked the write app configurations. For some reason it's not picking it up on my app. My phone is a s7 edge if that matters. Thanks for helping me with this, I appreciate it.
```

---
