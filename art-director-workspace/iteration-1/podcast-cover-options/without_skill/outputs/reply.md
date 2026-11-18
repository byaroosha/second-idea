I can't generate images in this chat, so I built these as SVGs instead: real square vector artwork with the title set, not mockups. Save any code block below as a `.svg` file and open it in a browser to see it.

I skipped the moon-and-stars-on-navy look on purpose. A lot of sleep shows use it, and yours would blend in.

## 1. One Lit Window

A dark apartment block with one window still lit. It tells a listener they're not the only one up, which is a warmer promise than most insomnia content makes. Serif title in navy and lamp yellow. Best if the show is personal and reassuring.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 1000">
  <defs>
    <radialGradient id="window-glow" cx="710" cy="312" r="300" gradientUnits="userSpaceOnUse">
      <stop offset="0" stop-color="#FFC857" stop-opacity="0.28"/>
      <stop offset="1" stop-color="#FFC857" stop-opacity="0"/>
    </radialGradient>
  </defs>
  <rect width="1000" height="1000" fill="#0F1535"/>
  <rect width="1000" height="1000" fill="url(#window-glow)"/>
  <g fill="#1D2757">
    <rect x="100" y="100" width="100" height="116" rx="8"/>
    <rect x="240" y="100" width="100" height="116" rx="8"/>
    <rect x="380" y="100" width="100" height="116" rx="8"/>
    <rect x="520" y="100" width="100" height="116" rx="8"/>
    <rect x="660" y="100" width="100" height="116" rx="8"/>
    <rect x="800" y="100" width="100" height="116" rx="8"/>
    <rect x="100" y="254" width="100" height="116" rx="8"/>
    <rect x="240" y="254" width="100" height="116" rx="8"/>
    <rect x="380" y="254" width="100" height="116" rx="8"/>
    <rect x="520" y="254" width="100" height="116" rx="8"/>
    <rect x="800" y="254" width="100" height="116" rx="8"/>
    <rect x="100" y="408" width="100" height="116" rx="8"/>
    <rect x="240" y="408" width="100" height="116" rx="8"/>
    <rect x="380" y="408" width="100" height="116" rx="8"/>
    <rect x="520" y="408" width="100" height="116" rx="8"/>
    <rect x="660" y="408" width="100" height="116" rx="8"/>
    <rect x="800" y="408" width="100" height="116" rx="8"/>
  </g>
  <rect x="660" y="254" width="100" height="116" rx="8" fill="#FFC857"/>
  <g font-family="Georgia, 'Times New Roman', serif" font-weight="700" font-size="190">
    <text x="100" y="715" textLength="595" fill="#FFF4DC">WIDE</text>
    <text x="100" y="900" textLength="800" fill="#FFC857">AWAKE</text>
  </g>
