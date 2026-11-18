# Second Idea

A Claude plugin that teaches Claude to art-direct image generation, so the images it makes or prompts for come out distinctive and creative instead of generic.

It works with whichever image tool is connected to Claude. With no image tool connected, Claude writes a finished prompt you can paste into Midjourney, Flux, GPT Image, Gemini, Stable Diffusion, Ideogram or any other model.

The name is the plugin's first rule: the first idea is everybody's first idea, so make the second one.

## Why

Image models fill every decision you leave open with the most common answer they have seen: subject in the centre, golden light, orange-and-teal colour, a smooth digital finish. That average is what "AI-looking" means.

This plugin has Claude make those decisions on purpose. The same request, with and without it:

> **Request:** a picture of a lighthouse
>
> **Typical prompt:** A beautiful lighthouse on a cliff at sunset, dramatic sky, highly detailed, 8k
>
> **Art-directed prompt** (idea: the last thing still awake): Two-colour linocut print in deep indigo and a single warm yellow on cream paper with visible fibre. A small lighthouse stands low in the bottom-right corner of a tall frame; the upper four-fifths is night sea and sky, carved in long horizontal gouge marks. The only yellow anywhere is the lamp and the thin wedge of beam it throws left across the water. Uneven ink coverage, slight misregistration between the two colours, hand-cut edges. Quiet and watchful. Portrait, 2:3.

## What the skill teaches

- **Reading the request**: when to serve your vision, when to make one bold interpretation, when to offer three different directions
- **Finding an idea**: twelve concept engines (metaphor, collision, scale, material swap, viewpoint, time, absence, genre transplant, constraint, inversion, tone against subject, specificity)
- **Five decisions** behind every image: medium, composition, light, palette, mood
- **Prompt writing**: concrete physical description, no booster words, no negations, style anchored in traditions instead of living artists' names
- **Generating**: choosing settings on purpose, switching off prompt "enhancers", varying decisions instead of seeds, being careful with your credits
- **Critique**: looking at the result, diagnosing what missed, changing one thing at a time
- **Sets**: keeping a series of images consistent

## Install

### Claude Code

Inside a Claude Code session:

```
/plugin marketplace add aroosha/second-idea
/plugin install second-idea@aroosha-plugins
```

### Claude desktop app or claude.ai

1. Open **Customize**, then **Plugins**.
2. Choose **Add**, then **Add marketplace**, and enter `aroosha/second-idea`.
3. Install **Second Idea** from that marketplace.

### As a standalone skill

Copy the `skills/create-image` folder to `~/.claude/skills/create-image`. It is then available in Claude Code as `/create-image`, without the plugin.

## Using it

Once installed, ask for an image the way you normally would. The skill loads by itself.

- "Make me an image of a fox"
- "I need cover art for my ambient album, it's called Low Tide"
- "Give me three directions for a poster for our jazz night"
- "Write a Midjourney prompt for a calm abstract piece in blues"
- "This came out too generic, how do I make it less AI-looking?"

To call it directly, type `/second-idea:create-image` followed by what you want.

## What it does and doesn't do

The plugin is instructions and reference text only. It contains no code, runs nothing on your machine, and sends no data anywhere. When Claude generates an image, it does so through an image tool you have already connected, under that tool's own terms and credits.

## What's inside

```
second-idea/
├── .claude-plugin/
│   ├── plugin.json
│   └── marketplace.json
├── skills/
│   └── create-image/
│       ├── SKILL.md                    the process Claude follows
│       └── references/
│           ├── concept-engines.md      turning a subject into an idea
│           ├── visual-vocabulary.md    mediums, composition, light, colour, traditions, moods
│           ├── model-notes.md          prompt dialects and settings per model family
│           ├── critique.md             symptom-to-fix table for results that miss
│           └── examples.md             seven requests worked through to a finished prompt
├── LICENSE
└── README.md
```

Claude reads `SKILL.md` whenever the skill triggers and opens the reference files only when it needs them.

## Making it yours

Fork the repository and edit two files to give the plugin your own taste:

- `references/visual-vocabulary.md`: add the mediums, palettes and traditions you love, and remove the ones you never want.
- `references/examples.md`: replace the examples with prompts of your own that produced images you were proud of. Claude calibrates on these.

To try a local copy before installing it, start Claude Code with:

```bash
claude --plugin-dir ./second-idea
```

## License

MIT. See [LICENSE](LICENSE).
