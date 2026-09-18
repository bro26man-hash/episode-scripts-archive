# iBioSim — Cross-Platform & Integration Struggles (2024–2026)

## The Jena/Xerces Crash (#637) — Most Discussed

**Error:**
```
java.lang.NoClassDefFoundError: Could not initialize class org.apache.jena.query.ARQ
Caused by: java.lang.NoClassDefFoundError: org/apache/xerces/util/XMLChar
```

**Context:** User Hatem-synbio was debugging Kenzo's toggle switch model using the iBioSim tutorial (page 94, automatic model generation).

**Root cause (from maintainer cjmyers):**
> "I'm pretty sure the issue has to do with trying to create a model using iGEM parts. iGEM parts do not have interaction information, so it is impossible to generate a model. Granted, there should be a better error than an exception."

**Key insight:** This isn't a bug — it's a UX failure. The tool should give a user-friendly error like "iGEM parts lack interaction information required for model generation. Try using the Cello library instead." Instead, it crashes with a cryptic Java exception.

**Recent commits (2026):**
- `74ac459` — Merge PR #645: headless stdout fix (Apr 2026)
- `e2d8b7a` — Filter unread progress stdout noise in headless mode (Mar 2026)
- `17c876e` — Update .gitignore for Java SDKMAN (Mar 2026)
- `9df4464` — Add missing full local build deps (Mar 2026)

## Cross-Platform Issues

| Issue | OS | Problem | Comments |
|---|---|---|---|
| #640 | Cross-platform | Java runtime exception | 1 |
| #638 | macOS | Can't run iBioSim 3.2.0 | 1 |
| #635 | Windows 11 | Cannot open iBioSim | 4 |

## Integration Failures

| Issue | Target | Problem | Date |
|---|---|---|---|
| #639 | SynBioHub | Can't upload design | May 2025 |
| #632 | LCP Synbiohub | Connection handshake failure | Apr 2024 |

## The Big Picture

iBioSim's broken SynBioHub integration is a direct consequence of the v1 API's aging architecture. When v3 launches with a proper Swagger API (#1106), this integration story may finally improve. But the cross-platform issues (Mac, Windows 11, Java crashes) suggest that desktop-based CAD tools are hitting a wall.

**The future is web-native.** Tools that run in the browser don't have OS-specific builds, don't require Java installations, and can be updated centrally. iBioSim's 305+ open issues are a symptom of a paradigm reaching its limit.