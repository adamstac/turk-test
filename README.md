# Turk Test Repository

Test repository for [Turk](https://github.com/adamstac/turk) — a self-hosted GitHub Actions runner controller.

## Workflows

| Workflow | Label | Description |
|----------|-------|-------------|
| [Test Ephemeral](.github/workflows/test-ephemeral.yml) | `turk-ephemeral-ubuntu-22.04` | Fresh container, destroyed after job |
| [Test Persistent](.github/workflows/test-persistent.yml) | `turk-persistent-ruby-builder-ubuntu-22.04` | Cloned from cached template |

## Usage

1. Install the Turk GitHub App on this repository
2. Run the Turk controller with webhook URL configured
3. Trigger workflows manually via Actions tab

## Label Format

```
turk-<mode>-[name-]<platform>
```

- **Ephemeral**: `turk-ephemeral-<platform>` — Fresh every time
- **Persistent**: `turk-persistent-<name>-<platform>` — Cloned from cached template
