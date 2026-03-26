# AcademicFlow Slide Design System

## Brand Guidelines & Design Tokens

---

## 1. Colors

### Primary Colors
| Name | HEX | Usage |
|------|-----|-------|
| **Brand Black** | `#111111` | Primary text, headings, default badges |
| **Brand Blue** | `#5551FF` | Accent color, interactive elements, highlights |
| **Brand Red** | `#FF7262` | Alerts, problems, input indicators |

### Neutral Colors
| Name | HEX | Usage |
|------|-----|-------|
| **White** | `#FFFFFF` | Slide background |
| **Gray 50** | `#F9FAFB` | Light backgrounds, cards |
| **Gray 100** | `#F3F4F6` | Borders, dividers |
| **Gray 200** | `#E5E7EB` | Subtle borders |
| **Gray 400** | `#9CA3AF` | Muted text |
| **Gray 500** | `#6B7280` | Subtitles, secondary text |
| **Background Dark** | `#222222` | Viewer/presentation background |

### Tailwind Config
```javascript
colors: {
    'brand-black': '#111111',
    'brand-blue': '#5551FF',
    'brand-red': '#FF7262',
    'brand-gray': '#F3F4F6',
    'brand-bg': '#FFFFFF',
}
```

---

## 2. Typography

### Font Family
**Inter** - Used for all text elements
```css
font-family: 'Inter', sans-serif;
```

### Type Scale
| Element | Size | Weight | Class |
|---------|------|--------|-------|
| **H1 (Title)** | 48px (3rem) | 800 (extrabold) | `text-5xl font-extrabold` |
| **H2 (Card Title)** | 24px (1.5rem) | 700 (bold) | `text-2xl font-bold` |
| **H3 (Section)** | 18px (1.125rem) | 700 (bold) | `text-lg font-bold` |
| **Subtitle** | 20px (1.25rem) | 500 (medium) | `text-xl font-medium` |
| **Body** | 14px | 400 (normal) | `text-sm` |
| **Small** | 12px | 400-600 | `text-xs` |
| **Badge** | 11px | 700 (bold) | `text-[11px] font-bold` |
| **Micro** | 10px | 700 (bold) | `text-[10px] font-bold` |

### Letter Spacing
- H1: `-0.03em` (`letter-spacing: -0.03em`)
- H2: `-0.02em` (`letter-spacing: -0.02em`)
- Badges: `tracking-wider` (0.05em)
- Labels: `tracking-widest` (0.1em)

---

## 3. Slide Layout

### Container
```css
.slide-container {
    width: 1280px;
    height: 720px;           /* 16:9 aspect ratio */
    padding: 48px 64px;      /* Fixed padding */
    background-color: #FFFFFF;
    overflow: hidden;
}
```

### Standard Header Structure
```html
<!-- HEADER -->
<div class="flex justify-between items-start mb-8 shrink-0">
    <div>
        <div class="inline-block bg-brand-black text-white text-[11px] font-bold px-3 py-1 rounded mb-3 uppercase tracking-wider">
            BADGE TEXT
        </div>
        <h1 class="text-5xl font-extrabold text-brand-black mb-1">
            Slide Title
        </h1>
        <p class="text-xl text-gray-500 font-medium">
            Subtitle or description text
        </p>
    </div>

    <!-- Optional: Right-side element -->
</div>
```

### Spacing System
| Token | Value | Usage |
|-------|-------|-------|
| `mb-1` | 4px | Between title and subtitle |
| `mb-3` | 12px | Between badge and title |
| `mb-8` | 32px | Header to content |
| `gap-8` | 32px | Between columns/cards |
| `gap-12` | 48px | Large content gaps |
| `p-6` | 24px | Card padding |

---

## 4. Components

### Badge
Standard badge for slide categorization:
```html
<div class="inline-block bg-brand-black text-white text-[11px] font-bold px-3 py-1 rounded mb-3 uppercase tracking-wider">
    BADGE TEXT
</div>
```

**Badge Color Variants:**
- Default: `bg-brand-black text-white`
- Blue: `bg-brand-blue text-white`
- Red: `bg-brand-red text-white`
- Light: `bg-gray-100 text-brand-black border border-gray-200`

### Card
```html
<div class="bg-white rounded-xl border border-gray-200 p-6 shadow-sm">
    <!-- Card content -->
</div>
```

**Card with Color Accent:**
```html
<div class="relative bg-white rounded-xl border border-gray-200 shadow-sm">
    <div class="h-1.5 w-full bg-brand-blue rounded-t-xl"></div>
    <div class="p-6">
        <!-- Card content -->
    </div>
</div>
```

