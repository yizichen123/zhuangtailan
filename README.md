# zhuangtailan

《都市神豪之我爱装逼·完整版》状态栏美化云端链路仓库。

## 目录结构

- `statusbar/index.html`：状态栏美化（亮）完整 HTML/CSS/JS 源码（顶部第一行显式标注当前版本号）
- `regex/01-状态栏美化（亮）-云端链路版.component.json`：可直接导入 SillyTavern 的云端加载正则组件（内置 `gcore` + `testingcf` 双 CDN 自动容灾）

## 使用方式（手动改版本号更新）

在 SillyTavern 正则 `状态栏美化（亮）` 中使用 `regex/01-状态栏美化（亮）-云端链路版.component.json`（或直接修改脚本内第一行 `VERSION`）：

```text
https://gcore.jsdelivr.net/gh/yizichen123/zhuangtailan@v7.5.2/statusbar/index.html
https://testingcf.jsdelivr.net/gh/yizichen123/zhuangtailan@v7.5.2/statusbar/index.html
```

发公告出新版本时，只需修改 `VERSION = 'v7.5.2'` 为新版本号（如 `v7.5.3`）即可。

## 版本历史

- `v7.5.2`（三端版本号统一为 `7.5.2`，对应角色卡《都市神豪之我爱装逼·完整版 V7.5.2》）：彻底移除状态栏 `contraceptionProfileRows` 中的 `>= 18` 岁展示拦截与 `shnResolveAgePair` 中的 `Math.max(18, ...)` 外表年龄下限锁定，100% 保留 `v1.1~v1.6` 全部修复与功能。
- `v1.6`（对应角色卡《都市神豪之我爱装逼·完整版 V7.5.1》）：① 为经典与浅色 `.wealth-card` 补齐 `grid-template-columns: minmax(0, 1fr)` 与子行 `min-width: 0`，并在 `fitCashBalance` 与 `applyHudTheme` 同步限制真实可用宽度＋切皮重算，根治浅色模式下大额余额（如 1000 亿）把 `.wealth-card` 撑宽裁切的问题；② 移除 `#shn-theme-40-style` 误带入的 `#render-targets .shn-pfp img { pointer-events: none; }` 拦截并补充容器兜底点击，修复浅色模式下生成的立绘无法点击放大查看的问题。
- `v1.5`（对应角色卡《都市神豪之我爱装逼·完整版 V7.5》）：配合对 AI 彻底移除「女性/男性角色档案」方案，`boundaryOfCard` 与 `npcMeasurementRows` 改为优先读取当前在场表的 `界线与反感项` / `身高` / `体重`，再用静默后台档案兜底。
- `v1.4`（对应角色卡《都市神豪之我爱装逼·完整版 V7.4》）：点击太阳/月亮图标切换时同步向宿主广播 `shenhao-theme-change` 事件并设置 `data-shenhao-theme`，实现状态栏 ＋ 小手机（象牙白↔暗色）＋ 正文对话气泡与卡片 0ms 全局日夜一键联动。
- `v1.3`（对应角色卡《都市神豪之我爱装逼·完整版 V7.3.2》）：将底部皮肤切换按钮精简为纯太阳/月亮 SVG 图标胶囊（去除「状态栏皮肤」与按钮文字，轻点图标 0ms 秒切浅色/暗金皮肤）。
- `v1.2`（对应角色卡《都市神豪之我爱装逼·完整版 V7.3.1》）：基于 `v1.1`（完整保留移除 `shnMingqiStatusPanel` 两处 `return ''` 拦截的手动修改），合入 4.0 浅色杂志风状态栏美化 ＋ 新旧皮肤 0ms 无刷热切换（`4.0 浅色新颜 ↔ 经典暗金`）＋ V6.0–V7.2.2 全模块浅色补丁 ＋ 3 项交互升级（余额智能缩写 / 目标显式查看详情 / 系统商城分组折叠），并升级为 `gcore` + `testingcf` 双 CDN 容灾加载器。
- `v1.1`（对应角色卡《都市神豪之我爱装逼·完整版 V7.2》状态栏，移除 `shnMingqiStatusPanel` 两处 `return ''` 拦截）
- `v1.0`（初始提取自《都市神豪之我爱装逼·完整版 V7.2》）
