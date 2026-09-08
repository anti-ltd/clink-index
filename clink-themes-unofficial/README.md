# Clink themes — unofficial

An unofficial collection of optional keyboard themes for Clink, using the same
JSON theme format, manifest, and release layout as `clink-themes`.

## Included themes

- **[NuPhy Light](Themes/nuphy-light.clinktheme)** — warm white letter caps,
  grey modifiers, and teal, red, and yellow accent caps.
- **[NuPhy Dark](Themes/nuphy-dark.clinktheme)** — charcoal letter caps,
  dark modifiers, and teal, red, and yellow accent caps.

Both are copied from Clink's debug presets in
`Sources/ClinkKit/Theme+Nuphy.swift`. They preserve the Mechanical 3D material,
30% inner radius, visible edges, medium-weight legends, teal plane toggle,
red Return, yellow spacebar, and active/pressed key colours. Omitted theme
properties use the same defaults as the debug presets.

These are NuPhy-inspired themes, with no affiliation with or endorsement by
NuPhy. This collection is separate from Clink's official theme catalog.

## Use a theme

Download a `.clinktheme` file from [`Themes/`](Themes) and import it into Clink.

After this repository has been published on GitHub and its first `latest`
release is available, open **General → Repositories** in Clink and add its
`owner/clink-themes-unofficial` address. Then open **Customize → Look**, choose
the repository's chip, and download a theme. Installed themes work offline.

## Build and publish

The repository contains:

```text
Themes/                       Importable .clinktheme JSON files
manifest.json                 Generated previews, asset URLs, hashes, and sizes
tools/build-manifest.py        Manifest generator
.github/workflows/release.yml  Publishes a latest release on pushes to main
PROMPT.md                     Theme creation guidance
VERIFY.md                     Review checklist
LICENSE.md                    Clink Community Assets License
```

Regenerate the manifest with:

```sh
python3 tools/build-manifest.py
```

Local builds default to `anti-ltd/clink-themes-unofficial`. If publishing under
a different owner, use:

```sh
GITHUB_REPOSITORY=your-name/clink-themes-unofficial python3 tools/build-manifest.py
```

GitHub Actions uses the actual repository name automatically. As in
`clink-themes`, a push to `main` that changes a theme, the builder, or the
workflow regenerates the manifest and publishes the theme files and manifest
to the `latest` release.

## Contribute

Export a theme from Clink, give it a stable lowercase ID and matching filename,
and place it in `Themes/`. Repository themes must contain only JSON theme data;
do not include image references or bundled artwork. Run the manifest builder
and follow [`VERIFY.md`](VERIFY.md) before publishing. [`PROMPT.md`](PROMPT.md)
provides a brief for creating another theme with an AI agent.

The copied themes and repository tooling are provided under
[`LICENSE.md`](LICENSE.md). The original debug presets remain in the app source.
