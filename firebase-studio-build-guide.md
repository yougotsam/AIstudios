# Firebase Studio Build Guide — ZeebsOS Homepage

This guide describes how to build the ZeebsOS homepage using Firebase Studio. It presents example blocks in a JSON-like format followed by styling tips.

## 1. Cinematic Hero Section
```json
{
  "type": "hero",
  "background": {
    "gradient": ["#0B0F1C", "#191970"]
  },
  "content": {
    "headline": {
      "text": "Meet ZeebsOS — Your Business Intelligence Avatar",
      "fontFamily": "Sora",
      "fontWeight": "700",
      "fontSize": "64px",
      "color": "#FFFFFF"
    },
    "tagline": {
      "text": "Automate | Accelerate | Scale",
      "fontFamily": "Sora",
      "fontWeight": "600",
      "fontSize": "24px",
      "color": "#FFD700"
    },
    "subheadline": {
      "text": "Automation with soul. The next-gen system that clones your influence, voice, and brand—so you grow 24/7.",
      "fontFamily": "IBM Plex Mono",
      "fontWeight": "400",
      "fontSize": "18px",
      "color": "#FFFFFF"
    },
    "ctaButtons": [
      {
        "text": "Talk to Zeebs",
        "backgroundColor": "#FF3366",
        "hoverGlow": true,
        "fontFamily": "IBM Plex Mono",
        "fontWeight": "700",
        "fontSize": "18px",
        "color": "#FFFFFF",
        "action": "openChat"
      },
      {
        "text": "Book Free Strategy",
        "backgroundColor": "transparent",
        "border": "2px solid #FF3366",
        "fontFamily": "IBM Plex Mono",
        "fontWeight": "700",
        "fontSize": "18px",
        "color": "#FF3366",
        "action": "navigateToBooking"
      }
    ]
  },
  "animation": {
    "orb": {
      "type": "glowingWaveform",
      "color": "#00FFF0",
      "size": "128px",
      "pulse": true,
      "interactive": true
    }
  },
  "layout": {
    "paddingVertical": "128px",
    "centerContent": true
  }
}
```

**Styling Tips**
- Use `background: linear-gradient(180deg, #0B0F1C 0%, #191970 100%);` for the hero background.
- Import **Sora** and **IBM Plex Mono** from Google Fonts or self-host them.
- Add a hover glow effect on the primary CTA using `box-shadow`.
- Animate the orb with a subtle pulse via CSS.
- Ensure the text and orb scale down smoothly on mobile.

## 2. Access Panels (3 Core Flows)
```json
{
  "type": "grid",
  "columns": 3,
  "gap": "40px",
  "cards": [
    {
      "icon": "⚡",
      "title": "AI Business Avatars",
      "text": "Clone your presence. AI agents that think, speak, and create content like you.",
      "background": "#1A1A1F",
      "color": "#FFFFFF",
      "hoverEffect": "blueGlow"
    },
    {
      "icon": "🎙️",
      "title": "Conversational Voice AI Agents",
      "text": "Automated, branded voice assistants for lead gen, service, and community.",
      "background": "#1A1A1F",
      "color": "#FFFFFF",
      "hoverEffect": "goldGlow"
    },
    {
      "icon": "🎬",
      "title": "AI-Powered Video Storytelling",
      "text": "Scroll-stopping video & branded content to amplify your message.",
      "background": "#1A1A1F",
      "color": "#FFFFFF",
      "hoverEffect": "blueGoldGlow"
    }
  ],
  "responsive": {
    "mobileStack": true,
    "mobileGap": "30px"
  }
}
```

**Styling Tips**
- Give each card rounded corners (`12px`) and padding (`30px`).
- Apply a glowing `box-shadow` on hover.
- Use bold titles (`20px`) and body text (`16px`).
- Stack cards vertically on mobile with smaller gaps.

## 3. Bold Glowing CTA
```json
{
  "type": "cta",
  "text": "Let’s build the system that builds you.",
  "buttons": [
    {
      "text": "Talk to Zeebs",
      "backgroundColor": "#FF3366",
      "hoverGlow": true,
      "action": "openChat"
    },
    {
      "text": "Book a Free Strategy Session",
      "backgroundColor": "transparent",
      "border": "2px solid #FF3366",
      "action": "navigateToBooking"
    }
  ],
  "background": "#0B0F1C",
  "textColor": "#FFFFFF",
  "padding": "80px 0",
  "layout": "centered"
}
```

**Styling Tips**
- Center all text and buttons.
- Add `20px` margin between the buttons.
- Use a pulsing glow on hover for the primary button.

## 4. Zeebs Dock / Chat Orb
```json
{
  "type": "floatingChatOrb",
  "position": "bottomRight",
  "size": "80px",
  "color": "#00FFF0",
  "pulse": true,
  "action": "openChatModal",
  "tooltip": "Talk to Zeebs"
}
```

**Implementation Tips**
- Use Firebase Studio’s floating component or a fixed-position `div`.
- Animate the pulse using CSS `@keyframes`.
- Display a tooltip on hover or focus.

## 5. Section Rhythm & Color Separation
- Alternate backgrounds between **Midnight Blue** (`#0B0F1C`) and **Slate Black** (`#1A1A1F`) for each section.
- Use **Cyber Gold** (`#FFD700`) and **Neon Cyan** (`#00FFF0`) for highlights and interactive elements.
- Add subtle glassmorphism overlays with `rgba` white at 5% opacity.

## 6. Loveline Teaser Section
```json
{
  "type": "teaser",
  "title": "AI After Hours — Loveline",
  "subtitle": "Explore late-night conversations around human potential, AI, and connection.",
  "ctaButtons": [
    {
      "text": "Listen Now",
      "backgroundColor": "#FF3366",
      "hoverGlow": true,
      "action": "navigateToPodcast"
    },
    {
      "text": "About Loveline",
      "backgroundColor": "transparent",
      "border": "2px solid #FF3366",
      "action": "navigateToAbout"
    }
  ],
  "background": "#1A1A1F",
  "textColor": "#FFFFFF",
  "padding": "60px 20px"
}
```

## End Goal & Next Steps

Use these blocks and tips as a starting point for building the ZeebsOS homepage in Firebase Studio. The end goal is a polished, responsive landing page that reflects your brand. After assembling the sections:

1. Preview the page in Firebase Studio and adjust copy, imagery, or animations as needed.
2. Connect the project to Firebase Hosting or your existing site.
3. Publish when everything renders and behaves as expected.

You can adapt or extend these examples to fit specific design and functionality requirements.
