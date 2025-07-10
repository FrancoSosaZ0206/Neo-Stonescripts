# To Do File

---

## Glossary

- [x] = completed
- [ ] = to do
- ... = in progress

---

## To Do List

- [ ] Ranged_Debuffing/private: at `track()`, fix tracker removal conditions so it only removes it when the stack count is equal to the max stack. Otherwise, when the set is removed, `canDebuff()` will look for current stack count only, ignoring travelling projectiles.
- [ ] Update Times meter:
  - [ ] display in **table format**.
  - [ ] display previous `n` times:
    - [ ] save previous `n` times to storage.
  - [ ] **color code** based on better/worse/same time.
  - [ ] **hide toggle**
  - [ ] **time format toggle**. Formats:
    - [ ] format digital (with frames)
    - [ ] Raw frames (as most speedrunners use it)
  - [ ] implement **partial times**/**checkpoints**

- [x] Arsenal:
  - [x] fix smartDebuff not working properly.

- [ ] Update all location scripts:
  - [ ] Rocky
    - [ ] Fix permapot not activating
    - [ ] update again with latest adjustments.
  - [ ] Deadwood
  - [ ] Caves
  - [ ] Mushroom
  - [ ] Halls
  - ... Mine:
    - [x] Add miniboss screens to the logic
    - [x] Fix exploding miniboss logic:
      - [ ] Make the `Eternity Staff` ability activation conditions more consistent (based on states?)
    - [x] Change permapot activation logic so that it only activates only after the potion is consumed
    - [x] BFG DS:
      - [x] Replace boss_screen as max screen with the last screen of `loc.id = "bronze_mine"` (in every difficulty)
    - [x] finish updating boss logic:
      - [x] add ranged fight section to `fight()` or at the boss logic section itself.
    - [x] recopilate boss screens and add them to the boss_screen assignment section.
    - [x] Test!
      - [x] does the *Explosive Wand*'s ability work against Enfused elites?
  - [ ] Ridge:
    - ... update again with latest adjustments.
  - [ ] Temple
