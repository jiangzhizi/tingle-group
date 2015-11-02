# tingle-group [![npm version](https://badge.fury.io/js/tingle-group.svg)](http://badge.fury.io/js/tingle-group)



`Group`是列表容器组件。封装了以下功能：

* 灵活配置间隔线和子元素的缩进值，而且间隔线和子元素的缩进值是相互独立的，使`IOS`和`Material`风格的多样式列表更加容易实现。
* 在支持`hairline`显示的设备上自动优化显示成极细的线。

## Usage

首先引入`Group`，其中`Group`下面包含`Head`和`List`两个子组件。

项目环境下，`Tingle`是全局变量：

```js
// ES5
var Group = Tingle.Group;
// ES2015
let {Group} = Tingle;
```

全局使用概览：

```js
...
render() {
    return (<Group>
        <Group.Head>title</Group.Head>
        <Group.List>
            <div>content</div>
            <div>content</div>
        </Group.List>
    </Group>);
}
```

## Group.List

#### className

描述：自定义样式的`class`名称。  
类型：`String`  
默认：`''`  
必选：否

示例：

```
<Group>
    <Group.List className="customClass">...</Group.List>
</Group>
```


#### lineIndent

描述：配置间隔线的缩进值。  
类型：`Number|String|Array`  

  - Number：设置左缩进，默认追加`px`作为单位，如：`lineIndent={10}`
  - String：设置左缩进，自定义长度单位，如：`lineIndent={'1rem'}`
  - Array：设置左右缩进，数组成员的类型为`Number`或`String`，默认处理如上。如：`lineIndent={[10, 10]}`

默认：无  
必选：否

示例：

```js
<Group>
    <Group.List lineIndent={10}>...</Group.List>
</Group>
```

#### itemIndent

描述：配置列表子元素的缩进值。  
类型：`Number|String|Array`  

  - Number：设置左缩进，默认追加`px`作为单位，如：`itemIndent={10}`
  - String：设置左缩进，自定义长度单位，如：`itemIndent={'1rem'}`
  - Array：设置左右缩进，数组成员的类型为`Number`或`String`，默认处理如上。如：`itemIndent={[10, 10]}`

默认：无  
必选：否

示例：

```js
<Group>
    <Group.List itemIndent={[10, 10]}>...</Group.List>
</Group>
```


## Links

- [Issues](http://github.com/tinglejs/tingle-group/issues)
