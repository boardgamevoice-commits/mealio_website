# Monthly Website Review & iOS Sync - 2026-09

## Executive Summary
This review documents the synchronization of the official landing page and policy documents (`mealio website`) with the **Mealio iOS application (v1.0.2 Build 4 / MVP v1.3)**. Following the definitive product naming decision in the iOS project, the website has been completely rebranded from the temporary name "DishPilot" back to **Mealio** (`Mealio - AI 智能厨房烹饪助手` / `Mealio — AI Cooking Companion`). 

All core product updates from the iOS app's latest release have been translated into customer-facing landing page sections, feature cards, and legal disclosures. This includes **Gemini 3.5 Flash multimodal streaming generation**, **Direct Manipulation cooking mode with tactile haptics**, **3-week meal planning**, **AI Nutrition Insights dashboard**, **Fair-use daily quotas with Google AdMob rewarded video unlocks**, and **Apple App Tracking Transparency (ATT) privacy compliance**.

---

## Month-over-Month Comparison (vs. 2026-06-19)
- **Previous Goals Met**:
  - [x] **Brand Unification**: Restored and unified branding across all HTML files, metadata, OpenGraph cards, and legal policies to **Mealio**.
  - [x] **Feature Parity**: Added full coverage for new v1.0.2 / MVP v1.3 capabilities (Direct Manipulation physics, 3-week planning, nutrition dashboard, rewarded unlocks).
  - [x] **Asset Synchronization**: Replaced placeholder icons with the official 1024x1024 iOS AppIcon (optimized 256x256 retina PNG), and created an authentic iPhone preview mockup (`assets/app-preview.png`) from real simulator screenshots.
  - [x] **Legal Compliance**: Updated `privacy.html` and `terms.html` to clearly articulate Google AdMob rewarded video mechanics, Apple ATT disclosures (`NSUserTrackingUsageDescription`), out-of-process PhotosPicker isolation, and iCloud backup exclusion for rebuildable image caches.
  - [x] **iOS Landing Page Best Practices**:
    - **Smart App Banner**: Added Apple official `<meta name="apple-itunes-app" content="app-id=6777829320">` for seamless 1-tap Safari installs.
    - **Apple Web Clip & Theme**: Added `<link rel="apple-touch-icon">` and `<meta name="theme-color">` for native iOS Home Screen bookmarks.
    - **Schema.org Structured Data**: Configured `SoftwareApplication` (Category: Food & Drink, Price: $0.00) and `FAQPage` rich search snippets.
    - **Cross-Device Conversion**: Generated high-contrast QR code companion (`assets/appstore-qr.png`) for instant iPhone camera scanning on desktop browsers.
    - **Interactive Product Showcase**: Added interactive 5-tab capability tour (Discovery, Direct Manipulation Cooking, Copilot, 3-Week Planner, Nutrition).
    - **Interactive FAQ Accordion**: Implemented 5 high-converting Q&As addressing common user hesitations (zero-login, privacy, offline support, quotas).
    - **Accessibility (A11y)**: Added Skip to Content link, `:focus-visible` styling, and `@media (prefers-reduced-motion: reduce)`.
- **Carried Over / In Progress**:
  - [ ] **Custom Domain Routing**: Ensure custom domain DNS records point to Netlify once deployment goes live.
  - [ ] **Multi-language Landing Page**: Prepare Simplified Chinese and Spanish landing page variants mirroring the iOS app's trilingual localization (`en`, `zh-Hans`, `es`).

---

## 1. Updated Web Pages & Synchronized Assets
- **Landing Page ([index.html](file:///Users/devfang/Cursor/mealio%20website/index.html))**:
  - Rebranded title, OpenGraph tags, and Twitter cards to Mealio.
  - Hero Section updated with Gemini 3.5 Flash badge, real iPhone mockup preview, floating micro-interaction badges, and direct link to the Apple App Store (`https://apps.apple.com/app/mealio/id6777829320`).
  - Features grid expanded to 8 cards covering multimodal generation, direct manipulation cooking mode, visual Copilot, 3-week meal planner, nutrition insights, rewarded unlocks, local recipe library, and zero-account privacy.
  - Workflow and safety grids updated with mandatory food safety and temperature checkpoint notices.
- **Privacy Policy ([privacy.html](file:///Users/devfang/Cursor/mealio%20website/privacy.html))**:
  - Updated AI model reference to Google Gemini 3.5 Flash via authenticated AI Gateway.
  - Added full section explaining Google AdMob rewarded videos, Apple ATT privacy consent, and strict zero-data-sale commitment.
  - Documented iOS 16+ `PhotosPicker` out-of-process sandboxing (0 permission dialogs on app launch) and `isExcludedFromBackup = true` for local image storage.
- **Terms of Use ([terms.html](file:///Users/devfang/Cursor/mealio%20website/terms.html))**:
  - Rebranded all legal references to Mealio.
  - Added terms governing daily fair-use AI quotas and optional rewarded video unlocks.
  - Sharpened culinary safety disclaimers (doneness assessment is supplemental; meat thermometer is required for poultry/pork; nutrition estimates are non-medical approximations).
- **Styles & Layout ([index.css](file:///Users/devfang/Cursor/mealio%20website/index.css))**:
  - Added responsive phone mockup frame with dark glassmorphic styling, floating badges, and smooth keyframe floating animations.
  - Enhanced mobile breakpoints to ensure flawless presentation across iPhone, iPad, and desktop viewports.
- **Assets ([assets/](file:///Users/devfang/Cursor/mealio%20website/assets/))**:
  - `icon.png`: Synced and exported from native iOS `AppIcon.appiconset/appicon.png` (256x256, 27 KB).
  - `app-preview.png`: Generated from native iPhone 17 Pro discovery screenshot (800x1738, 241 KB).

---

## 2. Security, Performance & Compliance Checklist
- [x] **No Secrets or API Keys**: Zero hardcoded API keys, tokens, or credentials in web source.
- [x] **Security Headers**: HSTS, CSP, X-Frame-Options, X-Content-Type-Options active in `netlify.toml`.
- [x] **Zero Third-Party Trackers**: Clean vanilla static build without third-party tracking scripts.
- [x] **App Store Compliance**: Complies with Apple Guideline 5.1.1 and App Tracking Transparency standards.
