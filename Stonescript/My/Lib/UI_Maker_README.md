# UI functions library

**Author:** IronHawk (Tom Crow)

## Description

This library offers a simple way to help make
UI component creation more concise and
straightforward.

All functions are one-liners!

> _**WARNING** -- functions can lead to crashes,_
> _errors or undefined behavior if misused. Please_
> _read their interfaces, making sure you understand_
> _how to use them._
>
> _For reference, [consult the manual](https://stonestoryrpg.com/stonescript/manual.html#user-interface)._

## Importing

### Desktop

`var uimkr = new UI_Maker`

### Mobile

Paste the file's text into the Mindstone.

## Usage

**Example** - returns a button with these properties:
- *location:* 1, 10 (x, y),
- *width, height:* 12, 5,
- *anchor:* top_center,
- *dock:* top_left,
- *text:* "Phrases!",
- *color:* red,
- *text color:* yellow,
- *border color:* magenta,
- *highlight color (when pressing):* rainbow,
- *border style:* 2,
- *while pressed:* call function "iLike"
- *before pressed:* call function "greetings"
- *after pressed:* call function "goodbye"
- *sound played when pressed:* buy

```c#
func greeting()
    >c0,-1,#red,Hello world!
func iLike()
    >c0,0,#yellow,I like trees .-.
func goodbye()
    >c0,1,#green,Goodbye world!

var button = uimkr.mkButton(1,10,12,5,
^            top_center,top_left,
^            "Phrases!",
^            #red,#yellow,#magenta,#rainbow,
^            2,
^            iLike,greetings,goodbye,
^            buy)
```

# GLOSSARY

Shared parameters between functions and their definitions:

- x: horizontal position (relative to dock)
- y: vertical position (relative to dock)

- w: width
- h: height

- anchor: position relative to the screen
- dock: position relative to parent UI component

- colorHex: color in hexadecimal (hex) format
- style: numeric ID used for drawing rectangular
        Components such as Panels and Buttons (range
        from -8 to 8)


Optional properties/parameters:

send 0 if you don't want to use them.
The default value will be used instead.

***

# Interfaces

## `func destroy(component)`

Recycles and nullifyes an UI component.

## `func mkPanel(x,y,w,h, anchor,dock, colorHex, style, child)`

Makes a panel component.

### Parameters

#### Common

- x
- y
- anchor
- dock

#### Optional

- w
- h
- colorHex = color of the panel.
- style
- child = initial child component to add.

## `func mkTextbox(x,y,w,h, anchor,dock, text, align, colorHex)`

Makes a textbox component.

### Parameters

#### Common

- x
- y
- anchor
- dock
  
#### Special

- text = textbox contents.
- align = text justification/alignment inside the textbox.
        Default: "left"
  
#### Optional
- w
- h
- colorHex = textbox color

## `func mkButton(x,y,w,h, anchor,dock, text, colorHex,colorT,colorB,colorH, style, pressedFunc,downFunc,upFunc, soundFx)`

Makes a button component.

### Parameters

#### Common

- x
- y
- anchor
- dock

#### Special

- text = button text
- colorHex = general color of the button (colors below override it)
- pressedFunc = function that the button will perform when pressedFunc

#### Optional

- w
- h
- colorT   = text color
- colorB   = border color
- colorH   = highlight color (when pressedFunc)
- downFunc   = function that the button will perform when press begins
- upFunc     = function that the button will perform when press ends
- soundFx  = sound effect when pressedFunc
  
***

Enjoy! ;)
