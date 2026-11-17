**English** | [简体中文](./readme-zh-cn.md)

<p align="center">
  <img src="./docs/brand/logo.png" width="120" height="120" alt="Questionnaire Star · Builder logo" />
</p>

<div align="center">

# Questionnaire Star · Builder

<p><strong>Compose questionnaires on a visual canvas</strong></p>

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

## Overview

A React and TypeScript questionnaire builder with a drag-and-drop editing canvas, component property panels, Redux-based editing history, questionnaire management pages and statistics views. The source also contains AI-assisted questionnaire authoring and advanced feature editors. Backend services and provider integrations must be configured separately.

## Capabilities

| Area | Scope |
| --- | --- |
| Visual editing | Arrange components with dnd-kit, edit properties and manage layers. |
| Question library | Text, input, choice, rating, matrix, ranking, file, signature and other question components. |
| Editing state | Redux Toolkit and redux-undo organize selection, copied components and undo history. |
| Management and statistics | List, starred and trash pages plus questionnaire statistics views. |
| Advanced authoring | AI chat and editors for conditional rules, validation and multi-page configuration. |

## Quick Start

Use a Node.js version supported by Vite 7 and the committed dependency lockfile.

```bash
git clone https://github.com/tuolola/questionnaire-star---react.git
cd questionnaire-star---react
npm ci
npm run dev
```

Open the URL printed by Vite, normally `http://localhost:5173`. The development proxy forwards `/api` to `http://localhost:3001`; run a compatible backend separately or update `vite.config.ts`. The API client expects `{ errno, data, msg }` responses and uses a bearer token for authenticated requests.

## Repository Layout

| Path | Responsibility |
| --- | --- |
| `src/pages/question/Edit/` | Canvas, panels and AI authoring |
| `src/pages/question/Stat/` | Questionnaire statistics views |
| `src/components/QuestionComponents/` | Question component definitions and editors |
| `src/store/` | Redux state and editing history |
| `src/services/` | API clients and model integration |
| `src/router/` | Application routes |
| `src/utils/` | Conditional logic and advanced feature helpers |

## Common Commands

| Command | Purpose |
| --- | --- |
| `npm run dev` | Start Vite development server |
| `npm run build` | TypeScript project build and Vite bundle |
| `npm run preview` | Preview a completed build |
| `npm run lint` | Run ESLint |
| `npm run format:check` | Check source formatting |

## Current Scope and Configuration

Routes include `/login`, `/register`, `/manage/list`, `/manage/star`, `/manage/trash`, `/question/edit/:id` and `/question/stat/:id`. A server must supply authentication, persistence and statistics APIs. Existing AI code calls a provider from the browser; a production integration should route through a server that keeps provider credentials private. Hardcoded credentials were removed from the migrated source and history. Advanced field editors do not by themselves provide production payment processing, file storage or complete respondent-side execution. The separate [respondent prototype](https://github.com/tuolola/qustion-star-c) does not yet implement all builder components.

## Visual Identity

Layered form tiles, selection handles and a chart distinguish the builder from the respondent logo.

## License and Third-Party Material

The source repository does not provide a project-level root license. Public visibility alone does not grant a general open-source license; confirm permission with the maintainer before reuse or redistribution. Third-party code, SDKs, fonts and assets retain their own included licenses.
