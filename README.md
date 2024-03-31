# Graphite CI

The Graphite CI buildkite plugin allows you to define _when_ to run CI.

Common optimizations include:

- Only running CI on the bottom N PRs of a [stack](https://stacking.dev)
- Only running CI once downstack CI has passed

## Usage

1. First, get your CI token from https://app.graphite.dev/ci

1. Then, add the CI step to your pipeline file:

```yml
steps:
  - plugins:
      - withgraphite/graphite-ci#main:
          graphite_token: 'XXX'
```

To instead use a
[specific version](https://github.com/withgraphite/graphite-ci-buildkite-plugin/tags) of
this action, replace `@main` with `@v1.0` (or whatever the current latest
version is).
