# Esk8 w/o any external chargers?

### Replies: 20 Views: 229

## \#1 Posted by: ZachTetra Posted at: 2019-01-15T04:45:16.554Z Reads: 95

```
Has anyone made their BMS/charger with the AC outlet plug as part of the board?  I'm thinking it would be easier if the AC/DC converter was inside the enclosure then the only things going in or out of the enclosure would be a 3 prong outlet on a short cable (clip it down the length of the board), the antispark power switch button, and the phase/sensor wires to the motor.  You could charge on the go and it would be really easy to waterproof since the 3 prong plugs have no voltage across them when they are unplugged from a power source so the prongs can be exposed and the other end is just a single thick round wire...then again this could be a terrible idea and set everything on fire...I don't know.  Thoughts/stories/opinions?
```

---
## \#2 Posted by: J_Dizzle Posted at: 2019-01-15T04:46:37.399Z Reads: 93

```
I don’t think that is any more convenient that a regular charger
```

---
## \#3 Posted by: ZachTetra Posted at: 2019-01-15T04:49:20.658Z Reads: 91

```
Probably should have mentioned, I was thinking of doing this for an electric nickle board for school, so something like a 6s 2000mah battery so it would be significantly light but you charge it in class
```

---
## \#4 Posted by: J_Dizzle Posted at: 2019-01-15T04:52:56.260Z Reads: 85

```
Wouldn’t adding an internal adapter just add unnecessary weight?
```

---
## \#5 Posted by: ZachTetra Posted at: 2019-01-15T04:54:38.908Z Reads: 81

```
Dunno...I don't have a charger or the adapter yet
```

---
## \#6 Posted by: ZachTetra Posted at: 2019-01-15T04:55:12.457Z Reads: 77

```
All I know is batteries are heavy AF and charging circuits can't be significantly heavier
```

---
## \#7 Posted by: J_Dizzle Posted at: 2019-01-15T04:58:49.264Z Reads: 72

```
Yes they can. With a 6s battery it is pretty big, why don’t you just use a bms?
```

---
## \#8 Posted by: ZachTetra Posted at: 2019-01-15T05:00:13.204Z Reads: 69

```
A BMS still needs a DC power supply right?
```

---
## \#9 Posted by: MysticalDork Posted at: 2019-01-15T05:00:26.401Z Reads: 68

```
It's a trade-off, off the same reason laptops have external power supplies: weight and space. And sometimes heat. By locating the power supply externally you leave more room for everything else (most esk8 charging solutions aren't small), and the heat generated by the charger isn't communicated to the board internals. I'd just use a waterproof DC plug on the board, (there are lots to choose from, e.g. SD13) and carry a charger with you. If you're going long distances with your board you'll probably have a bag or backpack for other stuff, so just chuck it in there.

Tldr, it's feasible but I don't know why you'd want to.
```

---
## \#10 Posted by: MysticalDork Posted at: 2019-01-15T05:01:39.828Z Reads: 66

```
Also 6s 2000mah being heavy lol try 10s 10ah. Or 20s 20Ah.
```

---
## \#11 Posted by: ZachTetra Posted at: 2019-01-15T05:01:55.275Z Reads: 63

```
How about a solar panel deck, just chain it to a bike rack in direct sun and soak up the power :laughing:
```

---
## \#12 Posted by: ZachTetra Posted at: 2019-01-15T05:03:23.923Z Reads: 61

```
I'm looking at a 12s2p 10ah...my spine hurts at the idea.  I've got a limited elastic carry strap so I wear it like a backpack...makes it feel half the weight, but I can't run
```

---
## \#13 Posted by: MysticalDork Posted at: 2019-01-15T05:06:11.890Z Reads: 58

```
Yeah, you'll be constrained for space. Just treat it like a laptop and carry an external brick. You'll also not have to deal with mains voltage inside your board.
```

---
## \#14 Posted by: ZachTetra Posted at: 2019-01-15T05:07:43.681Z Reads: 54

```
So overall a generally poor idea?  Thanks for your input guys, this is much easier than finding out the hard way!
```

---
## \#15 Posted by: MysticalDork Posted at: 2019-01-15T05:12:46.468Z Reads: 49

```
It's doable, and if you had a real need to do it, it's not too hard to do. But if it's just for "convenience" I think it'd be a pain. On both of my builds I ended up nearly running out of space and had to get creative fitting things in, and that was on a long board with no charger in it. If you're trying to fit a 12s20ah battery on a nickel board, that's a challenge in and of itself.
```

---
## \#16 Posted by: ZachTetra Posted at: 2019-01-15T05:14:14.911Z Reads: 42

```
Oh absolutely not, the big battery is for a 40" board...I was thinking 6s 2ah lipo for the nickel board
```

---
## \#17 Posted by: MysticalDork Posted at: 2019-01-15T05:16:11.882Z Reads: 44

```
You know that's gonna give you like 3 miles of range, right?
```

---
## \#18 Posted by: ZachTetra Posted at: 2019-01-15T05:17:53.242Z Reads: 45

```
There is no need to go more than 3 miles on a college campus in under 2 hours...basically I ride to class and stick it to the wall, probably hidden in my backpack, then ride it to the next class with a full battery again
```

---
## \#19 Posted by: MysticalDork Posted at: 2019-01-15T05:21:03.453Z Reads: 46

```
Fair enough. Seems more doable with those constraints, especially if you use a small (2-3A brick-style charger. I'd use a waterproof connector like SD-13, and have a detachable AC cord that plugs into that, rather than having something potentially floppy permanently attached to the board.
```

---
## \#20 Posted by: b264 Posted at: 2019-01-15T12:36:43.730Z Reads: 40

```
It's not unnecessary if you can charge it when you get to where you're going
```

---
