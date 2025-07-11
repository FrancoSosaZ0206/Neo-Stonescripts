# FILE INFO

Library with my personal weapons, special stats and loadouts.

**Author:** IronHawk (Tom Crow)

## Description

This library defines tools aiming to simplify the usage of a player's items, storing upgraded/enchanted stats, and making them easily available.

> **WARNING:** this library heavily depends on the current state of your items to work properly, if not at all.
>
> It is therefore strongly advised to adapt to your save's progress before using it.
>
> Make sure you carefully read and understand it first.

## Features

- Item aliases
- Fully fledged loadout function with modes.
- Auto debuffing and dashing functions.
- Enchanted/Upgraded stats.

## Dependencies

- my combat library.
- my stats library.

## Importing

### Desktop

1. Download the script.
1. Put it into the `Stonescript` folder.
1. In your Mindstone, write:

    `var a = new MyArsenal`

### Mobile

Copy-paste the script into your Mindstone.

## Usage

**Example:** activate the Cinderwisp's devour ability when the Ignition limit is reached.

```
?foe.debuffs.string = a.maxIgnitions_Boosted
  activate cinderwisp
```

---

## GLOSSARY

### Aliases Terminology

#### Main types

- s = sword
- bs = big sword
- h = hammer
- sh = shield
- w = wand
- st = staff
- b = crossbow

#### Elements

- P = poison
- V = vigor
- A = aether
- F = fire
- I = ice
- S = stone (technically not an element, but it's counted as one for filtering purposes).

#### Archetypes

- dmg = damage (D affix)
- eff = effect (buff/debuff)
- def = defensive (A affix)
- h = hidden (staves and wands only)

#### Special types

- D = dashing
- T = towering
- C = compound
- R = repeating
- Q = quarterstaff
- B = bardiche
- HH = heavy hammer

#### Examples:

- bsIeff = **b**ig **s**word **I**ce **eff**ect (dI/Chill)
- shPdef = **sh**ield **P**oison **def**ensive
- wFh = **w**and **F**ire **h**idden (Explosive Wand)

### *"Smart Debuffing"*

It's a faster, more efficient method to debuff with ranged weapons.

It counts the amount of times a debuffing weapon is cast, instead of counting the foe's debuffs, eliminating the time it takes for the projectiles to land.

---

## Renamed Items

- **Unbroken Faith**      = `*max sword stone (enchanted: speed)`
- **Broken Faith**        = `*max sword stone (enchanted: speed)`
- **Mamba Negra**         = `*max sword poison D (enchanted: speed)`
- **Dothaneel**           = `*max sword vigor D (enchanted: speed)`
- **Void Slayer**         = `*max sword aether D (enchanted: speed)`
- **Vantum Phoenix**      = `*max sword fire D (enchanted: speed)`
- **Bifrost**             = `*max sword ice D (enchanted: speed/crit)`

- **Death's Kiss**        = `*max sword -big poison dP shiny (enchanted: speed)`
- **Soulfetcher**         = `*max sword -big vigor dL +21/ (enchanted: speed/L)`
- **Existential Crisis**  = `*max sword -big aether dU +21` (enchanted: speed)
- **Existential Dread**   = `*max sword big aether dU +21/` (enchanted: speed, unmake chance)
- **Almafuerte**          = `*max sword -big ice dI (enchanted: speed)`

- **theVwand**            = `*max wand vigor D golden`
- **Frosty Crust**        = `*max wand ice dI`

- **Subspace Bubble**     = `*max shield dashing HoH24`
- **Speedy Hammer**       = `*max hammer stone`
- **Kubikiribocho**       = `*max bardiche (enchanted: crit/damage)`
- **Mjölnir**             = `*max heavy_hammer (enchanted: damage)`
- **Guardian's Wrath**    = `*max heavy_hammer shiny (enchanted: armor fatigue)`

---

## Function Interfaces

### `func ldtF(mode)`

#### Description

Loadout function.

- Acts as a big, custom loadout command that works with item aliases.
- Handles most (if not all) situations.
- Works with the Permapot strategy.

#### Parameters

- **`mode`**

TO DO: Add ldtF() modes here.

---

Enjoy! ;)
