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
