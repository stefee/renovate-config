# renovate-config

This is a collection of [GitHub-hosted presets](https://docs.renovatebot.com/config-presets/#github-hosted-presets) for Renovate dependency bot. 🤖

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

You can also use any individual **semantic presets** without using the base preset. Here's a configuration that groups things but doesn't auto-merge them:

```
{
  "extends": [
    "config:base",
    "github>stefee/renovate-config:groupMinorUpdates",
    "github>stefee/renovate-config:groupLinterUpdates",
    "github>stefee/renovate-config:groupNodeUpdates"
  ]
}
```

## Semantic Presets

A description for each preset can be found in the JSON file for the preset stored in this repo.

### PR Group presets

* [`github>stefee/renovate-config:groupMinorUpdates`](./groupMinorUpdates.json)
* [`github>stefee/renovate-config:groupLinterUpdates`](./groupLinterUpdates.json)
* [`github>stefee/renovate-config:groupNodeUpdates`](./groupNodeUpdates.json)

### Auto-Merge presets

* [`github>stefee/renovate-config:automergeMinor`](./automergeMinor.json)
* [`github>stefee/renovate-config:dontAutomergeNode`](./dontAutomergeNode.json)
* [`github>stefee/renovate-config:dontAutomergeTestFrameworks`](./dontAutomergeTestFrameworks.json)

### Package Pattern presets

These presets can be used to apply custom rules to a set of packages using [`packageRules`](https://docs.renovatebot.com/configuration-options/#packagerules).

* Node.js sources - [`github>stefee/renovate-config:node`](./node.json)
* Testing frameworks - [`github>stefee/renovate-config:testFrameworks`](./testFrameworks.json)
