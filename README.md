# ScanPrice

Point your phone camera at a room and see what things cost. Every few seconds the app snaps a frame, an AI vision model names up to 8 objects and estimates a realistic US market price for each, and animated price tags float over the live camera view.

## This repo
- `index.html` – a self-contained **demo** for GitHub Pages. It uses your camera locally (or an illustrated sample scene) and shows **simulated sample prices**. There's no AI and nothing is uploaded.

## The real app
Built on Base44 (React + Tailwind, Base44 auth, the `Core.UploadFile` and `Core.InvokeLLM` integrations). Each scan uploads one frame and asks the model for JSON (`name`, `price`, `x`, `y` for up to 8 items). The production build is a compiled bundle tied to Base44's hosted backend, so it isn't included here.

Created by Walter Henderson Jr.
