---
name: ux-older-people
description: UX design rules for older adults (60+). Apply this skill whenever designing, reviewing, or generating any screen, component, flow, or interface intended for older adult users — including onboarding, home screens, forms, settings, navigation, checkout, dashboards, health apps, or any other UI. Trigger on phrases like "for seniors", "for older adults", "for older adults", "age-friendly", "accessible for grandparents", "senior-friendly", "adultos mayores", or when the target audience is explicitly 60+. Also trigger when reviewing an existing design for age-friendliness. Read the references/ folder for detailed research sources behind each rule.
---

# UX Design Rules for Older Adults

> Evidence-based design system for screens, components, and flows targeting users aged 60+.
> Every rule below is grounded in peer-reviewed research and validated guidelines from studies across the US, Europe, China, Korea, Japan, Australia, the Middle East, and Southeast Asia.
> For the full research backing, read `references/research-sources.md`.

---

## Golden Rules

Two principles override everything else. Every specific rule below flows from these:

1. **One primary action per screen.** Each screen helps the user complete a single, focused task. Secondary options are hidden or minimized.
2. **Reduce the number of elements and options on screen.** Less clutter means less cognitive load. If it's not essential to the current task, remove it.

---

## 1. Touch Targets & Motor

Aging brings reduced dexterity, hand tremors, and lower precision. Touchscreens lack the tactile feedback of physical buttons, making errors more frequent.

| Rule | Spec | Why |
|---|---|---|
| Minimum touch target | **16mm / ~64px** (ideal 20mm / ~80px for 70+) | Targets <6mm drop below 80% hit rate. 15-16mm showed optimal efficiency and lowest error in controlled studies (Jin et al.; Yeh 2025). |
| Minimum spacing between targets | **3mm / ~12px** gap | 3mm spacing significantly reduced accidental taps vs. 0mm (Jin et al.). |
| Button shape | Rounded rectangles or circles, visually raised | Older adults prefer skeuomorphic affordances. Flat buttons create "click uncertainty." |
| Primary action position | **Center or upper-right** of the screen | Older adults perform best when buttons are at the top or right of the display (Yeh 2025). |
| Touch offset compensation | Add **asymmetric padding** (extra right-side hit area for right-handed users) | Right-handed older adult users systematically deviate rightward; tremors intensify this (Shao et al. 2023). |
| Reduce touch sensitivity | Lower control sensitivity to prevent involuntary taps | Users should be able to rest hands on screen without accidental activation (JMIR 2023). |
| Avoid complex gestures | Use **single tap only** as primary input; avoid pinch, multi-finger, long-press, double-tap | Skin aging, wrinkles, and tremors cause loss of screen contact during gestures (JMIR 2023). Gestures are advanced features with no UI hints to recall them. |
| Zoom: use +/- buttons | Provide explicit zoom buttons instead of requiring pinch-to-zoom | Pinch requires two-finger dexterity that exceeds many older adults' abilities (Lepicar et al.). |

---

## 2. Typography & Readability

Vision loss is the most commonly reported disability in adults over 70. Reading on screens is harder with age due to reduced contrast sensitivity, slower processing, and difficulty discriminating colors.

| Rule | Spec | Why |
|---|---|---|
| Body text minimum | **18px** (16px absolute floor) | Studies consistently recommend 16px as starting point, with 18-20px preferred for primary content. |
| Critical text / titles | **24-30px** | Morey et al. recommend 30pt for critical text, 20pt for secondary. |
| Font family | **Sans-serif, high x-height, clear character differentiation** (e.g., distinguish l, I, 1) | Avoid decorative, condensed, or all-caps fonts. Prioritize readability over aesthetics. |
| Line height | **1.5× to 1.8× font size** | WCAG recommends 1.5× minimum; 1.6-1.8× is optimal for older adults. |
| Letter spacing | **0.12× to 0.16× font size** | Improves character discrimination for aging eyes. |
| Paragraph spacing | **2× to 2.5× font size** | Prevents text blocks from feeling overwhelming. |
| Text alignment | **Left-aligned** (LTR) or natural reading direction | Justified text creates uneven spacing that hinders reading. |
| Adjustable text size | Provide **in-app font size control** (at least 3 levels) | Many older adults use reading glasses or set system-wide large fonts. Honor both system settings and offer in-app adjustment. |
| Avoid text over images | Never place text on busy backgrounds without a solid overlay | Reduces legibility and increases cognitive effort. |

