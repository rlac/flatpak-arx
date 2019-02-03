# Arx Libertatis Flatpak

A [Flatpak](https://flatpak.org) build of [Arx Libertatis](http://arx-libertatis.org/), a cross-platform port of Arx Fatalis.

## Installation

For now, you can build locally. Install flatpak-builder, then:

```bash
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
flatpak install org.freedesktop.Sdk//18.08
flatpak-builder --install --user builddir org.arx_libertatis.ArxLibertatis.json --force-clean
```

To uninstall:

```bash
flatpak remove org.arx_libertatis.ArxLibertatis
```

## Playing

Either launch the game using the launcher icon, or run from the command line with:

```bash
flatpak run org.arx_libertatis.ArxLibertatis
```

### Setup

Arx Libertatis requires the Arx Fatalis data files to play. You can [buy a DRM free copy from GOG](https://www.gog.com/game/arx_fatalis).

When running the game, it will give you the option to select the .exe setup file downloaded from GOG to extract the required data files.
