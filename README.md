# Closet Crush

A preppy, girly outfit maker. Add photos of your clothes, set today's weather and where you're going, and it styles flat-lay outfits around winter 2026 trends.

## How new pieces are added

1. Pick, drop or paste photos.
2. Each photo is cut out into a sticker by an AI background-removal model, and a clothing-recognition model guesses what it is (its top 3 guesses show as one-tap chips).
3. You review every piece before it joins your closet: fix the type, color, pattern or vibe, or switch between the sticker and the original photo.
4. Optional: search Google Images or Google Lens for the exact item, copy or save the product photo, and paste or upload it to use a cleaner shop picture instead.

Everything runs in your browser. Photos never leave your device; the models are downloaded once (about 70 MB) and cached.

## Closet tools

- Grid or swipe view (right to keep, left to remove).
- Select mode: tap Select (or long-press a piece), tap several pieces, delete them all at once. Every delete has Undo.

## Models

- Background removal: [briaai/RMBG-1.4](https://huggingface.co/briaai/RMBG-1.4) (8-bit). Bria's license allows non-commercial use only.
- Clothing recognition: [Xenova/mobileclip_s0](https://huggingface.co/Xenova/mobileclip_s0) (Apple MobileCLIP-S0), with text labels precomputed for clothing types, patterns and vibes.
- Runtime: [Transformers.js](https://github.com/huggingface/transformers.js) 3.7.5 in a Web Worker.
