
Component/part/module file structure
[moved to Nitro Part Template](https://github.com/nitroUI/nitro-part-template/blob/master/README.md)

```

+----------------------------------------------+
|                                              |
|                                              |
|     [+] <nitro-part>                         |
|      |                                       |   bin        = comopnent specific executable utility files
|      +------>[ ] bin                         |
|      |                                       |   src        = part implementation code and libs live here
|      +------>[ ] docs                        |
|      |                                       |   src/lib    = common js files across implementations
|      +------>[+] src                         |
|      |        |                              |   src/res    = common media/images for implementations
|      |        |                              |
|      |        +------>[ ] lib                |   src/impl   = implementations supported by this componen
|      |        |                              |
|      |        +------>[ ] res                |   build.json = config for building implementation version
|      |        |                              |
|      |        +------>[+] impl               |   part.json  = part definition config for Nitro assembly
|      |                 |                     |
|      |                 +--->[+]<name>        |
|      |                       |               |   Generated Files
|      |                       +-->build.json  |
|      +------>[ ] part.json                   |   dist       = generated distrib file, assembled part tha
|      |                                       |                can be deployed in a ui sandbox, to larger
|      +------>[G] .nitro                      |                deployed library or to test suite
|      |                                       |
|      +------>[G] dist                        |   .nitro     = generated partid & semvar number
|                                              |
|                                              |
|                                              |
+----------------------------------------------+

```
