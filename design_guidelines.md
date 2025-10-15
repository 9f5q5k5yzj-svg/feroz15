# Design Guidelines: Esoteric Birthday Wishlist

## Design Approach
**Reference-Based Aesthetic**: Digicam nighttime photography - blurry city lights, film grain texture, moody exposure, soft glows, and dreamy atmosphere. Drawing inspiration from late-night street photography and Y2K digital camera aesthetics.

## Core Design Principles
- **Mobile-first experience**: Optimized for phone viewing with generous touch targets
- **Atmospheric depth**: Layered backgrounds, subtle glows, and film grain textures
- **Smooth, dreamy interactions**: Gentle animations that feel ethereal and sophisticated
- **Esoteric minimalism**: Clean layouts with moody, artistic touches

## Color Palette

**Dark Mode Primary Colors:**
- Deep Navy: 220 40% 12% (main background)
- Midnight Blue: 220 35% 18% (card backgrounds)
- Soft Cream: 45 20% 92% (primary text)
- Muted Blue-Grey: 220 15% 65% (secondary text)

**Accent Colors:**
- Electric Blue: 210 85% 65% (CTAs, links, price tags)
- Light Sky: 200 70% 80% (highlights, hover states)

**Atmospheric Effects:**
- Subtle radial gradients with dark blue (220 45% 8%) to navy
- Film grain overlay at 3-5% opacity
- Soft blue glows around interactive elements (box-shadow with Electric Blue at 15% opacity)

## Typography

**Font Families:**
- Primary: Inter or Helvetica Neue (clean, modern, readable on mobile)
- Accent: Space Grotesk or similar geometric sans (for headers, marquee text)

**Type Scale:**
- Hero Marquee: text-6xl to text-8xl, font-bold, tracking-tight
- Section Headlines: text-3xl to text-4xl, font-semibold
- Wishlist Item Titles: text-xl, font-medium
- Body Text: text-base to text-lg, leading-relaxed
- Price Tags: text-sm to text-base, font-semibold
- Footer Links: text-sm

## Layout System

**Spacing Primitives**: Use Tailwind units of 4, 6, 8, 12, 16, 20, 24 for consistent rhythm
- Section padding: py-16 md:py-24
- Card spacing: p-6 to p-8
- Element gaps: gap-4, gap-6, gap-8

**Container System:**
- Max width: max-w-6xl for content sections
- Mobile: px-6 for comfortable edge spacing
- Hero: Full viewport width with inner padding

## Component Library

**Header:**
- Fixed or sticky positioning with backdrop blur
- Dark navy background (Midnight Blue) with subtle transparency
- Logo/title on left, navigation/contact links on right
- Mobile: Hamburger menu or simplified nav
- Height: h-16 to h-20

**Hero Section:**
- Full viewport height (min-h-screen) with video background
- Video: Looped, muted, object-cover with subtle overlay (dark gradient 40% opacity)
- Marquee text: Infinite horizontal scroll, large typography, Electric Blue or Soft Cream
- Film grain texture overlay across entire section

**Intro Section:**
- Centered content with max-w-2xl
- Headline: Large, dramatic typography with subtle glow effect
- Body text: Muted Blue-Grey, generous line height
- Background: Subtle radial gradient from center

**Wishlist Grid:**
- Single column on mobile, 2-3 columns on desktop (grid-cols-1 md:grid-cols-2 lg:grid-cols-3)
- Card design: Midnight Blue background with subtle border (border-Electric Blue/20)
- Card hover: Lift effect (translate-y-[-4px]) with increased glow
- Image: aspect-square or 4:3, rounded corners (rounded-lg), soft blur on edges
- Price tag: Floating badge with Electric Blue background, positioned top-right on image
- Link button: Outlined style with Electric Blue, subtle backdrop blur

**Footer:**
- Dark Navy background with film grain texture
- Centered content with social/contact links
- Icons: Electric Blue with hover glow effects
- Spacing: py-12 with divider line above (border-Muted Blue-Grey/30)

## Visual Effects

**Film Grain Texture:**
- CSS noise filter or SVG grain overlay
- Applied to hero, cards, and footer at 2-4% opacity
- Creates authentic digicam aesthetic

**Glow Effects:**
- Interactive elements: box-shadow with 0 0 20px Electric Blue at 20% opacity
- Hover states: Increase glow intensity and size
- Price tags: Subtle inner glow for luminosity

**Blur Techniques:**
- Video overlay: Slight gaussian blur (1-2px) for dreamy effect
- Button backgrounds: backdrop-filter blur-md on glass-morphic elements
- Image edges: Subtle fade using gradient masks

**Marquee Animation:**
- Smooth infinite scroll (30-40s duration)
- Text repeats 3-4 times for seamless loop
- Slight opacity variation (80-100%) for depth

## Images

**Hero Section:**
- Background video (placeholder ready for user's file)
- Dimensions: 1920x1080 minimum, MP4 format
- Characteristics: Nighttime city scenes, blurry lights, digicam aesthetic
- Treatment: 30-40% dark overlay, subtle blur filter

**Wishlist Item Images:**
- Aspect ratio: Square (1:1) or 4:3 for consistency
- Treatment: Rounded corners (rounded-lg), subtle vignette effect
- Hover: Slight zoom (scale-105) with smooth transition
- 6-8 placeholder items showing varied products

## Responsive Behavior

**Mobile (< 768px):**
- Stack all content in single column
- Larger touch targets (min 44x44px)
- Simplified marquee text (smaller font size)
- Card padding reduces to p-4
- Hero height: min-h-[80vh] for better fold content

**Tablet (768px - 1024px):**
- 2-column wishlist grid
- Balanced spacing with py-20 sections
- Moderate marquee text size

**Desktop (> 1024px):**
- 3-column wishlist grid maximum
- Full atmospheric effects
- Larger marquee text with more dramatic animations

## Accessibility

- Maintain dark mode throughout with sufficient contrast (WCAG AA)
- Video: Autoplay muted with accessible controls hidden
- Focus states: Visible Electric Blue outline (ring-2 ring-Electric Blue)
- Touch targets: Minimum 48px for mobile interactions
- Alt text placeholders for all images