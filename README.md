# growth-blog

该仓库采用「master 占位 + content 内容」的分支结构：

| 分支 | 内容 | 用途 |
| ---- | ---- | ---- |
| `master` | 占位页（中国 · 地大物博 介绍页） | GitHub Pages 默认展示的占位页面 |
| `content` | 完整博客站点（SelfTechHub，Hugo 构建产物，CNAME: blog.irudder.me） | 实际博客内容 |

## 切换发布分支

在 **GitHub → 本仓库 → Settings → Pages → Build and deployment → Branch** 中，把发布分支从 `master` 切换到 `content`，博客（blog.irudder.me）即恢复为完整站点。

## 内容更新流程

```bash
git checkout content          # 切到内容分支
# 用 hugo 构建后同步 public 目录（或直接修改后提交）
git add -A && git commit -m "update"
git push origin content
```

> 站点源文件（Markdown 内容、Hugo 配置与主题）位于本地项目 `life/` 目录，构建产物提交到本仓库 `content` 分支。
