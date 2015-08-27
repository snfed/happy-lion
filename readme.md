# Happy Lion

客官看这里，空调打折啦 >w<  
http://banrikun.github.io/happy-lion/

## 这尼玛是啥？

Happy Lion 是一个卖萌的 CSS3 动画库，原型为苏宁易购的吉祥物小狮子。  
虽然暂时并没有什么卵用，但还是期待群众们一起来完善……

## 正确的姿势：

### 如何使用？

第一步：添加基础的 HTML 结构

```
<!-- Happy Lion Start -->
<div class="happy-lion">
    <div class="lion-face">
        <div class="lion-nose"></div>
    </div>
</div>
<!-- Happy Lion End -->
```

第二步：引入 CSS 文件，添加需要的特效

```
...
<div class="happy-lion hl-fly">
...

```

### 如何拓展？

为了减少标签嵌套，Happy Lion 使用了大量的伪元素，尽管如此，我们依然可以使用 CSS3 强大的属性制作多样的动态效果。如果您觉得现有的 HTML 标签无法满足需求，则可以添加新的标签，例如：


```
<!-- Happy Lion Start -->
<div class="happy-lion">
    <div class="lion-face">
        <div class="hl-smile-l"></div>
        <div class="hl-smile-r"></div>
        <div class="lion-nose"></div>
    </div>
</div>
<!-- Happy Lion End -->
```

这样并不会对现有的其它效果产生影响，当然，我们可能也需要一个开发规范。

## 做个约定吧！

Happy Lion 采用 Sass 编写，其中 `_base.scss` 存放了基础的样式，而特效则存放于单独的 `_*.scss` 文件。如此便可以在 `style.scss` 中 `@import` 指定的特效，实现按需编译。

同时，我们约定将 `happy-lion` 和 `lion-*` 作为保留关键词。除此之外，建议您使用 `hl-特效名-*` 的方式命名，避免冲突。

## 各部件名称：

`.happy-lion::before`  

头：外部圆角矩形 （正）

`.happy-lion::after`

头：外部圆角矩形 （斜）

`.lion-face`  

脸：包含眼、鼻、嘴，主体为白色圆角矩形（嘴）

`.lion-face::before`

眼：黑色圆 （左）

`.lion-face::after`

眼：黑色圆 （右）

`.lion-nose`

鼻：由于形状特殊，这里使用了图形遮盖，故不建议拆分