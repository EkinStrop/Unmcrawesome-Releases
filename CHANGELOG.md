# Unmcrawesome 1.9.7

- Improved export stability on older Qualcomm devices, especially for H.264/HEVC hardware encoding.
- Custom H.264 bitrate selection now behaves correctly on affected devices, so high bitrate choices are respected.
- Reduced background preview-cache interruptions/noise when starting export from the editor.
- Improved removable storage disconnect handling to prevent preview/frame corruption issues in affected sessions.

# Unmcrawesome 1.9.6

- Fixed DNG frame export compatibility so files open correctly in Adobe apps like Photoshop/Lightroom.
- Fixed a color cast in exported DNG frames by correcting raw black/white level metadata.
- Fixed export job cards showing the wrong resolution after crop/rotation edits.
- Added aspect ratio display to export job cards so you can see the final editor ratio at a glance.
- Added a compact Project settings bar in the timeline for quick color profile and frame rate changes.
- Refined clip/project context menus with tighter sizing to reduce empty space and improve readability.
- Fixed Export Queue "Edit" routing so timeline exports reopen the timeline project instead of the single-video editor.

# Unmcrawesome 1.9.5

- Fixed incorrect external storage disconnect warnings for files on internal storage.
- Improved detection of removable storage disconnects to reduce false alerts.
- Fixed portrait videos playing in landscape or stretched in the player.

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
