# mouseless_user

Mouseless's keymap and settings (`config.yaml`), version-controlled. Plan: `../mouseless-config-plan.md`.

## Install (method 1: symlink)

Quit Mouseless, back up the live file, then:

```bash
MLS="$HOME/Library/Application Support/Mouseless"
mv "$MLS/configs/config.yaml" "$MLS/configs/config.yaml.orig"
ln -s /Users/Shared/_accessibility/mouseless_user/config.yaml "$MLS/configs/config.yaml"
```

Never commit `licenses/` or `logs/` (see `.gitignore`).

## Bindings the Talon/Joy-Con setup depends on

- `toggle free mode`: Option tap only (F13 not bound)
- `exit free mode`: unbound (Escape not bound)
- free-mode wheel up/down/left/right: F17-F20
- `free_mode_auto_off_s: 0`

## Test results

To be filled in: T1 (symlink survives save), T3 (live reload?), T4 (diff clean?), T6 (last save wins across accounts).

## Fallback (method 2)

If Mouseless replaces the symlink on save, restore the real file and use a copy script like `joymapper_user/sync-settings.sh`.
