# React Native中的props

props为properties的简写
------
props与state区别？ props是不可变的，state是可变的
<br>
## props的默认赋值
### 可通过static defaultProps={...}默认赋值
例如：
<br>

    class MyComponent extends Component{
       static defaultProps={
      ...
       }
    }

### 可通过[componentName].defaultProps={...}默认赋值
例如：
<br>

     class MyComponent extends Component{
     }
     MyComponent.defaultProps={
     ...
     }

----
## props验证类型
### 类型如下：
<br>

    optionalArray: React.PropTypes.array,//数组类型
    optionalBool: React.PropTypes.bool,//布尔类型
    optionalFunc: React.PropTypes.func,//函数类型
    optionalNumber: React.PropTypes.number,//数字类型
    optionalObject: React.PropTypes.object,//对象类型
    optionalString: React.PropTypes.string,//字符串类型
    optionalNode: React.PropTypes.node,// 可以被渲染的对象 numbers, strings, elements 或 array
    optionalElement: React.PropTypes.element,//  React 元素
    optionalMessage: React.PropTypes.instanceOf(Message),// 用 JS 的 instanceof 操作符声明 prop 为类的实例。
    optionalEnum: React.PropTypes.oneOf(['News', 'Photos']),// 用 enum 来限制 prop 只接受指定的值。
    optionalUnion: React.PropTypes.oneOfType([// 可以是多个对象类型中的一个
      React.PropTypes.string,
      React.PropTypes.number,
      React.PropTypes.instanceOf(Message)
    ]),
    optionalArrayOf: React.PropTypes.arrayOf(React.PropTypes.number), // 指定类型组成的数组
    optionalObjectOf: React.PropTypes.objectOf(React.PropTypes.number),// 指定类型的属性构成的对象
    optionalObjectWithShape: React.PropTypes.shape({// 特定 shape 参数的对象
      color: React.PropTypes.string,
      fontSize: React.PropTypes.number
    }),
    requiredFunc: React.PropTypes.func.isRequired,// 任意类型加上 `isRequired` 来使 prop 不可空。
    requiredAny: React.PropTypes.any.isRequired,// 不可空的任意类型

