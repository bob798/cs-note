### 功能点

- 模板语言
- 计算属性与监听器
- 列表渲染
- 条件渲染
- 事件处理
- 表单输入绑定
- class与style 绑定
- 组件基础 

### 疑问

- 父子组件初始化顺序
- 缓存中的组件初始化顺序
- 快速定位问题

### 引入第三方工具包

lodash 方法，

```vue
import snakeCase from 'lodash/snakeCase'
import isArray from 'lodash/isArray'
import map from 'lodash/map'
import mapKeys from 'lodash/mapKeys'
// 驼峰转下划线
snakeCase (o) {
      if (isArray(o)) {
        return map(o, this.snakeCase)
      }
      return mapKeys(o, (value, key) => snakeCase(key))
    }
```

使用 示例

https://vuejsexamples.com/