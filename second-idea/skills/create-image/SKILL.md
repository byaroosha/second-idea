---
name: create-image
description: Art-direct image generation so results come out distinctive, artistic and creative instead of generic. Use whenever the user asks to create, generate, draw, paint, illustrate, design or imagine an image, artwork, illustration, poster, cover, wallpaper, concept art, character, pattern or "a picture of" something; whenever they want a prompt for Midjourney, Flux, GPT Image, Gemini, Imagen, Stable Diffusion, Ideogram or any other image model; and whenever they want results to look less generic or less "AI", want style ideas, or want variations on an image, even if they never say the word artistic.
---

# Art-directed image creation

An image model fills every decision you leave open with the most common answer it has seen: subject in the centre, eye level, soft golden light, orange-and-teal colour, a smooth digital finish. Unguided output looks generic because it is, quite literally, the average.

An image reads as artistic when the choices that matter were made on purpose, and at least one of them is a choice the model would not have made by itself. So work the way an art director does: find an idea, make the choices, describe them in concrete physical terms, then look hard at what comes back.

## Start by reading whose vision this is

How much to invent depends on how much the user has already decided.

- **They have a vision**: a specific scene, a named style, reference images. Serve it. Bring craft to whatever they left open (light, framing, material detail) and leave their concept alone. Replacing someone's idea with a cleverer one is not help.
- **They named a subject and left the rest open**: "a fox", "something for above my desk". That is an invitation. Make one bold interpretation and show it. A finished image is a better question than any question you could ask.
- **They want to explore**: "give me ideas", "surprise me", or work that matters to them, such as a cover or a poster. Offer three directions that differ in *idea*, not three flavours of one idea, in a line or two each. Make the one they choose, or all three when generating is cheap. When you can only hand over prompts, write a full prompt for each direction, since prompts cost nothing.

Ask before making only when the user has a hard requirement you cannot guess: the exact wording that must appear, brand rules you haven't seen. Anything you can choose sensibly, such as a print format, you should choose, and say what you chose in one line so they can redirect you.

## 1. Find the idea

Ask what the image is *about*, beyond what it is *of*. "A lighthouse" is a subject. "The last thing still awake" is an idea, and it already tells you most of the picture: night, one warm light, a frame that is mostly dark water.

When the subject is plain, push it through one of these moves and keep whichever gives you an image you can already see:

| Move | What it does | Example |
|---|---|---|
| Metaphor | Shows the feeling through a stand-in | Burnout as a matchbook with one match left |
| Collision | Puts the subject where it doesn't belong | A koi pond filling a parking space |
| Scale | Makes the small monumental or the vast tiny | A commuter crossing a keyboard the size of a plaza |
| Material swap | Builds the subject from the wrong stuff | A thunderstorm in embroidery thread |
| Viewpoint | Looks from where nobody stands | A dinner party seen from inside the fridge |
| Time | Shows before, after, or everything at once | The birthday table the next morning |
| Absence | Shows the subject by its trace | A dog, as the worn patch on the sofa |
| Genre transplant | Borrows the rules of an unrelated tradition | Rush hour as an illuminated manuscript |
| Constraint | Removes options until a style appears | Two inks only; nothing but circles |

One idea per image. Two ideas compete for the frame and both arrive weakened. The test: you can say the idea in one sentence, and someone looking at the image would get it without hearing the sentence.

`references/concept-engines.md` has the full set with worked examples. Read it when the first idea you had is the one anyone would have, or when you are offering directions.

## 2. Make five decisions

Each of these, left unstated, gets the average answer. Decide all five, and break a default on purpose in at least one.

- **Medium.** What is it physically made of? Linocut, gouache, wet-plate photograph, cut paper, glazed ceramic. Name the material and its flaws: misregistered ink, paper fibre, brush drag, film grain. The flaws are what make a medium convincing instead of a digital imitation of it.
- **Composition.** Where is the viewer standing, how much of the frame is empty, where does the eye land first? Off-centre subjects, hard crops, high or low viewpoints and generous empty space all step away from the default.
- **Light.** One source, with a direction and a quality: raking window light, a single bare bulb, overcast noon, sodium streetlamps. Light does most of the emotional work, so "dramatic lighting" wastes the opportunity.
- **Palette.** Few colours, named: "indigo, bone and one cadmium yellow", not "vibrant colours". Decide which colour dominates and which appears only once.
- **Mood.** Choose one word, then convert it into things you can see, because models render objects and light, not adjectives. "Lonely" becomes a small figure, a wide empty frame and a single lit window.

`references/visual-vocabulary.md` has vocabulary for all five, including a table that turns mood words into visible devices. Read it when you want options beyond the ones that come to mind first.

## 3. Write the prompt

Write for a natural-language model unless you know the target wants something else. `references/model-notes.md` covers Midjourney parameters, tag-based Stable Diffusion models and the settings that matter.

