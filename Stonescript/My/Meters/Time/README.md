# FILE INFO

Time display utility

**Author:** IronHawk (Tom Crow)

**Version:** 3.0.0

## Features

- Displays `loc.bestTime`, `loc.averageTime`
and `totaltime` in digital format (second presition).
- Optional, frame-presition mode.
- Printing and UI modes.
- Coloring.
- UI: self managed - just call the function and
forget about it!

## Importing

### Desktop

Put this file in `Stonescript/UI` or your
directory of preference (within `Stonescript/`),
then do this:

`var t = import <YourDirectory>/Time/public`

### Mobile

Copy-Paste `./public.txt` and any dependencies
into your Mindstone.

## Usage

__Example__ - initialize the meter in `0,3` (x,y),
in red, in the `slim`, non-speedrun version, and
in the `ui` mode:

`t.main(0, 1, "#red", "slim ui")`

> *Keep in mind that the speedrunning mode needs to*
> *update constantly, which may cause some lag.*

***

## Function interfaces

### `func main(x, y, colorHex, mode)`

#### Description

Initializes and manages the times meter.

#### Parameters

- `x`, `y`: display coordinates (relative to the top left
border of the screen).
- `colorHex`: display color, in RGB hexadecimal format
(`#rrggbb`)
- `mode`: display mode.

	Valid `mode` values:

	- Primary (should go first)
		- `"normal"`, `"default"`: returns the full version
		of the Meter.
		- `"slim"`, `"small"`: returns a smaller version of
			it, containing less information.

	- Secondary
		- `"speedrun"`: displays times with frame
		presition

	- Tertiary (Should go at the end)
		- `"ui"`: makes an UI panel containing the meter.
		- `"print"`: prints the meter normally.
		- `"print ascii"`: prints the meter in ascii mode.

## CHANGELOG

- **v1.2:**
	- Now you can choose a slim version
		of the meter in all functions.
- **v1.3:**
	- showSpeedOmeterUI() renamed to "speedOmeterUI".
	- added import: UI_Maker.txt
	- speedOmeterUI now uses functions from
		the import "UI_Maker.txt".
- **v1.4:**
	- Fixed bug that prevented displaying
		the meter before the first
		second of each run.
- **v1.5:**
	- Now all functions that show the meter
		depend on speedOmeterToStr().
- **v1.6:**
	- formatSpeedrun(): now 1 digit frames
		are prefixed with a zero ('0').
	- myFormatDigital() and formatSpeedrun()
		moved to Utilities.
	- fixed tt update frequency. Now
		it updates every frame as it should.
- **v1.7:**
	- renamed all functions and variables
		containing "speedOmeter" to "som".
	- isAscii now belongs to Print() as
		one of two modes of a new parameter: isAscii.
	- uiSom() -> mkUI().
	- mkUI(): if isSlim, the panel will now be borderless.
	- ToString(): '#' replaced back with ' '.
		Now not all functions replace it again, but those who do
		delegate that task to Utilities -> replaceInStr().
- **v1.8:**
	- Renamed functions: removed "Som" from them
		to make them more concise and cohesive with
		object-oriented programming and the "new" keyword.
	- Added Import: Performance, to centralize dependencies
		and upgrade performance.
- **v1.9:**
	- Variable updates are now done in function Update().
- **v2.0:**
	- Fixed bug that messed with ui panel updates
	- Changed mode of use: now you only need to
		import and use the function "main".
	- Updates and ui components are now handled
		internally.
	- Renamed to "Times"
- **v2.1:**
	- Added dependency: UI_Maker
	- Added canUpdate().
	- Now Update() only modifies the data when called is true.
	- Update() should now only be called if canUpdate() returns true.
	- Merged isSlim and isSpeedrun with mode
	- Added error handling
	- main >> Main_Times
	- Added entry sanitization for mode
	- Upgraded Main_Times() description
	- Merged speedrun and normal (or "Digital") times into one of each.
	- u.myFormatDigital() calls replaced by time.FormatDigital()

- **v2.2:**
	- Main_Times >> main
	- Fixed flickering/vanishing bugs for the UI
	mode; now it's persistent and updates properly.

- **v3.0.0:**
  - Modularized and encapsuled private modules
  - Rearranged project files and layout.
  - Fixed ui persistence bugs.

***

Enjoy! ;)