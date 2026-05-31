# Hynek Mac Video Compressor 🎬

Jednoduchá a rychlá macOS aplikace napsaná v čistém **SwiftUI**, která slouží k efektivní kompresi videí na přesně stanovenou cílovou velikost (ideální pro limity na Discordu, Slacku nebo e-mailech).

## Vlastnosti 
- **Drag & Drop:** Stačí video jednoduše přetáhnout z Finderu přímo do aplikace.
- **Inteligentní posuvník:** Nabízí cílové velikosti (4 MB, 8 MB, 16 MB...). Nepustí vás na větší velikost, než má původní video.
- **Podpora moderních kodeků:** Možnost volby mezi univerzálním **H.264** a úspornějším **H.265 (HEVC)**.
- **Apple kompatibilita:** Videa v H.265 obsahují správný tag `hvc1`, takže jdou bez problému přehrát ve Finderu i QuickTime Playeru.
- **Reálný Progress Bar:** Dvoufázový ukazatel průběhu (2-pass encoding) parsuje data přímo z FFmpegu a ukazuje přesný stav v procentech.

---

## Požadavky pro spuštění

Aplikace momentálně běží v režimu, kdy využívá systémový FFmpeg nainstalovaný na vašem Macu. Pro správné fungování musíte mít nainstalovaný **Homebrew** a balíčky **ffmpeg** a **ffprobe**.

Pokud je ještě nemáte, otevřete Terminál a zadejte:

```bash
# 1. Instalace Homebrew (pokud ho nemáte)
/bin/bash -c "$(curl -fsSL [https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh](https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh))"

# 2. Instalace potřebných nástrojů
brew install ffmpeg ffprobe
