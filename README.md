# Gamers Mancos

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
