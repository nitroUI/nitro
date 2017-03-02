# Introduction
Nitro UI is an **experimental** Abstract Part Assembly sytem for generating components, independent of their underlying API. The general idea is that by abstracting away implementation details and idiosyncracies we can create components that are slightly more agnostic with the aim of being slightly more future-proof. 

Our first attempt down this path is in drafting specification for components for Nitro called **Parts** and building a handful of simple parts against this pattern to try and validate our ambitious premise. 

## Nitro Repo Naming Convention

Nitro Modules follow the following convention

| Repo Type          | Repo Namespace | Example |
| ------------- |:------------------- | :-----| 
| Module     | *nitro-[module-name]*  | `nitro-util` | 
| Tag        | *tag-[tag-name][?-sub-name]* | `tag-button`  |   
| Theme      | *theme-[themeid]* | `theme-zero`    |  
| Skin       | *theme-[themeid]-[skinid]*  | `theme-zero-fresh`    |  
| Scripts    | *bin-[script-name][?-sub]* |`bin-start-robot`  | 
| Doc        | *doc-[doc-name][?-sub]* |`doc-requirements`  |   
| Misc       | *misc-[misc-name]*     | `misc-scripts`	|  

- **Module** - Top-level modules include the nitro prefix, these are either utilities, plugins, or other major features.
- **Tag** - Source code HTML and custom-HTML tags used to generate distributable tag packages and follow the Nitro Tag Definition Specification.
- **Theme** - Themes are a collection of partial rendering rules (mostrly structural) for creating basic tag structures; Nitro uses the Zero Theme based on Normalize.css as the default theme recipe.
- **Skin** - Skins are the higher-fidelity styles like color, font-families, and iconography that are used to complete the UX specifications of a particular styleguide (the deltas).
- **Scripts** - Add-on executable (bin) shell files that augement Nitro in someway but aren't critical to the overall system. They can be Python, Bash, JavaScript, or Ruby etc. and are automatically hoisted to Nitro's `./bin` directory when included. 
- **Doc** - Collection of project-wide documentation or notes. Individual repos have their own READMEs, etc.
- **Misc** - Anything else that doesn't fall within the scope of the above namespaces should be namespaced with misc- non-namespaced repos are discouraged.

## Simple Parts Specification

The Simple Parts Specification outlines the *draft* guidance for creating, testing, and publishing new Parts. Because this pattern will be foundational to the entire system, we'll need a strategy to safely synchronize updates (probably via an update/migrate script and other semver-friendly strategies)

This current draft specification can be found in the [Nitro Parts Spec](https://github.com/nitroUI/nitro-parts-spec/blob/master/README.md) repo.

## Todo
- [ ] Component Pattern
- [ ] Component List
- [ ] Component Detail
- [ ] Component Build
