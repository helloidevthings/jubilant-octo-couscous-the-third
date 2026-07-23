# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Next.js 16.1 application using React 19.2 with the React Compiler enabled. The project follows the Next.js App Router architecture with the source code located in `src/app/`.

## Development Commands

### Running the Development Server
```bash
npm run dev
```
The app runs on http://localhost:3000

### Building for Production
```bash
npm run build
```

### Starting Production Server
```bash
npm start
```

### Linting
```bash
npm run lint
```

## Architecture

### Project Structure
- **`src/app/`** - App Router directory containing pages, layouts, and route components
  - `layout.js` - Root layout component with font configuration (Geist Sans and Geist Mono)
  - `page.js` - Home page component
  - `*.module.css` - CSS Modules for component-specific styles
  - `globals.css` - Global stylesheet
- **`public/`** - Static assets (SVG files for icons and logos)
- **`@/*`** path alias maps to `./src/*` (configured in jsconfig.json)

### Key Configuration

**React Compiler**: Enabled in `next.config.mjs` with `reactCompiler: true`. This is an experimental optimization feature that compiles React components for better performance.

**ESLint**: Uses the Next.js Core Web Vitals preset with custom global ignores for build artifacts (`.next/`, `out/`, `build/`, `next-env.d.ts`).

### Font Optimization
The app uses `next/font` to optimize and load Google Fonts (Geist and Geist Mono). Fonts are configured with CSS variables in the root layout.
