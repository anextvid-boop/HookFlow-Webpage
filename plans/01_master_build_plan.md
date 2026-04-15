# HookFlow Webpage: Master Build Plan

**Date**: 2026-04-15
**Goal**: Build a 100% static, fast, premium landing page repository for HookFlow (iOS app).

## 1. Project Architecture

The repository will be structured to be instantly deployable to GitHub Pages. It will contain only standard vanilla web technologies (HTML/CSS) to ensure permanence and ultra-fast performance without build steps.

**File Structure**:
- `index.html` — Premium landing page.
- `terms.html` — Terms of Use Endpoint (Required for Apple).
- `privacy.html` — Privacy Policy Endpoint (Required for Apple).
- `style.css` — Core branding and CSS variables mapped to Apple's design language.
- `plans/` — Catalog of future update plans, starting with this document.

## 2. Design System & Aesthetics (Apple `.ultraThinMaterial` / Glassmorphism)

- **Layout**: Mobile-first using CSS Flexbox. Font sizes will utilize `clamp()` to transition dynamically up to Desktop.
- **Colors**:
  - `hfBackground`: `#0D0D0D` (Pure spatial base)
  - `hfSurface`: `rgba(255, 255, 255, 0.05)` with `backdrop-filter: blur(20px)` and Safari prefix `-webkit-backdrop-filter`.
  - `hfAccent`: `#FF264C` (Neon Premium Red)
  - Text Primary: `rgba(255, 255, 255, 1.0)`
  - Text Secondary: `rgba(255, 255, 255, 0.6)`
- **Typography Stack**:
  - `font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;`
  - Weights: `800`/`700` (Headers), `500` (Buttons/Subtitles), `400` (Paragraphs).

## 3. Marketing Copy Structure

### Index Page (`index.html`)

**Hero Section**:
- **H1**: `HookFlow: AI Video Studio`
- **H2**: `Teleprompter & Captions`
- **Hook**: "Step into the ultimate mobile recording studio. Automatically transcribe your voice into scrolling teleprompter scripts and export flawless cinematic videos instantly."

**About / Feature Breakdown**:
"HookFlow is your all-in-one cinematic production studio natively built for iOS. Whether you are a solo creator, a pro-seller, or an educator, HookFlow removes the friction between capturing your voice and publishing professional content. Speak directly into the microphone to instantly generate high-fidelity, highly accurate scrolling teleprompter scripts in real-time. Lock your script, hit record, and perfectly perform your lines without ever looking away from the lens. Stop fumbling between three different apps just to film a single reel. Become the director of your own studio."

**Pricing Model Cards**:
Glassmorphic cards featuring the tiers:
1. **Creator Pro (Monthly)**: £9.99 / month
2. **Creator Pro (Yearly - Best Value)**: £79.99 / year *(7-Day Free Trial badge)*
3. **Pro Seller**: £149.99 / year

### Legal Endpoints

*Note: Use "HookFlow" as the official company entity and `support@hookflow.app` for all point-of-contact references in the legal phrasing.*

**Terms (`terms.html`)**:
Standard EULA addressing Apple Auto-Renewable Subscriptions (processed via iTunes, auto-renewal, manage in device settings, 24-hours cancellation policy).

**Privacy (`privacy.html`)**:
Strict declaration highlighting that HookFlow processes all recordings securely and does not harvest or sell recorded video or audio data off-device natively.

## 4. Animation Language

- **Global Physics**: `--apple-spring: cubic-bezier(0.175, 0.885, 0.32, 1.275);`
- **Interaction Transitions**: `transition: all 0.4s var(--apple-spring);`
- **Entrance**: Fade-ups (`translateY(20px)` to `0`, `opacity` from `0` to `1` over 0.8s `ease-out`).
- **Accent Glow Overrides**: Buttons feature a pulse shadow on hover: `box-shadow: 0 4px 20px rgba(255, 38, 76, 0.4);`

## 5. Deployment Process

### Remote Repository
- **URL**: `https://github.com/anextvid-boop/HookFlow-Webpage.git`
- **Branch**: `main`

Once files are validated, the codebase is strictly pushed to the repository above. It is ready to be directly hosted on GitHub pages configured with a custom domain linking to `hookflow.app/privacy` and `hookflow.app/terms`.
