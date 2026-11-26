# zhuangtailan

《都市神豪之我爱装逼·完整版》状态栏美化云端链路仓库。

## 目录结构

- `statusbar/index.html`：状态栏美化（亮）完整 HTML/CSS/JS 源码（顶部第一行显式标注当前版本号）
- `regex/01-状态栏美化（亮）-云端链路版.component.json`：可直接导入 SillyTavern 的云端加载正则组件（内置 `gcore` + `testingcf` 双 CDN 自动容灾）

## 使用方式（手动改版本号更新）

在 SillyTavern 正则 `状态栏美化（亮）` 中使用 `regex/01-状态栏美化（亮）-云端链路版.component.json`（或直接修改脚本内第一行 `VERSION`）：

```text
https://gcore.jsdelivr.net/gh/yizichen123/zhuangtailan@v1.3/statusbar/index.html
https://testingcf.jsdelivr.net/gh/yizichen123/zhuangtailan@v1.3/statusbar/index.html
```

发公告出新版本时，只需修改 `VERSION = 'v1.3'` 为新版本号（如 `v1.4`）即可。

## 版本历史

- `v1.3`（对应角色卡《都市神豪之我爱装逼·完整版 V7.3.2》）：将底部皮肤切换按钮精简为纯太阳/月亮 SVG 图标胶囊（去除「状态栏皮肤」与按钮文字，轻点图标 0ms 秒切浅色/暗金皮肤）。
- `v1.2`（对应角色卡《都市神豪之我爱装逼·完整版 V7.3.1》）：基于 `v1.1`（完整保留移除 `shnMingqiStatusPanel` 两处 `return ''` 拦截的手动修改），合入 4.0 浅色杂志风状态栏美化 ＋ 新旧皮肤 0ms 无刷热切换（`4.0 浅色新颜 ↔ 经典暗金`）＋ V6.0–V7.2.2 全模块浅色补丁 ＋ 3 项交互升级（余额智能缩写 / 目标显式查看详情 / 系统商城分组折叠），并升级为 `gcore` + `testingcf` 双 CDN 容灾加载器。
- `v1.1`（对应角色卡《都市神豪之我爱装逼·完整版 V7.2》状态栏，移除 `shnMingqiStatusPanel` 两处 `return ''` 拦截）
- `v1.0`（初始提取自《都市神豪之我爱装逼·完整版 V7.2》）
