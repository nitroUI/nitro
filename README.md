# Introduction
Nitro UI is a collection of open-source evergreen webcomponents called **Abstract Tags**, based on Nitro's [Abstract Tag Specification](https://github.com/nitroUI/ATS). In adopting the ATS pattern for creating tags, Nitro attempts to blackbox implementation details of underlying "view-only" UI libraries like React, Vue, Polymer, and Mithril.

In exposing a consistant, but implementation-indepedent featureset, Nitro enables the creation of re-usable webcomponents that are slightly more evergreen, agnostic, and future-forward (EAF).

# Nitro's Goal

We are big fans of native web technology, webcomponents and the HTML5 custom-tag spec. As Nitro evolves with available technology and brainpower, we encourage you future contributors and end-users to help keep Nitro UI true to it's eternal goal of being "more EAF".

-----
## Creating Tags from Parts

Parts are tag specifications and source code; once built these parts are packaged into tags. Tags are consumed by the end-user, or person using the parts in an application or module.


-----
## Component Creators
If you're building a Nitro Part, think in terms of Parts 

| Term                     | General Meaning  |
| -------------------------|:---------------- |
| *part*                   | smallest standalone component (atomic)      | 
| *component*              | a collection of two or more parts           | 
| *module*                 | a collection of two of parts and components | 
| *application*            | 

-----
## Component Consumers
If you're using Nitro Components, think in terms of Tags

-----
## Nitro Repo Naming Convention

### Main Repos
These top-level repos don't follow the repo naming convention.

| Repo          | Repo Namespace   | Desc  |
| ------------- |:---------------- | :-----| 
| [Nitro](https://github.com/nitroUI/nitro)         | *nitroUI/nitro*  | Nitro Main | 
| [Bolt](https://github.com/nitroUI/bolt)          | *nitroUI/bolt*   | Nitro CLI utility | 
| [ATS](https://github.com/nitroUI/ats)           | *nitroUI/ATS*    | Nitro Abstract Tag Specification | 

-----

### Sub Repos
Use these convention for creating new sub-repos to help make it easy to identify repos by their uses cases. 

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



