### dwm-hide-and-restore-win.diff

[Englist Ver.](./README.md)

此补丁允许 [dwm](https://dwm.suckless.org/) 用户通过快捷键隐藏和恢复他们的窗口

中文翻译: [KiteAB](https://github.com/KiteAB)

![demo](./demo.gif)

### Requirements
需要有 [awesomebar 补丁](http://dwm.suckless.org/patches/awesomebar/)

### 安装
想要应用此补丁, 首先需要下载 `.diff` 文件并将它放到 `dwm` 文件夹, 
然后输入:
```bash
cd path/to/dwm/source/
patch < dwm-hide-and-restore-win.diff
```
然后, 你可能希望浏览 `config.def.h` 并自定义快捷键 (不要忘记将这些复制到 `config.h`):
```diff
+	{ MODKEY,                       XK_o,      hidewin,        {0} },
+	{ MODKEY|ShiftMask,             XK_o,      restorewin,     {0} },
+   { MODKEY,                       XK_w,      hideotherwins,  {0}},
+   { MODKEY|ShiftMask,             XK_w,      restoreotherwins, {0}},
```

### 使用
在默认情况下, `MOD` + `o` 快捷键用来隐藏 (最小化) 当前窗口, 
而 `MOD` + `Shift` + `o` 快捷键用来恢复在当前标签下最近一次隐藏的窗口

使用 `MOD` + 'w', 你将隐藏除当前窗口以外的所有窗口, 它就像将当前窗口最大化一样, 
使用 `MOD` + 'Shift' + 'w', 你能恢复所有在当前标签下的窗口

使用 `focusstack` 键值, 你可以将窗口更改为在其他所有窗口都被隐藏的情况下显示

### 作者
[@theniceboy](https://github.com/theniceboy)

### Todo
**This part is the temp part so i don't will translate it.**

- [ ] Submit this patch to [dwm patches](https://dwm.suckless.org/patches/)

