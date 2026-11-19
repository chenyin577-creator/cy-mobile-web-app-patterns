# CY 手机网页版 APP 常用开发模式

这是一个供 Codex 开发手机网页应用时使用的技能插件。它把「换一台手机还能接着用」作为验收目标，让 Codex 在开发时就处理好同一账号的多设备登录、已有云数据库的接入、离线修改，以及发布新版时的旧数据保留。

## 安装到 Codex

使用支持 `codex plugin` 的 Codex CLI，在终端执行：

```sh
codex plugin marketplace add https://github.com/chenyin577-creator/cy-mobile-web-app-patterns.git --ref main
codex plugin add mobile-cloud-apps@personal-app-recipes
```

打开一个新 Codex 对话，就可以说：

> 按「CY 手机网页版 APP 常用开发模式」帮我做一个拜访笔记应用。我有云端数据库，两台手机要用同一个账号；旧手机里的草稿和离线笔记也要保留。

也可以用 `$mobile-cloud-apps:multi-device-app` 指定这项技能。

## 怎么验收

用同一条笔记走一遍：在 A 手机离线新增，联网后等云端确认；在 B 手机登录，找到并改动这条笔记；再回到 A 手机核对改动。发布新版后，从原入口打开，检查账号、笔记和未提交草稿是否仍能接着用。

[阅读完整开发方法](plugins/mobile-cloud-apps/skills/multi-device-app/SKILL.md) · [查看跨设备验收与排查表](plugins/mobile-cloud-apps/skills/multi-device-app/references/acceptance.md)
