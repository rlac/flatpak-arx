# Arx Libertatis Flatpak

A [Flatpak](https://flatpak.org) build of [Arx Libertatis](http://arx-libertatis.org/), a cross-platform port of Arx Fatalis.

## Installation

For now, you can build locally. Install flatpak-builder, then:

```bash
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
flatpak install org.freedesktop.Sdk//18.08
flatpak install org.freedesktop.Platform//18.08
flatpak-builder --install --user builddir org.arx_libertatis.ArxLibertatis.json --force-clean
```

To uninstall:

```bash
flatpak remove org.arx_libertatis.ArxLibertatis
rm -Rf ~/.var/app/org.arx_libertatis.ArxLibertatis
```

## Playing

Either launch the game using the launcher icon, or run from the command line with:

```bash
flatpak run org.arx_libertatis.ArxLibertatis
```

### Setup

Arx Libertatis requires the Arx Fatalis data files to play. See the [Arx Libertatis wiki](http://wiki.arx-libertatis.org/Installing_the_game_data_under_Linux) for more information (note: this Flatpak includes cabextract and innoextract). When selecting the data directory to install to during initial setup, ensure you select 'user: /home/...' as other paths will not be writable from within the sandbox.
