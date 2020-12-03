```
hello.go
>>>>>>
package main
import "fmt"
func main() {
	fmt.Println("Hello ハロー ฮัลโหล 무매")
}
<<<<<<

sandbox.go
>>>>>>
package main

import (
	"fmt"
	"time"
)

func main() {
	fmt.Println("Welcome to the playground!")
	fmt.Println("The time is", time.Now())
}
<<<<<<

package.go
>>>>>>
package main
import (
	"fmt"
	"math/rand"
)
func main() {
	fmt.Println("My favorite number is", rand.Intn(10))
}
<<<<<<

imports.go
>>>>>>
package main
import (
	"fmt"
	"math"
)
func main() {
	fmt.Printf("Now you have %g problems.\n", math.Sqrt(7))
}
<<<<<<

exportname.go
>>>>>>
package main
import (
	"fmt"
	"math"
)
func main() {
	fmt.Println(math.pi)
}
<<<<<<

functions.go
>>>>>>
package main
import "fmt"
func add(x int, y int) int {
	return x + y
}
func main() {
	fmt.Println(add(42, 13))
}
<<<<<<

functions2.go
>>>>>>
package main
import "fmt"
func add(x, y int) int {
	return x + y
}
func main() {
	fmt.Println(add(42, 13))
}
<<<<<<

multiresult.go
>>>>>>
package main
import "fmt"
func swap(x, y string) (string, string) {
	return y, x
}
func main() {
	a, b := swap("hello", "world")
	fmt.Println(a, b)
}
<<<<<<

nameresult.go
>>>>>>
package main
import "fmt"
func split(sum int) (x, y int) {
	x = sum * 4 / 9
	y = sum - x
	return
}
func main() {
	fmt.Println(split(17))
}
<<<<<<

variable.go
>>>>>>
package main
import "fmt"
var c, python, java bool
func main() {
	var i int
	fmt.Println(i, c, python, java)
}
<<<<<<

varinit.go
>>>>>>
package main
import "fmt"
var i, j int = 1, 2
func main() {
	var c, python, java = true, false, "no!"
	fmt.Println(i, j, c, python, java)
}
<<<<<<

shortvar.go
>>>>>>
package main
import "fmt"
func main() {
	var i, j int = 1, 2
	k := 3
	c, python, java := true, false, "no!"
	fmt.Println(i, j, k, c, python, java)
}
<<<<<<

basictype.go
>>>>>>
/*
int  int8  int16  int32  int64
uint uint8 uint16 uint32 uint64 uintptr
byte rune float32 float64 complex64 complex128
*/
package main
import (
	"fmt"
	"math/cmplx"
)
var (
	ToBe   bool       = false
	MaxInt uint64     = 1<<64 - 1
	z      complex128 = cmplx.Sqrt(-5 + 12i)
)
func main() {
	fmt.Printf("Type: %T Value: %v\n", ToBe, ToBe)
	fmt.Printf("Type: %T Value: %v\n", MaxInt, MaxInt)
	fmt.Printf("Type: %T Value: %v\n", z, z)
}
<<<<<<


zero.go
>>>>>>
package main
import "fmt"
func main() {
	var i int
	var f float64
	var b bool
	var s string
	fmt.Printf("%v %v %v %q\n", i, f, b, s)
}
<<<<<<

typeconv.go
>>>>>>
package main
import (
	"fmt"
	"math"
)
func main() {
	var x, y int = 3, 4
	var f float64 = math.Sqrt(float64(x*x + y*y))
	var z uint = uint(f)
	fmt.Println(x, y, z)
}
<<<<<<

vi consant.go
>>>>>>
package main
import "fmt"
const Pi = 3.14
func main() {
	const World = "世界"
	fmt.Println("Hello", World)
	fmt.Println("Happy", Pi, "Day")
	const Truth = true
	fmt.Println("Go rules?", Truth)
}
<<<<<<

vi for.go
>>>>>>
package main
import "fmt"
func main() {
	sum := 0
	for i := 0; i < 10; i++ {
		sum += i
	}
	fmt.Println(sum)
}
<<<<<<

for2.go
>>>>>>
package main
import "fmt"
func main() {
	sum := 1
	for ; sum < 1000; {
		sum += sum
	}
	fmt.Println(sum)
}
<<<<<<

for3
>>>>>>
package main
import "fmt"
func main() {
	sum := 1
	for sum < 1000 {
		sum += sum
	}
	fmt.Println(sum)
}
<<<<<<

for4
>>>>>>
package main
func main() {
	for {
	}
}
<<<<<<

if.go
>>>>>>
package main
import (
	"fmt"
	"math"
)
func sqrt(x float64) string {
	if x < 0 {
		return sqrt(-x) + "i"
	}
	return fmt.Sprint(math.Sqrt(x))
}
func main() {
	fmt.Println(sqrt(2), sqrt(-4))
}
<<<<<<

if2.go
>>>>>>
package main
import (
	"fmt"
	"math"
)
func pow(x, n, lim float64) float64 {
	if v := math.Pow(x, n); v < lim {
		return v
	}
	return lim
}
func main() {
	fmt.Println(
		pow(3, 2, 10),
		pow(3, 3, 20),
	)
}
<<<<<<

switch.go
>>>>>>
package main

import (
	"fmt"
	"runtime"
)

func main() {
	fmt.Print("Go runs on ")
	switch os := runtime.GOOS; os {
	case "darwin":
		fmt.Println("OS X.")
	case "linux":
		fmt.Println("Linux.")
	default:
		// freebsd, openbsd,
		// plan9, windows...
		fmt.Printf("%s.\n", os)
	}
}
<<<<<<

switch2.go
>>>>>>
package main

import (
	"fmt"
	"time"
)

func main() {
	fmt.Println("When's Saturday?")
	today := time.Now().Weekday()
	switch time.Saturday {
	case today + 0:
		fmt.Println("Today.")
	case today + 1:
		fmt.Println("Tomorrow.")
	case today + 2:
		fmt.Println("In two days.")
	default:
		fmt.Println("Too far away.")
	}
}
<<<<<<

swtich3.go
>>>>>>
package main
import (
	"fmt"
	"time"
)
func main() {
	t := time.Now()
	switch {
	case t.Hour() < 12:
		fmt.Println("Good morning!")
	case t.Hour() < 17:
		fmt.Println("Good afternoon.")
	default:
		fmt.Println("Good evening.")
	}
}
<<<<<<

defer.go
>>>>>>
package main
import "fmt"
func main() {
	defer fmt.Println("world")
	fmt.Println("hello")
}
<<<<<<

defer2.go
>>>>>>
package main
import "fmt"
func main() {
	fmt.Println("counting")
	for i := 0; i < 10; i++ {
		defer fmt.Println(i)
	}
	fmt.Println("done")
}
<<<<<<

point.go
>>>>>>
package main
import "fmt"
func main() {
	i, j := 42, 2701
	p := &i         // point to i
	fmt.Println(*p) // read i through the pointer
	*p = 21         // set i through the pointer
	fmt.Println(i)  // see the new value of i
	p = &j         // point to j
	*p = *p / 37   // divide j through the pointer
	fmt.Println(j) // see the new value of j
}
<<<<<<

struct.go
>>>>>>
package main
import "fmt"
type Vertex struct {
	X int
	Y int
}
func main() {
	fmt.Println(Vertex{1, 2})
}
<<<<<<

struct2.go
>>>>>>
package main
import "fmt"
type Vertex struct {
	X int
	Y int
}
func main() {
	v := Vertex{1, 2}
	v.X = 4
	fmt.Println(v.X)
}
<<<<<<

struct3.go
>>>>>>
package main
import "fmt"
type Vertex struct {
	X int
	Y int
}
func main() {
	v := Vertex{1, 2}
	p := &v
	p.X = 1e9
	fmt.Println(v)
}
<<<<<<

struct4
>>>>>>
package main
import "fmt"
type Vertex struct {
	X, Y int
}
var (
	v1 = Vertex{1, 2}  // has type Vertex
	v2 = Vertex{X: 1}  // Y:0 is implicit
	v3 = Vertex{}      // X:0 and Y:0
	p  = &Vertex{1, 2} // has type *Vertex
)
func main() {
	fmt.Println(v1, p, v2, v3)
}
<<<<<<

array
>>>>>>
package main
import "fmt"
func main() {
	var a [2]string
	a[0] = "Hello"
	a[1] = "World"
	fmt.Println(a[0], a[1])
	fmt.Println(a)
	primes := [6]int{2, 3, 5, 7, 11, 13}
	fmt.Println(primes)
}
<<<<<<

slide
>>>>>>
package main
import "fmt"
func main() {
	primes := [6]int{2, 3, 5, 7, 11, 13}
	var s []int = primes[1:4]
	fmt.Println(s)
}
<<<<<<

slide2
>>>>>>
package main
import "fmt"
func main() {
	names := [4]string{
		"John",
		"Paul",
		"George",
		"Ringo",
	}
	fmt.Println(names)
	a := names[0:2]
	b := names[1:3]
	fmt.Println(a, b)
	b[0] = "XXX"
	fmt.Println(a, b)
	fmt.Println(names)
}
<<<<<<

slide3
>>>>>>
package main
import "fmt"
func main() {
	s := []int{2, 3, 5, 7, 11, 13}
	s = s[1:4]
	fmt.Println(s)
	s = s[:2]
	fmt.Println(s)
	s = s[1:]
	fmt.Println(s)
}
<<<<<<

slide4
>>>>>>
package main
import "fmt"
func main() {
	s := []int{2, 3, 5, 7, 11, 13}
	printSlice(s)
	// Slice the slice to give it zero length.
	s = s[:0]
	printSlice(s)
	// Extend its length.
	s = s[:4]
	printSlice(s)
	// Drop its first two values.
	s = s[2:]
	printSlice(s)
}
func printSlice(s []int) {
	fmt.Printf("len=%d cap=%d %v\n", len(s), cap(s), s)
}
<<<<<<

slidenil.go
>>>>>>
package main
import "fmt"
func main() {
	var s []int
	fmt.Println(s, len(s), cap(s))
	if s == nil {
		fmt.Println("nil!")
	}
}
<<<<<<

slidemake.go
>>>>>>
package main
import "fmt"
func main() {
	a := make([]int, 5)
	printSlice("a", a)
	b := make([]int, 0, 5)
	printSlice("b", b)
	c := b[:2]
	printSlice("c", c)
	d := c[2:5]
	printSlice("d", d)
}
func printSlice(s string, x []int) {
	fmt.Printf("%s len=%d cap=%d %v\n",
		s, len(x), cap(x), x)
}
<<<<<<

append.go
>>>>>>
package main
import "fmt"
func main() {
	var s []int
	printSlice(s)
	// append works on nil slices.
	s = append(s, 0)
	printSlice(s)
	// The slice grows as needed.
	s = append(s, 1)
	printSlice(s)
	// We can add more than one element at a time.
	s = append(s, 2, 3, 4)
	printSlice(s)
}
func printSlice(s []int) {
	fmt.Printf("len=%d cap=%d %v\n", len(s), cap(s), s)
}
<<<<<<

range.go
>>>>>>
package main
import "fmt"
var pow = []int{1, 2, 4, 8, 16, 32, 64, 128}
func main() {
	for i, v := range pow {
		fmt.Printf("2**%d = %d\n", i, v)
	}
}
<<<<<<

range2.go
>>>>>>
package main
import "fmt"
func main() {
	pow := make([]int, 10)
	for i := range pow {
		pow[i] = 1 << uint(i) // == 2**i
	}
	for _, value := range pow {
		fmt.Printf("%d\n", value)
	}
}
<<<<<<

exercise
>>>>>>
package main
import "golang.org/x/tour/pic"
func Pic(dx, dy int) [][]uint8 {
}
func main() {
	pic.Show(Pic)
}
<<<<<<

map.go
>>>>>>
package main
import "fmt"
type Vertex struct {
	Lat, Long float64
}
var m map[string]Vertex
func main() {
	m = make(map[string]Vertex)
	m["Bell Labs"] = Vertex{
		40.68433, -74.39967,
	}
	fmt.Println(m["Bell Labs"])
}
<<<<<<

map2.go
>>>>>>
package main
import "fmt"
type Vertex struct {
	Lat, Long float64
}
var m = map[string]Vertex{
	"Bell Labs": Vertex{
		40.68433, -74.39967,
	},
	"Google": Vertex{
		37.42202, -122.08408,
	},
}
func main() {
	fmt.Println(m)
}
<<<<<<

map3
>>>>>>
package main
import "fmt"
type Vertex struct {
	Lat, Long float64
}
var m = map[string]Vertex{
	"Bell Labs": {40.68433, -74.39967},
	"Google":    {37.42202, -122.08408},
}
func main() {
	fmt.Println(m)
}
<<<<<<

map4
>>>>>>
package main
import "fmt"
func main() {
	m := make(map[string]int)
	m["Answer"] = 42
	fmt.Println("The value:", m["Answer"])
	m["Answer"] = 48
	fmt.Println("The value:", m["Answer"])
	delete(m, "Answer")
	fmt.Println("The value:", m["Answer"])
	v, ok := m["Answer"]
	fmt.Println("The value:", v, "Present?", ok)
}
<<<<<<

funcval
>>>>>>
package main
import (
	"fmt"
	"math"
)
func compute(fn func(float64, float64) float64) float64 {
	return fn(3, 4)
}
func main() {
	hypot := func(x, y float64) float64 {
		return math.Sqrt(x*x + y*y)
	}
	fmt.Println(hypot(5, 12))
	fmt.Println(compute(hypot))
	fmt.Println(compute(math.Pow))
}
<<<<<<

funcval2
>>>>>
package main
import "fmt"
func adder() func(int) int {
	sum := 0
	return func(x int) int {
		sum += x
		return sum
	}
}
func main() {
	pos, neg := adder(), adder()
	for i := 0; i < 10; i++ {
		fmt.Println(
			pos(i),
			neg(-2*i),
		)
	}
}
<<<<<

meth
>>>>>
package main
import (
	"fmt"
	"math"
)
type Vertex struct {
	X, Y float64
}
func (v Vertex) Abs() float64 {
	return math.Sqrt(v.X*v.X + v.Y*v.Y)
}
func main() {
	v := Vertex{3, 4}
	fmt.Println(v.Abs())
}
<<<<<

methfunc
>>>>>
package main
import (
	"fmt"
	"math"
)
type Vertex struct {
	X, Y float64
}
func Abs(v Vertex) float64 {
	return math.Sqrt(v.X*v.X + v.Y*v.Y)
}
func main() {
	v := Vertex{3, 4}
	fmt.Println(Abs(v))
}
<<<<<

methtype
>>>>>
package main
import (
	"fmt"
	"math"
)
type MyFloat float64
func (f MyFloat) Abs() float64 {
	if f < 0 {
		return float64(-f)
	}
	return float64(f)
}
func main() {
	f := MyFloat(-math.Sqrt2)
	fmt.Println(f.Abs())
}
<<<<<

methpoint
>>>>
package main
import (
	"fmt"
	"math"
)
type Vertex struct {
	X, Y float64
}
func (v Vertex) Abs() float64 {
	return math.Sqrt(v.X*v.X + v.Y*v.Y)
}
func (v *Vertex) Scale(f float64) {
	v.X = v.X * f
	v.Y = v.Y * f
}
func main() {
	v := Vertex{3, 4}
	v.Scale(10)
	fmt.Println(v.Abs())
}
<<<<

methpoint2
>>>>>
package main
import (
	"fmt"
	"math"
)
type Vertex struct {
	X, Y float64
}
func Abs(v Vertex) float64 {
	return math.Sqrt(v.X*v.X + v.Y*v.Y)
}
func Scale(v *Vertex, f float64) {
	v.X = v.X * f
	v.Y = v.Y * f
}
func main() {
	v := Vertex{3, 4}
	Scale(&v, 10)
	fmt.Println(Abs(v))
}
<<<<<

image
>>>>>
package main
import (
	"fmt"
	"image"
)
func main() {
	m := image.NewRGBA(image.Rect(0, 0, 100, 100))
	fmt.Println(m.Bounds())
	fmt.Println(m.At(0, 0).RGBA())
}
<<<<<

gofunc
>>>>>
package main
import (
	"fmt"
	"time"
)
func say(s string) {
	for i := 0; i < 5; i++ {
		time.Sleep(100 * time.Millisecond)
		fmt.Println(s)
	}
}
func main() {
	go say("world")
	say("hello")
}
<<<<<

channel
>>>>>
package main
import "fmt"
func sum(s []int, c chan int) {
	sum := 0
	for _, v := range s {
		sum += v
	}
	c <- sum // send sum to c
}
func main() {
	s := []int{7, 2, 8, -9, 4, 0}
	c := make(chan int)
	go sum(s[:len(s)/2], c)
	go sum(s[len(s)/2:], c)
	x, y := <-c, <-c // receive from c
	fmt.Println(x, y, x+y)
}
<<<<<

buffchan
>>>>>
package main
import "fmt"
func main() {
	ch := make(chan int, 2)
	ch <- 1
	ch <- 2
	fmt.Println(<-ch)
	fmt.Println(<-ch)
}
<<<<<

channel2
>>>>>
package main
import (
	"fmt"
)
func fibonacci(n int, c chan int) {
	x, y := 0, 1
	for i := 0; i < n; i++ {
		c <- x
		x, y = y, x+y
	}
	close(c)
}
func main() {
	c := make(chan int, 10)
	go fibonacci(cap(c), c)
	for i := range c {
		fmt.Println(i)
	}
}
<<<<<

select
>>>>>
package main
import "fmt"
func fibonacci(c, quit chan int) {
	x, y := 0, 1
	for {
		select {
		case c <- x:
			x, y = y, x+y
		case <-quit:
			fmt.Println("quit")
			return
		}
	}
}
func main() {
	c := make(chan int)
	quit := make(chan int)
	go func() {
		for i := 0; i < 10; i++ {
			fmt.Println(<-c)
		}
		quit <- 0
	}()
	fibonacci(c, quit)
}
<<<<<

select2
>>>>>
package main
import (
	"fmt"
	"time"
)
func main() {
	tick := time.Tick(100 * time.Millisecond)
	boom := time.After(500 * time.Millisecond)
	for {
		select {
		case <-tick:
			fmt.Println("tick.")
		case <-boom:
			fmt.Println("BOOM!")
			return
		default:
			fmt.Println("    .")
			time.Sleep(50 * time.Millisecond)
		}
	}
}
<<<<<

mutex
>>>>>
package main
import (
	"fmt"
	"sync"
	"time"
)
// SafeCounter is safe to use concurrently.
type SafeCounter struct {
	mu sync.Mutex
	v  map[string]int
}
// Inc increments the counter for the given key.
func (c *SafeCounter) Inc(key string) {
	c.mu.Lock()
	// Lock so only one goroutine at a time can access the map c.v.
	c.v[key]++
	c.mu.Unlock()
}
// Value returns the current value of the counter for the given key.
func (c *SafeCounter) Value(key string) int {
	c.mu.Lock()
	// Lock so only one goroutine at a time can access the map c.v.
	defer c.mu.Unlock()
	return c.v[key]
}
func main() {
	c := SafeCounter{v: make(map[string]int)}
	for i := 0; i < 1000; i++ {
		go c.Inc("somekey")
	}
	time.Sleep(time.Second)
	fmt.Println(c.Value("somekey"))
}
<<<<<

mutex2
>>>>>
package main
import (
	"fmt"
	"sync"
	"time"
)
// SafeCounter is safe to use concurrently.
type SafeCounter struct {
	mu sync.Mutex
	v  map[string]int
}
// Inc increments the counter for the given key.
func (c *SafeCounter) Inc(key string) {
	c.mu.Lock()
	// Lock so only one goroutine at a time can access the map c.v.
	c.v[key]++
	c.mu.Unlock()
}
// Value returns the current value of the counter for the given key.
func (c *SafeCounter) Value(key string) int {
	c.mu.Lock()
	// Lock so only one goroutine at a time can access the map c.v.
	defer c.mu.Unlock()
	return c.v[key]
}
func main() {
	c := SafeCounter{v: make(map[string]int)}
	for i := 0; i < 1000; i++ {
		go c.Inc("somekey")
	}
	time.Sleep(time.Second)
	fmt.Println(c.Value("somekey"))
}
<<<<<

https://tour.golang.org/welcome/1
https://golang.org/pkg/
https://golang.org/doc/articles/wiki/
https://medium.com/quick-code/top-online-courses-to-learn-go-programming-language-golang-for-beginners-c228c615946c
https://stackify.com/learn-go-tutorials/

```
