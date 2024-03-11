# Собеседование

### Корректен ли код?

~~~go
package main

import (
	"fmt"
)

func main() {
	fmt.Println("Documentation is for users.")
	var m map[string]int64
	m["one"] = 1
	m["two"] = 2
}
~~~

### Что не так? 

~~~go
package main

import (
	"fmt"
	"strings"
)

func main() {
	arr := []interface{}{"str", int(22), false}

	for _, a := range arr {
		switch a.(type) {
		case int:
			a = a * 2
		case bool:
			a = !a
		case string:
			a = strings.ToUpper(a)
		}
		fmt.Printf("%#v\n", a)
	}
}
~~~





### Что выведет программа? 

~~~go
package main

type MyError struct {
	String string
}

func (m MyError) Error() string {
	return m.String
}

func foo() *MyError {
	return nil
}

func main() {
	var err error

	if err = foo(); err != nil {
		println("Error!!")
	} else {
		println("Ok")
	}

}

~~~

### Что выведет программа? 

~~~go
package main

import "fmt"

func main() {

	var m = map[int]int{}
	m[0] = 3
	m[1] = -5
	m[2] = 4
	m[3] = 7

	for _, val := range m {
		fmt.Printf("val = %d\n", val)
	}

}

~~~


