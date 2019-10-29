### dwm-hide-and-restore-win.diff
This patch allows [dwm](https://dwm.suckless.org/) users to hide and restore 
windows via keyboard shortcuts.
![demo](./demo.gif)

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
 	{ MODKEY,                       XK_l,      setmfact,       {.f = +0.05} },
+	{ MODKEY,                       XK_v,      hidewin,        {0} },
+	{ MODKEY|ShiftMask,             XK_v,      restorewin,     {0} },
 	{ MODKEY|ShiftMask,             XK_Return, zoom,           {0} },
```

### Usage
By default, after applying the patch, `MOD` + `v` is the shortcut to hide 
(minimize) the current window, and `MOD` + `Shift` + `v` is the shortcut to 
restore the most recent hidden window in the current tag.

### Author
[@theniceboy](https://github.com/theniceboy)

### Todo
- [ ] Submit this patch to [dwm patches](https://dwm.suckless.org/patches/)

