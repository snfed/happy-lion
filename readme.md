# Happy Lion

客官看这里，空调打折啦 >w<  
http://banrikun.github.io/happy-lion/

## 这尼玛是啥？

Happy Lion 是一个卖萌的 CSS3 动效库，原型为苏宁易购的吉祥物小狮子。  
虽然暂时并没有什么卵用，但还是期待群众们一起来完善……

## 做个约定吧！

Happy Lion 采用 Sass 编写，其中 `_base.scss` 存放了基础的样式，而特效则存放于单独的 `_*.scss` 文件。如此便可以在 `style.scss` 中 `@import` 指定的特效，实现按需编译。

同时，我们约定将 `happy-lion` 和 `lion-*` 作为保留关键词。除此之外，建议您使用 `hl-特效名-*` 的方式命名，避免样式冲突。

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