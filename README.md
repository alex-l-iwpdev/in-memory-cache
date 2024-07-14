# Неделя 1. ДЗ 

### Install

``` go get github.com/alex-l-iwpdev/in-memory-cache```

``` go mod tidy  ```

``` go mod vendor  ```


### Use: 

Creat a new cache ```cache := cache.New()```

Set cache value ```cache.Set("userId", 42)```

Get cache value  ```cache.Get("userId")```

Delete cache item by key ```cache.Delete("userId")```
```
import (
	"github.com/alex-l-iwpdev/lessom-go-one/internal/database"
)

func main() { 
    cache := cache.New()

	cache.Set("userId", 42)
	userId := cache.Get("userId")

	fmt.Println(userId)

	cache.Delete("userId")
	userId := cache.Get("userId")

	fmt.Println(userId)
}
```
