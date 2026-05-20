# Unmcrawesome 2.3.4

## Added

- Added an HSL color mixer next to the Color category. Each of the eight bands (Red, Orange, Yellow, Green, Aqua, Blue, Purple, Magenta) has its own Hue, Saturation, and Luminance sliders, letting you fine-tune individual colors without affecting the rest of the image. The sliders themselves preview the result as a live color gradient, and the Saturation and Luminance gradients update in real time as the Hue slider moves so you can see exactly which color and brightness the slider is heading toward. The 3-way color wheels (Shadows / Midtones / Highlights) now live under the same HSL category so all the per-color grading tools are in one place.

## Changed

- Replaced the old flash-switch between editing categories with a soft fade so the controls cross-fade in and out when you tap a different category.

## Fixed

- Fixed color matrix not loading on the first scrub into a new timeline clip. Each clip's matrix now applies correctly from the very first frame, including the first clip in a multi-clip timeline after navigating between clips.
- Fixed switching DCP profiles in the editor having no visible effect on the preview. Changing the selected profile now actually updates the colors.
- Fixed DCP looking like it briefly turned off whenever a slider was touched. The hue/saturation and look table parts of the DCP were being skipped during slider drags in the low-resolution interaction preview; they now apply consistently across both the idle and interaction previews.
- Stopped the edit panel from dropping the preview to low-resolution interaction mode on stray taps over empty panel area. The interaction preview now only kicks in when a slider is actually being dragged.
- Fixed long Vulkan exports freezing on a single frame partway through and repeating it until the end. Affected every export codec on long clips. Multi-minute exports now finish cleanly.
- Fixed the Straighten slider under the Crop category doing nothing. It now rotates the image again in both the live preview and the exported video, and the preview updates continuously as you drag the slider instead of only after letting go.
- Stopped a long press on the preview from briefly switching to the original image while you are in the Crop category. Long-press to compare is now disabled in Crop mode so you can drag the grid handles without the preview swapping under your finger.

---

**BUG REPORTS:** Bug reports will only be acknowledged if the issue can be reproduced. A screen recording showing the issue and a logcat capture are both required. Please follow this simple structure:

- Which device are you using?
- What is happening exactly?
- Steps to reproduce the issue.
- Screen recording showing the issue (required).
- Logcat capture (required, can be captured from Settings).

**ON BUG FIXES & EXPECTATIONS:** Bug fixes are not guaranteed. Android is a jungle with thousands of different devices, and as a solo hobby project there is simply no way for me to address every single device-specific issue. If something can't be fixed on your device, you'll have to live with it.

# Unmcrawesome 2.3.3

## Added

## Changed

- Faster multi-clip timeline exports, especially around clip switches and crossfade transitions. Two source decoders are now kept warm at once and GPU resources are reused across clips.

## Fixed

- Fixed intermittent magenta and green colour fringing on HEVC and H.264 exports, most visible on moving subjects.
- Fixed timeline exports producing black frames for the entire duration of every crossfade between two clips. All transition types affected.
- Fixed occasional green/magenta corruption on a single transition frame between two clips of different resolutions.

---

**BUG REPORTS:** Bug reports will only be acknowledged if the issue can be reproduced. A screen recording showing the issue and a logcat capture are both required. Please follow this simple structure:

- Which device are you using?
- What is happening exactly?
- Steps to reproduce the issue.
- Screen recording showing the issue (required).
- Logcat capture (required, can be captured from Settings).

**ON BUG FIXES & EXPECTATIONS:** Bug fixes are not guaranteed. Android is a jungle with thousands of different devices, and as a solo hobby project there is simply no way for me to address every single device-specific issue. If something can't be fixed on your device, you'll have to live with it.

# Unmcrawesome 2.3.2

## Added

## Changed

- The Quad Bayer remosaic step now runs entirely on the GPU. Previously part of this work was handled on the CPU, so playback and export should feel a bit lighter on the device, and the remosaicing itself should look slightly cleaner thanks to the improved pipeline.
- Reworked the sharpening tool so that both the amount and radius sliders feel less aggressive at the same numeric values. Previously even moderate settings could produce visible halos and over-sharpened edges, so the effective intensity of both sliders has been roughly halved across the entire range to give finer, more usable control without changing the slider limits or breaking existing saved edits.

## Fixed

- Fixed an issue where the RAW frame would not be demosaiced correctly on some older generation GPUs when using the Vulkan rendering path, which could produce garbled or visibly incorrect colors instead of a clean image.
- Fixed a pink/magenta tint that could appear on certain Bayer sensor layouts (GRBG and GBRG) when playing back clips on some older Adreno GPUs. The fix that previously landed for the Vulkan editor preview has now been extended to the OpenGL gallery player so playback in the main menu also displays correct colors on those devices.
- Fixed an issue where the vignette slider only worked in the dark direction. Pulling the slider toward the negative side now correctly applies a light vignette, brightening the edges of the frame, instead of doing nothing as it did before.
- Fixed an issue where edit settings from the last clip you opened in the editor could leak into other clips during normal gallery playback. For example, applying a CFA pattern override on one video and then going back to play a different one would re-apply that override to the new clip until the app was restarted; playback now correctly uses each clip's own settings.
- A handful of smaller under the hood fixes for stability and consistency.

---

**BUG REPORTS:** Bug reports will only be acknowledged if the issue can be reproduced. A screen recording showing the issue and a logcat capture are both required. Please follow this simple structure:

- Which device are you using?
- What is happening exactly?
- Steps to reproduce the issue.
- Screen recording showing the issue (required).
- Logcat capture (required, can be captured from Settings).

**ON BUG FIXES & EXPECTATIONS:** Bug fixes are not guaranteed. Android is a jungle with thousands of different devices, and as a solo hobby project there is simply no way for me to address every single device-specific issue. If something can't be fixed on your device, you'll have to live with it.

# Unmcrawesome 2.3.1

## Added

## Changed

## Fixed

- Fixed cropped HEVC 10-bit exports that could freeze on input-buffer devices or squeeze 4:3 footage into 16:9 output on native 10-bit surface devices.

# Unmcrawesome 2.3.0

## Added

## Changed

- Replaced AMaZE demosaic with RCD. After careful investigation via RawTherapee, RCD seems to be the best balance between fine details, color fringing, chromatic-aberration-like pixels on dark edges in contrasty scenes, and moire. RCD is more expensive in its current state, so export performance will be affected, sometimes a lot and sometimes less. This might improve in the future, but there are no guarantees. I prefer quality over export performance. Because demosaicing changed completely, new bugs are likely in areas that worked fine before, so it may take a few updates to polish everything.

## Fixed
