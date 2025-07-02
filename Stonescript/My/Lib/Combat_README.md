# FILE INFO

Combat functions library

**Author:** IronHawk (Tom Crow)

## Description

This library provides some game-related functions to make the ask of doing a farming script easier.

## Features

- Community known speedrun strategies and tools, incapsulated in functions.
- Ability function checks.
- Min-maxing functions.
- Fully automatic double-screen ability managers -- just imput the target screens and let it work its magic!

## Dependencies

- my utilities library.
- my stats library.

## Importing

### Desktop

1. Download the script.
1. Put it into the `Stonescript` folder.
1. In your Mindstone, write:

    `var c = new Combat`

### Mobile

Copy-paste the script into your Mindstone.

## Usage

**Example:** check if the Blade of the Fallen God can be activated and use it.

```
?c.canUseAbility("blade")
  c.useAbility_TH("blade", "blade")
```

> Tip: Some variables require being updated. Call `c.Init()` at the top of your script if you're gonna use them.

---

## Function Interfaces

### `func canUseAbility(abilityID)`

#### Description

Returns true if a given weapon's special ability can be activated.

#### Parameters

- **`abilityID`:** the ability's internal identifier (ID).

  Valid `abilityID` values:

  - `blade`: Blade of the Fallen God
  - `mask`: Cultist Mask
  - `arm`: Skeleton Arm. **Requires gaining at least 1 pick pocket buff.**
  - `bash`: Bashing Shield
  - `dash`: Dashing Shield
  - `bardiche`
  - `heavy_hammer`
  - `quarterstaff`
  - `mind`: Mindstone
  - `hatchet`
  - `voidweaver`: Aether Talisman's summon
  - `cinderwisp`: Fire Talisman's summon
  - `staff + <name>`, `staff + <element>`: Hidden staves
  - `wand + <name>`, `wand + <element>`: Hidden wands
  - `<element>_talisman`: Talismans

### `func useAbility_TH(abilityID, itemName)`

#### Description

Activates a two-handed item's ability.

#### Parameters

- **`abilityID`:** the ability's internal identifier (ID).

  Valid abilityID values:

  - `blade`: Blade of the Fallen God
  - `arm`: Skeleton Arm
  - `bardiche`
  - `heavy + hammer`: Heavy Hammer
  - `quarterstaff`
  - `staff + <element> + hidden`: Hidden staves

- **`itemName`**: your item to activate.

### `func useAbility_OH(abilityID, itemName, hand)`

#### Description

Activates a one-handed item's ability.

#### Parameters

- **`abilityID`:** the ability's internal identifier (ID).

  Valid abilityID values:

  - `hatchet`
  - `mask`: Cultist Mask
  - `<element> + talisman`: Talismans
  - `wand <element> + hidden`: Hidden wands

- **`itemName`:** your item to activate.

### `func isEquipped(itemName)`

#### Description

Returns true if a given item is equipped.

### `func isCasting(itemName)`

#### Description

Returns true if an attack is being casted.

### `func canUseAbility_DS(itemName)`

#### Description

Checks if a weapon ability can be used in 2 screens
of distance, according to a certain screen index.

### `func canSummon(summonName)`

#### Description

Checks if a summon can be invoked by its respective talisman.

### `func canHide(summonName)`

Checks if a summon can be hidden by its respective talisman.

### `func devour(summonName)`

#### Description

Activates a summon's "Devour" ability.

#### Parameters

- **`summonName`**: the name of the summon.

  Valid summonName values:

  - `voidweaver`
  - `cinderwisp`

### `func canUnmakeVoidweaver()`

#### Description

Checks if the Voidweaver's devour ability
will successfully unmake a foe.

### `func canKillCinderwisp(cinderwispDmg, margin)`

#### Description

Checks if the cinderwisp's "devour" ability damage
will kill the foe.

#### Parameters

  - **`cinderwispDmg`**: damage dealt by cinderwisp for each ignition.

  - **`margin`**: number representing a health margin to add to the remaining foe's health. This is necessary because the ability has a cast time that will alter the estimations done here. Send 0 if you don't want to use a margin.

### `func isCinderwispCap(ignitions_cap)`

#### Description

Checks if the maximum amount of ignition debuffs have been applied to a certain foe.

#### Parameters

- **`ignitions_cap`**: maximum number of ignition debuffs that can be applied. Varies on upgrade level or boosted stat.

### `func canEngage()`

#### Description

Returns true if the player is engaging in a fight.

This enables the player to benefit from effects
that are applied when engaging, like ai or A/a
affix items.

### `func moonjuggle(weapon1, weapon2)`

#### Description

Moonjuggling is a trick that boosts dps with 2 swords whose attack speed stat is maxed out (+21 enchantment).

Requires **AAC** (Attack Animation Cancelling).

It's a cycle that repeats every 3 frames:
  - In the first 2, the *Moondial Stone* is held with each sword, boosting their attack speed even further.
  - In the last one, both swords are held to spend the cooldown frame in a single frame.

### `func burst(weaponsArr)`

#### Description

Moonjuggling variant, aka Bursting.
Requires a minimum of 2 swords to cycle through.
Works with an unlimited number of swords

#### Parameters

- **`weaponsArr`**: array with all the swords to use. Every sword must have a +21 enchanted boosting its attack speed stat.

#### Usage example

```
burst([sword fire *max +21,
^      sword ice *max +21,
^      sword poison *max +21,
^      sword vigor *max +21,
^      sword aether *max +21])
```

### `func AAC(itemLeft, itemRight)`

#### Description

**AAC** = _**A**ttack **A**nimation **C**ancelling_

Widely used trick to enable a massive attack speed boost.

It works by skipping the "perf" state of an item, interrupting it by switching to another item momentarily.

### `func canSmoothCast(is1f)`

#### Description

Smooth Casting is a trick where you hold the triskelion stone every certain amount of frames to enable walking while dealing damage.

Requires berserk potion or a 1 frame cast, ranged item, such as the Repeating Crossbow or a Socketed Staff with a +21 attack speed enchantment.

### `func canKbFarm()`

#### Description

Checks if the player can use "Knockback Farming", a strategy where you can walk while damaging and pushing back foes, minimizing the time the stonehead is still.

Requires Smooth Casting.

### `func canStutterStep()`

#### Description

Stutterstepping is a technique that enables walking with the Triskelion Stone while inside its attack range (where the player would normally stop to attack) to walk faster.

---

Enjoy! ;)
