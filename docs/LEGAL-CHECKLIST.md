# Protecting an indie app studio

> **Not legal advice.** This is a general checklist to take to a licensed attorney in your state. Laws differ by location and by what each app does. Nothing here prevents a lawsuit; the aim is to make one less likely, cheaper to defend, and unable to reach personal assets.

A privacy policy is necessary but not sufficient. It covers one risk (misdescribing data handling). The rest:

## 1. Business structure (biggest lever)
- A sole proprietor is personally liable for business debts and claims. An LLC (or similar) separates personal assets from the business **only if** it is kept separate in practice: its own bank account, contracts signed in the company name, no mixing of funds.
- `terms.html` currently names an individual as the "Service Provider". If an LLC exists or is formed, the terms, policies, copyright lines and the App Store seller name should name the company instead.
- An organization Apple Developer account (needs a D-U-N-S number) lists the company, not you personally, as seller.

## 2. Insurance
Ask a business insurance broker about: general liability, **tech errors & omissions**, and **cyber liability**. These are what typically pay legal defense costs for app-related claims. Defense costs are often the real expense even when you win.

## 3. Terms of use / EULA
- Every app should have terms covering license scope, disclaimer of warranties, limitation of liability, termination, governing law. Apple provides a standard EULA by default; custom terms replace it and must not conflict with Apple's requirements.
- Terms are per-app: the existing terms are written for MotorScribe (including user-generated-content and Google Play wording). Do not reuse them unreviewed for apps with different features.
- Limitation-of-liability clauses are limited by consumer protection law and cannot exclude everything.

## 4. Disclaimers that match what the app does
- Fitness/health features: "not medical advice; consult a physician before exercise."
- Hardware-adjacent features (e.g., 3D printing: heat, fumes, fire, machine damage): safety disclaimer, and tell users to supervise prints and verify G-code.
- Accuracy-dependent tools: say what the output is not guaranteed to be.
Put them in terms **and** where the user sees the risk, such as the screen where the action happens.

## 5. Privacy and platform compliance
- Policy text must match actual code and the App Store privacy label / Play Data Safety form.
- Misstating data practices can draw regulator action (e.g., FTC in the US) regardless of size.
- Children under 13 (COPPA in the US): the policies say apps are not directed at children; make sure app content and store age ratings agree.
- If you ever add accounts, analytics, ads, cloud sync or crash reporting, the policy, the labels and possibly consent flows must change first.
- Apps with user-generated content need reporting, blocking and a contact method (Apple requirement); consider registering a DMCA designated agent.

## 6. Intellectual property
- Open-source licenses: comply with each license's notice requirements (e.g., Forge uses Clipper2, Boost Software License). Keep a third-party notices file and show it in-app.
- Unity assets, fonts, audio and art: keep the license/receipt for every purchased or downloaded asset.
- Trademark: search before committing to an app or brand name; consider registering the studio name. Copyright in your code exists automatically; registration helps if you ever have to enforce it.
- Anyone else who writes code, art or music for you (contractors, friends): get a written work-for-hire / IP assignment **before** they start.
- Your novel is separate: keep dated drafts and consider copyright registration before publication.

## 7. Housekeeping
- Business email on a studio-owned domain rather than a personal Gmail; it looks more credible and survives account changes.
- Keep records: policy changelog (see `CHANGELOG.md`), version history of what each app shipped and which policy applied.
- Business license, tax registration and separate accounting as your state requires.
- Have an attorney review the entity setup, terms and policies once. A few hours of review is cheap relative to a claim.