### Pills / Tags
```html
<span class="bg-blue-50 text-brand-blue font-bold text-xs px-2 py-1 rounded">
    Label
</span>
```

### Stat Number (Large)
```html
<div class="text-8xl font-extrabold text-brand-black">
    900
</div>
<div class="text-xl text-gray-500 font-medium">
    Description
</div>
```

---

## 5. Slide Types

### 1. Cover/Title Slide
- Centered layout
- Large title with decorative badges
- No header badge required

### 2. Statement Slide
- Single large number or text
- Minimal elements
- High impact

### 3. Content Slide (Standard)
- Header with badge + title + subtitle
- Content area below
- Consistent header position

### 4. Grid/Card Slide
- Header (standard)
- 2-4 column grid of cards
- Cards with color accents

### 5. Timeline Slide
- Header (standard)
- Horizontal timeline visualization
- Phase markers

---

## 6. Visual Elements

### Shadows
```css
/* Card shadow */
box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1),
            0 2px 4px -1px rgba(0, 0, 0, 0.06);

/* Slide shadow (in viewer) */
box-shadow: 0 0 100px rgba(0, 0, 0, 0.5);
```

### Border Radius
| Size | Value | Usage |
|------|-------|-------|
| `rounded` | 4px | Badges, small elements |
| `rounded-lg` | 8px | Buttons, inputs |
| `rounded-xl` | 12px | Cards, containers |
| `rounded-full` | 9999px | Pills, avatars |

### Dividers
```html
<div class="w-full h-px bg-gray-100"></div>
```

---

## 7. Icons

**Library:** Phosphor Icons
```html
<script src="https://unpkg.com/@phosphor-icons/web"></script>
```

**Usage:**
```html
<i class="ph-bold ph-arrow-right"></i>
<i class="ph-fill ph-check-circle"></i>
```

**Styles:** `ph-thin`, `ph-light`, `ph-regular`, `ph-bold`, `ph-fill`, `ph-duotone`

---

## 8. Required Imports

```html
<!-- Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">

<!-- Tailwind CSS -->
<script src="https://cdn.tailwindcss.com"></script>

<!-- Icons -->
<script src="https://unpkg.com/@phosphor-icons/web"></script>

<!-- Tailwind Config -->
<script>
    tailwind.config = {
        theme: {
            extend: {
                colors: {
                    'brand-black': '#111111',
                    'brand-blue': '#5551FF',
                    'brand-red': '#FF7262',
                    'brand-gray': '#F3F4F6',
                    'brand-bg': '#FFFFFF',
                },
                fontFamily: {
                    sans: ['Inter', 'sans-serif'],
                }
            }
        }
    }
</script>
```

---

## 9. Slide Template

```html
<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Slide Title</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://unpkg.com/@phosphor-icons/web"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        'brand-black': '#111111',
                        'brand-blue': '#5551FF',
                        'brand-red': '#FF7262',
                        'brand-gray': '#F3F4F6',
                        'brand-bg': '#FFFFFF',
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <style>
        body {
            margin: 0;
            padding: 0;
            background-color: #222;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            font-family: 'Inter', sans-serif;
        }

        .slide-container {
            width: 1280px;
            height: 720px;
            background-color: #FFFFFF;
            position: relative;
            display: flex;
            flex-direction: column;
            padding: 48px 64px;
            box-sizing: border-box;
            box-shadow: 0 0 100px rgba(0,0,0,0.5);
            overflow: hidden;
        }
    </style>
</head>
<body>
    <div class="slide-container">

        <!-- HEADER -->
        <div class="flex justify-between items-start mb-8 shrink-0">
            <div>
                <div class="inline-block bg-brand-black text-white text-[11px] font-bold px-3 py-1 rounded mb-3 uppercase tracking-wider">Badge</div>
                <h1 class="text-5xl font-extrabold text-brand-black mb-1">Slide Title</h1>
                <p class="text-xl text-gray-500 font-medium">Subtitle goes here.</p>
            </div>
        </div>

        <!-- CONTENT -->
        <div class="flex-grow">
            <!-- Your content here -->
        </div>

    </div>
</body>
</html>
```

---

## 10. Do's and Don'ts

### Do's
- Keep badge text short (1-2 words)
- Use consistent header structure across content slides
- Maintain 48px/64px padding
- Use brand colors consistently
- Keep text concise and scannable

### Don'ts
- Don't use more than 3 colors per slide
- Don't vary badge positions between content slides
- Don't use fonts other than Inter
- Don't overcrowd slides with text
- Don't use shadows on text
