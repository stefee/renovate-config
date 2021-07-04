# renovate-config

This is a collection of [GitHub-hosted presets](https://docs.renovatebot.com/config-presets/#github-hosted-presets) for Renovate dependency bot.

## Usage

In your `renovate.json`:

```
{
  "extends": [
    "github>stefee/renovate-config"
  ]
}
```

If you would like to [auto-merge](https://docs.renovatebot.com/configuration-options/#automerge) minor upgrades, here is a recommended configuration for doing that:

```
{
  "extends": [
    "github>stefee/renovate-config",
    "github>stefee/renovate-config:automergeMinor",
    "github>stefee/renovate-config:dontAutomergeNode",
    "github>stefee/renovate-config:dontAutomergeTestFrameworks"
  ]
}
```

## Semantic Presets

A description for each preset can be found in the JSON file for the preset stored in this repo.

### Auto-Merge presets

* [`github>stefee/renovate-config:automergeMinor`](./automergeMinor.json)
* [`github>stefee/renovate-config:dontAutomergeNode`](./dontAutomergeNode.json)
* [`github>stefee/renovate-config:dontAutomergeTestFrameworks`](./dontAutomergeTestFrameworks.json)
