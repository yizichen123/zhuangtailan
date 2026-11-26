# zhuangtailan

《都市神豪之我爱装逼·完整版》状态栏美化云端链路仓库。

## 目录结构

- `statusbar/index.html`：状态栏美化（亮）完整 HTML/CSS/JS 源码（提取自 `都市神豪_完整版_V7.2.png`）
- `regex/01-状态栏美化（亮）-云端链路版.component.json`：可直接导入 SillyTavern 的极简云端加载正则组件

## 使用方式（手动改版本号更新）

在 SillyTavern 正则 `状态栏美化（亮）` 中使用 `regex/01-状态栏美化（亮）-云端链路版.component.json`（内部通过 `gcore.jsdelivr.net` 加载）：

```text
https://gcore.jsdelivr.net/gh/yizichen123/zhuangtailan@v1.1/statusbar/index.html
```

发公告出新版本时，只需修改链接中 `@` 后面的版本号（例如将 `@v1.1` 改为新版本号）即可。

## 当前版本

- `v1.1`（对应角色卡《都市神豪之我爱装逼·完整版 V7.2》状态栏，移除 `shnMingqiStatusPanel` 两处 `return ''` 拦截）
