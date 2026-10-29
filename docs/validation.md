# Release validation

Release candidate: **0.1.0**, prepared 2026-10-19.

## Passed locally

- Parsed the palette and all shipped TOML files.
- Checked the required palette keys against the published Omarchy theme-registry schema.
- Ran Omarchy 4.0.5-1's actual `omarchy theme set hackers-1995` in a network-disabled Bubblewrap environment, with the real home directory hidden behind a clean temporary home.
- Included `.git` in that isolated theme directory so Omarchy used its installed-community-theme staging rules.
- Disabled runtime hooks and wallpaper changes for the isolated installation using Omarchy's headless mode.
- Verified generated Foot foreground `00ff41`, background `010603`, and black-on-green selection.
- Verified the generated Neovim configuration uses Aether and the green palette. No personal Neovim Lua override was needed for that installation.
- Checked generated text configurations for unresolved template placeholders.
- Checked the public preview and background image dimensions and sizes.
- Checked for symlinks, unsupported executable theme files, absolute home-directory paths, and common credential patterns in release text files.
- Visually inspected the 1920 × 1080 four-app preview with real source code, directory listings, live monitoring, and Strata.
- Captured the preview with the existing Foot and compositor transparency settings, without changing the user configuration.
- Verified the replacement forest photograph has a CC BY 4.0 license record; added attribution and separate image licensing in CREDITS.md.
- Included image attribution in README.md as well, because marketplace installs do not include CREDITS.md.

The preview uses the author's optional editor and Strata profiles and window transparency, as described in the README. It is not a screenshot of an otherwise uncustomized Omarchy installation.

## Publication and registry submission

The intended public repository is `Waffles46/omarchy-hackers-1995-theme`. The replacement photo is credited under CC BY 4.0; the existing personal forest photograph remains excluded. Submit the public repository URL to the [official theme registry](https://github.com/omacom/omarchy-theme-registry#submit-your-theme) after publication.

Add the `omarchy-theme` GitHub topic when publishing. The original wallpaper is larger than the registry's 8 MiB per-background warning threshold; it is below the hard image limit and is intentionally retained unchanged.

The registry's remote validator has not run: it needs the published GitHub repository. Maintainer acceptance and catalog publication are not implied by the local checks.

## References

- [Omarchy theme distribution guide](https://omarchy.org/manual/making-your-own-theme/)
- [Theme registry](https://github.com/omacom/omarchy-theme-registry)
- [Registry file and palette rules](https://github.com/omacom/omarchy-theme-registry/blob/master/packages/schema/src/constants.ts)
