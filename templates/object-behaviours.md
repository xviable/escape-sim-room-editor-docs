> [Object Behaviours](https://github.com/xviable/escape-sim-room-editor-docs/wiki/Object-Behaviours) > **Item Name**

---

# Item Name
Animations are the heart and soul of every good room. Not only will they make it seem more alive, but they are also used in a multitude of workarounds! So keep on reading, even if you think you know your way around animations already.

### Properties

EDIT WAYPOINT
Used to set the end-point of an animation.

DURATION
Shows the seconds which it will take the animation to go from start to end-point. An animation with 0 seconds duration will instantly teleport the object.

OUTPUT VALUE
This number will be sent out to locks that are linked to the animation ON COMPLETE.

INTERPOLATION
SMOOTH or LINEAR. Smooth gives an animation a more natural look, by changing speed at the beginning and end of the animation. Linear will make the animation move at a constant speed.

BOUNCE
This will make the animation animate backwards after it completed its path.

LOOP
This will keep the animation playing once triggered. If bounced, it will move back and forth. If not bounced, the item will teleport to its original position and then repeat the animation.

AUTOPLAY
The animation is triggered as soon as the level is started. Most useful in combination with "loop" for ambience animations.

DELAY
It will take so many seconds before the animations starts playing, when the animated object is activated for the first time. If the object is activated again, it will not be delayed again! This is sad and I hope it gets fixed.

PICKABLE
This allows you to make an animated item also be a pickable. Often it is needed to make pickable items be animated even when they are not intended to move in any way! More on that a bit further down in the tips.

ON COMPLETE
The items/actions that get triggered after the animation reached its endpoint. If connected to a lock the animation will send a "1" on complete and a "0" on complete of the reverse animation.

### Helpful Tips

IMPORTANT: You cannot make animations be keys to a slot. So make the item pickable, assign it as key, and THEN make it an animation with "pickable" checked. This way it works, cause the item carries over its key properties.

0 Seconds animations can be used to swap objects seamlessly! This can be useful if you want a Button to first not work but later open something, for example.

Animations do not obey physics, but will move with their "parent" and act like a static in game. This is why they will help you when your key will not stay in the drawer because of physical obstacles. Or of you want to plaster apickable item to a pickable, or to the wall, or to a moving painting, etc.
Just link the key to the intended slot, animate a key, tick the pickable box, do not give it an animation path and place it on the wall. It will stick to it until your player picks it up!

Under some circumstances the item types will carry over to the animation status. E.g. of you have a crate and the lid is pickable and then you set it to be an animation, it will cause no issues if the chest is static or draggable. But it will cause problems in your inventory! Looking at a small chest with an animated lid (even with pickable unchecked) can allow the lid to simply be picked off, since the former "pickable" status carries over. To fix this issue make the lid not be an animation, set it to "static" and then make it an animation again.

Animations can be used as timers! Just place an Empty, make it an animation (no path setting needed) and let the animation take 30 seconds. You now have a 30 seconds timer for things you set to happen "on completion" of it. If you set it on loop, you have a timer that gives out an activation signal every 30 seconds.

Do not make looped animated objects be pickables. Once you force an object to be loop animated in inventory it freezes you in examine mode.

If an animated pickable is triggered while in inventory, nothing happens. If you put it back on the floor, it will be able to run its animation, if activated.

