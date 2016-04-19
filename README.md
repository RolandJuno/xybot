# xybot
Alternate firmware for the Makeblock XY Plotter

I got frustrated by the Makeblock XY Plotter firmware when using it with the laser
engraver and the MDraw software. When it moved over a long path, it included an
acceleration and deceleration function. The net effect of this causes the lines
from the laser engraver to be more faint since it's moving over the surface
faster.

This modification tracks the pen and laser engraver's status (up/down, or on/off)
and will perform moves accordingly.

* If the pen is up or laser is off, moves happen very quickly with acceleration and
deceleration. The speed can be adjusted using the speed setting inside MDraw.

* If the pen is down or the laser is on, moves happen at a constant speed,
regardless of the speed setting inside MDraw.

