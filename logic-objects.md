# Logic Objects
There are many different tools called "Logic Objects" in Escape Simulator that enable you to do special things in your room that would otherwise be difficult or impossible.

## Physical
### Transparent

A transparent plane that supports full and partial transparency.

####  Common uses for a transparent
1. It can be used anywhere you'd normally use a "Plane" shape
1. It can create text to overlay on top of objects, or to create floating text by replacing the texture
1. It can be used to make an object face a different way in zoomables, inventory, and placement without having another object visible

<img src="https://user-images.githubusercontent.com/2043673/193335450-e88304ea-2aab-417b-af9e-f2a2a2dc1751.png" width="700">

--- 

### Transparent (Double-sided)

A transparent plane that supports full and partial transparency, but is also visible from the back side (unlike a plane or a transparent)

####  Common uses for a double-sided transparent
1. It can be used to create double-sided notes or pages
1. It can be used anywhere you'd normally use a single-sided transparent or Plane

<img src="https://user-images.githubusercontent.com/2043673/193336177-f7f6d7fc-c0da-4799-b78a-62844faed868.png" width="700">

--- 

### Obstacle

An invisible barrier that can prevent the player from walking in its space.

#### Common uses for an obstacle prop
1. When you want to stop a player from going somewhere they may get stuck at if they go there
1. It can be used to stop a player temporarily from entering a space when used in combination with an activator or an animation

<img src="https://user-images.githubusercontent.com/2043673/193336378-7b9d61fd-ca48-4877-abf5-4f1c5a323b13.png" width="700">

---

### Collider

An invisible barrier that will stop items and clicks from going through an area, but by default, not the player.

#### Common uses for a collider prop
1. Can be used to create a new "hit box" for a custom model
1. Can be used to create a new "hit box" for something that has had its collider disabled
3. Can be used to prevent someone from interacting with a button or slot

<img src="https://user-images.githubusercontent.com/2043673/193336543-8cb35b06-c705-443a-af5b-8af2ca8c15c2.png" width="700">

--- 

## Tools
### Empty

An object without any physical properties.

<img src="https://user-images.githubusercontent.com/2043673/193335381-a0a2d8a8-76f0-44af-a78a-fddfd4bf4f3b.png" width="700">

#### Common uses for an empty
1. Used as a parent for other objects to allow you to:
    - Move all the children at once
    - Organize items into groups
    - Act as an inbetween to prevent scaling issues
1. It can be animated to:
    - Be used as a timer
    - Move child objects
    - Stack animations since objects can only store one animation
 
 ---

### Visibility Activator

A logic object that when sent a "1" as an input will hide or show some target object(s), disable or enable their colliders, or disable their renderer.

#### Common uses for a visibility activator

1. Used to hide an object until after a lock is unlocked or a puzzle is solved
1. Used to hide effects until you want to display them later
1. Used to hide many objects to keep performance higher in an area a player has not yet explored
1. Used to disable the collider of an object so that everything will pass through it
2. Used to make a player drop an item

To trigger a Visibility Activator, target it with a Button, an Animation, Locks or other logic objects. 

"Gotchas": 
- Disabling a property of an object while it is in a player inventory or in a slot will make the player drop the prop on the player's current location and disable the Targeted properties of the prop.
- If none of the Targeting checkmarks are checked the Activator Component goes through the list of Targeting Objects but does nothing to the objects. 

<img src="https://user-images.githubusercontent.com/2043673/193336635-b2a0dadc-1244-4197-8923-6da8d2663bb2.png" width="700">

---

### Lock
Locks are a logic object that, when sent its configured password, will "unlock" and can send an output to another logic object or other objects with specific "Behavior" <!-- TODO: Set a link to behaviors page --> properties set. Locks are used to trigger events when certain requirements are met.

#### Common uses for a lock
1. Used to make a lock in game have actual functionality
2. To trigger an animation when something specific happens
3. To make a display show something
4. To trigger the finish/victory screen

Locks accept input from Dials, Turnables, Buttons, Slots, Triggers and OTHER LOCKS

<img src="https://user-images.githubusercontent.com/2043673/193336705-26e33b39-45cc-4461-802e-4f0e1376e59c.png" width="700">

### Slot
Slots are used to create a location that an item can be inserted into. When the "correct" item is inserted it will send an output to another logic object or other objects with specific "Behavior" <!-- TODO: Set a link to behaviors page --> properties set.

#### Common uses for a slot
1. Creating a keyhole that will trigger an animation or lock
2. To allow someone to place an item in a specific place

"Gotchas":
- Remember if you make a "door lock" to parent the slot to the door, so that it will move with the door when it opens, or else you will end up with floating keys!
- Slots can only be occupied by one item at a time.

