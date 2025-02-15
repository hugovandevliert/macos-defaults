---
title: Flash clock time separators | Menu Bar
description: When enabled, the clock indicator (which by default is the colon) will flash on and off each second.
head:
  - - meta
    - property: 'og:title'
      content: macOS defaults > Menu Bar > Flash clock time separators
  - - meta
    - property: 'og:description'
      content: When enabled, the clock indicator (which by default is the colon) will flash on and off each second.
---

# Flash clock time separators

When enabled, the clock indicator (which by default is the colon) will flash on and off each second.

<!-- break lists -->

- **Tested on macOS**:
  - Ventura
  - Monterey
  - Big Sur
  - Catalina
  - Mojave
- **Parameter type**: bool

## Set to `false` (default value)

The time separator stays solid continuously.

```bash
defaults write com.apple.menuextra.clock "FlashDateSeparators" -bool "false" && killall SystemUIServer
```

<video autoplay loop muted playsinline width="727" height="40" style="max-width: 100%; height: auto">
  <source src="./images/FlashDateSeparators/false.mp4" type="video/mp4">
  Example output with value set to false
</video>

## Set to `true`

The time separator flashes every second.

```bash
defaults write com.apple.menuextra.clock "FlashDateSeparators" -bool "true" && killall SystemUIServer
```

<video autoplay loop muted playsinline width="727" height="40" style="max-width: 100%; height: auto">
  <source src="./images/FlashDateSeparators/true.mp4" type="video/mp4">
  Example output with value set to true
</video>

## Read current value

```bash
defaults read com.apple.menuextra.clock "FlashDateSeparators"
```

## Reset to default value

```bash
defaults delete com.apple.menuextra.clock "FlashDateSeparators" && killall SystemUIServer
```
