# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static fundraising website for Igreja Batista Belém — a Baptist church reconstruction project in Belém, Brazil. No build process, no dependencies, no framework.

## Running the Site

Open `index.html` directly in a browser. No server, build step, or package manager needed.

## Architecture

The entire site lives in a single file: **`index.html`** (~1,800 lines). It contains:
- All HTML structure
- Embedded `<style>` block with CSS (custom properties, Grid, Flexbox, media queries)
- Embedded `<script>` block with vanilla JavaScript (lightbox, donation amount selector, smooth scroll)

**Page sections in order:** Hero → História → Galeria → Necessidades → Doação → Impacto → Footer

## Design System

Colors are defined as CSS custom properties at the top of the `<style>` block:
- `--verde-escuro: #1A3A2A` — hero/header background
- `--dourado: #C8922A` — accents and CTAs
- `--creme: #F5EFE0` — light text
- `--marrom: #3D2B1A` — body text

Typography: **Playfair Display** (headings) + **Lato** (body), both from Google Fonts.

Responsive breakpoint: `768px` (single breakpoint, mobile-first).

## Assets

- `assets/` — restoration photos used in gallery (antes/durante/depois)
- `logo_ibb.png` — current logo displayed in the hero section
- `logo_ibb_old.png` — previous logo, kept for reference

## Key JavaScript Behaviors

- **Lightbox**: clicking any `.gallery-item img` opens a full-screen modal; Escape key or clicking outside closes it
- **Donation amounts**: preset buttons toggle `.active` class and populate a hidden input; custom input clears selection
- **WhatsApp integration**: contact buttons use `wa.me/` links with pre-filled messages

## Language

All user-facing content is in **Brazilian Portuguese**.
