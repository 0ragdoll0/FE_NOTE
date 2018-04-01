# BFC(Block Formatting Context,块级格式化上下文)
* 布局规则
> In a block formatting context, each box’s left outer edge touches the left edge of the containing block 
* 创建
> 1. 设置float属性    
> 2. 设置position不为static/relative    
> 3. 设置display为：table-cell,table-caption,inline-block,flex,or inline-flex
> 4. 设置overflow属性不为visible（可设置为hidden等）-->较优
* 使用
> 1. 消除Margin Collapse      
>    原理：只有当元素在同一个BFC中时，垂直方向上的margin才会clollpase.如果它们属于不同的BFC，则不会有margin collapse.    
>    方法：设置需要消除边距折叠的元素的overflow:hidden     

> 2. 消除浮动     
>    原理：BFC布局规则       
>    方法：设置父元素为float或overflow:hidden（IE需要另外再设置zoom：1）

> 3. 阻止文本换行（float元素后文字呈环绕形式）      
>     原理：This is true even in the presence of floats (although a box’s line boxes may shrink due to the floats), unless the box establishes a new block formatting context (in which case the box itself may become narrower due to the floats).    
>     方法：为p创建BFC
