# GENtle2 — Legacy Debt & the 12-Year Refactor

## Overview

GENtle2 is a web-based DNA editor for synthetic biology. Written in JavaScript (Node.js + Express + Gulp). A re-think of the original GENtle desktop application for the web. 106 stars.

## The Problem: 75+ Open Issues, Most Dating to 2014

### Refactor Milestone 1: Canvas events & RES/annotation cards
| Issue | Title | Date | Comments |
|---|---|---|---|
| #164 | Display feature details when hovering | Jul 2014 | 0 |
| #163 | Tracking mouse events in `Artist` | Jul 2014 | 0 |
| #159 | Tracking shapes in `Artist` | Jul 2014 | 6 |

### Refactor Milestone 2: Sequence opening/editing
| Issue | Title | Title | Date |
|---|---|---|---|
| #132 | Replace non-allowed chars on Genebank import | Jun 2014 |
| #130 | Bug with selection using up arrow | Jun 2014 |

### Persistent Bugs (no milestone)
| Issue | Bug | Date |
|---|---|---|
| #162 | Selection disappears via context menu | Jul 2014 |
| #161 | Selection disappears with hotkeys | Jul 2014 |
| #158 | Creating feature clears plasmid map | Jul 2014 |
| #156 | Caret moves unexpectedly during selection | Jul 2014 |
| #154 | Plasmid map title overflows | Jul 2014 |

## The Story

GENtle2 has **75+ open issues dating to 2014**. The maintainer (`alexandremeunier`) has created Refactor milestones targeting Canvas events, RES/annotation cards, and sequence opening/editing, but progress is glacial.

With only 6 comments on the most discussed issue (#159) and a 9+ year timeline for the refactor, this is a **cautionary tale about sustaining open-source scientific software**.

## What Went Wrong?

1. **No TypeScript** — 2014-era JavaScript with no type safety
2. **No tests** — No CI pipeline to catch regressions
3. **No contributors** — 10+ years with the same maintainer
4. **Canvas API limitations** — HTML5 Canvas is notoriously difficult for interactive UIs
5. **Single maintainer** — No community to share the burden

## Contrast with Syn-Zeug

Syn-Zeug (Rust + Svelte + WASM) has **10 open issues, all feature requests, zero bug reports**. This is what sustainable open-source looks like:
- Modern type-safe language (Rust)
- Modern framework (Svelte)
- Web-deployable (WASM)
- Active contributor onboarding (reviewer guidance for new contributors)

## Episode Angle

**"Why Do Good Tools Go Bad?"** — GENtle2's 12-year refactor is not a technology problem. It's a community problem. The lesson for content creators: open-source sustainability requires **contributors**, not just code.