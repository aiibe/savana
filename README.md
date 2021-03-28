# Savana (alpha)

A boilerplate built with SvelteKit connected to your Fauna database.

`This is expiremental. Use it at your own risk.`

## Required

- Node version >= 12.17

## Installation

```javascript
npm install
npm run dev -- --open
```

## Deploy on Vercel

1. Go to your Vercel dashboard and create a `new project`
2. Connect it to your Github repo

At import step, make sure to override Vercel build command to `npm run build` and output source to `.vercel_build_output`. Else, you will get an `404 Error` once your site is deployed.
