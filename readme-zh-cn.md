[English](./README.md) | **简体中文**

<p align="center">
  <img src="./docs/brand/logo.png" width="120" height="120" alt="Questionnaire Star · Builder logo" />
</p>

<div align="center">

# 问卷星 · B 端

<p><strong>从组件编排到问卷管理与统计的可视化工作台</strong></p>

<p>
  <a href="https://github.com/tuolola/questionnaire-star---react"><img src="https://img.shields.io/badge/GitHub-Repository-2563eb?style=for-the-badge" alt="GitHub repository" /></a>
  <a href="https://gitee.com/guolola/questionnaire-star---react"><img src="https://img.shields.io/badge/Gitee-Original-0f766e?style=for-the-badge" alt="Original Gitee repository" /></a>
</p>

<p>
  <img src="https://img.shields.io/badge/Frontend-React%2018-2563eb?style=flat-square" alt="Frontend: React 18" />
  <img src="https://img.shields.io/badge/Build-Vite%207-7c3aed?style=flat-square" alt="Build: Vite 7" />
  <img src="https://img.shields.io/badge/Language-TypeScript-3178c6?style=flat-square" alt="Language: TypeScript" />
  <img src="https://img.shields.io/badge/UI-Ant%20Design%205-0f766e?style=flat-square" alt="UI: Ant Design 5" />
</p>

</div>

## 项目简介

基于 React 与 TypeScript 的问卷管理与可视化编辑前端，包含拖拽画布、组件属性面板、Redux 编辑历史、问卷管理页面和统计视图。源码还包含 AI 辅助问卷编写与高级功能配置界面；后端服务及模型服务需要单独配置。

## 核心能力

| 模块 | 说明 |
| --- | --- |
| 可视化编辑 | 使用 dnd-kit 编排组件，编辑属性并管理图层。 |
| 题型组件 | 提供文本、输入、选择、评分、矩阵、排序、文件、签名等组件。 |
| 编辑状态 | 通过 Redux Toolkit 与 redux-undo 管理选择、复制和撤销历史。 |
| 管理与统计 | 提供列表、标星、回收站页面及问卷统计视图。 |
| 高级编写 | 包含 AI 对话、条件规则、校验规则与多页配置编辑器。 |

## 快速开始

准备 Vite 7 支持的 Node.js 版本，并使用仓库锁文件安装依赖。

```bash
git clone https://github.com/tuolola/questionnaire-star---react.git
cd questionnaire-star---react
npm ci
npm run dev
```

打开 Vite 输出的地址，通常为 `http://localhost:5173`。开发代理将 `/api` 转发到 `http://localhost:3001`，请另行启动兼容后端或修改 `vite.config.ts`。接口客户端使用 `{ errno, data, msg }` 响应格式，并为鉴权请求附加 Bearer Token。

## 项目结构

| 目录 / 文件 | 职责 |
| --- | --- |
| `src/pages/question/Edit/` | 画布、面板与 AI 编写 |
| `src/pages/question/Stat/` | 问卷统计视图 |
| `src/components/QuestionComponents/` | 题型组件及属性编辑器 |
| `src/store/` | Redux 状态与编辑历史 |
| `src/services/` | 接口客户端与模型集成 |
| `src/router/` | 应用路由 |
| `src/utils/` | 条件逻辑与高级功能工具 |

## 常用命令

| 命令 | 用途 |
| --- | --- |
| `npm run dev` | 启动 Vite 开发服务 |
| `npm run build` | TypeScript 项目检查与 Vite 打包 |
| `npm run preview` | 预览已构建产物 |
| `npm run lint` | 运行 ESLint |
| `npm run format:check` | 检查源码格式 |

## 当前范围与配置

主要路由包括 `/login`、`/register`、`/manage/list`、`/manage/star`、`/manage/trash`、`/question/edit/:id` 与 `/question/stat/:id`。鉴权、持久化和统计接口需要后端实现。现有 AI 代码从浏览器调用服务商；生产集成应通过服务端保护模型凭据，迁移已清理源码及历史中的硬编码密钥。高级题型编辑器本身不等于已接入真实支付、文件存储或完整填写端逻辑。独立 [C 端原型](https://github.com/tuolola/qustion-star-c) 尚未实现全部 B 端组件。

## 视觉标识

以分层表单、编辑控制点与统计图形体现编排和分析，与 C 端使用相近但有区分的视觉语言。

## 许可证与第三方材料

原仓库未提供项目根级许可证。公开仓库本身不等于授予通用开源许可；使用、修改或分发前，请联系维护者确认授权。第三方源码、SDK、字体及资源继续遵循各自附带的许可证。
