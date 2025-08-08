---
layout: default
title: 添加 Open with Code Insiders
---

# 添加 Open with Code Insiders

最近的 Visual Studio Code Insiders 的右键菜单不见了，用脚本添加Open with Code Insiders解决。

## file: Open with Code Insiders.reg

```reg
Windows Registry Editor Version 5.00

; 添加到文件夹背景右键菜单
[HKEY_CLASSES_ROOT\Directory\Background\shell\Open with Code Insiders]
@="Open with Code Insiders"
"Icon"="C:\\Program Files\\Microsoft VS Code Insiders\\Code - Insiders.exe"

[HKEY_CLASSES_ROOT\Directory\Background\shell\Open with Code Insiders\command]
@="\"C:\\Program Files\\Microsoft VS Code Insiders\\Code - Insiders.exe\" \"%V\""

; 添加到文件夹图标右键菜单
[HKEY_CLASSES_ROOT\Directory\shell\Open with Code Insiders]
@="Open with Code Insiders"
"Icon"="C:\\Program Files\\Microsoft VS Code Insiders\\Code - Insiders.exe"

[HKEY_CLASSES_ROOT\Directory\shell\Open with Code Insiders\command]
@="\"C:\\Program Files\\Microsoft VS Code Insiders\\Code - Insiders.exe\" \"%1\""
```

<div class="datenote">
    <span>尹永贤</span><br>
    <span>2025-08-08</span><br>
    <span>上海</span>
</div>