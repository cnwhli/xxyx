# 修仙模拟器 - Cloudflare Worker 部署指南

这是一个基于 HTML5、CSS3 和 JavaScript 开发的修仙模拟器游戏，可以部署到 Cloudflare Worker 上运行。

## 项目结构

- `index.js` - Cloudflare Worker 主文件，包含游戏的所有代码
- `wrangler.toml` - Cloudflare Worker 配置文件
- `README.md` - 项目说明文档

## 部署步骤

### 1. 安装 Wrangler CLI

```bash
npm install -g wrangler
```

### 2. 登录 Cloudflare

```bash
wrangler login
```

### 3. 配置项目

编辑 `wrangler.toml` 文件，修改以下内容：

```toml
name = "your-project-name"
[[routes]]
pattern = "your-domain.com/*"
zone_name = "your-domain.com"
```

### 4. 本地开发

```bash
wrangler dev
```

### 5. 部署到 Cloudflare

```bash
wrangler deploy
```

## 游戏功能

- 角色创建：选择灵根、分配属性点
- 修炼系统：积累灵气，提升境界
- 突破系统：突破当前境界，获得属性提升
- 任务系统：完成任务获得奖励
- 机缘系统：随机事件，影响角色发展

## 技术栈

- HTML5 + CSS3 + JavaScript
- Tailwind CSS v3
- Font Awesome
- Cloudflare Worker

## 注意事项

- 游戏数据存储在浏览器的 localStorage 中
- 如需添加云端存储功能，可以扩展 `/api/` 路径下的功能
- 可以通过修改 `wrangler.toml` 文件配置自定义域名