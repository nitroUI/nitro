
Component/part/module file structure

<pre>
+---+                          +
+[ ]+ COMPONENT_ROOT           |
  +                            |
  |                            |
  +------>[] bin               |   bin = component specific executable utility files
  |                            |
  |                            |
  +------>[] lib               |   lib = common js files across implementations
  |                            |
  |                            |
  +------>[] res               |   res = common media/images for implementations
  |                            |
  |                            |
  +------>[] impl              |   impl = implementations supported by this component
  |        +                   |
  |        +--->[]react        |
  |        |    +              |   build.json = config for building implementation version
  |        |    +->build.json  |
  |        |                   |
  |        +--->[]vue          |   nitro.json = part definition config for Nitro assembly
  |        |                   |
  |        |                   |
  |        +--->[]bootstrap    |   dist** = generated distrib file, assembled part that
  |                            |            can be deployed in a ui sandbox, to larger
  +------>[+] part.json        |            deployed library or to test suite
  |                            |
  +------>[+] .nitro           |
  |                            |   .nitro = generated partid & semvar number
  |                            |
  +------>[] dist**            +
</pre>
