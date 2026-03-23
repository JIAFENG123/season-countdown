# 四季倒计时（北京时间）

一个简洁的静态网页，用于实时展示中国节气四季倒计时：

- 当前季节（按立春/立夏/立秋/立冬划分）
- 当前季节剩余时间（天/时/分/秒）
- 距离下次立春/立夏/立秋/立冬的倒计时
- 固定按北京时间（`Asia/Shanghai`）计算

## 目录结构

```text
testbe/
  ├─ index.html
  └─ README.md
```

## 本地运行

这是纯静态页面，无需安装依赖，直接打开即可：

1. 双击 `index.html`
2. 或使用本地静态服务器预览（推荐）

例如使用 Node：

```bash
npx serve .
```

## Render 部署（Static Site）

### 方式一：单独仓库（推荐）

将 `testbe` 目录内容放到仓库根目录后，在 Render 创建 `Static Site`：

- **Build Command**：留空
- **Publish Directory**：`.`

### 方式二：放在大仓库子目录

如果保留当前结构（`testbe/index.html`），在 Render 创建 `Static Site` 时：

- **Build Command**：留空
- **Publish Directory**：`testbe`

## 说明

- 页面时间每秒刷新
- 为保证跨地区一致性，计算不依赖访问者本地时区
- 移动端已做基础适配（小屏布局、安全区、可读性优化）
