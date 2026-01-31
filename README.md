# Gamers Mancos

[![CI](https://github.com/ragnarok22/gamers-mancos/actions/workflows/ci.yml/badge.svg)](https://github.com/ragnarok22/gamers-mancos/actions/workflows/ci.yml)
[![Astro](https://img.shields.io/badge/Astro-5-bc52ee?logo=astro&logoColor=white)](https://astro.build)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-4-06B6D4?logo=tailwindcss&logoColor=white)](https://tailwindcss.com)
[![GSAP](https://img.shields.io/badge/GSAP-3-88CE02?logo=greensock&logoColor=white)](https://gsap.com)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org)
[![ESLint](https://img.shields.io/badge/ESLint-9-4B32C3?logo=eslint&logoColor=white)](https://eslint.org)
[![Prettier](https://img.shields.io/badge/Prettier-3-F7B93E?logo=prettier&logoColor=black)](https://prettier.io)
[![pnpm](https://img.shields.io/badge/pnpm-10-F69220?logo=pnpm&logoColor=white)](https://pnpm.io)

Sitio web para presentar al crew de Gamers Mancos. Pantalla completa con estilo cyber/neon, animaciones con GSAP y una galeria interactiva de gamers.

## Stack

- [Astro](https://astro.build) v5
- [Tailwind CSS](https://tailwindcss.com) v4 (via Vite plugin)
- [GSAP](https://gsap.com) para animaciones

## Estructura

```text
/
├── public/
│   ├── background.png          # Fondo del escenario
│   ├── logo.png                # Logo de Gamers Mancos
│   └── gamers/                 # Fotos de los gamers
│       ├── carlos-lugones.jpg
│       ├── heber.png
│       └── reinier.jpeg
├── src/
│   ├── components/
│   │   └── GamersArena.astro   # Componente principal
│   ├── layouts/
│   │   └── Layout.astro
│   ├── pages/
│   │   └── index.astro
│   └── styles/
│       └── global.css          # Paleta de colores y tokens
└── package.json
```

## Agregar un gamer

Editar el array `gamers` en `src/components/GamersArena.astro`:

```ts
{
  id: "nuevo",
  name: "Nombre Real",
  gamerTag: "TagDelGamer",
  photo: "/gamers/nuevo.jpg",
  bio: "Descripcion corta del gamer.",
  socials: {
    twitch: "https://twitch.tv/nuevo",
    youtube: "https://youtube.com/@nuevo",
    instagram: "https://instagram.com/nuevo",
    twitter: "https://twitter.com/nuevo",
  },
}
```

Colocar la foto en `public/gamers/`.

## Comandos

| Comando        | Accion                               |
| :------------- | :----------------------------------- |
| `pnpm install` | Instala dependencias                 |
| `pnpm dev`     | Servidor local en `localhost:4321`   |
| `pnpm build`   | Build de produccion en `./dist/`     |
| `pnpm preview` | Preview del build antes de desplegar |
| `pnpm format`  | Formatea el codigo con Prettier      |
