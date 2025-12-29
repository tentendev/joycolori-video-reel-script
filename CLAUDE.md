# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a creative content project for JOY COLORi (lab-grown diamond jewelry brand) containing:
- AI system prompts for video proposal generation
- Static HTML video proposal presentations
- Image assets for storyboards and covers

## Repository Structure

- `system_prompt_video_proposal_generator.md` - Master system prompt defining the AI Video Creative Director workflow for generating interactive HTML video proposals
- `joycolori_reel_proposal.html` - Main brand campaign proposal ("給 22 歲的妳")
- `joycolori_reel_valentines_proposal.html` - Valentine's Day campaign variant
- `joycolori_reel_bridal_proposal.html` - Bridal collection variant
- `images/` - Generated storyboard frames, cover options, and campaign posters

## HTML Proposal Architecture

Each proposal HTML file follows Material Design 3 styling with:
- Tabbed interfaces for social copy variations (6 versions) and BGM options (3 versions)
- Interactive modals for viewing/copying Nano Banana JSON prompts
- Sprite-based storyboard thumbnails with `background-position` for grid navigation
- Navigation bar linking between campaign variants

### Key JavaScript Functions
- `openTab(evt, tabName)` - Switch social copy variations
- `openAudioTab(evt, tabName)` - Switch BGM options
- `showPromptModal(element)` - Display JSON prompts from `data-json` attributes
- `copyPrompt()` - Copy modal content to clipboard

## System Prompt Workflow Phases

1. **Strategic Core & Concept** - Brief analysis, hook definition, persona targeting
2. **Visual & Directorial Style** - Aesthetics, camera specs, Nano Banana prompt format
3. **Storyboard** - Scene-by-scene with time, visual, audio, copy, and image prompts
4. **Social Media Power Pack** - Caption variations with matched cover art concepts
5. **Audio Atmosphere** - Suno AI prompt variations for BGM

## Nano Banana JSON Format

All image generation prompts use this structure:
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

## Local Development

Open HTML files directly in browser - no build step required. Files are self-contained with inline CSS/JS and CDN-loaded fonts (Google Fonts, Material Symbols).
