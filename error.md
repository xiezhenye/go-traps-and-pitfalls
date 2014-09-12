错误处理
========

go 语言惯例上使用返回值来实现错误处理，如

    func foo() error {
     ...
    }
    
    func main() {
      err := foo()
      if err != nil {
        ...
      }
    }

