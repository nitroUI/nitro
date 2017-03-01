# Introduction
Nitro UI is an **experimental** Abstract Part Assembly sytem for generating components, independent of their underlying API. The general idea is that by abstracting away implementation details and idiosyncracies we can create components that are slightly more agnostic with the aim of being slightly more future-proof. 

Our first attempt down this path is in drafting specification for components for Nitro called **Parts** and building a handful of simple parts against this pattern to try and validate our ambitious premise. 


## Simple Parts Specification

The Simple Parts Specification outlines the *draft* guidance for creating, testing, and publishing new Parts. Because this pattern will be foundational to the entire system, we'll need a strategy to safely synchronize updates (probably via an update/migrate script and other semver-friendly strategies)

This current draft specification can be found in the [Nitro Parts Spec](https://github.com/nitroUI/nitro-parts-spec/blob/master/README.md) repo.

## Todo
- [ ] Component Pattern
- [ ] Component List
- [ ] Component Detail
- [ ] Component Build