</svg>
```

## 2. 3:07

The bedside clock every insomniac knows, glowing red in a black room. It's dry, a little funny, and clearly about insomnia rather than sleep in general. Best if the tone is candid or wry.

```svg
<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 1000 1000">
  <defs>
    <radialGradient id="clock-glow" cx="500" cy="730" r="520" gradientUnits="userSpaceOnUse">
      <stop offset="0" stop-color="#FF3B2F" stop-opacity="0.22"/>
      <stop offset="1" stop-color="#FF3B2F" stop-opacity="0"/>
    </radialGradient>
    <path id="eight" d="M26 20 L46 0 H144 L164 20 L144 40 H46 Z M170 26 L190 46 V144 L170 164 L150 144 V46 Z M170 176 L190 196 V294 L170 314 L150 294 V196 Z M26 320 L46 300 H144 L164 320 L144 340 H46 Z M20 176 L40 196 V294 L20 314 L0 294 V196 Z M20 26 L40 46 V144 L20 164 L0 144 V46 Z M26 170 L46 150 H144 L164 170 L144 190 H46 Z"/>
  </defs>
  <rect width="1000" height="1000" fill="#0B0A0D"/>
  <rect width="1000" height="1000" fill="url(#clock-glow)"/>
  <g font-family="'Helvetica Neue', Helvetica, Arial, sans-serif" font-weight="700" font-size="210" fill="#F4EFE6">
    <text x="100" y="251" textLength="550">WIDE</text>
    <text x="100" y="441" textLength="800">AWAKE</text>
  </g>
  <!-- unlit segments, faintly visible like a real display -->
  <g fill="#FF3B2F" fill-opacity="0.12">
    <use xlink:href="#eight" x="100" y="560"/>
    <use xlink:href="#eight" x="466" y="560"/>
    <use xlink:href="#eight" x="710" y="560"/>
  </g>
  <!-- lit segments: 3 : 0 7 -->
  <g fill="#FF3B2F">
    <path transform="translate(100 560)" d="M26 20 L46 0 H144 L164 20 L144 40 H46 Z M170 26 L190 46 V144 L170 164 L150 144 V46 Z M26 170 L46 150 H144 L164 170 L144 190 H46 Z M170 176 L190 196 V294 L170 314 L150 294 V196 Z M26 320 L46 300 H144 L164 320 L144 340 H46 Z"/>
    <rect x="358" y="645" width="40" height="40"/>
    <rect x="358" y="775" width="40" height="40"/>
    <path transform="translate(466 560)" d="M26 20 L46 0 H144 L164 20 L144 40 H46 Z M170 26 L190 46 V144 L170 164 L150 144 V46 Z M170 176 L190 196 V294 L170 314 L150 294 V196 Z M26 320 L46 300 H144 L164 320 L144 340 H46 Z M20 176 L40 196 V294 L20 314 L0 294 V196 Z M20 26 L40 46 V144 L20 164 L0 144 V46 Z"/>
    <path transform="translate(710 560)" d="M26 20 L46 0 H144 L164 20 L144 40 H46 Z M170 26 L190 46 V144 L170 164 L150 144 V46 Z M170 176 L190 196 V294 L170 314 L150 294 V196 Z"/>
  </g>
</svg>
```

## 3. Eyes Open

Two wide, tired eyes on bright yellow, with WIDE spaced out to the full width. It's the loudest of the three and the one most likely to get noticed among dark covers. Best if the show is light and conversational; it would undersell a clinical one.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 1000">
  <rect width="1000" height="1000" fill="#FFD43B"/>
  <!-- whites of the eyes -->
  <g fill="#FFFDF7" stroke="#17130E" stroke-width="20">
    <circle cx="280" cy="290" r="170"/>
    <circle cx="720" cy="290" r="170"/>
  </g>
  <!-- small pupils: the wired, can't-switch-off stare -->
  <g fill="#17130E">
    <circle cx="280" cy="290" r="58"/>
    <circle cx="720" cy="290" r="58"/>
  </g>
  <g fill="#FFFDF7">
    <circle cx="300" cy="270" r="15"/>
    <circle cx="740" cy="270" r="15"/>
  </g>
  <!-- bags under the eyes -->
  <g fill="none" stroke="#17130E" stroke-width="16" stroke-linecap="round">
    <path d="M157 466 A215 215 0 0 0 403 466"/>
    <path d="M597 466 A215 215 0 0 0 843 466"/>
  </g>
  <g font-family="'Arial Black', 'Helvetica Neue', Helvetica, Arial, sans-serif" font-weight="900" font-size="195" fill="#17130E">
    <text x="100" y="715" textLength="800">WIDE</text>
    <text x="100" y="900" textLength="800">AWAKE</text>
  </g>
</svg>
```

## My pick

One Lit Window. The single yellow square still reads at thumbnail size, and it gives the show a feeling as well as a topic. If your tone is more irreverent than comforting, go with Eyes Open.

## Before you upload

- **Export size:** 3000 × 3000 px, PNG or JPG, RGB. Apple Podcasts accepts square art from 1400 to 3000 px, and the same file works in other podcast apps. Figma, Canva, or Inkscape will open the SVG and export it.
- **Fonts:** the titles use fonts already on most computers (Georgia, Helvetica or Arial, Arial Black), so the letters can look slightly different from one machine to another. Convert the text to outlines before exporting, or swap in a typeface you have a license for.
- **Check it small:** I can't preview renders here, so I haven't seen these on screen. Look at each one at about 60 px wide, roughly how it appears in a podcast app list, and tell me if anything looks off.

Tell me which direction is closest and I'll refine it: colors, typeface, the time on the clock, or a version with a host name added.
