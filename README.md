# Portfolio 2026

Interactive developer portfolio showcasing project case studies, immersive 3D experiences, shader demos, and smooth animations. Built with **Vue 3**, **TypeScript**, **Vite**, **Three.js**, **GSAP**, **Lenis**, and **Howler**.

## Features

- 🎨 **Interactive 3D Graphics** - Three.js powered 3D models and scenes
- ✨ **Smooth Animations** - GSAP and Lenis for fluid motion and scroll effects
- 🌍 **Bilingual Content** - English and German support via i18n
- 🎵 **Audio Integration** - Howler for sound sprites and audio management
- 🎬 **Shader Effects** - GLSL shaders compiled via vite-plugin-glsl
- ⚡ **Performance Optimized** - Built with Vite for fast development and production builds
- 📱 **Responsive Design** - Modern styling with SCSS and CSS Grid

## Scripts

| Command        | Description                          |
| -------------- | ------------------------------------ |
| `npm run dev`   | Dev server on port **3000** (`strictPort`) |
| `npm run build` | `vue-tsc` then production bundle to `dist/` |
| `npm run preview` | Serve the production build locally |
| `npm run typecheck` | Typecheck only (`vue-tsc -b`) |

## Content

- **Projects**: `src/content/projects/{en,de}/<slug>.ts` — copy, tags, media, links. Slugs must align with `projectIds` in `src/content/projects/index.ts`.
- **Previews / listing**: `src/content/projects/previews/`.
- **Tags**: variants and labels live in `src/components/tagVariants.ts` (used by `Tag.vue` and content types).

## Stack (high level)

- **Frontend Framework**: Vue 3 with `<script setup>` syntax and TypeScript
- **Build Tool**: Vite with fast HMR and optimized production builds
- **Styling**: SCSS with shared mixins and CSS Grid (`src/assets/styles/`)
- **3D Graphics**: Three.js with custom shaders and models (`src/three/`)
- **Animations**: GSAP for timeline animations and Lenis for smooth scrolling
- **Audio**: Howler for sound management and sprite audio (`src/features/sounds/`)
- **Internationalization**: Custom i18n system (`src/i18n/`)
- **State Management**: Composables pattern for reactive state

## Project Structure

```
src/
├── animations/         # Animation sequences and waypoints
├── assets/             # Images, models, textures, videos, sounds, styles
├── components/         # Vue components (UI, icons, effects)
├── composables/        # Vue composables for state and logic
├── content/            # Project case studies and metadata
├── features/           # Feature modules (home, projects, sounds)
├── i18n/               # Internationalization messages and utilities
├── three/              # Three.js scenes, objects, shaders, utilities
├── types/              # TypeScript type definitions
├── utils/              # Utility functions and helpers
├── App.vue             # Root component
└── main.ts             # Application entry point
```

## Content Organization

- **Projects**: `src/content/projects/{en,de}/<slug>.ts` — copy, tags, media, links. Slugs must align with `projectIds` in `src/content/projects/index.ts`
- **Previews/Listing**: `src/content/projects/previews/` — project metadata for listings
- **Tags**: `src/components/tagVariants.ts` — tag definitions and variants
- **Localized Content**: `src/i18n/messages/` — language-specific strings

## Audio System

- Sound sprites managed in `src/features/sounds/`
- Sprite definitions in `sounds/` directory (AC3 and JSON format)
- Contact and room audio modules with sprite playback

## Getting Started

1. **Install dependencies**:
   ```bash
   npm install
   ```

2. **Start development server**:
   ```bash
   npm run dev
   ```

3. **Build for production**:
   ```bash
   npm run build
   ```

4. **Preview production build**:
   ```bash
   npm run preview
   ```

## Technologies Used

- **Vue 3** - Progressive JavaScript framework
- **TypeScript** - Type safety and better DX
- **Vite** - Next generation build tool
- **Three.js** - WebGL 3D library
- **GSAP** - Animation library
- **Lenis** - Smooth scroll library
- **Howler** - Audio library
- **Sass** - CSS preprocessor

## License

Personal project. All rights reserved.

---

Made with ✨ by [David H]
