# Unmcrawesome 1.9.4

- Fixed timeline gestures so one-finger timeline scrolling works again while preserving clip long-hold interactions.
- Expanded custom crop ratios for timeline/grading/export with: 1.19:1, 1.37:1, 1.43:1, 1.50:1, 5:4, 1.66:1, 1.75:1, 1.85:1, 2.00:1, 2.20:1, 2.35:1, 2.39:1, 2.40:1, 2.55:1, 2.59:1, 2.76:1, and 4:5.
- Added end-to-end crop consistency so selected custom ratios match in grading preview, timeline preview, and final export.
- Added interactive crop grid in timeline grading so you can drag/reposition free and preset crops directly in preview.
- Added persistent MCRAW repositories with default source selection, including onboarding setup, Settings management, and timeline media picker switching.
- Added a simple dolly (zoom effect) for clips, with adjustable amount and speed.
- Improved timeline export details so "Original" now clearly reflects the effective output resolution when crop/aspect settings are applied.
- Improved export jobs/history to show the real exported resolution, include bitrate info, and display a thumbnail from the timeline source.
- Improved timeline hardware bitrate handling: Draft/Standard/High/Maximum now scale with device codec limits, and Custom bitrate now follows supported device ranges instead of using a fixed value.

# Unmcrawesome 1.9.3

- Improved sharpening
- Slight improvement on temporal denoising (still WIP)
- Fixed missing audio track when importing MCRAW in timeline
- Fixed grading preview/playback to respect per-clip boundaries instead of the full timeline
- Some other minor fixes

# Unmcrawesome 1.9.2

- Fix timeline zoom desync where clips stopped expanding past ~160%
- Keep ruler and clips aligned at high zoom
- Add filmstrip thumbnail strip in video tracks
- Add track controls: lock, favorite, visibility
- Improve clip name readability over the filmstrip
