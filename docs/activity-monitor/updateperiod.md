---
title: Update Frequency | Activity Monitor
description: How frequently Activity Monitor should update its data, in seconds.
head:
  - - meta
    - property: 'og:title'
      content: macOS defaults > Activity Monitor > Update Frequency
  - - meta
    - property: 'og:description'
      content: How frequently Activity Monitor should update its data, in seconds.
---

# Update Frequency

How frequently Activity Monitor should update its data, in seconds.

<!-- break lists -->

- **Tested on macOS**:
  - Ventura
  - Monterey
- **Parameter type**: int
  - 1
  - 2
  - 5

## Set to `1`

Very often (1s)

```bash
defaults write com.apple.ActivityMonitor "UpdatePeriod" -int "1" && killall Activity\ Monitor
```

## Set to `2`

Often (2s)

```bash
defaults write com.apple.ActivityMonitor "UpdatePeriod" -int "2" && killall Activity\ Monitor
```

## Set to `5` (default value)

Normally (5s)

```bash
defaults write com.apple.ActivityMonitor "UpdatePeriod" -int "5" && killall Activity\ Monitor
```

## Read current value

```bash
defaults read com.apple.ActivityMonitor "UpdatePeriod"
```

## Reset to default value

```bash
defaults delete com.apple.ActivityMonitor "UpdatePeriod" && killall Activity\ Monitor
```
