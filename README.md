### dwm-hide-and-restore-win.diff
This patch allows [dwm](https://dwm.suckless.org/) users to hide and restore 
windows via keyboard shortcuts.
![demo](./demo.gif)

### Requirements
This patch requires the [awesomebar patch](http://dwm.suckless.org/patches/awesomebar/).

### Installation
To apply this patch, first download the `.diff` file to the `dwm` folder, 
and then do:
```bash
cd path/to/dwm/source/
patch < dwm-hide-and-restore-win.diff
```
Then, you might want to take a look at your `config.def.h` and customize 
keyboard shortcuts (don't forget to copy those to `config.h`):
```diff
+	{ MODKEY,                       XK_o,      hidewin,        {0} },
+	{ MODKEY|ShiftMask,             XK_o,      restorewin,     {0} },
+   { MODKEY,                       XK_w,      hideotherwins,  {0}},
+   { MODKEY|ShiftMask,             XK_w,      restoreotherwins, {0}},
```

### Usage
By default, after applying the patch, `MOD` + `o` is the shortcut to hide 
(minimize) the current window, and `MOD` + `Shift` + `o` is the shortcut to 
restore the most recent hidden window in the current tag.
Use `MOD` + 'w', you will hide others windows in this tag, which is just like fullscreen but isn't. 
Use `MOD` + 'Shift' + 'w', you can restore all windows which is hidden in this tag.
Use the shortcut of focusstack, you can change the window to display if other windows are all hidden.

### Author
[@theniceboy](https://github.com/theniceboy)

### Todo
- [ ] Submit this patch to [dwm patches](https://dwm.suckless.org/patches/)

