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
