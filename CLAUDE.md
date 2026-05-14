# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**Vibe Coding Manual** — a single-file static website (`index.html`) serving as a comprehensive guide for 5 vibe coding tools: Claude, GitHub, Supabase, Vercel, and VS Code.

No build system, no package manager. All code lives in `index.html` with inline CSS and JS. External dependencies via CDN only (Google Fonts, Font Awesome).

## Design Spec

**Colors:**
- Page background: `#0d1f0d` (dark green)
- Nav background: `#1a1a1a` (dark gray)
- Sidebar background: `#162016`
- Accent yellow: `#f5c518`
- Tool brand colors: Claude `#d97706`, GitHub `#ffffff`, Supabase `#3ecf8e`, Vercel `#ffffff`, VS Code `#007acc`

**Layout:** Fixed top nav + fixed left sidebar (desktop) + scrollable main content + footer. Hamburger menu for mobile.

## Navigation Structure

**Top nav tabs:** Home | Claude | GitHub | Supabase | Vercel | VS Code | (separated) 사용자매뉴얼

**Sidebar menus per tool:**
- **Claude:** 소개, 설치방법, 기본사용법, 고급기능, 프롬프트 엔지니어링, 토큰 절감방안, Anthropic 이야기
- **GitHub:** 소개, 설치방법, 기본사용법, 협업 워크플로우, GitHub Flow, 마크다운 문법, GitHub Actions
- **Supabase:** 소개, 설치방법, 데이터베이스, 인증, API, 스토리지, RLS & 보안, 벡터DB & AI
- **Vercel:** 소개, 설치방법, 배포방법, 도메인 설정, 환경변수
- **VS Code:** 소개, 설치방법, 기본사용법, 확장프로그램, 단축키
- **사용자매뉴얼:** 시작하기, 화면구성, 주요기능, 자주 묻는 질문

## Key Interactions

- Tab click → switch active tool, update sidebar, show content (fade transition)
- Sidebar item click → scroll to or show corresponding content section
- Logo click (nav or sidebar) → go to home
- Copy buttons on code/command snippets → Clipboard API
- Mobile: hamburger toggles sidebar overlay

## Home Page

Hero section with title "바이브코딩 완벽 매뉴얼" + bold yellow subtitle → 5 tool cards (with brand-color top border) → vertical timeline installation roadmap (with copy buttons on commands).

## Footer

3-column layout, column titles in uppercase yellow: ABOUT | GUIDES | LINKS
