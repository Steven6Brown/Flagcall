# Flagcall — Project Brief

Use together with the *Aquila Digital — Mobile & Web App Build Standards*. This brief is the product source of truth; anything not listed under Confirmed is not decided.

## 1. Project overview
Flagcall is an application for Aquila Digital LLC. Ask a rules question by voice or text and get a short, correct answer with the rule cited.

- **Platform scope:** iOS (assumed: see below).
- **Primary users:** Players, coaches, parents and league organizers in pickup games and rec leagues.
- **Primary user outcome:** Settle a rules argument on the spot with a trustworthy, citable answer.

## 2. Confirmed requirements
- Standalone app.
- Answers are short and cite the rule.
- Voice input.

## 3. Reasonable assumptions (change freely)
- Proposed starting sports (not yet confirmed): pickleball, softball, disc golf, youth soccer.
- iOS first, SwiftUI, iOS 17+; speech recognition on-device where available.
- Answers come from a curated, versioned rules library written in plain language. Any language model only rephrases an already-selected entry and never supplies rule numbers or facts of its own (outputs validated before display).
- When no entry matches, the app says it is not sure and points to the official rulebook instead of guessing.

## 4. Open questions (decide before building the affected part)
- Which sport ships first, and which rulebook edition and year?
- Rulebooks are copyrighted by their governing bodies. Plan: original plain-language summaries with rule-number citations, no copied text. Needs confirmation, and possibly permission, before launch.
- Required "unofficial / not affiliated" wording.
- How to reuse the rules-matching approach from the golf app: separate rewrite, or shared package? (Affects repo structure.)
- Pricing model (e.g. one sport free, more sports paid).

## 5. Out of scope
- Live-game officiating features.
- Scorekeeping.
- Social features.

## 6. Project context
| Item | Value |
|---|---|
| Project type | Mobile app |
| Platform | Swift / SwiftUI, iPhone (assumed) |
| Backend | NONE |
| Database | LOCAL (bundled rules library) |
| Authentication | NONE |
| Hosting / deployment | App Store |
| Analytics | NONE |
| AI / ML | LOCAL (speech + optional rephrase) |
| Sensitive data classes | AUDIO (voice question, processed transiently, not retained). No account data. |
| Data processing location | ON-DEVICE |

## Notes
- Never present a ruling the library cannot support.

## 7. Documents to keep (per the build standards)
README.md · SECURITY.md · ARCHITECTURE.md · PRIVACY.md · TESTING.md · CHANGELOG.md · .env.example (names only)
