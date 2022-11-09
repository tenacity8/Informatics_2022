# Лабортаорная работа "Функции" 
## Иванова Мария Алексеевна, 12 вариант 


## Цель работы 
Осуществить решение задачи программой на языке go.

## Задача
 ```
y = a^(X^2-1) - lg(x^2 - 1) + (x^2-1)^(1/3)
 ```

Для задачи 1: a = 1.6, Xн = 1.2, Xк = 3.7, delX = 0.5
Для задачи 2: a = 1.6, x1 = 1.28, x2 = 1.36, x3 = 2.47, x4 = 3.68, x5 = 4.56 

## Выполнение работы 
ЗАДАЧА 1.

```go 
package main

import (
	"fmt"
	"math"
)

func main() {

	var a = 1.6

	for x := 1.2; x <= 3.7; x += 0.5 {
		b := math.Pow(x, 2) - 1
		y := math.Pow(a, b) - math.Log10(b) + math.Pow(b, (1/3))
		fmt.Println("x = ", x, " ", "y = ", y)
	}
}
```
После выполения данной программы получим следующий вывод: 

```go
x =  1.2   y =  2.5862858871069654
x =  1.7   y =  3.154548318387074
x =  2.2   y =  6.494509067428108
x =  2.7   y =  19.42848945770503
x =  3.2   y =  76.95952903579777
x =  3.7   y =  389.19490352065037
```


ЗАДАЧА 2.

```go 
package main

import (
	"fmt"
	"math"
)

func main() {

	var a = 1.6
	var znach = [5]float64{1.28, 1.36, 2.47, 3.68, 4.56}

	for _, x := range znach {
		b := math.Pow(x, 2) - 1
		y := math.Pow(a, b) - math.Log10(b) + math.Pow(b, (1/3))
		fmt.Println("x = ", x, " ", "y = ", y)
	}
}
```
После выполнения данной программы получим следующий вывод: 

```go
x =  1.28   y =  2.5448338516669176
x =  1.36   y =  2.5615887682504983
x =  2.47   y =  11.287362958564565
x =  3.68   y =  363.10883719818236
x =  4.56   y =  10971.28636918291
```