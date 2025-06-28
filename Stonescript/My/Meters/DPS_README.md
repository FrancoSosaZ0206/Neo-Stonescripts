# FILE INFO

Damage-per-second display utility

**Author:** Pikarizard Charikachu xD

**Modified by:** IronHawk (Tom Crow)

**Version:** v2.2

## Description

Displays various stats to help you in
min-maxing your damage output. Only
works on bosses. Also coded so that it
only records stats the moment you
damage bosses. Neat right?

## Importing

### Desktop

Put this file in `Stonescript/UI` or your
directory of preference (inside Stonescript),
then do this:

`var dps_meter = import <YourDirectory>/DPS`

### Mobile

Copy-paste this script and any dependencies
into your Mindstone.

## Usage

__Example__ - initialize the meter in `0,3` (x,y),
in yellow, refreshing every 7 frames, in the
`slim`, `ui` mode:

`dps_meter.Main_DPS(0,3,"#yellow", 7, "slim ui")`

## CHANGELOG

- v1.1:
  - Removed unnecessary information
    from the print command.
  - Changed variable names for
    major clarity.
  - Added commentary explaining some
    of the process.
- v1.2:
  - Changed display mode to functional.
    Now, to print the data, you need
    to call a function.
- v1.3:
  - Changed file name:
    DPS Checker >>> DPS Meter.
- v1.4:
  - Added UI and toString style functions.
- v1.5:
  - Added "DPSMeterEnabled" global variable:
    Now, to enable the functions and procedure,
    this variable has to be set to [true].
- v1.6:
  - changed dpsMeterUpdate() to public.
  - uiDPSMeter() and dpsMeterUpdate() have
    a new "mode" parameter, allowing to display
    less information in a slim design if desired.
- v1.7:
  - minor bug fixes and improvements.
- v1.8:
  - Renamed all functions and variables:
    "DPSmeter" -> "dpsm".
  - Added new variable: dpsmRefresh, which
    is used to control the refresh rate of
    the meter's UI panel.
  - uiDPSMeter() -> mkDpsmUI().
  - removed "dps_" from some variable names.
  - dpsmUpdate(): now it doesn't depend on changes
    of "_old" variables, though it still updates them.
  - Added imports: Utilities, Performance for performance
    and centralization of dependencies.
  - Other minor changes.
- v1.9:
  - Renamed functions and variables: removed "dpsm"
    from them to make them more concise and cohesive with
    object-oriented programming and the "new" keyword.
  - Renamed variables:
    - Enabled -> ENABLED
    - Refresh -> refreshRate
  - "_old" variables deprecated. Now the original
    ones are used.
  - Update() - mode parameter and "_old" vars deprecated.
- v2.0.0:
  - Removed function dpsUpdate().
  - All variable updates and calculations are now
    done in function Update().
- v2.1:
  - Updates and ui components are now handled internally.
  - Added ToString() and Print() functions.
  - Global variables are now adjusted in the main() function.
  - Rearranged script layout -- now there's 2 sections:
    public and private.
  - Renamed file to "DPS".
- v2.2:
  - Added dependency: UI_Maker
  - Added canUpdate().
  - Now Update() only modifies the data when called is true.
  - Update() should now only be called if canUpdate() returns true.
  - refreshRate >> frameRate
  - Merged isSlim with mode
  - Added error handling
  - main >> Main_DPS
  - added entry sanitization for mode
  - upgraded Main_DPS() description

***

Enjoy! ;)