- **Lead with the medium and the idea.** Early words carry the most weight on most models, and the medium decides how everything after it is rendered.
- **Describe what is physically there.** Nouns, materials, positions, named colours. "Moody" gives the model almost nothing; "one desk lamp, everything outside its pool of light falling to black" produces the mood. The same goes for the user's own adjectives: when they ask for "moody" or "cinematic", deliver it through what is in the frame, and keep the word only if it still adds something.
- **Leave out the boosters.** "Beautiful, stunning, masterpiece, 8k, ultra-detailed" say nothing about this particular image and pull it toward the polished average you are trying to leave.
- **Say what is there, not what isn't.** Many models read "no people" and paint people. Write "an empty street". If the tool has a separate negative-prompt field, put exclusions there.
- **Keep it to one paragraph, around 50 to 120 words.** Beyond that, details start getting dropped. If it won't fit, the image is carrying more than one idea.
- **Anchor style in traditions, techniques and eras**: ukiyo-e woodblock, Bauhaus poster, cyanotype, Dutch still life. When the user wants the look of a living artist, describe the qualities instead of using the name: the line, the shapes, the palette, the materials. That is fairer to working artists, many tools strip or refuse names anyway, and a description gives finer control than a name does.
- **For words in the image**, give the exact text in quotes, keep it short, and describe where it sits and what the lettering looks like rather than naming a font.
- **Use settings for what settings do.** When you call an image tool yourself, put aspect ratio, image count, seed and reference images in its parameters and leave them out of the prose. When you hand a prompt to the user to paste elsewhere, end it with the format (or the target model's own parameter syntax), because the text is all they will carry across.

A plain request, "a picture of a lighthouse", written both ways:

> **Default:** A beautiful lighthouse on a cliff at sunset, dramatic sky, highly detailed, 8k

> **Art-directed** (idea: the last thing still awake): Two-colour linocut print in deep indigo and a single warm yellow on cream paper with visible fibre. A small lighthouse stands low in the bottom-right corner of a tall frame; the upper four-fifths is night sea and sky, carved in long horizontal gouge marks. The only yellow anywhere is the lamp and the thin wedge of beam it throws left across the water. Uneven ink coverage, slight misregistration between the two colours, hand-cut edges. Quiet and watchful. Portrait, 2:3.

The second is not better because it is longer. It is better because every sentence is a decision.

## 4. Make it

Look through the tools available in this session for one that generates images, and read its parameters before calling it; they differ a lot between providers.

- Set the aspect ratio from the composition and from where the image will be used, never by default.
- If the tool has a setting that rewrites or "enhances" prompts, turn it off for an art-directed prompt. It exists to add detail to thin prompts, and it will sand yours back toward the average.
- When you make several images, vary a decision (the medium, the viewpoint, the idea), not just the seed. Four near-identical images teach nobody anything.
- Generating usually spends the user's credits. One image for a direct request is covered by the request; before larger batches, upscales or premium tiers, say what you are about to run.

**If they asked for a prompt**, the prompt is the deliverable: give it in a code block, ready to paste, in the dialect of the model they named.

**If they asked for an image and there is no image tool**, say so in a line and deliver the finished prompt the same way, with the aspect ratio and the kind of model it suits. If the concept is flat, geometric, typographic or line-based, also offer to draw it directly as an SVG. Don't force photographic or painterly ideas into vector shapes.

## 5. Look, then improve

When the result comes back in a form you can view, look at it before you present it. A prompt is a guess about what the model will do, and the image is the only evidence.

- Does the idea read within two seconds?
- Is the medium convincing, or a smooth digital imitation of it?
- Where does the eye land first, and is that the right place?
- Which default crept back in: a centred subject, extra clutter, a glossy finish, a wider palette than you asked for?
- Is anything broken: hands, lettering, merged objects?

Change one thing per round, or you will not know what helped. When most of the image is right, prefer the tool's edit or reference feature over rolling again, and state what has to stay the same. After two or three rounds of your own, stop and show the best one with a note on what is still off. From there the user's taste is the judge, not yours.

`references/critique.md` maps common symptoms to fixes.

## 6. Show the work

Lead with the image (or the prompt). Follow with two or three lines: the idea, and the choices that carry it. Then offer two specific next moves that are real alternatives, such as "the same idea as a cyanotype" or "pull back until the figure is tiny". They asked for an image, so keep the reasoning short, and include the prompt itself when they are likely to reuse it or have asked for it.

Carry their reactions forward. If they loved the grainy one and passed over the clean one, that is a brief for everything else in the conversation.

## Series and sets

For several images that belong together, write the style once as a fixed paragraph (medium, palette, light, texture, framing rule) and reuse it word for word, changing only the sentence that describes the subject. Reuse the seed or a style reference too if the tool supports one. Consistency comes from repeating the same words, not from describing the same style again in new ones.

## Reference files

- `references/concept-engines.md`: ways to turn a plain subject into an idea, with worked examples. Read when the obvious idea is the only one you have, or when offering directions.
- `references/visual-vocabulary.md`: mediums, composition, light, colour, texture, art traditions, and a mood-to-visuals table. Read when choosing the look.
- `references/model-notes.md`: how prompt style and settings differ between model families. Read when the user names a model, or the tool exposes settings you are unsure about.
- `references/critique.md`: a symptom-to-fix table for results that miss. Read when a result is off and the cause isn't obvious.
- `references/examples.md`: complete worked examples, from request to finished prompt, across different styles. Read to calibrate, not to copy.
