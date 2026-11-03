MUSE — REEL THUMBNAILS
======================

Drop your 8 reel cover screenshots here, named EXACTLY:

  reel1.webp   → https://www.instagram.com/reel/DaiiHdCNkku/
  reel2.webp   → https://www.instagram.com/reel/Dai-iyjNbe3/
  reel3.webp   → https://www.instagram.com/reel/DaK9P-LqvF4/
  reel4.webp   → https://www.instagram.com/reel/DZAFPTotbDK/
  reel5.webp   → https://www.instagram.com/reel/DYZyvk_M7MK/   (Alkaram collab — featured)
  reel6.webp   → https://www.instagram.com/reel/DXom2W_DG0f/
  reel7.webp   → https://www.instagram.com/reel/DXhUKlOjCk-/
  reel8.webp   → https://www.instagram.com/reel/DWEgOW4jGtG/

HOW TO GET EACH IMAGE (2 min on your phone):
  1. Open the reel in Instagram — it shows the cover frame
  2. Take a screenshot
  3. Crop to just the video area if you like (optional)
  4. Save as reel1.webp ... reel8.webp and put them in this folder

Portrait images (9:16) look best. .webp, .png, or .webp all work
(if you use .png/.webp, keep the same names, e.g. reel1.png).

Once they're here, run `npm run build` — the cards show them automatically.
Until then, cards show an elegant branded placeholder.

PLAYING REELS ON THE SITE (autoplay)
====================================
Instagram's embed often refuses to play reels inline (especially reels with
licensed music) and sends people to the app instead. To have reels autoplay
on the website, add the video files here and point each reel at its file:

  reel1.mp4 ... reel7.mp4  (vertical 9:16, 720p, ideally under 3 MB each)

then in src/reels.ts add  video: "/reels/reel1.mp4"  to that reel's line.
Reels with a video autoplay muted (tap the speaker to unmute); the home
carousel moves to the next reel when each clip ends. Reels without a video
fall back to the Instagram embed.
