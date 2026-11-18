# Critique and repair

Use this when a result misses and the cause isn't obvious. Find the symptom, change the one thing it points to, and generate again.

## Reading an image

Look in this order, because earlier problems make later ones irrelevant.

1. **Idea.** Cover the prompt. What would a stranger say this image is about? If the answer is only the subject ("it's a lighthouse"), the idea didn't land.
2. **First glance.** Where does the eye go in the first second? That spot should hold the idea.
3. **Medium.** Does it look made of the stated material, or like a smooth render wearing that material as a filter?
4. **Palette.** Count the colours. More than you asked for means the model drifted back to its default.
5. **Defaults.** Centred subject, eye-level view, glow, shallow depth of field, symmetrical "epic" framing: did you choose these, or did they arrive by themselves?
6. **Breakage.** Hands, faces, lettering, objects merging into each other, repeated elements that should be unique.

## Symptom to fix

| Symptom | Likely cause | Fix |
|---|---|---|
| Looks like generic AI art | Decisions left open; booster words | Name the medium and two of its flaws, cut the palette to three named colours, delete every quality adjective |
| Glossy, plastic, over-polished | Model default finish; prompt enhancer on | Add physical imperfection (grain, paper fibre, brush drag), specify matte surfaces, turn off prompt enhancement, lower guidance if the tool exposes it |
| The idea doesn't read | Too many elements, or the idea lives in the words and not in anything visible | Reduce to one visual statement, enlarge or isolate the element that carries the idea, remove secondary props |
| Too busy | List-like prompt; every noun got rendered | Cut nouns, state how much of the frame is empty and where |
| Subject is centred again | No placement given | State the position concretely: "low in the bottom-right corner", "cut off by the left edge" |
| Medium looks like a filter | Medium named but not described | Describe how the thing was made: carved, torn, stitched, printed in two passes. Move the medium to the first words |
| Palette wider than asked | Colours implied by objects (grass, sky, skin) | Name the colour of the objects themselves: "grey-blue grass", or choose a medium that enforces it (two-ink print, cyanotype) |
| An element is missing | Prompt too long; element mentioned late | Move it earlier, shorten everything else, or add it in an edit pass |
| An unwanted element keeps appearing | Negation in the prompt, or a strong association ("beach" brings people) | Remove the negation and describe the positive state ("deserted", "bare"), or use the negative-prompt field |
| Lettering is garbled | Too much text; model weak at type | Shorten to a few words in quotes, describe placement and lettering style, or generate without text and add type afterwards |
| Flat, lifeless light | No light source stated | Name one source, its direction and its quality |
| Mood is wrong | Mood given as an adjective | Convert it into visible things (see the mood table in `visual-vocabulary.md`) |
| Faces or hands are off | Small in frame, or complex pose | Simplify the pose, hide or crop the hands, make the figure larger or far smaller, or choose a medium that abstracts (cut paper, woodblock) |
| Too literal, no surprise | First idea used | Return to `concept-engines.md` and run the subject through two different engines |
| Too strange for the purpose | Engine overpowering the brief | Keep the medium and palette, swap the idea for a quieter one such as absence or viewpoint |
| Images in a set don't match | Style re-described in different words each time | Reuse one fixed style paragraph word for word, and the same seed or style reference |
| Everything is right except one area | Nothing wrong with the prompt | Use the tool's edit or inpaint feature on that area, stating what must stay identical |

## Iteration discipline

- **One change per round.** Two changes at once and you cannot tell which helped.
- **Edit when it's nearly right, roll again when it's wrong.** Edits preserve what works. A new roll throws it away.
- **For edits, state the keep-list.** "Change the sky to overcast grey. Keep the composition, the figure, the palette and the paper texture exactly as they are."
- **Know when to stop.** Two or three rounds on your own, then show the best with an honest note about what is still off. The user may like the thing you were about to fix.
- **Keep the prompt that worked.** When a result lands, give the user the exact prompt and settings so they can return to it.
