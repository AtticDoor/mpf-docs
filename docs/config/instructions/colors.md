---
title: Specifying Colors in Config Files
---

# Specifying Colors in Config Files


Colors in config files can be specified by name (like "red") or by hex
value ("ff0000").

You can see a list of valid color names (and their respective colors)
[here](http://htmlcolorcodes.com/color-names/).

In addition to the 140 standard named colors, MPF adds the following
color options:

* `on` - turns on an LED with that LED's `default_color:` setting.
    (Default is "white" if you don't specify a color.)

* `off` - maps (0,0,0) which is more intuitive than "black" when
    you're working with LEDs.

* `stop` - removes the current color being displayed allowing a color from a lower priority light_player or
    show_player to become visible.

You can also specify color by hex string. If you do this, do *NOT* put a
`#` in it, since YAML files use those for comments which are ignored.

* CORRECT: `color: ff0000`
* WRONG: `color: #ff0000`

## Specifying opacity / alpha

For colors which will be processed by the media controller (such as
slide background and widget colors), you can optionally add two more
characters to a hex color to specify the alpha value.

For example:

* `ff0000ff` (fully opaque)
* `ff000080` (50% opacity)

See the [Widget Opacity & Transparency](../../mc/widgets/opacity.md)
documentation for details.
