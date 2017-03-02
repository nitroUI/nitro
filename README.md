# Introduction
Nitro UI is an **experimental** Abstract Part Assembly sytem for generating components, independent of their underlying API. The general idea is that by abstracting away implementation details and idiosyncracies we can create components that are slightly more agnostic with the aim of being slightly more future-proof. 

Our first attempt down this path is in drafting specification for components for Nitro called **Parts** and building a handful of simple parts against this pattern to try and validate our ambitious premise. 

## Nitro Repo Naming Convention

Nitro Modules follow the following convention

| Repo Type          | Repo Namespace | Example | Description |
| ------------- |:------------- | :-----| :-----|
| Module     | `nitro-[module-name]` | `nitro-util` | Top-level modules are usually utilities, plugins, or documentation and include the nitro-prefix, other repos have prefix specific to their use-case |
| Tag       | `tag-[tag-name][?-sub-name]` | `tag-button`  |   All components/modules/tags that follow the Nitro Tag Definition Specification.  |
| Theme    | `theme-[theme-name]` | `theme-zero`    |  Theme Engines for Nitro |
| Skin       | `theme-[theme-name]-[skin-name]`  | `theme-zero-fresh`    |  Skin packages for Nitro Themes  |
| Scripts    | `bin-[script-name][?-sub]` |`bin-start-robot`  |   Add-on executable shell scripts  |
| Doc        | `doc-[doc-name][?-sub]` |`doc-requirements`  |   Document collections  |
| Misc       | `misc-[misc-name]`     | `misc-scripts`	|  Any other resource should be namespaced with misc-.  |


## Simple Parts Specification

The Simple Parts Specification outlines the *draft* guidance for creating, testing, and publishing new Parts. Because this pattern will be foundational to the entire system, we'll need a strategy to safely synchronize updates (probably via an update/migrate script and other semver-friendly strategies)

This current draft specification can be found in the [Nitro Parts Spec](https://github.com/nitroUI/nitro-parts-spec/blob/master/README.md) repo.

## Todo
- [ ] Component Pattern
- [ ] Component List
- [ ] Component Detail
- [ ] Component Build