---

## 3. Color & Contrast

Color perception changes with age: the lens yellows, reducing blue sensitivity. Contrast sensitivity declines. Some colors become indistinguishable.

| Rule | Spec | Why |
|---|---|---|
| Minimum contrast ratio | **7:1** for body text (WCAG AAA) | WCAG AA (4.5:1) is the legal floor, but 7:1 is strongly recommended for older adults. |
| Default theme | **Light mode** (dark text on light background) | Older adults favor positive polarity to minimize mental fatigue (Sethi & Ziat 2023). Cognitive scores are higher in light mode (Tandfonline 2025). |
| Offer both themes | Provide dark mode as an **option**, not default | Some users with specific eye conditions prefer dark mode. Always let users choose. |
| Avoid problematic colors | **No red text**, minimal blue-only elements, avoid red/green combinations | Blues appear faded to seniors. Red is difficult to read. Red/green pairs fail for color blindness. |
| Use color + another signal | Never convey meaning through color alone | Always pair color with text labels, icons, or patterns. |
| High-contrast UI chrome | Borders, separators, and active states must be clearly distinguishable | Flat design with subtle differences causes "click uncertainty." |

---

## 4. Icons & Visual Language

Older adults process skeuomorphic icons faster and more accurately than flat icons. Icons without text labels are a major usability barrier.

| Rule | Spec | Why |
|---|---|---|
| Always pair icon + text label | **No icon-only buttons** (except universally known: ✕ close, ← back) | All older adults performed poorly searching for flat icons alone. Icon + text was the most effective combination across all cognitive levels (PMC 2022). |
| Prefer skeuomorphic style | Icons should resemble real-world objects with depth, shadow, texture | Skeuomorphic icons are searched more quickly and accurately by older adults (ScienceDirect 2020). Flat design is slower and less accurate for seniors across visual search, identifying clickable objects, and navigation. |
| Icon size | Minimum **28×28px**, recommended **32-40px** | Must be large enough to recognize and tap. |
| Semantic closeness | Icons should visually represent their function literally | Abstract or metaphorical icons confuse users. A phone icon for "call" works; a abstract shape does not. |
| No hamburger menu without label | If using ☰, always add the word **"Menu"** next to it | Less experienced users don't recognize ☰ as navigation (NNGroup 2026). |
| Make clickable things look clickable | Buttons should look raised/tappable. Links should be underlined. | Extreme flat design obscures discoverability. |

---

## 5. Navigation & Information Architecture

Navigating through apps is the highest-priority area for improvement (entropy weight analysis, China 2024). Cognitive decline makes users lose track of where they are.

| Rule | Spec | Why |
|---|---|---|
| Linear navigation | **One clear path** through each task flow | Linear paths and logical workflows reduce cognitive load and improve task completion (PMC 2025 systematic review). |
| Persistent visible navigation | **Fixed bottom tab bar** (mobile) or **fixed sidebar** (desktop/tablet) | Avoid hidden navigation (drawer, hamburger-only). Navigation must be always visible. |
| Maximum 4-5 tabs/options | Limit primary navigation to **4-5 items maximum** | Menus with too many options are a critical usability barrier (Awan 2021). |
| Always show "where I am" | Highlight current section/page clearly | Users with memory issues need constant location awareness. |
| Always show "how to go back" | Prominent, persistent **Back button** + Home button | "Return" and "Home" serve as safe points. Users should never feel trapped (Toptal). |
| Avoid deep hierarchies | Maximum **2 levels** of navigation depth | Users who can't remember steps to reach a screen get lost. Reduce sublevels. |
| No multi-step memory tasks | Don't split tasks across screens if they require remembering previous inputs | If splitting is necessary, show a persistent summary of previous choices. |
| Static menus | Avoid menus that change based on context or user behavior | Predictability is critical. Users learn fixed patterns through repetition. |
| Breadcrumbs on web | Show path trail on desktop/web interfaces | Helps users understand hierarchy and retrace steps. |

