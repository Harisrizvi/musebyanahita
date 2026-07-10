MUSE — HERO SCROLL IMAGE SEQUENCE
==================================

Drop your hero banner frames in THIS folder.

NAMING (important — must be zero-padded, sequential):
  frame-0001.jpg
  frame-0002.jpg
  frame-0003.jpg
  ...
  frame-0120.jpg   (etc.)

RECOMMENDED:
  - Count:   60–150 frames (120 is a good sweet spot)
  - Format:  .jpg (smaller) or .webp (best) — if you use .webp,
             change the extension in ScrollSequence config (see below)
  - Size:    1920×1080 (16:9) or 1600×2000 (portrait) — keep them
             all the SAME dimensions
  - Weight:  aim for < 200 KB per frame (compress them!) so the
             total sequence stays light

HOW TO GET FRAMES FROM A VIDEO (using ffmpeg):
  ffmpeg -i salon.mp4 -vf "fps=24,scale=1600:-1" frame-%04d.jpg
  (that pulls 24 frames per second, scaled to 1600px wide)

AFTER ADDING FRAMES:
  Open  src/components/ScrollSequence.tsx  and set:
    FRAME_COUNT   = <how many frames you added>
    FRAME_PATH    = "/hero-sequence/frame-"   (leave as-is)
    FRAME_EXT     = ".jpg"                     (or ".webp")
  Then run:  npm run build

That's it — the scroll sequence will play your frames automatically.
