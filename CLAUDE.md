# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Creative content project for JOY COLORi (lab-grown diamond jewelry brand) containing AI system prompts for video proposal generation and static HTML presentation decks.

## Key Files

- `system_prompt_video_proposal_generator.md` - Master AI Video Creative Director prompt for generating interactive HTML proposals
- `joycolori_reel_proposal.html` - Main brand campaign ("給 22 歲的妳")
- `joycolori_reel_valentines_proposal.html` - Valentine's Day variant
- `joycolori_reel_bridal_proposal.html` - Bridal collection variant
- `index.html` - Redirect to main proposal (for Vercel deployment)

## HTML Proposal Architecture

Single-file static HTML using Material Design 3 with:
- Tabbed interfaces for 6 social copy variations and 3 BGM options
- Modals for viewing/copying Nano Banana JSON prompts (`data-json` attributes)
- Sprite-based storyboard grids using `background-position` navigation
- Inter + Noto Sans TC fonts via Google Fonts CDN

### JavaScript Functions
- `openTab(evt, tabName)` / `openAudioTab(evt, tabName)` - Tab switching
- `showPromptModal(element)` - Display JSON from `data-json`
- `copyPrompt()` - Clipboard copy

## Image Assets

`images/` contains timestamp-suffixed grid sprites and individual cover variants:
- `*_grid_*.png` - Composite sprite sheets for storyboards/hooks
- `*_cover_v[1-6]_*.png` - Individual cover options per social copy variant

## Nano Banana Prompt Format

```json
{
  "model": "nanobananapro",
  "style_preset": "cinematic-reality|lifestyle-vlog|studio-product",
  "aspect_ratio": "9:16|4:5",
  "prompt": "...",
  "negative_prompt": "...",
  "consistency_seed": 42
}
```

## Development

No build step - open HTML files directly in browser. Deployed on Vercel with `cleanUrls: true`.