---

## 6. Input & Forms: Minimize Typing

Almost all older adults in studies had difficulty with virtual keyboards. Keys are too small, require precision, and lack tactile feedback. This is one of the highest-impact areas.

| Rule | Spec | Why |
|---|---|---|
| Prefer selection over typing | Use **buttons, pickers, toggles, radio buttons, segmented controls** | Predefined options eliminate keyboard struggles entirely. |
| Use radio buttons for ≤5 options | Show all options visible at once, no dropdown required | Dropdowns hide options and add a tap. Radio buttons let users scan and choose. |
| Large dropdown alternatives | For long lists, use **searchable picker with large touch targets** | Standard dropdowns have tiny text and scroll areas. |
| Offer voice input | Provide a **microphone button** on every text field | Voice input was significantly faster and preferred over typing by older adult users (JMIR 2020 RCT). Users tolerate dictation challenges to avoid typing (NNGroup 2024). |
| Autofill and defaults | Pre-fill known data; use smart defaults | Reduce the amount users need to type. Every keystroke avoided is friction removed. |
| One field per screen (complex forms) | For critical flows (signup, checkout), show **one input at a time** | Progressive disclosure reduces overwhelm. One question per screen. |
| Large keyboard targets | If keyboard is required, use **number pads for numeric input** with minimum 12.5mm button size | 7.5mm keypads had the worst performance; 12.5-17.5mm were optimal (ScienceDirect 2020). |
| Flexible input acceptance | Accept phone numbers, dates, postal codes in **multiple formats** | Rigid format requirements frustrate users. Parse "(555) 555-5555" and "5555555555" equally. |
| Clear field labels | Labels **above** the field (not placeholder-only) | Placeholder text disappears on focus, causing users to forget what to enter. |

---

## 7. Onboarding & Help

Older adults learn best through repetition, step-by-step guidance, and clear purpose explanations. They are not "digital natives" — many started using the web without formal training.

| Rule | Spec | Why |
|---|---|---|
| Slow, step-by-step onboarding | **One concept per screen**, with clear "why" explanation | Slow, thorough guides that explain what to do and why are essential (UserGuiding). |
| Show value immediately | Explain **what the app does for them** before asking for input | Perceived usefulness is the most important predictor of adoption (Wang et al.). |
| Favor video tutorials | Short video demonstrations > text instructions | Users can watch and replay. Contextual video is more effective than text help (JMIR 2023). |
| Provide templates, not blank states | Offer **ready-to-use defaults** instead of requiring configuration | Minimize extra steps; get as close to a turnkey solution as possible. |
| Contextual help | Show help **at the point of need**, not in a separate help section | Searching through help systems is very time-consuming and often unsuccessful for older adults (JMIR 2023). |
| Explain technical terms | Define web/app terms inline ("tap the Menu button — the three lines at the top") | Many seniors don't know terms like "URL", "homepage", "download" (NNGroup). |
| No jargon | Use plain language at an **8th-grade reading level** | Average privacy policy readability is 12th-grade; average older adult reads at 8th-grade (IEEE Spectrum 2025). |
| Reassure safety | Explicitly state "you can't break anything" and "you can always undo" | Fear of "breaking" technology is a sincere and widespread concern (Worky 2024). |

---

## 8. Error Prevention & Recovery (Forgiving Design)

Older adults have lower tolerance for errors. When something goes wrong, they're more likely to blame themselves and abandon the task entirely.

