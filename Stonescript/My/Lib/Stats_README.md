# FILE INFO

Stats library

**Author:** IronHawk (Tom Crow)

## Description

This library contains a pack of stats from the
game, as well as querie functions to consult
and reference.

It's static, so updates in-game won't be
reflected here. It is therefore advised to
keep values updated.

## Features

// TODO

## Importing

### Desktop

Put this file in `Stonescript/UI` or your
directory of preference (inside `Stonescript`),
then do this:

`var s = import <YourDirectory>/Stats`

### Mobile

Copy-paste this script and any dependencies
into your Mindstone.

## Usage

Example - // TODO

// TODO

---

Enjoy! ;)

---

# More info about stats

## Hitbox and Splash Area

Source [here](https://discord.com/channels/423242655498240000/609453573113249924/1283482516287918153).

### Hitbox + Splash table

> So here are the main hitboxes, with slashes ('/')
> showing splash area to the right vs odd-width foe.
> 
> All hitbox widths are odd unless it says even,
> which means splash rounds down while main hit
> rounds up.

```
000000000111111111 |                DESCRIPTION                | PAR
123456789012345678 |                                           | ITY
-------------------|-------------------------------------------|------
..bbbbbBbbbbb////. | bardiche, bfg                             | 
...sssSsss/....... | skeleton arm (has 1 aoeX)                 | 
..ccCcc////....... | basic crossbow left                       | 
...ccCcc////...... | basic crossbow right                      | 
....ccCcc////..... | heavy crossbows (all), heavy hammer       | 
..ssSss///........ | sword left, staff melee, hammer left      | even
...ssSss///....... | sword right, big sword left, hammer right | even
....ssSss///...... | big sword right                           | even
..wWw////......... | wand left, torch left, harmonic           | 
...rRr////........ | runestone left, runestone right           | 
....wWw////....... | wand right, staff magic, torch right      | 
G////............. | grappling                                 | 
tTt////........... | stone throw left                          | 
.tTt////.......... | stone throw right                         | 
..pPp////......... | punch, kick                               | 
.hhhHhhh////...... | hatchet (has 5 aoeX)                      | even
.ssSss///......... | shovel                                    | even
....ffffffffffffff | fissure left (up to 63)                   | even
......ffffffffffff | fissure right (up to 65)                  | even
```

### How it works:

> The top row of the table is distance to the enemy
> and the letters are where that hitbox will hit.
> For example, bardiche will hit an enemy at
> distance 12, but not 13.
> 
> Enemies have their own collision width extending to
> the right, which is why you don't miss when
> swinging at dist 1.
> 
> When a projectile hits the first enemy, it
> splashes and hits the rest, using a different
> calculation:
> 
> For most projectiles, it grows the projectile
> hitbox by 4 units on both sides, 2 units vertically
> (to the area shown with slashes), but there is a
> bug that will shift the enemy hitbox left by half
> their collision width with the splash collision
> detection, so actually you get +1 range on top of
> this if the enemy is 3-wide, +2 if its 5-wide, etc.
> 
> I don't recall how even enemy widths round, it might
> depend if the projectile hitbox is even or odd, [...].

Source [here](https://discord.com/channels/423242655498240000/609453573113249924/1378196531706073178).

## Engaging info

### Conditions

> You get the armor when the enemy goes to state 2, [...] Maybe check how many foes there are and how much armor you gained, and do some math to check whether you got all? Idk.

Source [here](https://discord.com/channels/423242655498240000/597668520888762388/1242108255178592339).

### Engage ranges

###### By Ket

Related files are downloaded in `Stonescript/Borrowed/`:

- **`wakeupTimes.txt`**
- **`wakeupStats.txt`**

Source [here](https://discord.com/channels/423242655498240000/609453573113249924/1198026098143932546).
