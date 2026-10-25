# ScanPrice

Point your phone camera at a room and see what things cost. Every few seconds the app snaps a frame, an AI vision model names up to 8 objects and estimates a realistic US market price for each, and animated price tags float over the live camera view.

## This repo
- `index.html` – a free working version for GitHub Pages, no sign-up. Objects are spotted on the phone itself (TensorFlow.js COCO-SSD, ~80 common household object types); pictures are never uploaded. Only the item names go to the free, keyless Pollinations text AI for a rough used-price estimate. Includes a running list with an estimated total (handy for a home insurance inventory), share/copy, a "What's it worth?" box for any typed item, and offline install (PWA).

## The real app
Built on Base44 (React + Tailwind, Base44 auth, the `Core.UploadFile` and `Core.InvokeLLM` integrations). Each scan uploads one frame and asks the model for JSON (`name`, `price`, `x`, `y` for up to 8 items). The production build is a compiled bundle tied to Base44's hosted backend, so it isn't included here.

Created by Walter Henderson Jr.
