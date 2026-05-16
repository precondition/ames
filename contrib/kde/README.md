# ames on KDE Wayland

The provided [config](./config) overwrites these functions using
the Wayland utilities `slurp`/`spectacle`/`wl-paste`:
- `get_selection()`
- `take_screenshot_region()`
- `take_screenshot_window()`
- `copied_text()`

`slurp` and `slop` may provide wrong coordinates on a scaled interface.
In this case, adjust the variable `scale` for your scaling. Note, the value
may not match the scaling - for me (150% on main monitor and 100% on second one)
it is 1.333 for `slop` and 2.0 for `slurp` 🤷.

For a detailed discussion on supporting Wayland for different compositors,
see the issue [Wayland Support #2](https://github.com/eshrh/ames/issues/2).