| Rule | Spec | Why |
|---|---|---|
| Confirm destructive actions | **Always require confirmation** for delete, send, pay, submit | Confirmation dialogs prevent irreversible mistakes. |
| Provide undo everywhere | Every action should be **reversible** with a clear "Undo" option | Reversibility is one of the strongest trust signals in UX (LogRocket 2025). |
| Constructive error messages | Explain **what went wrong + how to fix it** in plain language | "Invalid input" means nothing. Say "Please enter your phone number with 10 digits." |
| Position errors visually | Show error messages **immediately next to the field**, with high contrast (red border + icon + text) | Subtle error messages placed elsewhere on screen are easily overlooked. |
| Never timeout silently | If a session or action times out, **explain why and save state** | Long timeouts let users think and decide. Never destroy work silently. |
| Increase timeouts | Allow **at least 2× the default timeout** for all timed interactions | Older adults need more time to interpret screens and decide next actions (JMIR 2023). |
| Save progress automatically | **Auto-save** forms and multi-step flows | If a user accidentally navigates away, their work should be preserved. |
| No dead ends | Every error screen must offer a **clear path forward** | "Try again" button, customer support number, or "Go home" — never just an error message. |

---

## 9. Feedback & Responsiveness

Older users need stronger, multimodal confirmation that their actions registered. Subtle feedback gets missed.

| Rule | Spec | Why |
|---|---|---|
| Clear visual feedback on tap | **Obvious button state change** (color, scale, or border) on press | Older users often can't tell if a button was pressed. Subtle changes get missed (JMIR 2023). |
| Haptic feedback | Use **gentle vibration** on tap confirmation | 63.2% of older adult users preferred slight haptic feedback; 73.6% said it reduced reliance on visual information (PMC 2025). |
| Multisensory feedback | Combine **visual + haptic + optional audio** | Perception limitations mean a single channel may fail. Multiple channels increase delivery probability (JMIR 2023). |
| Loading feedback always | Show **spinner or progress indicator** for any wait >500ms | Users must know the system is working. A blank screen causes anxiety and abandonment. |
| Use skeleton screens | For page loads >2 seconds, show **placeholder layout** | Skeleton screens reduce perceived wait time and give a mental model of the page. |
| Extend feedback duration | Keep success/error messages visible for **at least 5 seconds** | Pop-ups that disappear in 2 seconds get missed. Let users read at their pace. |
| Progress indicators for flows | Show **"Step 2 of 4"** in multi-step processes | Users need to know how far they've come and how much is left. |

---

## 10. Privacy, Security & Trust

67% of older adults have been scam victims. Privacy concerns sometimes outweigh perceived benefits. Trust must be built through transparency and simplicity.

| Rule | Spec | Why |
|---|---|---|
| Plain language permissions | Explain **why** each permission is needed in one sentence before requesting | "We need your camera to let you scan documents" — not a wall of legal text. |
| No dark patterns | **Never** induce unwanted downloads, subscriptions, or payments | China's senior mode regulations explicitly ban designs that lure extra payments. |
| No ads in age-friendly modes | Remove advertising from senior interfaces | Ads create confusion, accidental taps, and erode trust (China MIIT regulations). |
| Easy access to human support | Provide a **visible "Call for Help" or "Talk to a Person" button** | In China's age-friendly designs, users 65+ can reach a human agent without navigating voice prompts or typing (PRNewswire 2021). |
| Simplified privacy settings | One-screen privacy dashboard showing who has access and why | Don't scatter settings across multiple menus. |
| Real-time transparency | Notify data access events in plain language | "Your doctor viewed your heart-rate data at 2pm" — banking apps already do this for transactions (IEEE Spectrum 2025). |
| Visible security indicators | Show lock icons, "Secure" labels, and verification badges prominently | Visual trust signals reduce anxiety. |

---

## 11. Device & Platform Considerations

Design rules apply across devices but with platform-specific adaptations.

