# Scoop Bucket of Monospace Fonts

<!-- Uncomment the following line after replacing placeholders -->
[![Tests](https://github.com/naderi/scoop-monospace-fonts/actions/workflows/ci.yml/badge.svg)](https://github.com/naderi/scoop-monospace-fonts/actions/workflows/ci.yml) [![Excavator](https://github.com/naderi/scoop-monospace-fonts/actions/workflows/excavator.yml/badge.svg)](https://github.com/naderi/scoop-monospace-fonts/actions/workflows/excavator.yml)

# Monospace Fonts Scoop Bucket

A [Scoop](https://scoop.sh/) bucket for installing **monospaced fonts** on Windows.

This bucket provides a convenient way to install programming and terminal fonts using Scoop, including fonts that are not available in the default Scoop buckets.

## Installation

First, make sure [Scoop](https://scoop.sh/) is installed.

Add this bucket:

```
scoop bucket add monospace-fonts https://github.com/naderi/scoop-monospace-fonts
```

Then install a font:

```
scoop install font-courier-prime
```

## Available Fonts

The bucket contains a collection of monospaced fonts suitable for:

- Software development
- Code editors
- Terminal applications
- Command-line interfaces
- Text editors
- IDEs

Browse the `bucket` directory to see all available fonts.

## Font Installation

Fonts are installed using Scoop manifests and a shared font installation helper.

The bucket supports both:

- **Per-user installation** — no administrator privileges required
- **System-wide installation** — using Scoop's global installation

For a system-wide installation:

```
sudo scoop install -g font-courier-prime
```

Per-user fonts are installed under:

```
%LOCALAPPDATA%\Microsoft\Windows\Fonts
```

System-wide fonts are installed under:

```
%WINDIR%\Fonts
```

The installation helper registers the fonts with Windows and notifies the system when the font collection changes.

## Supported Formats

The bucket supports:

- TrueType (`.ttf`)
- OpenType (`.otf`)

The original font format supplied by each font author is preserved.

## Updating Fonts

To update a font:

```
scoop update font-courier-prime
```

To update all installed fonts:

```
scoop update *
```

## Uninstalling

Remove a font with:

```
scoop uninstall font-courier-prime
```

The bucket's font helper removes the font files and their Windows font registrations.

## Contributing

Contributions are welcome.

If you would like to add a monospaced font, please submit a pull request containing a Scoop manifest in the `bucket` directory.

Please ensure that:

- The font is actually monospaced.
- The font is legally redistributable under its license.
- The manifest uses the official download source where possible.
- The download URL and SHA-256 hash are correct.
- The font files are installed and uninstalled cleanly.

### Manifest Naming Convention

All font manifests follow a consistent naming convention:

- Use \*\*lowercase\*\* characters.
- Always start the manifest name with `font-`.
- Replace spaces with \*\*dashes (`-`)\*\*.
- Replace underscores (`_`) with \*\*dashes (`-`)\*\*.
- Use the font's commonly recognized name where possible.

### Examples

```text
font-courier-prime.json
font-google-sans-code.json
font-jetbrains-mono.json
font-ibm-plex-mono.json
font-source-code-pro.json
```

## License

This repository contains Scoop manifests and installation scripts. **Individual fonts retain their respective licenses** and are not necessarily licensed under the same license as this repository.

Please refer to each font's manifest and the font author's license for licensing information.

## Disclaimer

This is an unofficial Scoop bucket. It is not affiliated with or endorsed by the authors or publishers of the fonts included in this repository.
