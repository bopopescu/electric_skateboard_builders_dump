# Using reverse torque to brake

### Replies: 11 Views: 1254

## \#1 Posted by: TSG_AU Posted at: 2017-06-23T22:33:46.353Z Reads: 147

```
Can you just used reverse torque to brake when going down a hill with a full battery?
```

---
## \#2 Posted by: rpn314 Posted at: 2017-06-23T22:53:29.669Z Reads: 143

```
Can you explain what you mean by reverse torque? and maybe some background to this question? I'll take a stab and try and guess what you're getting at anyways:

My rough understanding of induction motors says that when you're braking electrically (ie not using a disk brake or some sort of physical friction on the stator) the controller forces the synchronous speed to be less than the motor speed and so the motor magnetic field starts to lag behind the field generated by the motion itself. This pushes the motor to rotate in the direction opposite to it's current rotation, thus producing braking. This by necessity then produces current in the opposite direction and that energy has to go somewhere. In our case, we can put most of that energy back into the batteries (which I'm sure you know can actually store some amount of energy). 

If the battery is already full, we have system in place to ensure the batteries don't get more energy than they can handle safely (ie not explode). VESCs know what the voltage of the battery is and can limit the amount going to the battery, and can cut things off if it gets over a certain point (ie Max Voltage in BLDC-Tool); BMS's do similar things. If that power can't go into the battery, then it either needs to stop being generated or it needs to be burned off by a resistor and turned into heat.
```

---
## \#3 Posted by: TSG_AU Posted at: 2017-06-23T23:58:13.488Z Reads: 123

```
My understanding of induction motors isn't that great, basically what I was trying to figure out was if you could generate a rotating magnetic field in the complete opposite direction direction to the rotor magnetic field, and have the interaction of the two slow the motor down. My understanding of motors falls apart here though, as where does the excess energy go, if not directly into heating the motor?
So what you're saying is that if you attempt to do that, the induced emf in the stator coils due to the rotor's field is such that it will always force current back into the battery (under braking)? It's not possible to be actively driving the stator coils with net current out of the battery to slow the motor down?
```

---
## \#4 Posted by: rpn314 Posted at: 2017-06-24T01:18:07.572Z Reads: 107

```
I was going on the assumption that the energy would go back to the speed controller. At that point the magnetic field in the motor is essentially being forced to pushed things in the direction such that energy being produced by the motor already rotating is greater than the magnetic field it's being pushed to and thus it would have to route it somewhere. 

I suppose heating the motor may be an option, by just not allowing it to flow backwards into the controller, but I think it's a terrible option. We have enough heat loss as is in the motor. Doing it on purpose I think will frankly melt them (at least the wires inside)
```

---
## \#5 Posted by: BigBoyToys Posted at: 2017-06-24T03:54:47.186Z Reads: 81

```
This sounds like the regen current setting vs the Motor Amp min setting in the vesc.

I believe running the motor in reverse while moving forward would consume energy not generate it.

Can one of our local experts comment on this?
```

---
## \#6 Posted by: rpn314 Posted at: 2017-06-24T05:59:59.517Z Reads: 74

```
[quote="BigBoyToys, post:5, topic:26021"]
I believe running the motor in reverse while moving forward would consume energy not generate it.
[/quote]

If it actually switches directions, yes, you'd be consuming energy. But if the motor is still moving forward and the speed controller is slowing it down, that is regen braking.
```

---
## \#7 Posted by: TSG_AU Posted at: 2017-06-24T06:28:50.821Z Reads: 66

```
So where could the energy output in the system be, if you've got electrical energy coming in from the battery as well as kinetic energy coming in from slowing down? As heat in the motor?
```

---
## \#8 Posted by: rpn314 Posted at: 2017-06-24T06:30:22.499Z Reads: 62

```
Well that's the point of regen braking. Energy is going to the battery instead of coming from it.
```

---
## \#9 Posted by: BigBoyToys Posted at: 2017-06-24T06:41:47.212Z Reads: 60

```
I was under the impression that if region current is set to 0 in the B LDC tool no regenerative current would be transferred to the battery , is this an incorrect assumption? 

Most Other ESCs don't even have regenerative braking
```

---
## \#10 Posted by: TSG_AU Posted at: 2017-06-24T06:48:17.229Z Reads: 63

```
Ah my bad, I thought when you said "If it actually switches directions" you meant that if the controller switched into reverse mode, when you actually meant that if the motor actually started spinning the reverse direction
```

---
## \#11 Posted by: rpn314 Posted at: 2017-06-24T14:02:17.490Z Reads: 47

```
[quote="TSG_AU, post:10, topic:26021, full:true"]
Ah my bad, I thought when you said "If it actually switches directions" you meant that if the controller switched into reverse mode, when you actually meant that if the motor actually started spinning the reverse direction
[/quote]


Oh yeah, sorry that wasn't clear. So many things are switching around I probably got a little lost! :sweat_smile:

[quote="BigBoyToys, post:9, topic:26021"]
I was under the impression that if region current is set to 0 in the B LDC tool no regenerative current would be transferred to the battery , is this an incorrect assumption?
[/quote]

You're correct, however the VESC does not have any method to brake other than regenerative. If you turn "Motor min" or "Battery Min" to zero, you get no braking whatsoever.

[quote="BigBoyToys, post:9, topic:26021"]
Most Other ESCs don't even have regenerative braking
[/quote]

I frankly am not as familiar with other ESC's. If they don't have regenerative braking, they probably have a set of resistors that burn that power coming back in from the motor themselves instead of sending it to the battery
```

---
