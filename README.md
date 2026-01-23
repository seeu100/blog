# 个人博客

这是一个使用Hugo静态网站生成器创建的个人博客，托管在GitHub Pages上。

## 技术栈

- **Hugo**：静态网站生成器
- **Ananke**：博客主题
- **GitHub Actions**：自动构建部署
- **GitHub Pages**：网站托管

## 快速开始

### 本地开发

1. **克隆仓库**
   ```bash
   git clone https://github.com/erwa/blog.git
   cd blog
   ```

2. **安装依赖**
   ```bash
   # 如需安装主题（如果还未安装）
   git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke
   ```

3. **启动开发服务器**
   ```bash
   hugo server --buildDrafts
   ```
   访问 `http://localhost:1313` 查看博客。

### 发布新文章

1. **创建新文章**
   ```bash
   hugo new content posts/文章标题.md
   ```

2. **编辑文章内容**
   修改 `content/posts/文章标题.md` 文件，添加文章内容。

3. **发布文章**
   将 `draft` 设置为 `false`，然后提交到GitHub：
   ```bash
   git add .
   git commit -m "添加新文章：文章标题"
   git push
   ```

4. **自动部署**
   GitHub Actions会自动构建并部署到GitHub Pages，通常需要1-2分钟完成。

## 项目结构

```
.
├── .github/          # GitHub Actions配置
├── archetypes/       # 内容模板
├── content/          # 文章内容
│   └── posts/        # 博客文章
├── public/           # 生成的静态网站（自动生成，忽略git）
├── resources/        # 资源文件（自动生成，忽略git）
├── themes/           # 主题
│   └── ananke/       # Ananke主题
├── hugo.toml         # Hugo配置文件
├── .gitignore        # Git忽略文件
└── README.md         # 项目说明
```

## 配置说明

- **hugo.toml**：包含站点基本配置，如标题、作者、描述等。
- **.github/workflows/hugo.yml**：GitHub Actions自动构建部署配置。

## 主题定制

如需定制主题，可以修改 `themes/ananke` 目录中的文件，或创建自己的主题。

## 参考文档

- [Hugo 官方文档](https://gohugo.io/documentation/)
- [Ananke 主题文档](https://github.com/theNewDynamic/gohugo-theme-ananke)
- [GitHub Actions 文档](https://docs.github.com/en/actions)
- [GitHub Pages 文档](https://docs.github.com/en/pages)