<img src="https://user-images.githubusercontent.com/2043673/193336832-8f8b8b03-ee8a-4cea-99b2-88d6fb14f00f.png" width="700">

---

### Script
![image](https://user-images.githubusercontent.com/2043673/193336906-9b235305-7af5-4ded-8fb7-3c68670cc9e4.png)

### Trigger
![image](https://user-images.githubusercontent.com/2043673/193336996-c8284a66-ca93-448b-9651-365cd3dd4d3e.png)

### Open Link
![image](https://user-images.githubusercontent.com/2043673/193337090-1fdb77df-912b-4797-8808-f8ca1e9cabec.png)

## Visuals and Effects
### Fog
![image](https://user-images.githubusercontent.com/2043673/193337155-9bf87a45-c4a6-4701-a55c-04675d73df5d.png)

### Light
![image](https://user-images.githubusercontent.com/2043673/193337266-37f93ddf-c5e8-40f0-87d8-857056a57e57.png)

### Sky Box
![image](https://user-images.githubusercontent.com/2043673/193337339-ef0ab9d1-eccd-427d-93ad-d0af70383d84.png)

### Sound
![image](https://user-images.githubusercontent.com/2043673/193337395-d6795eea-ecf7-4922-b8f1-a225f9fd1706.png)

### Display
![image](https://user-images.githubusercontent.com/2043673/193337470-1df89d2f-1c79-49fc-9595-b9e7086ffb18.png)

### Post-Processing
![image](https://user-images.githubusercontent.com/2043673/193337544-f89a20df-d497-46e4-a05d-622365c3b145.png)

## Events
### Spawn Point
![image](https://user-images.githubusercontent.com/2043673/193337657-62e5c95f-acf0-49ba-b319-35c0b395a08d.png)

### Teleport
![image](https://user-images.githubusercontent.com/2043673/193337732-10ba970c-ae01-4dc0-83cc-5cc55f95e8cf.png)

### Finish
![image](https://user-images.githubusercontent.com/2043673/193337781-bba52757-a774-415e-a30d-0b994dbf40ec.png)


## Index
- [Collider](https://github.com/xviable/escape-sim-room-editor-docs/blob/main/logic-objects.md#collider)
- [Display](https://github.com/xviable/escape-sim-room-editor-docs/blob/main/logic-objects.md#display)
- [Empty](https://github.com/xviable/escape-sim-room-editor-docs/blob/main/logic-objects.md#empty)
- [Finish](https://github.com/xviable/escape-sim-room-editor-docs/blob/main/logic-objects.md#finish)
- [Fog](https://github.com/xviable/escape-sim-room-editor-docs/blob/main/logic-objects.md#fog)
- [Light](https://github.com/xviable/escape-sim-room-editor-docs/blob/main/logic-objects.md#light)
- [Lock](https://github.com/xviable/escape-sim-room-editor-docs/blob/main/logic-objects.md#lock)
- [Obstacle](https://github.com/xviable/escape-sim-room-editor-docs/blob/main/logic-objects.md#obstacle)
- [Open Link](https://github.com/xviable/escape-sim-room-editor-docs/blob/main/logic-objects.md#open-link)
- [Post-Processing](https://github.com/xviable/escape-sim-room-editor-docs/blob/main/logic-objects.md#post-processing)
- [Script](https://github.com/xviable/escape-sim-room-editor-docs/blob/main/logic-objects.md#script)
- [Sky Box](https://github.com/xviable/escape-sim-room-editor-docs/blob/main/logic-objects.md#sky-box)
- [Slot](https://github.com/xviable/escape-sim-room-editor-docs/blob/main/logic-objects.md#slot)
- [Sound](https://github.com/xviable/escape-sim-room-editor-docs/blob/main/logic-objects.md#sound)
- [Spawn Point](https://github.com/xviable/escape-sim-room-editor-docs/blob/main/logic-objects.md#spawn)
- [Teleport](https://github.com/xviable/escape-sim-room-editor-docs/blob/main/logic-objects.md#teleport)
- [Transparent](https://github.com/xviable/escape-sim-room-editor-docs/blob/main/logic-objects.md#transparent)
- [Transparent (Double-Sided)](https://github.com/xviable/escape-sim-room-editor-docs/blob/main/logic-objects.md#transparent-double-sided)
- [Trigger](https://github.com/xviable/escape-sim-room-editor-docs/blob/main/logic-objects.md#trigger)
- [Visibility Activator](https://github.com/xviable/escape-sim-room-editor-docs/blob/main/logic-objects.md#activator)
