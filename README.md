# vulkan-spirv-pretty
Wrapper over vulkan-spirv library that makes working with spirv in Javascript even easier

## A goal is to have something closer to human readable spirv code:
```javascript
const Spirv = require('vulkan-spirv-pretty')(1, 2); //version 1.2

const spirv = (new Spirv())
  .function("main", code => {
    code
      .nop()
      .nop()
  })
  .function("some_function", code => {
    code
      .var("variableName", _some_variable_type)
      .nop()
      .nop()
      .while( _some_condition_, code => {
        code
          .nop()
          .nop()
      })
  })

```