# Weight vs Speed: doing math for electric skateboard builds

### Replies: 6 Views: 2309

## \#1 Posted by: rafn97 Posted at: 2015-12-20T18:41:29.533Z Reads: 165

```
Is there a way to calculate (proper formuals) for checking how a weight of a person impacts the speed of the electric skateboard?
```

---
## \#2 Posted by: longhairedboy Posted at: 2015-12-21T13:48:19.495Z Reads: 142

```
This might help. I'm still trying to understand all of this myself because i'm not an engineer or a physics guru (i'm an artist), despite my family being filled with them. 

http://www.physicsclassroom.com/class/energy/Lesson-1/Power

Power = (Force * Displacement) / Time

So if you know how far you're going and how much time it took, you can use your weight as the force and figure out your wattage. 

Somebody please correct me if i'm wrong and of course please offer more detail on how to do these calculations and what units we should be using. I prefer metrics.
```

---
## \#4 Posted by: trbt555 Posted at: 2015-12-21T15:41:47.949Z Reads: 138

```
The basic physics behind this question are fairly straightforward but but I doubt you’ll find a formula
that will tell you the speed of a board that accepts the weight of the rider as an input. Perhaps some skater dude made a final thesis on this somewhere. There are just too many variables to account for such as temperature, air pressure,
rider aerodynamics, drive train configuration, bearings, wheel hardness, pavement surface roughness etc...

Here is an over-simplified view into the basics:
<img src="/uploads/db1493/original/2X/f/f9574c4bdcda98d914c97a98d00a15e7229616a6.JPG" width="605" height="500">

On flat ground the vector of your weight [W] is perpendicular (it's vertical) to the vector
of the force needed to propel you (which is parallel to the pavement, thus horizontal) and consequently has little effect on your cruising speed.

Newton's second law governs your acceleration: Force equals mass times acceleration *F=m.a*
To accelerate a mass [m] with acceleration [a] you need to exert a force F.

The force F is exerted by the Torque [M] at the wheels on the pavement. *F = M/r* where r is the radius of your wheels.
So the heavier you are, the slower you will accelerate for a given torque. Same for baking: the heavier you are the smaller the deceleration will be.
Your weight will only marginally affect your cruising speed because when you’re not accelerating, you only need to overcome drag [V] generated by the air and your drivetrain, both of which aren’t really very influenced by your weight except for the fact that heavy guys are usually bigger and will generate more wind drag and soft wheels will give more friction. But that's where all those variables come into play and where it will get very complictated very fast.

On aerodynamic drag: it's proportional to the square of your speed, so if you go twice as fast you’ll
need four times as much force to maintain that speed, once you reach it.

On hills, obviously your weight will come into play. Just ask any cyclist.

Here, one component of your weight vector will be parallel to the pavement (W.sin(α)) and will want to slow you down constantly (negative acceleration), and one will be perpendicular to the pavement and will have little to no effect, just like on flat ground.

To accelerate at the same rate as on flat ground you’ll need to exert more force: F +  W.sin(α)
To maintain constant speed you’ll not only need to constantly overcome drag V but also W.sin(α).

The steeper the hill, the worse it becomes.

@longhairedboy : work is force times displacement, but it's the force along the trajectory of movement that counts. your weight isn't along your trajectory unless you're on a hill (W.sin(α)).

Anyway, unless your an engineering student looking for an interesting thesis subject, you'd best just gather empirical data from users on the forum.
```

---
## \#5 Posted by: longhairedboy Posted at: 2015-12-21T17:03:52.716Z Reads: 116

```
Thanks for the reply @trbt555 

My approach has always been to just build it, try it out, and over engineer everything. It  has worked well so far. It seems like the deeper i go into the hole of trying to math things, the deeper the hole gets. But it does help to understand some of what's going on. 

But to oversimplify, 

If you're a big dude, get a big battery pack  and some big motors.
```

---
## \#6 Posted by: evoheyax Posted at: 2015-12-21T17:33:49.930Z Reads: 117

```
@trbt555 good job explaining this so far. To pick up on what you left on.

Torque = rFsin(θ)

- r = the radius where the torque is being applied, i.e. radius of your drive wheel attached to your wheel. (not the radius of the wheel itself)
- F = The force being applied.
- θ = the angle between the radius and the force

We can do some cool things and come up with:

Torque = mr^2α

- m = the mass of what the torque is being applied to (not the mass of yourself)
- r = the radius of the wheel torque being applied to
- α = the angular acceleration, which is defined as the change in angular velocity / the change in time. And angular velocity is defined as the change in θ (the angle) / the change in time.

With this better understanding of torque, you could come up with a formula with weight being the only variable for the perfect condition (this is what we did in my physics class often, as getting the real equations, like @trbt555 said, involves way too many variables, and is the kind of thing a physics major may do for a thesis. I am a Computer Science, so while I enjoy physics, my knowledge is still somewhat limited.)

Also, some background knowledge in vectors and free body diagrams (like what @trbt555 drew) would help you understand this a little better.

(please note: I may have made some over assumptions here: If I made any mistakes, please let me know and I will fix them)
```

---
## \#7 Posted by: trbt555 Posted at: 2015-12-21T20:01:03.124Z Reads: 105

```
You could measure your acceleration by measuring the time it takes to get to a certain speed. Knowing your mass you could calculate the force exerted and knowing that force and the distance you covered, you could calculate the work.again, knowing the time would allow you to calculate the power of your setup.

Or you could just look up your motor specs on the internet and have a beer instead. ;-)
```

---
