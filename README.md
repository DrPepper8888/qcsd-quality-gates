# AI-assisted Code Development Quality Gates & Auto-healing

质量门禁&自动修复，适合AI辅助个人开发，保证代码质量，减少低级错误。

## 📋 功能

- ✅ 完整的6步质量门禁检查
- ✅ 自动治理常见问题（依赖错误/路径错误/语法错误/启动失败）
- ✅ 标准化文件结构（Next.js项目）
- ✅ 遵循 Conventional Commits 国际提交规范
- ✅ 结合腾讯全AI自动化研发实践，适配个人开发者多项目并行开发

## 触发条件

- 每次开发新项目，必须执行质量门禁检查
- 每次输出代码给用户，必须过一遍门禁，自动修复问题再交付
- 用户要求检查质量，立即强制执行

## 质量门禁

### 1. 需求阶段
- 需求完整清晰，所有核心需求点都已记录
- 模糊歧义点已经澄清
- 需求范围符合「单人可开发」

### 2. 架构设计阶段
- 技术选型适合个人开发，依赖最小化
- 文件结构符合标准化
- 数据库设计合理，索引正确

### 3. 编码阶段
- TypeScript语法正确
- 所有import路径正确
- 变量函数命名清晰
- 没有冗余代码，注释够用
- 所有需求点都已实现

### 4. 依赖检查
- `package.json` 包含所有需要的依赖
- 没有多余依赖
- 版本选择稳定

### 5. 环境配置
- `.env.example` 包含所有需要的环境变量
- 每个配置项有说明注释

### 6. 交付前整体检查
- 所有需求点都已实现
- `README.md` 完整（介绍+配置+启动命令）
- 数据库初始化SQL完整
- `.gitignore` 正确

## 自动治理

- **依赖安装报错** → 自动分析错误，修改版本或移除冲突依赖
- **import路径错误** → 自动查找正确路径修复
- **语法错误** → 自动修正语法和类型错误
- **启动失败** → 自动读取错误日志，定位问题修复
- **缺失文件** → 自动创建

## 标准化文件结构 (Next.js)

```
project-name/
├── app/
│   ├── page.tsx
│   ├── layout.tsx
│   ├── globals.css
│   └── types.ts
├── lib/
│   ├── supabase.ts
│   ├── openai.ts
│   └── *.ts
├── public/
├── data/
├── .env.example
├── .gitignore
├── package.json
├── tsconfig.json
├── next.config.js
├── tailwind.config.ts
├── postcss.config.js
├── README.md
└── *-init.sql
```

## 代码质量标准

- TypeScript：正确类型，不滥用any
- 命名：清晰见名知意
- 注释：复杂逻辑有注释
- 样式：优先Tailwind CSS，不写冗余CSS
- 冗余：删除没用的代码

## 作者

辛昊洋 + 智慧鸭🦆

## 许可证

MIT
