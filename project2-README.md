## 网站性能优化项目
### 关键渲染路径
在index.html中：

1. 对字体的样式规则进行内联式的媒体查询方法。
2. 对外联的css/print.css样式表进行print媒体查询。
3. 对外联的js文件进行异步加载。
4. 把内联的js代码放在html文档里body中的最后位置。
### 去除卡顿
在views/js目录下的main.js中，主要修改两大问题：

1. 修改函数changePizzaSizes（第443行）中对size的判断、更改方式和避免document.querySelectorAll（）的重复使用。
2. 修改查询document.body.scrollTop（第508行）属性的方式，把其提出循环之外，避免大量的重复强制布局。

