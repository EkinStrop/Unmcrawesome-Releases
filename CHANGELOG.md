# Unmcrawesome 2.3.0

## Added

## Changed

- Replaced AMaZE demosaic with RCD. After careful investigation via RawTherapee, RCD seems to be the best balance between fine details, color fringing, chromatic-aberration-like pixels on dark edges in contrasty scenes, and moire. RCD is more expensive in its current state, so export performance will be affected, sometimes a lot and sometimes less. This might improve in the future, but there are no guarantees. I prefer quality over export performance. Because demosaicing changed completely, new bugs are likely in areas that worked fine before, so it may take a few updates to polish everything.

## Fixed

# Unmcrawesome 2.2.9

## Added

- Added an HD preview toggle to the phone timeline editor for full-resolution timeline preview during editing, playback, and scrubbing, with pinch-to-zoom support.

## Changed

## Fixed

- Fixed tablet/desktop timeline preview so selecting a clip no longer jumps the preview away from the current playhead position, and scrubbing now previews the clip under the playhead even when another clip is selected.
- Fixed HD timeline scrubbing so the preview follows the correct clip while scrubbing across clip boundaries.
- Fixed MotionCam clips recorded with active 16:9 frame areas being shown as padded 4:3 clips with black bars in the gallery, thumbnails, and timeline.
