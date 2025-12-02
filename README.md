[![lint config](https://img.shields.io/badge/lint-standard-brightgreen.svg)](https://github.com/standard/eslint-config-standard)
# Remix Starter Template
Refer to the [Remix documentation](https://remix.run/docs/en/main) to learn more.
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
Start the development server on `http://localhost:5173`:
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
## Production
Build the application for production:
```bash
# npm
npm run build
# pnpm
pnpm build
# yarn
yarn build
# bun
bun run build
```
Locally preview production build:
```bash
# npm
npm run preview
# pnpm
pnpm preview
# yarn
yarn preview
# bun
bun run preview
```
Check out the [deployment documentation](https://remix.run/docs/en/main/guides/deployment) for more information.
## Todo
- [ ] eventually replace `"radix-ui": "https://pkg.pr.new/radix-ui@2847",` when the "Compound component" bug is fixed:
  - https://github.com/radix-ui/primitives/issues/2847
- [ ] check back on this prettier-plugin-organize-imports thread:
  - https://github.com/simonhaenisch/prettier-plugin-organize-imports/issues/89
- [ ] figure out why enabling AST parsing for organize-imports solves all my "import order" problems???
  - https://github.com/simonhaenisch/prettier-plugin-organize-imports/issues/89
- [ ] eventually remove explicit `prettier.config.mjs` flag in `package.json` once Prettier >3.2 recognizes `.mjs` config files natively
- [ ] figure out why `'selector-class-pattern': null` in ./stylelint.config.mjs is necessary for organize-imports not to break, aka why @layer base breaks stylelint. thank god for @remix-run/css removing the need to have custom font imports via @font-face
## notes
- [ ] the pnpm jimp override in package.json is from: https://github.com/remix-run/remix/issues/847
- give this a try later, like on the 8kb bundle size page where I got it from:
```html
<svg class="hidden" xmlns="http://www.w3.org/2000/svg">
  <desc>https://performance.dev/optimizations/</desc>
  <filter id="noise" height="300%">
    <feTurbulence
      baseFrequency="0.05 0.03"
      numOctaves="3"
      result="n0"
    ></feTurbulence>
    <feDisplacementMap
      in="SourceGraphic"
      in2="n0"
      result="m0"
      scale="6"
    ></feDisplacementMap>
    <feComposite
      in="SourceGraphic"
      in2="m0"
      operator="atop"
      result="c0"
    ></feComposite>
    <feTurbulence baseFrequency="2" numOctaves="3" result="n1"></feTurbulence>
    <feDisplacementMap
      in="c0"
      in2="n1"
      result="m1"
      scale="2"
    ></feDisplacementMap>
    <feComposite in="c0" in2="m1" operator="atop" result="c1"></feComposite>
    <feOffset dx="-2" dy="-2" in="c1"></feOffset>
  </filter>
</svg>
<svg class="hidden" xmlns="http://www.w3.org/2000/svg">
  <filter id="grain">
    <feTurbulence
      baseFrequency="0.05 0.03"
      numOctaves="3"
      result="n0"
    ></feTurbulence>
    <feDisplacementMap
      in="SourceGraphic"
      in2="n0"
      result="m0"
      scale="6"
    ></feDisplacementMap>
    <feComposite
      in="SourceGraphic"
      in2="m0"
      operator="atop"
      result="c0"
    ></feComposite>
    <feTurbulence baseFrequency="2" numOctaves="3" result="n1"></feTurbulence>
    <feDisplacementMap
      in="c0"
      in2="n1"
      result="m1"
      scale="2"
    ></feDisplacementMap>
    <feComposite in="c0" in2="m1" operator="atop" result="c1"></feComposite>
    <feOffset dx="-2" dy="-2" in="c1"></feOffset>
  </filter>
</svg>
```

# PR Update: 2025-12-03 02:02:22
