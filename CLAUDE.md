# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

AI学習プラットフォーム - YouTube動画を活用したUdemyライクな講座プラットフォームのMVP開発。AIでプログラム開発したいエンジニア・非エンジニア向けの学習サービス。

## Essential Commands

```bash
npm run dev        # Start development server on http://localhost:3000
npm run build      # Create production build
npm run start      # Start production server
npm run lint       # Run ESLint for code quality checks
```

## Architecture Overview

### Tech Stack

- **フロントエンド**: Next.js 15.4.3 (App Router), React 19.1.0, TypeScript
- **スタイリング**: Tailwind CSS v4
- **データベース**: Supabase (PostgreSQL)
- **認証**: Supabase Auth (Google OAuth)
- **動画**: YouTube埋め込み
- **デプロイ**: Vercel

### Directory Structure

```
src/
└── app/                # Next.js App Router pages
    ├── layout.tsx      # Root layout with fonts and metadata
    ├── page.tsx        # Home page component
    └── globals.css     # Global styles with Tailwind directives
```

### Key Configuration

- **TypeScript**: Path alias `@/*` maps to `./src/*`
- **ESLint**: Configured with Next.js recommended rules using flat config format
- **Development**: Uses Turbopack for faster development builds

## Development Workflow

When developing new features:

1. Place all new pages in `src/app/` following Next.js App Router conventions
2. Create reusable components in `src/components/` (create directory if needed)
3. Use the `@/` import alias for cleaner imports from the src directory
4. Follow the existing TypeScript strict mode configuration

## Important Notes

- No test framework is currently configured
- No environment variables are set up yet
- The project uses the latest stable versions of all dependencies
- Tailwind CSS v4 is configured with PostCSS (not the legacy config format)