# Nuxt Minimal Starter

Look at the [Nuxt documentation](https://nuxt.com/docs/getting-started/introduction) to learn more.

## Setup

Make sure to install dependencies:

```bash
# npm
npm install

# pnpm
pnpm install

# yarn
yarn install

# bun
bun install
```

## Development Server

Start the development server on `http://localhost:3000`:

```bash
# npm
npm run dev

# pnpm
pnpm dev

# yarn
yarn dev

# bun
bun run dev
```

## Static Production Build

Generate the static site for deployment:

```bash
npm run generate
```

The local static build is written to:

```bash
.output/public
```

## Deploying To Netlify

This project includes `netlify.toml`, so Netlify can build it automatically.

Use these settings if entering them manually:

- Build command: `npm run generate`
- Publish directory: `dist`
- Node version: `20`

Netlify's Nuxt static preset writes the deployable output to `dist` during its build. Netlify will provide HTTPS automatically. The config also adds basic browser security headers and cache headers for generated assets.

## Preview Production Build Locally

```bash
npm run generate
npm run preview
```
