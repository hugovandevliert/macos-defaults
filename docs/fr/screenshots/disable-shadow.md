---
title: Enlever l'ombre | Capture d'écran
---

::: warning Attention
La langue française n'est plus supportée sur macos-defaults.com. Cette page redirigera automatiquement vers la version anglaise correspondante en 2024.
:::

# Enlever l'ombre

Afficher ou non une ombre en prenant une capture d'une app (`⌘ cmd`+`⇧ shift`+`4` puis `espace`).

<!-- break lists -->

- **Testé sur macOS**:
  - Ventura
  - Monterey
  - Big Sur
  - Catalina
- **Type de paramètre**: bool

## Avec la valeur `false` (par défaut)

Ajouter l'ombre aux captures

```bash
defaults write com.apple.screencapture "disable-shadow" -bool "false"
```

<img
  src="../../screenshots/images/disable-shadow/false.png"
  alt="Exemple avec la valeur false"
  width="740" height="574" style="height: auto"
/>

## Avec la valeur `true`

Supprimer l'ombre des captures

```bash
defaults write com.apple.screencapture "disable-shadow" -bool "true"
```

<img
  src="../../screenshots/images/disable-shadow/true.png"
  alt="Exemple avec la valeur true"
  width="740" height="550" style="height: auto"
/>

## Lire la valeur courante

```bash
defaults read com.apple.screencapture "disable-shadow"
```

## Remettre la valeur à l'état initial

```bash
defaults delete com.apple.screencapture "disable-shadow"
```
