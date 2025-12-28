# Django Blog Project

这是一个基于 Django 框架构建的简单博客应用。该项目旨在练习 Django 的模型设计、表单处理、用户认证以及对象级别的权限控制。

项目实现了《Python编程：从入门到实践》中 **19-1 (Blog)** 和 **19-5 (Protected Blog)** 的练习要求。

## 📋 功能特性 (Features)

### 1. 基础博客功能 (Basic Blog Functionality)
- **应用结构**：包含一个名为 `blogs` 的核心 App。
- **数据模型**：
  - `BlogPost` 模型：包含标题 (`title`)、正文 (`text`) 和发布日期 (`date_added`)。
- **文章展示**：
  - 主页按时间顺序（最新的在前）展示所有博客文章。
- **表单处理**：
  - 提供创建新文章的表单。
  - 提供编辑现有文章的表单。

### 2. 用户权限与保护 (User Authentication & Permissions)
- **用户关联**：每篇博客文章都与特定的用户账户绑定。
- **访问控制**：
  - **公开访问**：所有人（包括未登录访客）都可以查看文章列表和文章详情。
  - **注册用户**：只有注册并登录的用户才能发布新文章。
  - **编辑权限保护**：虽然登录用户可以编辑文章，但在后端视图层进行了严格检查，**确保用户只能编辑属于自己的文章**，防止越权操作。

### 3. 管理后台 (Admin Site)
- 已配置 Superuser。
- 可通过 Django Admin 后台管理所有文章和用户数据。

## 🛠️ 技术栈 (Tech Stack)
- **Python 3.x**
- **Django**
- **SQLite** (默认数据库)
- **HTML/CSS** (Bootstrap 简单样式)

## 🚀 如何运行 (How to Run)

1. **克隆仓库**
   ```bash
   git clone https://github.com/Counterflow47/bll.git
   cd bll