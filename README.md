# 🖌️ Paint – MS Paint in your browser

A tiny, tongue-in-cheek recreation of classic Microsoft Paint, rebuilt for the web.  
Same vibes, no `C:\Windows\System32` required.

<img width="806" height="625" alt="Screenshot 2025-12-02 at 14 30 56" src="https://github.com/user-attachments/assets/ab18bdc5-92a6-4813-8b6c-be346ffee936" />


> 💾 Fan project – not affiliated with or endorsed by Microsoft.
>
> Built just for fun, nostalgia and doodling in meetings.

---

## ✨ Features

- 🎨 **Classic UI clone**  
  Pixel-perfect window chrome, menu bar, toolbar and color palette inspired by old-school MS Paint.

- 🖍️ **Drawing on the `<canvas>`**  
  Freehand drawing with the pencil/brush tool on a resizable canvas.

- 🧽 **Eraser & clear canvas**  
  Oops? Just erase or wipe the whole thing and start again.

- 🎯 **Color picker**  
  Click a swatch in the palette to switch drawing color instantly.

---

## 🚀 Live demo

👉 **[Open Paint in your browser](https://paint.anatole.co)**  

---

## 📦 Getting started

Clone the repo:

```bash
git clone https://github.com/hopeugetherpes/paint.git
cd paint
corepack enable
pnpm install --frozen-lockfile
pnpm dev
```

Use Node.js 20.9 or newer and the pnpm version pinned in `package.json`.
Vercel detects the Next.js project and the committed pnpm lockfile automatically.

## 🔐 Dependency maintenance

Run `pnpm audit` to check all dependencies, including development and optional
packages. Security overrides in `pnpm-workspace.yaml` keep every transitive
copy of PostCSS, Sharp and Lodash on patched releases.

The styles use Tailwind CSS 4 to avoid the unpatched `braces` dependency in the
older build pipeline. The existing Paint colours, fonts and layout are preserved.
Supported browsers are Safari 16.4+, Chrome 111+ and Firefox 128+.

Validate changes with `pnpm build` and `pnpm exec tsc --noEmit`.