### Mobile (Smartphone)
- Screen is small — one action per screen is critical
- Touch targets at the **upper 60%** of the screen (bottom area is hard to reach one-handed)
- Avoid landscape-only layouts
- Support system-level accessibility settings (Dynamic Type on iOS, font scaling on Android)

### Tablet / iPad
- Preferred device for many seniors due to larger screen
- Use the extra space for **larger text and buttons**, not more features
- Avoid cramming desktop-density information into tablet layouts
- Consider split-view layouts for forms: labels left, inputs right

### Desktop / Web
- Support keyboard navigation fully
- Use **visible focus indicators** (not just outline — use background color change)
- Minimum click target: **44×44px**
- Avoid hover-only interactions (tooltips, dropdown menus that require hover)
- Provide visible scrollbar (don't auto-hide)

### Cross-Platform
- **Consistency**: Same navigation structure, same terms, same icon meanings across all platforms
- **Personalization profiles**: Let users set preferences once and sync across devices
- Support system-level accessibility: font size, high contrast, reduce motion, screen reader

---

## 12. Emotional Design & Tone

Technology anxiety is real and measurable. Design must actively build confidence.

| Principle | Application |
|---|---|
| **Warm, encouraging language** | "Great job!" after completing a step. Never use cold, technical confirmations. |
| **No patronizing tone** | Avoid childish design. Seniors find overly simplified "senior modes" boring if they strip useful features (ACM 2024). Balance simplicity with respect. |
| **Celebrate progress** | Show completion states and small wins. |
| **Reduce fear of consequence** | Before any important action, explain what will happen and that it can be undone. |
| **Familiar metaphors** | Use real-world analogies. A "folder" for organization, a "mailbox" for messages. |
| **Cultural sensitivity** | Iconography, color meaning, and reading patterns vary by culture. Don't assume Western conventions are universal. Consider RTL layouts, CJK typography rules, and cultural color associations. |
| **Support family involvement** | Allow a "helper" or "family member" role that can assist with setup without taking over the account. Family support is the #1 buffer against digital anxiety (JMIR 2026). |

---

## Quick Checklist

Before shipping any screen for older adult users, verify:

- [ ] One primary action per screen
- [ ] Touch targets ≥ 16mm with ≥ 3mm spacing
- [ ] Body text ≥ 18px, contrast ≥ 7:1
- [ ] All icons have text labels
- [ ] No typing required (or voice/selection alternative provided)
- [ ] Navigation is always visible with clear "back" and "home"
- [ ] Destructive actions require confirmation
- [ ] Error messages explain what happened + how to fix it
- [ ] Loading states provide visual feedback
- [ ] No jargon — plain language throughout
- [ ] No dark patterns, hidden charges, or intrusive ads
- [ ] Tested with actual users aged 60+

---

## Regulatory Compliance

Be aware of these legal frameworks when designing for older adults:

- **WCAG 2.2 Level AA** — Minimum legal standard in most jurisdictions (EU, US, many others). Target Level AAA where possible.
- **European Accessibility Act (EAA)** — Enforceable since June 28, 2025. Applies to private sector products including e-commerce, banking, transport, and electronics across all EU member states.
- **China MIIT Age-Friendly Regulations** — Require larger fonts, ban pop-up ads in senior mode, mandate human agent access without complex IVR.
- **ADA (Americans with Disabilities Act)** — Applies to digital products in the US.
- **EN 301 549** — European standard for ICT accessibility, supports both EAA and the Web Accessibility Directive.

---

*This skill is based on 40+ peer-reviewed studies, systematic reviews, and guidelines from institutions including NNGroup, JMIR, PMC/NIH, Monash University (Australia), Universidad Politécnica de Madrid (Spain), Tongji University (China), Yonsei University (Korea), and research from China, Japan, South Korea, Saudi Arabia, Malaysia, Thailand, the UK, Germany, and the US. See `references/research-sources.md` for the full bibliography.*
