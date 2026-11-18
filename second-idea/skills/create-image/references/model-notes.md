# Model notes

How prompt style and settings differ between model families. Image models change fast, and version numbers, parameter names and limits here will go stale. When the tool's own schema or current documentation disagrees with this file, trust those.

## Contents

- Three prompt dialects
- Settings that matter
- Aspect ratio
- Editing and references

## Three prompt dialects

The art direction stays the same across models. Only the phrasing changes.

### Natural-language models

GPT Image, Gemini image models and Imagen, Flux, Ideogram, Recraft, Seedream, Stable Diffusion 3 and later, and most models offered through aggregator tools.

- Write full sentences in one descriptive paragraph. This is the dialect the main skill file teaches.
- They follow spatial relations ("low in the bottom-right corner") and long descriptions reasonably well.
- Put text for the image in quotes. These models are the strongest at lettering, though short text is still safer.
- Weight syntax such as `(word:1.3)` does nothing here and can end up rendered as literal text.
- Many have no negative-prompt field. Phrase everything positively.

### Midjourney

- Accepts sentences, and also responds well to shorter, denser phrasing. Its house aesthetic is strong, so an art-directed prompt often needs that aesthetic turned down.
- Settings are written as parameters at the end of the prompt. The long-standing ones:
  - `--ar 2:3` aspect ratio
  - `--stylize` (or `--s`) how much of Midjourney's own taste is applied; lower values follow the prompt more literally
  - `--style raw` reduces the default beautification
  - `--chaos` (or `--c`) how different the images in one grid are from each other; useful when exploring
  - `--weird` (or `--w`) pushes toward unconventional results
  - `--no` things to exclude
  - `--seed` repeatability
  - `--sref` a style reference image or code, for consistent sets
- Parameter ranges and reference features change between versions. Check the current documentation before quoting numbers.

### Tag-based Stable Diffusion models

Stable Diffusion 1.5, SDXL and the many community fine-tunes, usually run through ComfyUI, Automatic1111 or similar.

- Comma-separated phrases work better than long sentences. Order still matters: medium and subject first.
- The text encoder reads prompts in chunks of about 75 tokens, and attention falls off with length. Keep prompts compact.
- Weights are supported in most interfaces: `(linocut print:1.2)` strengthens a phrase, values under 1 weaken it. Stay within roughly 0.8 to 1.4.
- There is a separate negative prompt. This is the right place for exclusions.
- An exception to "leave out the boosters": some fine-tunes were trained with quality or score tags in their captions, and for those models the tags are functional. Follow the model card for that specific checkpoint.
- Style often comes from a LoRA or the checkpoint itself. Ask which the user has loaded, since it overrides much of what the prompt says about style.

Converting the lighthouse example from the main file into this dialect:

```
two-colour linocut print, deep indigo and warm yellow ink on cream paper, small lighthouse low in bottom-right corner, tall composition, vast night sea and sky, long horizontal gouge marks, thin yellow beam across water, uneven ink, slight misregistration, visible paper fibre
Negative: photograph, 3d render, gradient, glossy, extra colours, text
```

## Settings that matter

Read the tool's schema, then set these on purpose. Names vary.

| Setting | What it does | Guidance |
|---|---|---|
| Aspect ratio or size | Shape of the frame | Decide from the composition; see below |
| Number of images | How many per call | One for a direct request; several when exploring, each varied by a decision |
| Seed | Fixes the randomness | Reuse to change one thing while keeping the rest; record it when a result lands |
| Prompt enhancement | The service rewrites the prompt before generating (also called magic prompt, prompt upsampling, enhance, auto-rewrite) | Turn off for an art-directed prompt where possible; it pulls toward the generic |
| Guidance or CFG | How strictly the image follows the prompt | Very high values look harsh and over-saturated; lower values look more natural but drift from the prompt. Start at the model's default |
| Quality or resolution tier | Detail, cost and time | Explore on the cheaper tier, then render the chosen one at high quality |
| Style or character reference | An image that fixes the look or a subject | The most reliable route to consistency across a set |
| Reference strength | How much a reference dominates | High for consistency, lower when the reference is only a mood |
| Negative prompt | Things to keep out | Use it when it exists, instead of negations in the main prompt |

## Aspect ratio

| Format | Suits |
|---|---|
| 2:3, 3:4, 4:5 portrait | Figures, posters, book covers, prints, anything tall or solitary |
| 1:1 square | Album covers, icons, symmetrical or centred compositions, tiles |
| 3:2, 4:3 landscape | Scenes, landscapes, editorial illustration |
| 16:9 | Headers, slides, desktop wallpaper, cinematic stills |
| 9:16 | Phone wallpaper, stories, vertical video frames |
| 21:9 and wider | Panoramas, banners; needs a composition that reads left to right |

If the final use needs a particular size, generate at the nearest supported ratio and crop, rather than describing the size in the prompt.

## Editing and references

- **Instruction edits** (most natural-language models): say what changes and what stays. "Replace the sky with flat overcast grey. Keep the figure, the composition, the palette and the paper texture exactly as they are."
- **Inpainting**: mask the area, and describe what belongs in it in the same medium words as the original prompt so it matches.
- **Image references**: say what the reference is for, such as style only, composition only, or this exact character, because the model cannot tell otherwise.
- **Upscaling**: last step, once the image is chosen. Creative upscalers invent detail and can change the medium's texture; keep their strength low for prints, drawings and anything flat.
