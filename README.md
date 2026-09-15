# 67 Park — Kimi island (optimized preview)

An optimized copy of the Kimi island preview at commit 01eb67b (build drive-35). Same game, same
models, same textures. Every change is transport or per-frame housekeeping: the loaded geometry,
materials and textures are byte-identical to the original.

- `island/ada_calisma.glb`: lossless meshopt transport compression, 19.2 MB → 10.5 MB.
- Six island patch files ship as verified difference files (`*.dd1.bin`) that rebuild the originals
  exactly (SHA-256 checked; the original `.bin` files stay as a fallback), 22.8 MB less to download.
- `island/lunapark-v1/lighthouse.glb`: lossless meshopt, 580 KB → 363 KB.
- The island preload queue no longer requests files the runtime has already fetched.
- Less per-frame allocation in the shadow cache and the chat speech bubbles.

Original preview: https://oscarbrendonn.github.io/67park-kimi-preview-20260914/
