# Nitro UI
Nitro UI is an **experimental** Abstract Part Assembly sytem for generating components, independent of their framework implementation. The general idea is that by abstracting away implementation details and idiosyncracies of frontend libraries we can create solutions that are slightly more evergreen and agnostic. 

Our first attempt down this path is in creating a pattern/SDK for creating components for Nitro called Parts and building a handful of simple parts against this pattern to try and validate our premise. 


## Evergreen Parts

The Nitro Parts Pattern outlines the *draft* structure for creating new Nitro components called Parts. The pattern will be used to power  the automation scripts for building and testing parts individually, collectively, and continuously. Because this pattern will be foundational to the entire system, any changes to the pattern will have to be versioned (and clearly communicated) to ensure compatibility; (we may want to look at how to migrate legacy components to newer versions).

The specification for parts is in the [Nitro Parts Template](https://github.com/nitroUI/nitro-parts-template/blob/master/README.md) repo.


## Atomic Parts Hierarchy 

The Atomic Parts Hierachy is a language for describing objects and relationships in the Nitro component assembly system. In their minimal form, **Elements** are abstract (dumb) containers with a special property called **Data**; this definition helps reinforce Nitro's *Data-First Strategy*. 

By organizaing and grouping these elements into more complex **Parts**, we can create higher-order elements called **Modules**. Modules can be customized, decorated or grouped together to create supermodules called **Applications** -- just to give you an idea of some basics. Underneath it all, we try to stay focused on the flow of data between related parts.

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
