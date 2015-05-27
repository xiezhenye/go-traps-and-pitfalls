# 语法设计

## 不纯洁的注释

缺少 attribute/annotation，使用注释来代替，违背最小惊奇原则。


## 导出方式

以名字区分是否导出
1 带来重构的麻烦，更改可见性会导致原有依赖的代码需要变动
2 导致 json 等库默认情况下对属性名要求大写开头的

## interface

interface 没有默认实现，也不能为 interface 类型添加方法

不能实现多个有相同函数签名的 interface
