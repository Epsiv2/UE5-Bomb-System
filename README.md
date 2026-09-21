# 💣 UE5 Bomb System

A gameplay bomb system created in **Unreal Engine 5** as part of my Unreal Engine development training.

The project focuses on creating an interactive bomb mechanic with pickup, equipping, planting, countdown, visual feedback and explosion effects.

---

## 🎮 Features

- 💣 Bomb pickup system
- 🔢 Bomb equip / unequip
- 🖐️ Bomb held in the player's hand
- ⏱️ Planting system with a 2-second planting duration
- 🔥 5-second detonation countdown
- 💡 Blinking warning light
- 🖥️ In-world countdown display
- 💥 Explosion VFX using Niagara
- 🔊 Spatial explosion sound
- 💨 Player knockback
- 💀 Radial explosion damage
- 🛢️ Physics interaction with nearby objects
- 🎯 Explosion radius and falloff

---

## 🛠️ Technologies

- **Unreal Engine 5**
- **Blueprints**
- **Enhanced Input**
- **Niagara**
- **UMG / Widget Components**
- **Physics**
- **Line Traces**
- **Collision & Overlap Detection**
- **Timers**

---

## ⚙️ How It Works

### 1. Pickup

The player can interact with the bomb using the interaction input.

A line trace checks whether the player is looking at a bomb.  
If the bomb can be picked up, it is stored in the player's inventory.

### 2. Equip

The bomb can be equipped and unequipped using the assigned input.

When equipped, the bomb is attached to a dedicated hand position on the player.

### 3. Plant

Holding the plant input starts a **3-second planting timer**.

Releasing the input before the timer finishes cancels the planting process.

After successful planting, the bomb is placed on the ground and the detonation sequence begins.

### 4. Countdown

The bomb starts a **5-second countdown**.

During the countdown:

- the warning light blinks
- the timer is updated every second
- the remaining time is displayed on the bomb

### 5. Explosion

When the countdown reaches zero, the bomb explodes.

The explosion:

- plays a spatial sound
- spawns a Niagara explosion effect
- applies radial damage
- launches the player away from the explosion
- applies radial impulse to nearby physics objects
- destroys the bomb actor

---

## 🎥 Demo

The project includes a gameplay demonstration showing the complete bomb mechanic.

**Gameplay video:**

`bomb-demo.mp4`

---

## 🧩 Blueprint Overview

The main systems used in the project include:

### BP_Bomb
Handles:

- pickup state
- bomb holder
- planting
- timers
- countdown
- blinking light
- explosion
- radial damage
- physics impulse

### BP_FirstPersonCharacter
Handles:

- bomb interaction
- pickup
- equip / unequip
- planting input
- held bomb reference

### WBP_BombDisplay
Handles the countdown displayed directly on the bomb.

### Enhanced Input
Used to control:

- bomb interaction
- equip / unequip
- bomb planting

---

## 📸 Project Screenshots

Blueprint screenshots and project documentation are available in the `Media` folder inside `Blueprints`.

---

## 🎯 What I Learned

This project helped me practice:

- gameplay programming with Blueprints
- working with Enhanced Input
- timers and event-driven gameplay
- actor references and communication between Blueprints
- line traces
- collision handling
- UMG widgets
- Niagara effects
- physics interaction
- radial damage and impulses
- combining multiple gameplay systems into one mechanic

---

## 📚 Project Purpose

This project was created as part of my Unreal Engine development training and was designed to practice building a complete gameplay mechanic from start to finish.
