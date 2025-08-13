# Pokédex — React + TypeScript

Un Pokédex moderne construit avec **Vite + React + TypeScript**, **Redux Toolkit**, **React Router** et **Tailwind CSS**.  
UI inspirée du design “cartes blanches + moitié colorée par type”, bandeau **jaune** en header, **favoris** avec cœur, **recherche**, et **défilement infini**.

---


## ✨ Fonctionnalités

- 🧾 **Cartes** blanches arrondies, moitié **colorée** selon le **type** principal.
- 📄 **Page détail** : image HD, types, taille/poids, stats.
- 📱 **Responsive** (grille 1–4 colonnes).
- 🧭 **Navigation** via React Router.

---

## Technologies

- **Vite** + **React** + **TypeScript**
- **Redux Toolkit** + `react-redux`
- **React Router`
- **Tailwind CSS** (PostCSS)
- **Axios**
- **PokeAPI** — https://pokeapi.co

---

## 🚀 Prise en main

### Prérequis
- **Node.js 18+**
- **npm** (ou pnpm/yarn)

### Installation
```bash
npm install
```

### Lancer en développement
```bash
npm run dev
```

### Build production
```bash
npm run build
npm run preview
```

---

## 🔌 Configuration Tailwind (PostCSS)

Si tu utilises **Tailwind v4** (recommandé) et que tu vois l’erreur
> “It looks like you're trying to use `tailwindcss` directly as a PostCSS plugin…”

fais ceci :

1) Installe le plugin PostCSS dédié :
```bash
npm i -D @tailwindcss/postcss autoprefixer
```

2) **postcss.config.js**
```js
import tailwind from "@tailwindcss/postcss";
import autoprefixer from "autoprefixer";

export default {
  plugins: [tailwind(), autoprefixer()],
};
```

3) **src/index.css**
```css
@tailwind base;
@tailwind components;
@tailwind utilities;

/* Thème clair façon Pokédex moderne */
html, body, #root { height: 100%; }
:root { color-scheme: light; }
body { @apply bg-neutral-50 text-slate-900; }
a { @apply text-slate-800; }
```

> Alternative : rester en Tailwind v3 — installe `tailwindcss@3` et utilise `tailwindcss()` dans `postcss.config.*`.

---


