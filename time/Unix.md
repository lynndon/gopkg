# func (t Time) Unix() int64

参数列表：

- 无

返回值：

- int64

功能说明：

返回Unix时间——t相对于January 1, 1970 UTC的时间间隔

代码实例：

	package main
	
	import (
		"fmt"
		"time"
	)
	
	func main() {
		t := time.Now()
		fmt.Println(t.Unix())
	}
	
	
	
# func Unix(sec int64, nsec int64) Time

参数列表：

- sec 秒
- nsec 纳秒

返回值：

- Time

功能说明：

返回参数指定的本地时间，秒和纳秒是从January 1, 1970 UTC开始计算。纳秒的取值区间为[0, 999999999]

代码实例：

	package main
	
	import (
	    "fmt"
	    "time"
	)
	
	func main() {
	    fmt.Println(time.Unix(1000, 340))
	    
	    //时间戳
	    t := time.Now().Unix()
	    fmt.Println(t)
	     
	    //时间戳到具体显示的转化
	    fmt.Println(time.Unix(t, 0).String())
	    
	    //如数时间戳是毫秒数，先除1000
	    fmt.Println(time.Unix(timestamp/1000, 0).String())
    	
	}
	
 
