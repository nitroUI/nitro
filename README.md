# Introduction
Nitro UI is an **experimental** Abstract Part Assembly sytem for generating components, independent of their underlying API. The general idea is that by abstracting away implementation details and idiosyncracies we can create components that are slightly more agnostic with the aim of being slightly more future-proof. 

Our first attempt down this path is in drafting specification for components for Nitro called **Parts** and building a handful of simple parts against this pattern to try and validate our premise. 


## Simple Parts Specification

The Simple Parts Specification outlines the *draft* guidance for creating, testing, and publishing new Parts. Because this pattern will be foundational to the entire system, we'll need a strategy to safely synchronize updates (probably via an update/migrate script and other semver-friendly strategies)

This current draft specification can be found in the [Nitro Parts Template](https://github.com/nitroUI/nitro-parts-template/blob/master/README.md) repo.


## Atomic Parts Hierarchy 

The Atomic Parts Hierachy is a language for describing objects and relationships in the Nitro component assembly system. In their minimal form, **Elements** are abstract (dumb) containers with a special property called **Data**; this definition helps reinforce Nitro's *Data-First Strategy*. 

By organizaing and grouping these elements into more complex **Parts**, we can create higher-order elements called **Modules**. Modules can be customized, decorated or grouped together to create supermodules called **Applications** -- just to give you an idea of some basics. Underneath it all, we try to stay focused on the flow of data between related parts.

## Sub-Atomic Parts Hierarchy 

Looks like this:

```
                         +
                         |
                         +
                     [--ABS--]
                     |   |   |
                     |   |   |
       +-------------+   |   +-----------------------+
       |                 |                           |
       |                 |                           |
       v                 v                           v
[VirtualEvent]    [VirtualElement]            [VirtualProperty]
       |                 |                           |
       |                 |                           |
      ...                |                           |
                     {Element}                   {Property}
                      |  |  |                     |  |  |
                      |  |  |                     |  |  |
                      |  |  |                     |  |  |
             +--------+  |  +-------+         +---+  |  +----+
             |           |          |         |      |       |
             v           v          v         v      v       v
    ...  {ATOMIC}   {COMPOSITE}  {NESTED}   {POS}  {SKIN} {GEOMTR} ...

```

## Todo
- [ ] Component Pattern
- [ ] Component List
- [ ] Component Detail
- [ ] Component Build
