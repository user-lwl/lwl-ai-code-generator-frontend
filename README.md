# lwl AI 代码生成器 - 前端

基于 Vue 3 + TypeScript + Ant Design Vue 构建的智能代码生成平台，让您通过自然语言对话快速创建完整的网站应用。

## ✨ 功能特性

### 🎯 用户功能
| 功能 | 描述 |
|------|------|
| 🚀 应用创建 | 通过提示词快速生成完整的网站应用 |
| 💬 AI 对话 | 与 AI 实时对话，交互式生成代码 |
| 👁️ 实时预览 | 即时查看生成的网站效果 |
| 📝 应用管理 | 编辑应用信息（名称、封面等） |
| 🗑️ 应用删除 | 删除不需要的应用 |
| 🚀 应用部署 | 一键部署到云端，获取可访问链接 |
| 📋 应用列表 | 分页查询、搜索个人应用 |
| ⭐ 精选应用 | 浏览平台精选的优秀应用 |

### 🔧 管理员功能
| 功能 | 描述 |
|------|------|
| 应用管理 | 删除、编辑任意应用 |
| 精选设置 | 将优质应用设为精选展示 |
| 多条件查询 | 支持按名称、创建者、类型等多维度搜索 |

## 📁 项目结构

```
src/
├── api/                    # API 接口层
│   ├── appController.ts    # 应用相关 API
│   ├── userController.ts   # 用户相关 API
│   └── typings.d.ts        # TypeScript 类型定义
├── components/             # 公共组件
│   ├── GlobalHeader.vue    # 全局头部导航
│   └── GlobalFooter.vue    # 全局底部信息
├── layouts/                # 布局组件
│   └── BasicLayout.vue     # 基础布局容器
├── pages/                  # 页面组件
│   ├── HomePage.vue        # 首页（应用列表 + 快速创建）
│   ├── app/                # 应用相关页面
│   │   ├── AppChatPage.vue # AI 对话生成页面
│   │   └── AppEditPage.vue # 应用信息编辑页面
│   ├── admin/              # 管理员后台
│   │   ├── AppManagePage.vue
│   │   └── UserManagePage.vue
│   └── user/               # 用户认证页面
│       ├── UserLoginPage.vue
│       └── UserRegisterPage.vue
├── stores/                 # Pinia 状态管理
│   └── loginUser.ts        # 当前登录用户状态
├── utils/                  # 工具函数
│   ├── constants.ts        # 全局常量
│   ├── format.ts          # 格式化工具
│   └── validation.ts      # 表单验证工具
├── router/                 # Vue Router 配置
│   └── index.ts
└── main.ts                # 应用入口文件
```

## 🛠️ 技术栈

| 分类 | 技术 | 版本 |
|------|------|------|
| 前端框架 | Vue | 3.x |
| 语言 | TypeScript | 5.x |
| UI 组件 | Ant Design Vue | 4.x |
| 路由 | Vue Router | 4.x |
| 状态管理 | Pinia | 2.x |
| 构建工具 | Vite | 6.x |
| HTTP 客户端 | Axios | 1.x |
| 时间处理 | Day.js | 1.x |
| 代码规范 | ESLint + Prettier | - |

## 🚀 快速开始

### 环境要求

- Node.js >= 18.0.0
- npm >= 9.0.0

### 安装依赖

```bash
npm install
```

### 开发模式

```bash
npm run dev
```

启动后访问: http://localhost:5173

### 构建生产版本

```bash
npm run build
```

### 代码检查

```bash
npm run lint
```

## 🔄 核心业务流程

### 应用创建流程
1. 用户在首页输入应用描述提示词
2. 系统创建应用实例，返回应用 ID
3. 跳转至对话页面，自动发送初始提示词
4. 通过 SSE 实时接收 AI 生成结果
5. 右侧预览区域实时渲染生成的网站

### 应用部署流程
1. 在对话页面点击「部署」按钮
2. 调用后端部署接口
3. 等待部署完成，获取访问 URL
4. 弹窗展示部署成功信息和访问链接

### 应用管理流程
1. 管理员进入应用管理后台
2. 使用筛选条件搜索目标应用
3. 执行编辑、删除或设置精选操作
4. 编辑操作跳转至应用详情页

## ⚠️ 注意事项

- 应用生成依赖后端 AI 服务
- 部署功能需配置云服务相关环境变量
- 管理员功能需登录管理员账号访问
- 预览功能依赖后端静态资源服务支持

## 📄 许可证

MIT License - 详见 [LICENSE](LICENSE) 文件