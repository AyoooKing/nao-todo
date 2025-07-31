# NaoTodo

## 🚀 项目简介

NaoTodo 是一个仿滴答清单的待办任务管理平台，旨在为用户提供简洁高效的任务管理体验。该平台采用 **Monorepo** 架构，支持 **Web、移动端、桌面端** 三个平台，基于 Vue3、Vite、NueUI、Pinia、Axios 以及 TypeScript 构建，确保了现代前端开发的性能和可维护性。通过 NaoTodo，用户可以轻松创建、编辑、删除任务，并设置任务的优先级和截止日期，从而有效管理日常待办事项。

## 🌐 站点地址

- [NaoTodo 在线版](https://nathan33.site/)

## 👨‍💻 开发者信息

- **作者**：Nathan Lee
- **GitHub 仓库**：[NaoTodo GitHub 仓库](https://github.com/Nathan3303/nao-todo)

## 🏗️ 技术架构

### 整体架构
项目采用 **Monorepo** 架构，使用 **pnpm workspace** 管理多包依赖，实现代码共享和统一管理。

```
nao-todo/
├── apps/                    # 应用层
│   ├── web/                # Web 应用 (Vue3 + Vite)
│   ├── mobile/             # 移动端应用 (UniApp)
│   └── desktop/            # 桌面端应用 (Electron)
├── packages/               # 共享包
│   ├── apis/              # API 接口层
│   ├── components/        # 通用组件库
│   ├── hooks/             # 自定义 Hooks
│   ├── stores/            # 状态管理
│   ├── types/             # TypeScript 类型定义
│   └── utils/             # 工具函数库
└── deploy/                # 部署配置
```

### 🛠️ 技术栈

#### 核心技术
- **前端框架**：Vue 3.5.13 + Composition API
- **构建工具**：Vite 5.4.6
- **包管理器**：pnpm (workspace)
- **编程语言**：TypeScript 5.4.5
- **状态管理**：Pinia 2.2.6
- **路由管理**：Vue Router 4.5.0
- **HTTP 请求**：Axios 1.7.8

#### UI 与样式
- **UI 框架**：NueUI 0.7.0-bp.4 (自研组件库)
- **移动端 UI**：Wot Design Uni (UniApp)
- **样式预处理**：PostCSS + PurgeCSS
- **图标系统**：Iconfont

#### 多端支持
- **Web 端**：Vue3 + Vite SPA
- **移动端**：UniApp (支持微信小程序、H5、App)
- **桌面端**：Electron 34.2.0

#### 开发工具
- **代码规范**：ESLint 9.15.0 + Prettier 3.4.0
- **类型检查**：vue-tsc 2.1.10
- **构建优化**：Rollup Plugin Terser

## 🎨 功能特性

### 核心功能
1. **任务管理** ✅
   - 创建、编辑、删除任务
   - 任务详情查看和编辑
   - 任务收藏和放弃
   - 任务复制和批量操作

2. **优先级与状态** ✅
   - 优先级：低、中、高、紧急四级
   - 状态：待办、进行中、已完成
   - 截止日期设置和提醒

3. **项目与分类** ✅
   - 创建和管理项目清单
   - 标签系统支持任务分类
   - 项目偏好设置（排序、视图等）

4. **检查事项 (Events)** ✅
   - 为任务添加子任务/检查清单
   - 进度跟踪和完成度统计
   - 支持检查事项的增删改

5. **评论系统** ✅
   - 任务评论和进度记录
   - 评论时间线展示
   - 富文本评论支持

### 视图与交互
6. **多视图模式** ✅
   - 📋 表格视图：详细列表展示
   - 📋 看板视图：Kanban 拖拽管理
   - 📅 日历视图：时间维度管理
   - 🔍 搜索视图：全局搜索功能

7. **智能过滤** ✅
   - 按项目、标签、状态过滤
   - 时间范围筛选（今日、明日、本周）
   - 收集箱、收藏、垃圾桶等特殊视图

8. **用户体验** ✅
   - 响应式设计，适配多端
   - 拖拽排序和操作
   - 快捷键支持
   - 加载状态和错误处理

### 高级功能
9. **AI 对话** 🚧
   - AI 助手聊天界面
   - 智能任务建议（开发中）

10. **番茄专注** 🚧
    - 专注模式计时器
    - 任务专注统计

11. **用户系统** ✅
    - 用户注册和登录
    - 个人资料管理
    - 头像上传和设置

12. **数据管理** ✅
    - 本地数据缓存
    - 云端数据同步
    - 数据导入导出

### 多端同步
13. **跨平台支持** ✅
    - Web 端：完整功能体验
    - 移动端：UniApp 多平台适配
    - 桌面端：Electron 原生应用

## 🚀 快速开始

### 环境要求
- Node.js >= 18.0
- pnpm >= 8.0

### 安装与运行

1. **克隆项目**
```bash
git clone https://github.com/Nathan3303/nao-todo.git
cd nao-todo
```

2. **安装依赖**
```bash
pnpm install
```

3. **启动应用**
```bash
# Web 端开发
pnpm webapp dev

# 移动端开发 (H5)
pnpm mobile dev:h5

# 移动端开发 (微信小程序)
pnpm mobile dev:mp-weixin

# 桌面端开发
pnpm desktop dev
```

4. **访问应用**
- Web 端：http://localhost:5173
- 移动端 H5：http://localhost:3000

### 构建部署
```bash
# 构建 Web 端
pnpm webapp build

# 构建移动端
pnpm mobile build:h5
pnpm mobile build:mp-weixin

# 构建桌面端
pnpm desktop build
```

## 📊 开发进度

### 完成度概览
- **🟢 已完成模块**：核心任务管理、项目管理、用户系统、多视图展示、评论系统、检查事项
- **🟡 开发中模块**：AI 对话功能、番茄专注模式
- **⚪ 规划中模块**：团队协作、数据统计分析、离线同步

| 模块 | Web端 | 移动端 | 桌面端 | 完成度 |
|------|-------|--------|--------|---------|
| 用户认证 | ✅ | ✅ | ✅ | 100% |
| 任务管理 | ✅ | ✅ | ✅ | 100% |
| 项目管理 | ✅ | ✅ | ✅ | 100% |
| 标签系统 | ✅ | ✅ | ✅ | 100% |
| 评论功能 | ✅ | ✅ | ✅ | 100% |
| 检查事项 | ✅ | ✅ | ✅ | 100% |
| 表格视图 | ✅ | ✅ | ✅ | 100% |
| 看板视图 | ✅ | ✅ | ✅ | 100% |
| 日历视图 | ✅ | ✅ | ✅ | 100% |
| 搜索功能 | ✅ | ✅ | ✅ | 100% |
| AI 对话 | 🚧 | 🚧 | 🚧 | 60% |
| 番茄专注 | 🚧 | 🚧 | 🚧 | 40% |

### 技术债务与优化
- [ ] 单元测试覆盖率提升
- [ ] 性能优化和代码分割
- [ ] 错误监控和日志系统
- [ ] 国际化支持 (i18n)
- [ ] 无障碍访问 (a11y) 优化

## 🏗️ 部署架构

### 生产环境
- **前端部署**：Nginx + 静态文件托管
- **CDN 加速**：静态资源分发
- **域名**：[nathan33.site](https://nathan33.site/)
- **SSL 证书**：HTTPS 安全访问

### Docker 部署
项目支持 Docker 容器化部署，配置文件位于 `deploy/` 目录：
- `nginx.conf`：Nginx 配置
- `docker-run-command.sh`：Docker 运行脚本
- `jenkins.build.sh`：CI/CD 构建脚本

## 📂 项目结构

### 核心包说明
- **`@nao-todo/apis`**：统一的 API 接口层，支持 v1 和 v2 版本
- **`@nao-todo/components`**：跨端复用的 Vue 组件库
- **`@nao-todo/hooks`**：自定义 Composition API hooks
- **`@nao-todo/stores`**：Pinia 状态管理模块
- **`@nao-todo/types`**：完整的 TypeScript 类型定义
- **`@nao-todo/utils`**：工具函数和辅助方法

### 数据模型
```typescript
// 主要数据模型
interface Todo {
  id: string
  name: string
  description: string
  state: 'todo' | 'in-progress' | 'done'
  priority: 'low' | 'medium' | 'high' | 'urgent'
  tags: string[]
  dueDate: { startAt: string; endAt: string }
  // ... 更多字段
}
```

## 📝 贡献指南

欢迎对 NaoTodo 做出贡献！在提交代码之前，请确保：

1. **代码规范**：通过 ESLint 和 Prettier 检查
2. **类型检查**：通过 TypeScript 类型检查
3. **功能测试**：确保新功能正常工作
4. **文档更新**：更新相关文档和注释
5. **提交信息**：使用清晰的提交信息格式

### 开发流程
```bash
# 1. Fork 项目并克隆
git clone your-fork-url

# 2. 创建功能分支
git checkout -b feature/your-feature

# 3. 开发和测试
pnpm install
pnpm webapp dev

# 4. 代码检查
pnpm run lint
pnpm run type-check

# 5. 提交更改
git commit -m "feat: add your feature"
git push origin feature/your-feature

# 6. 创建 Pull Request
```

## 🏆 项目亮点

### 技术创新
- **自研 NueUI 组件库**：基于 Vue3 的轻量级 UI 框架
- **Monorepo 架构**：统一管理多端应用和共享包
- **类型安全**：完整的 TypeScript 类型定义体系
- **高性能**：Vite 构建 + 代码分割优化

### 用户体验
- **多端一致性**：Web、移动端、桌面端统一交互体验
- **响应式设计**：适配各种屏幕尺寸和设备
- **直观易用**：简化操作流程，降低学习成本
- **丰富交互**：拖拽排序、快捷键、实时反馈

### 开发效率
- **模块化设计**：高度解耦的组件和工具库
- **开发工具链**：完整的 ESLint、Prettier、TypeScript 配置
- **热更新开发**：Vite 快速开发体验
- **部署自动化**：Docker + CI/CD 流水线

## 📈 性能指标

| 指标 | Web端 | 移动端 | 桌面端 |
|------|-------|--------|--------|
| 首屏加载 | < 2s | < 3s | < 1s |
| 包体积 | ~500KB | ~800KB | ~15MB |
| 内存占用 | ~50MB | ~80MB | ~150MB |
| 支持设备 | 现代浏览器 | iOS/Android/小程序 | Windows/macOS/Linux |

## 🔮 未来规划

### 2024 Q1
- [ ] AI 智能助手完善
- [ ] 团队协作功能
- [ ] 离线数据同步
- [ ] 性能优化 2.0

### 2024 Q2
- [ ] 移动端原生体验优化
- [ ] 数据统计与分析
- [ ] 第三方集成 (GitHub、Notion)
- [ ] 插件系统架构

### 长期目标
- [ ] 微服务后端架构
- [ ] 实时协作编辑
- [ ] 智能工作流推荐
- [ ] 企业级权限管理

## 📜 许可证

NaoTodo 项目遵循 [MIT 许可证](https://github.com/Nathan3303/nao-todo/blob/main/LICENSE)。你可以自由地使用、复制、修改和分发该项目，但请保留原作者和版权信息。

## 🙏 致谢

### 开源贡献
感谢所有参与 NaoTodo 项目开发、测试、反馈的用户和贡献者！

### 技术支持
特别感谢以下开源项目为 NaoTodo 提供的强大技术支持：

- **[Vue.js](https://vuejs.org/)**：渐进式 JavaScript 框架
- **[Vite](https://vitejs.dev/)**：下一代前端构建工具
- **[Pinia](https://pinia.vuejs.org/)**：Vue 状态管理库
- **[TypeScript](https://www.typescriptlang.org/)**：JavaScript 的超集
- **[UniApp](https://uniapp.dcloud.net.cn/)**：跨端开发框架
- **[Electron](https://www.electronjs.org/)**：桌面应用开发框架
- **[Axios](https://axios-http.com/)**：HTTP 客户端库

### 设计灵感
- **[滴答清单](https://www.dida365.com/)**：产品设计理念参考
- **[Todoist](https://todoist.com/)**：功能交互灵感来源

---

<div align="center">

**⭐ 如果这个项目对你有帮助，请给个 Star 支持一下！**

[![Star History Chart](https://api.star-history.com/svg?repos=Nathan3303/nao-todo&type=Date)](https://star-history.com/#Nathan3303/nao-todo&Date)

</div>
