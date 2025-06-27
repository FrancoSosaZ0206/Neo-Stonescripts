# FILE INFO

Multi-location, general script.

**Written by:** IronHawk (Tom Crow).

## Description

I have several farming scripts and libraries for
this game. Some time after I started scripting, I
noticed the increased baggage I needed to carry
everywhere, everytime I had to look or change
something. That was really tedious, so I decided to
write a main script to unify all. That way, I don't
need to worry about what location I'm in, and what
its corresponding script is. I just have to put this
script in the Mindstone, enter the location I want,
and voilà!

And the cherry on top: if I go to a different
location, it will automatically switch to its
corresponding script. Neat, right!

## Importing

### Desktop

Save this file into the `Stonescripts` folder and
import it using the correct path to the file.

**Example:** if the file is saved in the Stonescript
folder,

`import main`

### Mobile

Copy-paste the `MOBILE` section that into the Mindstone.
Then, upload this script and any others you are using to
the web, and replace the URL template with the link to this
file.

**URL example template** (GitHub repo):

```
https://raw.githubusercontent.com/<USER_NAME>/
<REPO_NAME>/main/<FILE_DIRECTORY>/<FILE_NAME>
```

Replace each `<>` with their respective values.

*Tip: break your link into several, shorter lines
like shown. Otherwise, the Mindstone could butcher
the line and break the script.*

## How to do changes in mobile

> *I'm on mobile, and after some changes to my
scripts, it won't work anymore! What happened!?*

This is due to the intricacies of how the process of
importing works on mobile. To put it simply, *the Mindstone
only updates upon opening the game and selecting "play"*,
so **any changes made while you're in-game will only be
applied the next time you enter.**

Furthermore, **any errors in the scripts used will also
prevent updates.**

As you can see, it's quite a finicky process.

> *Alright, so what do I do?*

To work around it, follow these steps **closely**:

1. Go to the Mindstone and comment out the script (find the
`COMMENT OUT HERE` headers and add `//` at the start of the
indicated line).
1. Enter any location and leave after a few seconds.
1. Close the game (**check that "saved!" pops up at the top
left corner**).
1. Change your script or dependencies and upload them to
your preferred website.
1. Wait for the changes to take effect. Waiting time varies
depending on your connection speed.
1. Enter the game. You should see a loading screen appear
for a short while, which means it caught the changes.
If so, repeat step 2. Else, exit once more
and try again later.
1. Go to the Mindstone again and uncomment the script.
1. Enter your desired location.

Make sure your script doesn't have any errors.
If everything is done correctly, you should see your
changes reflected in-game.

I recommend debugging on PC or by pasting your script
directly in the Mindstone, though. Importing in mobile
is ideal for when your scripts are already done, in my
opinion.

***

Enjoy! ;)