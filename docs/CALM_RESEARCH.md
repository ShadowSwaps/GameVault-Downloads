# Calm theme design

Calm in 0.3.7 uses dim slate and forest surfaces, muted sage accents and off-white text. This follows the owner's preference for a quiet, darker appearance. It is a design choice, not a claim that one palette is calming for everyone.

## Evidence and limits

- Wilms and Oberfeld, *Color and emotion: effects of hue, saturation, and brightness* (2018), tested 62 participants with controlled color patches. Brighter and more saturated colors produced higher rated arousal; hue also mattered. This supports reducing bright, saturated surfaces, but the experiment does not establish a universally calming application theme. [Study abstract](https://pubmed.ncbi.nlm.nih.gov/28612080/).
- A systematic review of 132 studies found many-to-many color/emotion associations across contexts. Blue and green often aligned with lower-arousal positive emotions; black is not automatically calming. [Review](https://link.springer.com/article/10.3758/s13423-024-02615-z).
- Dim surfaces still need readable text and recognizable controls. The theme tests enforce at least 4.5:1 for normal interface text, and 3:1 for Calm field boundaries and focus accents. [WCAG text contrast](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html), [non-text contrast](https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html).
- Calm removes card lift, hero glow and decorative overlays. The other themes retain their normal appearance and continue to honor the operating system's reduced-motion preference. [W3C reduced-motion technique](https://www.w3.org/WAI/WCAG22/Techniques/css/C39).

## Applied choices

| Element | Calm color or behavior |
| --- | --- |
| Background | `#172222` |
| Panels | `#202d29` |
| Text | `#d6e1df` |
| Secondary text | `#aebfb8` |
| Accent | `#9fbcaf` |
| Inputs | Dark native controls with visible boundaries |
| Motion | No card lift or button transitions |
| Hero and companion panels | Steady surfaces without bright glows |

Game covers keep their original artwork. Calm changes interface surfaces rather than dimming or recoloring the user's images. Theme preferences, backup compatibility and unfinished form preservation remain covered by the existing theme tests.
