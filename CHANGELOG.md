> Important: Transfer and working-space features are still in active development. Please do not report bugs/issues related to these features yet.

# Unmcrawesome 1.9.8

### Added

- Added full project aspect ratio preset selection in New Project, matching the editor crop ratio options.
- Added live Aspect Ratio switching in Timeline Project settings (alongside color profile and frame rate).
- Added favorite aspect ratios with a star toggle, and favorites are now remembered app-wide for all projects.
- Added missing 50 fps and 100 fps frame rate options in project settings.
- Added right-edge safety padding in timeline tracks to reduce gesture-navigation conflicts near the screen edge.
- Added live clip reordering while dragging with smoother swap behavior.
- Added a quick Snap action directly in the timeline bottom bar for faster gap compaction access.
- Added clip move mode toggle in the timeline bar: Locked for live swap/reorder and Free Move for manual gap creation.

### Added (Work In Progress)

- Added new transfer functions for grading and timeline workflows: Cineon Log, V-Log, DaVinci Intermediate, ACEScct, Canon Log 3, S-Log3, LogC3, F-Log, and Linear.
- Added matching wide-gamut working spaces: Cineon Film, V-Gamut, DaVinci Wide Gamut, ACES AP1, Cinema Gamut, S-Gamut3, S-Gamut3.Cine, ARRI Wide Gamut, and F-Gamut.

### Changed

- Project aspect ratio now acts as the timeline canvas rule, so clips with different shapes fit inside it instead of being cropped.
- Timeline and editor preview now better reflect project framing, including expected black bars when needed.
- Improved first imported clip behavior so project resolution is derived while respecting the chosen project aspect ratio.
- Removed the custom project aspect ratio option from New Project in favor of the expanded preset list.
- Improved the Project aspect ratio popup so it stays compact and scrolls instead of expanding across the screen.
- Redesigned the New Project window to better handle large aspect ratio lists and make setup easier to scan.
- Increased New Project window width for a less cramped layout.
- Improved player Calibration UX by replacing the bottom popout with a scrollable context menu from the Calibration button.
- Improved timeline clip dragging with smarter edge auto-scroll for long timelines.
- Set clip move mode to default to Locked for new and existing projects.
- In Free Move, dragging a clip can now create gaps while moving following clips together as a train.
- Improved lock mode consistency so clips no longer create gaps while in Locked mode.
- Improved free-move dragging so clips no longer visually jump back before a second drag.
- Updated locked reordering to preserve existing gaps instead of collapsing clips together.
- Improved Timeline Project submenu scrolling with a bottom fade cue so it is clearer when more options are available.
- Improved update-check error reporting so unsupported/strict AOSP network stacks now show actionable failure reasons.

### Fixed

- Fixed an issue where MCRAW video export could fail on some devices with "Failed to open MCRAW metadata".
- Fixed timeline export sizing so Original follows the project aspect/output framing more reliably.
- Fixed LUT selection feedback so the currently chosen LUT is also clearly highlighted in the LUT list.
- Fixed timeline play/pause stutter and startup audio repetition during editor playback.
- Fixed a project load issue where clips could reopen with an unintended gap at the start of the timeline.
- Fixed repeated preview cache restart spam after reopening some saved projects, improving timeline stability.
- Fixed clip drag grip stability so the dragged clip stays aligned with your finger during slow interactions and swaps.
- Fixed timeline gap preview behavior so empty gaps now display black instead of showing a stale frame from a previous clip.
- Fixed HEVC 10-bit Rec.2020-10 SDR delivery metadata being signaled as PQ on some devices.

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
