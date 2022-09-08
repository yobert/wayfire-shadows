# Window Shadows Plugin for Wayfire

This is a plugin for wayfire that adds window shadows. The code was initially a
fork of <https://gitlab.com/wayfireplugins/windecor> but only a small part of
that remains in the code.

## Compile and install

This branch targets wayfire master version. If you want to build for wayfire 0.7.x, switch to the branch `backport0.7`.

You should have first compiled and installed wlroots, wf-config and wayfire.

- Get the sources
  - `git clone https://github.com/timgott/wayfire-shadows.git`
- Enter the cloned folder
  - `cd wayfire-shadows`
- Configure the project with meson (change `/usr` to your Wayfire installation prefix if necessary)
  - `meson build --prefix=/usr --buildtype=release`
- Compile and install using ninja
  - `ninja -C build && sudo ninja -C build install`

## Screenshots

By default, the plugin will add fast and nice shadows around windows that use server side decorations.
![image](https://raw.github.com/timgott/wayfire-shadows/screenshots/screenshots/screenshot_stripes.png)

Bonus: The plugin can additionally make the focused window glow.
![image](https://raw.github.com/timgott/wayfire-shadows/screenshots/screenshots/screenshot_glass_glow.png)

<details>
<summary>Config used in last screenshot</summary>
```
[decoration]
active_color = \#A8A0C9A4
border_size = 4
inactive_color = \#20252338
title_height = 0

[winshadows]
glow_color = \#97AFCD26
glow_radius = 40
shadow_color = \#00000033
shadow_radius = 20
```
</details>
