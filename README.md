# Kototoki Dotfiles

Development environment configuration for Kototoki LLC (合同会社言季).

## Managed by

- [chezmoi](https://www.chezmoi.io/) - cross-platform dotfile manager
- [1Password CLI](https://developer.1password.com/docs/cli) - secret reference

## Bootstrap on a new machine

```bash
# 1. Install chezmoi
sh -c "$(curl -fsLS get.chezmoi.io)" -- -b ~/.local/bin

# 2. Initialize from this repo
~/.local/bin/chezmoi init kototoki-jp/dotfiles

# 3. Apply
~/.local/bin/chezmoi apply
```

## Structure

| Path | Purpose |
|---|---|
| `dot_zshrc.tmpl` | Zsh main config |
| `dot_gitconfig.tmpl` | Git config (email pulled from 1Password) |
| `dot_config/starship.toml` | Prompt config |
| `dot_config/mise/config.toml` | Runtime versions |
| `.chezmoidata/machines.yaml` | Machine-specific data |

## Secrets

**No secret values are stored in this repository.**
All sensitive references use `{{ onepasswordRead "op://..." }}` and are
resolved at apply-time from the 1Password vault.

## License

MIT

