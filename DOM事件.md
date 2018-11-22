# DOM事件详解

**事件**是**JavaScript**和**HTML**交互的基础

>我们常说的DOM0级事件，DOM2级事件甚至DOM3级事件分别代表着：不同的阶段DOM标准对事件的实现方式

## DOM0级
  在DOM标准中其实是没有level 0这一标准的，它只是我们人为定义的一个历史参考点，可以理解为最早支持的DHTML。

  **绑定的方式如下：**

```html
  <div id='box' onclick="alert('click点击')"></div>
  // 或
  <script>
    document.getElementById('box').onclick = function () {
      alert('click点击')
    }
  </script>
```

## DOM level 1
  level 1标准没有定义相关的事件标准，所以没有对应的DOM1级事件

## DOM level 2
  level 2标准针对DOM事件，定义了事件处理模型，就是事件流，包含事件捕获，处于目标阶段，事件冒泡三个阶段，并添加了绑定事件addEventListener和移除事件removeEventListener API。

  捕获阶段 window -> document -> body -> target

  处于目标阶段

  冒泡阶段 target -> body -> document -> window

## DOM level 3
  level 3标准针对DOM事件，添加了自定义事件api。更多的对事件的补充和规范。
