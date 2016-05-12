pomo.sh
=======

pomo.sh is a simple [Pomodoro](http://en.wikipedia.org/wiki/Pomodoro_Technique) 
timer written in bash with minimal dependencies.  It is designed to be easy to 
use from the command-line and integrates nicely into status bar such as 
[xmobar](http://projects.haskell.org/xmobar/).

This version was edited for easier integration into i3blocks.
Left-clicking the blocklet starts a timer. Right-clicking pauses a timer, 
and middle-clicking stops the timer.

Pomicons are used for looks.

Installation
------------

Place `pomodoro` in your `/usr/libexec/` (or wherever your other i3blocks scripts are)

Put this snippet in your `i3blocks.conf`:

```
[pomodoro]
label=
interval=1
```

Configuration
-----

Variables in the script:

`POMO_FILE`

Location of the Pomodoro file used to store the duration of the Pomodoro
period (mostly using timestamps).  Multiple Pomodoro timers can be run by
using different files.  Default: $HOME/.local/share/pomo.

`POMO_WORK_TIME`

Duration of the work period in minutes.  Default: 25.

`POMO_BREAK_TIME`

Duration of the break period in minutes.  Default: 5.

Dependencies
------------

bash, GNU coreutils (cat, cut, date, printf, sleep, stat, touch, wc), 
[Pomicons](https://github.com/gabrielelana/pomicons)

License
-------

MIT.

See also
--------

`Pymodoro <https://github.com/dattanchu/pymodoro>`_ contains many more features but
I wanted something a little simpler.
