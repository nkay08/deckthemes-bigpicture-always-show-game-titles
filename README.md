# Always Show Game Labels

A CSS Loader theme that always shows the game title under the capsule in the
Steam Deck / Big Picture Mode library and home screens.

## Install

Copy this folder to `~/homebrew/themes/`:

```sh
cp -r "Always-Show-Game-Labels" ~/homebrew/themes/
```

Then open CSS Loader's Quick Access menu, scroll to the bottom and press
**Refresh**, and enable the theme.

## How it works

The Steam UI hides game titles with an inline `display: none` on an element
that has *no class*, only an id. This theme re-selects that element with the
adjacent-sibling selector `.LibraryItemBox.Panel + div[id]` and forces it
visible with `!important`.

The readable class names (`LibraryItemBox`, `InRecentGames`, `GamepadLibrary`)
are automatically translated to the current hashed class names by CSS Loader's
`css_translations.json`, so the theme keeps working across Steam client updates.
