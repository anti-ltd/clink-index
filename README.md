<p align="center">
  <img src="README-assets/clink-icon.png" width="96" alt="Clink app icon">
</p>

<h1 align="center">Clink index</h1>

<p align="center">Everything you can add to Clink, in one place.</p>

Clink is an open iOS keyboard. The app ships with a curated set of themes, layouts, languages, and tools, but most of the content people actually use lives in separate repositories. This index collects all of them so you can browse, fork, or contribute from a single starting point.

## Documentation and feedback

Read the [Clink usage guides](https://anti.ltd/docs/clink) on ANTI. Public documentation is maintained there; the GitHub wiki sync is retired.

Report bugs and request features through Clink's in-app **Feedback** page. Reports stay private until a moderator publishes them. Follow published feedback and release updates on the [ANTI feedback board](https://www.anti.ltd/feedback?appId=clink&platform=ios).


## Automation notice

This index is maintained largely by automation. Treat it as a generated hub, not a hand-edited monorepo.

## Official Clink repositories

[Language packs](https://github.com/anti-ltd/clink-language-packs) · [Layouts](https://github.com/anti-ltd/clink-layouts) · [Profiles](https://github.com/anti-ltd/clink-profiles) · [Themes](https://github.com/anti-ltd/clink-themes) · [Affiliate themes](https://github.com/anti-ltd/clink-themes-affiliate) · [NuPhy Inspired themes](https://github.com/anti-ltd/clink-themes-nuphy) · [Beams themes](https://github.com/anti-ltd/clink-themes-beams) · [Panels](https://github.com/anti-ltd/clink-panels) · [Actions](https://github.com/anti-ltd/clink-actions) · [Plugins](https://github.com/anti-ltd/clink-plugins) · [Fonts](https://github.com/anti-ltd/clink-fonts) · [Sounds](https://github.com/anti-ltd/clink-sounds)

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

### Affiliate themes

Approved partner themes, included by default in Clink under **Affiliate**, immediately after **Official**. Downloads are free and read-only. The repository starts with an empty catalog while awaiting the first affiliate.

Read more in [clink-themes-affiliate](https://github.com/anti-ltd/clink-themes-affiliate).

### NuPhy Inspired themes

17 themes inspired by NuPhy keyboards, available in their own built-in catalog. The info button compares the physical keyboard with its Clink theme and links to [NuPhy](https://nuphy.com/). Comparison images are hosted in repository releases and load on demand.

Read more in [clink-themes-nuphy](https://github.com/anti-ltd/clink-themes-nuphy).

### Beams themes

22 free keyboard themes, each with paired light and dark appearances. Shallow 3D Retro keycaps with the Soft finish, fine Grain surfaces, and coordinated colourways are available under **Beams**, a default linked, non-removable theme repository on iOS and Android. Themes download from the repository's GitHub release and remain available offline after installation.

The repository contains editable palettes, paired `.clinktheme` files, native preview images, and manifest generation checks. GitHub Actions publishes the downloads after validation; the first release must exist before Clink can install themes.

Read more in [clink-themes-beams](https://github.com/anti-ltd/clink-themes-beams).

### Panels

Custom keyboard panels that replace the keyboard with a focused tool. The official repository includes Kaomoji (expressive text faces), Snippets (frequently used text), and Fonts (decorative Unicode styles).

Panels contain constrained logic. Clink asks for explicit permission before downloading panel code from any repository. The files are small and readable, so they are a good place to start when making your own.

Read more in [clink-panels](https://github.com/anti-ltd/clink-panels).

### Actions

Text transformations that run directly from the keyboard: changing case, reversing a word, formatting a title, inserting a small reply. Each action is a `.clinkext` file with a constrained `transform(text)` function.

Actions contain executable-style logic, so Clink asks for explicit permission before downloading them. The official actions are small and readable examples you can copy and modify.

Read more in [clink-actions](https://github.com/anti-ltd/clink-actions).

### Plugins

Scripts that run alongside the keyboard rather than inside a panel. A plugin hooks into typing (`on_open`, `on_key`, `on_word`) and can drive the keyboard's own controls, such as putting a live typing speed on the space bar. It draws its settings with the panel builders and can place them on a native settings screen. The official repository includes WPM Spacebar, Language Badge, Language Flag and Language Emoji. The language plugins show text, bundled MIT-licensed flag artwork or a flag emoji in any space bar corner while leaving the caption free.

Plugins need a Clink Pro membership to run, and like actions and panels they download only after an explicit trust decision for the repository.

Read more in [clink-plugins](https://github.com/anti-ltd/clink-plugins).

### Fonts

Redistributable font packs that Clink can install and use in custom themes. Font binaries stay separate from themes, so a theme stores only the verified PostScript name of the selected face.

The repository accepts fonts whose licences permit redistribution and embedding. The current example is Basic, a small OFL-licensed sans-serif font that exercises the full pipeline from discovery through Core Text registration.

Read more in [clink-fonts](https://github.com/anti-ltd/clink-fonts).

### Sounds

Key-sound packs for Clink: short, conditioned click samples in `.clinkpack` format. The official repository has 17 packs. Four are the originals (Clicky Blue, Tactile Brown, Typewriter, and Marble) and thirteen are rendered from editable synthesis recipes, covering wood, ceramic, metal, stone, paper, and Shot, a joke pack that fires a blast and racks the pump on every key. Each pack contains metadata and mono 44.1 kHz WAV samples. Packs cannot run code.

You can record or import sounds in Clink, export a pack, and publish it through this repository. The included tools handle conditioning, manifest generation, and validation.

Read more in [clink-sounds](https://github.com/anti-ltd/clink-sounds).

## How the repositories work together

A typical Clink setup uses several repositories at once: a language pack for prediction, a theme for the look, a layout for key positions, and maybe a sound pack for feedback. Each repository is independent; you can mix and match anything from any source.

Clink verifies every download: public HTTPS GitHub releases only, SHA-256 hash matching, size limits, and file-type checks. Data-only packs cannot run code. Packs that contain logic (actions, panels, plugins) require a separate, explicit trust decision before Clink downloads them.

## Adding your own repository

Each repository includes instructions for editing its content. For repositories that supply downloadable packs, the general publishing pattern is:

1. Fork the repository you want to contribute to.
2. Add your files following the repository's format.
3. Run the included validation tools.
4. Push to `main`. GitHub Actions builds the manifest and publishes the release.

For a repository with a published pack manifest, open **General → Repositories** in Clink and add `owner/repository`. Your content appears under its own source chip and stays separate from the official packs.

## Make content with an AI agent

Every official content repository includes a `PROMPT.md` file. Give its contents to an AI coding agent together with the kind of pack you want to make—for example, “Create a warm dark theme inspired by amber glass” or “Make a Colemak layout.” The prompt gives the agent the repository’s actual file format, examples to inspect, safety rules, and the commands to run before it finishes.

Start by forking the relevant repository, then open it in your agent and say:

```text
Read PROMPT.md and create [describe the theme, layout, pack, or tool I want].
```

Review the resulting file and test it in Clink before pushing. The prompts keep agents scoped to content and generated manifests; they do not replace your review of the content, licences, or publishing changes.

## Licensing

Each repository carries its own licence. Content you publish should be yours to share. Attribution and licence information belong in the individual repository's README or pack description.

## Platform availability

Every content repository has a `platforms.json` policy. `default` applies to all its packs; `overrides` selects individual IDs. The accepted targets are `ios`, `android`, and `both`. All current content defaults to `both`; only `clink-themes-affiliate` overrides Quiche Industries day and night to `ios`. Release builders write this as each manifest entry’s `platform` field. An older entry without the field remains available on both platforms.

Keep the app’s bundled restrictions and standalone builders synchronized with `python3 Tools/sync_repository_platforms.py` in the Clink app checkout, then run the same command with `--check`. The bundled restriction also covers older cached Quiche manifests on Android. Regenerate the affiliate debug previews with `python3 Tools/EmbedAffiliateThemes.py` after changing their policy.
