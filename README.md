# Nitro UI
Nitro UI (monorepo)


## Nitro Parts Pattern 

The Nitro Parts Pattern outlines the *draft* structure for creating adding new Nitro components called Parts. The pattern is used for writing automation scripts that build and test the parts individually and collectively. Because this pattern is foundational to the entire system, any changes to the pattern will have to be versioned to ensure compatibility; (we may want to look at how to migrate legacy components to newer versions).

The specification for parts is in the [Nitro Part Template repo](https://github.com/nitroUI/nitro-part-template/blob/master/README.md)


## Nitro Assembly Hierarchy 

The Nitro Assembly Hierachy is a language for describing objects and relationships in the Nitro component assembly system. **Elements** in their minimal form are abstract containers for data; this definition helps reinforce Nitro's *Data-First Strategy*. 

By organizaing and grouping these elements into more complex **Parts**, we can create higher-order elements called **Modules**. Modules can be customized, decorated or grouped together to create supermodules called **Applications** -- just to give you an idea of some basics.

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
