# Introduction
Nitro UI is a collection of open-source evergreen webcomponents called **Abstract Tags**, based on Nitro's [Abstract Tags Specification](https://github.com/nitroUI/nitro-tag-spec). In adopting the ATS pattern for creating tags, Nitro attempts to blackbox implementation details of underlying "view-only" UI libraries like React, Vue, Polymer, and Mithril.

In exposing a consistant, but implementation-indepedent featureset, Nitro enables the creation of re-usable webcomponents that are slightly more evergreen, agnostic, and future-forward (EAF).

# Nitro's Goal

We are big fans of native web technology, webcomponents and the HTML5 custom-tag spec. As Nitro evolves with available technology and brainpower, we encourage you future contributors and end-users to help keep Nitro UI true to it's eternal goal of being "more EAF".

## Nitro Repo Naming Convention

Nitro Repos follow a convention to help keep the listing organized, and quickly identify repos by their uses cases. Non-namespaced repos are discouraged.

| Repo Type          | Repo Namespace | Example |
| ------------- |:------------------- | :-----| 
| Module     | *nitro-[module-name]*  | `nitro-util` | 
| Tag        | *tag-[tag-name][?-sub-name]* | `tag-button`  |   
| Theme      | *theme-[themeid]* | `theme-zero`    |  
| Skin       | *theme-[themeid]-[skinid]*  | `theme-zero-fresh`    |  
| Scripts    | *bin-[script-name][?-sub]* |`bin-start-robot`  | 
| Doc        | *doc-[doc-name][?-sub]* |`doc-requirements`  |   
| Misc       | *misc-[misc-name]*     | `misc-scripts`	|  

-----

- **Module** - Top-level modules include the nitro prefix, these are either utilities, plugins, or other major features.

- **Tag** - Source code HTML and custom-HTML tags used to generate distributable tag packages and follow the Nitro Tag Definition Specification.

- **Theme** - Themes are a collection of partial rendering rules (mostrly structural) for creating basic tag structures; Nitro uses the Zero Theme based on Normalize.css as the default theme recipe.

- **Skin** - Skins are the higher-fidelity styles like color, font-families, and iconography that are used to complete the UX specifications of a particular styleguide (the deltas). Since skins derive from a theme, they are namespaced with the theme they are associated with.

- **Scripts** - Add-on executable (bin) shell files that augement Nitro in someway but aren't critical to the overall system. They can be Python, Bash, JavaScript, or Ruby etc. and are automatically hoisted** to Nitro's `./bin` directory when included. (** will be)

- **Doc** - Collection of project-wide documentation or notes. Individual repos have their own READMEs, etc.

- **Misc** - Anything else that doesn't fall within the scope of the above namespaces should be namespaced with misc.

-----

## Abstract Tag Specification

The Tag Specification outlines the *draft* guidance for creating, testing, and publishing new component Tags. Because this pattern will be foundational to the entire system, we'll need a strategy to safely synchronize updates (probably via an update/migrate script and other semver-friendly strategies)

This current draft specification can be found in the [Nitro Tags Spec](https://github.com/nitroUI/nitro-tag-spec) repo.


