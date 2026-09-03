<p align="center">
  <img src="https://raw.githubusercontent.com/anti-ltd/clink-language-packs/main/icon-1024.png" width="96" alt="Clink app icon">
</p>

<h1 align="center">Clink index</h1>

<p align="center">Everything you can add to Clink, in one place.</p>

Clink is an open iOS keyboard. The app ships with a curated set of themes, layouts, languages, and tools, but most of the content people actually use lives in separate repositories. This index collects all of them so you can browse, fork, or contribute from a single starting point.

## Official Clink repositories

[Language packs](https://github.com/anti-ltd/clink-language-packs) · [Layouts](https://github.com/anti-ltd/clink-layouts) · [Profiles](https://github.com/anti-ltd/clink-profiles) · [Themes](https://github.com/anti-ltd/clink-themes) · [Panels](https://github.com/anti-ltd/clink-panels) · [Actions](https://github.com/anti-ltd/clink-actions) · [Fonts](https://github.com/anti-ltd/clink-fonts) · [Sounds](https://github.com/anti-ltd/clink-sounds)

## What is in each repository

### Language packs

Dictionaries, next-word models, neural ranking, and input-method tables for over 30 languages. Everything stays on the device after download. A pack needs only a word list to start; prediction models and neural ranking are optional extras.

The repository includes tools for building compact lexicons, training next-word models from sentence corpora, compiling IME conversion tables, and exporting Core ML neural models. Publishing is automatic through GitHub Actions.

Read more in [clink-language-packs](https://github.com/anti-ltd/clink-language-packs).

### Layouts

Keyboard layouts beyond what Clink ships in the app. Each layout is a small JSON file that maps letters to key positions. The repository includes Clink Flow, a two-thumb optimized arrangement, as a readable starting point for making your own.

You can design a layout visually in Clink and export a `.clinklayout` file, or write one by hand. Publishing is automatic.

Read more in [clink-layouts](https://github.com/anti-ltd/clink-layouts).

### Profiles

Ready-made keyboard setups you can browse, install, and copy. A profile is a small JSON file that changes only the settings you want to override from Clink Default. Smoothest, Fastest, and Big Keys are the current examples.

You can make a profile by editing a copy of an existing one. Every profile is data only and cannot run code.

Read more in [clink-profiles](https://github.com/anti-ltd/clink-profiles).

### Themes

Over 20 open keyboard themes across dark, light, and Liquid Glass styles. Themes are JSON files that set colours, materials, gradients, fonts, and type treatment. They cannot contain photos or executable code.

The repository includes a manifest generator and validator. Publish by adding a `.clinktheme` file and pushing to main.

Read more in [clink-themes](https://github.com/anti-ltd/clink-themes).

### Panels

Custom keyboard panels that replace the keyboard with a focused tool. The official repository includes Kaomoji (expressive text faces), Snippets (frequently used text), and Fonts (decorative Unicode styles).

Panels contain constrained logic. Clink asks for explicit permission before downloading panel code from any repository. The files are small and readable, so they are a good place to start when making your own.

Read more in [clink-panels](https://github.com/anti-ltd/clink-panels).

### Actions

Text transformations that run directly from the keyboard: changing case, reversing a word, formatting a title, inserting a small reply. Each action is a `.clinkext` file with a constrained `transform(text)` function.

Actions contain executable-style logic, so Clink asks for explicit permission before downloading them. The official actions are small and readable examples you can copy and modify.

Read more in [clink-actions](https://github.com/anti-ltd/clink-actions).

### Fonts

Redistributable font packs that Clink can install and use in custom themes. Font binaries stay separate from themes, so a theme stores only the verified PostScript name of the selected face.

The repository accepts fonts whose licences permit redistribution and embedding. The current example is Basic, a small OFL-licensed sans-serif font that exercises the full pipeline from discovery through Core Text registration.

Read more in [clink-fonts](https://github.com/anti-ltd/clink-fonts).

### Sounds

Key-sound packs for Clink: short, conditioned click samples in `.clinkpack` format. The official repository includes Clicky Blue, Tactile Brown, Typewriter, and Marble. Each pack contains metadata and mono 44.1 kHz WAV samples. Packs cannot run code.

You can record or import sounds in Clink, export a pack, and publish it through this repository. The included tools handle conditioning, manifest generation, and validation.

Read more in [clink-sounds](https://github.com/anti-ltd/clink-sounds).

## How the repositories work together

A typical Clink setup uses several repositories at once: a language pack for prediction, a theme for the look, a layout for key positions, and maybe a sound pack for feedback. Each repository is independent; you can mix and match anything from any source.

Clink verifies every download: public HTTPS GitHub releases only, SHA-256 hash matching, size limits, and file-type checks. Data-only packs cannot run code. Packs that contain logic (actions, panels) require a separate, explicit trust decision before Clink downloads them.

## Adding your own repository

Every repository above includes instructions for forking it and publishing your own content. The general pattern is:

1. Fork the repository you want to contribute to.
2. Add your files following the repository's format.
3. Run the included validation tools.
4. Push to `main`. GitHub Actions builds the manifest and publishes the release.

In Clink, open **General → Repositories** and add `owner/repository`. Your content appears under its own source chip and stays separate from the official packs.

## Make content with an AI agent

Every official content repository includes a `PROMPT.md` file. Give its contents to an AI coding agent together with the kind of pack you want to make—for example, “Create a warm dark theme inspired by amber glass” or “Make a Colemak layout.” The prompt gives the agent the repository’s actual file format, examples to inspect, safety rules, and the commands to run before it finishes.

Start by forking the relevant repository, then open it in your agent and say:

```text
Read PROMPT.md and create [describe the theme, layout, pack, or tool I want].
```

Review the resulting file and test it in Clink before pushing. The prompts keep agents scoped to content and generated manifests; they do not replace your review of the content, licences, or publishing changes.

## Licensing

Each repository carries its own licence. Content you publish should be yours to share. Attribution and licence information belong in the individual repository's README or pack description.
