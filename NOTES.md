# Design notes — Nature of Hope (Omarchy Kids theme)

> **This theme reuses the `miasma` palette verbatim and adds only OldJobobo's kid-safe wallpapers.** Same rationale ships in every theme in this batch, so the thinking travels with any repo we share.

## What this is
One of a small set of **Kids** Omarchy themes. Each one **reuses an existing Omarchy theme's palette, copied verbatim**, and adds only OldJobobo's **kid-safe wallpapers**. We deliberately did **not** invent new color schemes — maximizing reuse is the goal, not a compromise.

## Why reuse (OldJobobo's guidance)
> "Keep them as normal `omarchy-[name]-theme` repos… For genuinely new themes, follow the usual structure with a README and a clear desktop preview. Where we're keeping an existing theme's colors and just adding kid-friendly wallpapers, I'd rather reuse that theme than maintain a duplicate."

His kid wallpapers turned out to be **kid-friendly reimaginings of motifs Omarchy already ships as themes** — so the matching palettes already exist and are well-tuned. Reinventing them would only create drift and maintenance duplicates. This theme is a good example: OldJobobo's "nature of **hope**" is the gentle, child-safe counterpart to Miasma's own "nature of **fear**" wallpaper — same series, same mood family, made kid-friendly.

## Why a separate repo with a curated `backgrounds/` (the safety point)
A dedicated kids theme controls its **entire** wallpaper set, so **no unreviewed image can ever appear** as the theme cycles backgrounds. Folding kid art *into* the upstream theme (e.g. dropping a wallpaper into `miasma`, whose own art is deliberately unsettling) would leave that theme's original, non-kid wallpapers in rotation. So the sweet spot is: **reuse the colors, but keep the kid wallpapers in their own curated set.**

## Scope — what a theme can and can't carry
A community-installable Omarchy theme's whole surface is "color" files: `colors.toml`, `icons.theme`, `backgrounds/`, `unlock.png`, and optional color-only app themes. Editor/terminal/`.lua` files are **ignored** on git install, so we don't ship them.

Everything else that makes a machine a safe "kids instance" — **curating which themes are even selectable** in the picker (otherwise a kid could pick an adult theme's wallpaper), content/DNS filtering, locking settings, disabling `theme-install` — is **Kids-setup / system config, not a theme**. It's out of scope for these repos and tracked as open questions below.

## The whole set (wallpaper → reused theme)
| Kid wallpaper(s) | Kids theme | Reuses palette | Motif it echoes |
|---|---|---|---|
| `friendly-wave` | `friendly-wave` | `flexoki-light` | Hokusai *Great Wave* (Omarchy's `kanagawa`) |
| `the-nature-of-hope` ×2 | **nature-of-hope** *(this repo)* | `miasma` | miasma's "nature of ___" series (fear → hope) |
| `cozy-nightscape`, `nighthawk-cocoa` | `cozy-night` | `nord` | nord's night-window & *Nighthawks* |
| `oh-my-ethereal` | `cozy-night` *(flagged)* | `nord` | really an `ethereal`-palette piece |

## Open questions for review
1. **Final form:** keep these as thin kids repos, or fold the kid wallpapers into the upstream themes / seed them via the Kids setup? (Reuse endpoint — Jobobo's call.)
2. **Dark base:** `miasma` was chosen for the direct "nature of fear → hope" tie; if its olive/muted palette feels off against the warm-amber wallpapers, `gruvbox` is a warmer fallback.
3. **Optional comfier UI:** bump the shell font base-size + spacing for younger kids? (Off by default.)
4. **Wallpaper resolution:** source art is 1672×941 (< 1080p) — higher-res originals available?
5. **Licensing/usage** terms for the wallpapers.
6. **Kids-instance safety beyond themes** (Kids-setup scope): curate the picker so only kid themes are selectable; content filtering; settings/app lockdown.

## Attribution
- Wallpapers © **OldJobobo**
- Palette reused from Omarchy's **Miasma** theme
- Draft implementation: **Harris / kenhara**
