类型系统
========

多态
----

    type Parent struct {}
    type Child1 struct { Parent }
    type Child2 struct { Parent }

interface 类型转换
------------------

在 go 中，可以把类型转换到它实现的接口上。

    type I interface{}
    type Foo struct{}
    var foo Foo
    i := I(foo)

这样可以编译通过并能正常运行。但是这样就不行：

    var fooSlice []Foo
    is := []I(fooSlice)
  
go 中并不能把一个类型的 slice 转换成它的接口的 slice。这是为什么呢？实际上这和 go 的 interface 的实现方式有关。


  
int 和 uint
-----------
