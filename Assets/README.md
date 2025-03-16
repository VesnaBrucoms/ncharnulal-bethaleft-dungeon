# Asset Guidelines

Complete guidelines at [Tamriel Rebuilt wiki](https://wiki.project-tamriel.com/wiki/Asset_Guidelines).

The following are highlights from the wiki, or info collated from Discord or experience.

## Meshes

Complete file paths are limited to *30* characters. (TLV/u/dwePipeGls_l.nif)

Don't worry about triangulising the quads as the exporter will handle that.

Each mesh segment is *usually* just flag 0.

Flags:

* 3 - Collision (1: hidden + 2: triangle collision)

### Animation

Create the animation by creating keyframes. Each animation must be named with the text group (Dope Sheet->Action). Export to .kf file if using the groups, then both nif files and kf must be included in the Meshes directory.

If hiding parts of the mesh during animations, have frames 0-1 set the visibility of all parts to enabled to ensure that all parts are exported.

## Textures

Resolution must be to the power of 2.

GIMP export settings:

| Setting | Value |
| ------- | ----- |
| Compression | BC1/DXT1 (opaque) OR BC3/DXT5 (trans) |
| Perceptual error metric | Enabled |
| Format | Default |
| Save | ... |
| Flip image vertically | Disabled |
| Mipmaps | Generate mipmaps |
| Transparent index | Disabled |
| **Mipmap options** |
| Filter | Lanczos (or Kaiser or Mitchell) |
| Wrap mode | Clamp (if not tiling) OR Repeat (if tiling) |
| Gamma correction | Enabled |
| Use sRGB colourspace | Enabled |
| Gamma | Default |
| Preserve alpha test | Disabled (opaque) OR Enabled (trans) |
| Alpha test threshold | 0.52 (trans) |

## Icons

aa