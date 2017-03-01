# Nitro UI
Nitro UI (monorepo)




## Nitro Parts Pattern 

The Nitro Parts Pattern outlines the *draft* structure for creating adding new Nitro components called Parts. The pattern is used for writing automation scripts that build and test the components individually and collectively. Because the parts pattern is foundational to the entire system, any changes to the underlying pattern will have to be versioned to ensure compatibility.

[See Nitro Part Template v1](https://github.com/nitroUI/nitro-part-template/blob/master/README.md)

## Nitro Element Hierarchy 

The Nitro Element Hierachy is a language for describing objects and relationships in the Nitro component assembly system. **Elements** in their minimal form are containers for byte data, no more no less. By organizaing and grouping these elements in a special way we create higher-order elements called **Modules**. Modules can be customized, decorated or grouped together to create supermodules called **Applications** -- and we haven't even gotten to the styling yet.

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
