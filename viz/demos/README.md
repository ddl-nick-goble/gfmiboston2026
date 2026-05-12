# Demo videos

Drop your demo recordings here with these exact filenames so the
deck picks them up automatically:

| Slide | File              | Demo                                          |
|-------|-------------------|-----------------------------------------------|
|  17   | `demo-01.mp4`     | Onboarding a new use case                     |
|  19   | `demo-02.mp4`     | Every model, in one place                     |
|  21   | `demo-03.mp4`     | Starting governance on a new model            |
|  23   | `demo-04.mp4`     | Governed agents inside Excel                  |
|  25   | `demo-05.mp4`     | Excel itself, as a governed model (Part 1)    |
|  26   | `demo-05b.mp4`    | Excel itself, as a governed model (Part 2)    |
|  28   | `demo-06.mp4`     | Customizing a policy                          |
|  30   | `demo-07.mp4`     | Compliance status, at a glance                |
|  32   | `demo-08.mp4`     | Generating documentation, automatically       |
|  34   | `demo-09.mp4`     | Keeping the human in the loop                 |

## Required encoding

- **Container:** `.mp4` (not `.mov`)
- **Codec:** H.264
- **Resolution:** 1920×1080 (matches the 16:9 slide canvas exactly)
- **Frame rate:** 30 fps (24 fps is fine for screen recordings)
- **Audio:** none (or strip it — the deck plays everything muted)
- **Web optimization:** `moov` atom at the start of the file (a.k.a.
  "fast start"). Most modern exporters do this; if your file feels slow
  to start, run it through `ffmpeg -i in.mp4 -c copy -movflags +faststart out.mp4`.

## Size budget

GitHub Pages caps each file at **100 MB** and each repo at **1 GB**.
For 19 minutes total across 10 clips (demo 5 is split into two halves),
target around **60–75 MB per file**
(roughly 5 Mbps at 1080p), which leaves comfortable headroom.

If a clip won't fit, re-encode it with HandBrake's "Web Optimized" toggle
at constant quality 22–24, or drop the bitrate further. Screen-recording
content compresses very well.
