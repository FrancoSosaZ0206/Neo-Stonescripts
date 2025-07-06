# To Do File

---

## Glossary

- [x] = completed
- [ ] = to do
- ... = in progress

---

## To Do List

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

- [ ] Update all location scripts:
  - [x] Rocky
  - [ ] Deadwood
  - [ ] Caves
  - [ ] Mushroom
  - [ ] Halls
  - ... Mine:
    - [x] Add miniboss screens to the logic
    - [ ] Fix exploding miniboss logic:
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
    - ... update again with Rocky's latest adjustments.
  - [ ] Temple
