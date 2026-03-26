# AcademicFlow Brand Guidelines

> Authoritative design system derived from [academicflow.studio](https://academicflow.studio). All AcademicFlow surfaces (website, add-in, docs, presentations) should follow these guidelines.

---

## 1. Brand Identity

**Product name:** AcademicFlow (one word, camelCase capital F)
**Tagline:** Intelligente Forschung. Souveräne Daten.
**Description:** Die erste KI-Schreibassistenz fur den DACH-Raum.
**Language:** German (de-DE) primary, English secondary.
**Tone:** Professional, academic, trustworthy, privacy-conscious.

---

## 2. Logo

| Variant | File | Use |
|---------|------|-----|
| Source vector | `logo.svg` | Master file, web |
| High-res | `logo-1024.png` | Print, presentations |
| Standard | `logo-500.png` | GitHub avatar, social |
| Small | `logo-200.png` | Favicons, thumbnails |

**Sizing:** Navbar: 36x36px. Footer: 32x32px. Minimum: 24x24px.
**Clear space:** Minimum half the logo width on all sides.
**Logo text:** Set in Geist, `font-bold tracking-tight text-slate-900`. Always next to the logo mark, never stacked.

---

## 3. Colors

### Primary

| Name | Hex | Tailwind | Usage |
|------|-----|----------|-------|
| Blue | `#3b82f6` | `blue-600` | Primary actions, CTAs, active states, links |
| Blue Dark | `#1e40af` | `blue-700` | Hover states on primary buttons |
| Blue Light | `#eff6ff` | `blue-50` | Highlight backgrounds, feature cards, icon containers |

### Neutrals

| Name | Hex | Tailwind | Usage |
|------|-----|----------|-------|
| Foreground | `#0f172a` | `slate-900` | Headings, primary text |
| Body text | `#475569` | `slate-600` | Secondary text, descriptions |
| Muted | `#94a3b8` | `slate-400` | Timestamps, metadata, footer text |
| Border | `#e2e8f0` | `slate-200` | Card borders, dividers |
| Light border | `#f1f5f9` | `slate-100` | Section dividers, subtle lines |
| Background | `#FDFDFD` | custom | Page background |
| Surface | `#ffffff` | `white` | Cards, navbar, inputs |
| Surface alt | `#f8fafc` | `slate-50` | Alternate section backgrounds |

### Semantic

| Name | Hex | Tailwind | Usage |
|------|-----|----------|-------|
| Success | `#059669` | `emerald-600` | Compliance, verified states |
| Warning | `#d97706` | `amber-600` | Announcements, caution |
| Error | `#dc2626` | `red-600` | Errors, fabrication alerts |
| Research | `#9333ea` | `purple-600` | Research category badges |

Each semantic color uses a `*-50` background with `*-100` border for badge/card containers.

### Text selection

```css
::selection {
  background-color: #dbeafe; /* blue-100 */
  color: #1e3a8a;            /* blue-900 */
}
```

---

## 4. Typography

### Font family

**Geist** (sans-serif) for all text. **Geist Mono** for code. Both loaded from Google Fonts, latin subset.

```css
--font-geist-sans: 'Geist', sans-serif;
--font-geist-mono: 'Geist Mono', monospace;
```

### Type scale

| Element | Size | Weight | Tailwind | Tracking |
|---------|------|--------|----------|----------|
| Hero headline | 4.5rem (72px) | 800 | `text-7xl font-extrabold` | `tracking-tight` |
| Page heading | 3rem (48px) | 800 | `text-5xl font-extrabold` | `tracking-tight` |
| Section heading | 2.25rem (36px) | 800 | `text-4xl font-extrabold` | `tracking-tight` |
| Card heading | 1.5rem (24px) | 700 | `text-2xl font-bold` | default |
| Large body | 1.25rem (20px) | 500 | `text-xl font-medium` | default |
| Body | 1rem (16px) | 400 | `text-base` | default |
| Small | 0.875rem (14px) | 600 | `text-sm font-semibold` | default |
| Badge | 10px | 700 | `text-[10px] font-bold uppercase` | `tracking-widest` |

### Line height

- Headlines: `leading-tight` or `leading-[1.1]`
- Body: `leading-relaxed`

---

## 5. Spacing

All spacing follows Tailwind's 4px base scale.

| Token | Value | Usage |
|-------|-------|-------|
| Section padding | `py-24 px-6` | Standard section vertical/horizontal |
| Hero top | `pt-32` | Below fixed navbar |
| Card padding | `p-6` or `p-8` | Interior card spacing |
| Component gap | `gap-4` to `gap-8` | Between sibling elements |
| Section gap | `gap-12` to `gap-20` | Between major blocks |
| Max width | `max-w-7xl` (1280px) | Container constraint |
| Article width | `max-w-4xl` (896px) | Long-form content |

---

## 6. Components

### Buttons

**Primary CTA**
```
bg-blue-600 hover:bg-blue-700 text-white font-bold
px-8 py-4 rounded-2xl shadow-xl shadow-blue-200
```

**Secondary**
```
bg-white border border-slate-200 hover:bg-slate-50
text-slate-900 font-bold px-8 py-4 rounded-2xl
```

**Navbar**
```
bg-slate-900 hover:bg-blue-600 text-white font-bold
px-5 py-2.5 rounded-full text-sm
```

**Link**
```
text-blue-600 font-bold inline-flex items-center gap-3
```
Pair with `ArrowRight` icon. On hover: `gap-4` (icon shifts right).

### Cards

**Standard**
```
bg-white p-6 rounded-2xl border border-slate-200
shadow-sm hover:shadow-md transition-shadow
```

**Feature highlight**
```
bg-slate-50 p-8 rounded-[2.5rem] border border-slate-100
```

**Icon container** (inside cards)
```
w-12 h-12 bg-blue-50 rounded-xl flex items-center justify-center
text-blue-600
```

### Badges

```
text-[10px] font-bold uppercase tracking-widest
px-2.5 py-1 rounded-full border
```

Color by category:
| Category | Background | Text | Border |
|----------|-----------|------|--------|
| Default | `blue-50` | `blue-700` | `blue-100` |
| Feature | `emerald-50` | `emerald-700` | `emerald-100` |
| Research | `purple-50` | `purple-700` | `purple-100` |
| Announcement | `amber-50` | `amber-700` | `amber-100` |
| Error/Alert | `red-50` | `red-700` | `red-100` |

### Navigation

```
fixed top-0 w-full z-50
bg-white/80 backdrop-blur-md border-b border-slate-100
```
Links: `text-sm font-semibold text-slate-500 hover:text-blue-600`

### Footer

```
bg-white border-t border-slate-100 py-20 px-6
```
Text: `text-slate-400 text-sm font-medium`
Links: `hover:text-blue-600 transition-colors`

### Forms

```
Input:  w-full px-4 py-3 rounded-xl border border-slate-200
Focus:  focus:border-blue-500 focus:ring-2 focus:ring-blue-200
Label:  text-sm font-semibold text-slate-700 mb-2
```

---

## 7. Icons

**Library:** Lucide React

**Standard sizes:** 16px (inline), 20px (buttons), 24px (cards), 48px (feature hero)

**Core icon set:**

| Icon | Usage |
|------|-------|
| `Search` | Source discovery |
| `ShieldCheck` | Verification, compliance |
| `Layout` | Word integration |
| `Lock` | Privacy, Sperrvermerk |
| `Database` | Data, Azure |
| `Globe` | DACH market |
| `ArrowRight` | CTAs, navigation |
| `CheckCircle2` | Success, completed |
| `AlertCircle` | Warnings, errors |
| `FileText` | Documents, whitepaper |
| `Zap` | Speed, AI power |
| `Cpu` | Technology, ML |

---

## 8. Border radius

| Token | Value | Usage |
|-------|-------|-------|
| `rounded-xl` | 12px | Inputs, icon containers |
| `rounded-2xl` | 16px | Cards, buttons |
| `rounded-3xl` | 24px | Large cards, compliance section |
| `rounded-[2.5rem]` | 40px | Feature highlight panels |
| `rounded-full` | pill | Badges, navbar CTA |

---

## 9. Shadows

| Level | Class | Usage |
|-------|-------|-------|
| Subtle | `shadow-sm` | Cards at rest |
| Medium | `shadow-md` | Navbar, hover state |
| Elevated | `shadow-lg` | Card hover, modals |
| Prominent | `shadow-xl shadow-blue-200` | Primary CTA |

---

## 10. Motion

**Duration:** 500ms default, 700ms for longer sequences.

**Entrance animations:**
```css
@keyframes slide-in-from-bottom-10 {
  from { transform: translateY(2.5rem); opacity: 0; }
  to   { transform: translateY(0); opacity: 1; }
}

@keyframes fade-in {
  from { opacity: 0; }
  to   { opacity: 1; }
}
```

**Hover transitions:** `transition-colors`, `transition-shadow`, `transition-all`
**Hover patterns:** Shadow elevation, border color shift to blue-200, icon translate-x.

---

## 11. Responsive breakpoints

| Breakpoint | Width | Behaviour |
|------------|-------|-----------|
| Base | <640px | Single column, stacked layout |
| `sm` | 640px | Minor adjustments |
| `md` | 768px | Multi-column grids, navbar links visible |
| `lg` | 1024px | Full layouts |

Design mobile-first. Enhance with `md:` and `lg:` prefixes.

---

## 12. Do's and Don'ts

**Do:**
- Use `blue-600` as the single accent color across all surfaces
- Keep text in `slate-900` (headings) and `slate-600` (body)
- Use Geist everywhere, including presentations
- Maintain generous whitespace (`py-24` section padding)
- Use rounded-2xl for cards and buttons consistently
- Pair icons with text labels

**Don't:**
- Use colors outside this palette (no brand-black `#111111`, no brand-red `#FF7262` from the old slide system)
- Mix font families (no Inter, no system fonts)
- Use shadows on text
- Overcrowd sections with more than 4 cards per row
- Use rounded-lg or smaller on cards (reserved for inputs/icons)
