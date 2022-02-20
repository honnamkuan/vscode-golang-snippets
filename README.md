[![Version](https://vsmarketplacebadge.apphb.com/version/honnamkuan.golang-snippets.svg
)](https://marketplace.visualstudio.com/items?itemName=honnamkuan.golang-snippets)
[![Installs](https://vsmarketplacebadge.apphb.com/installs/honnamkuan.golang-snippets.svg
)](https://marketplace.visualstudio.com/items?itemName=honnamkuan.golang-snippets)
[![Ratings](https://vsmarketplacebadge.apphb.com/rating/honnamkuan.golang-snippets.svg)](https://marketplace.visualstudio.com/items?itemName=honnamkuan.golang-snippets)

# VS Code Go Snippets
-------------------

If you find this extension useful, please consider to [buy me a coffee][coffee] ☕ 😉

This extension contains code snippets for Go language in [VS Code][code].


## Installation

In order to install an extension you need to launch the Command Palette (`Ctrl + Shift + P` or `Cmd + Shift + P`) and type Extensions.
There you have either the option to show the already installed snippets or install new ones. Search for `honnamkuan.golang-snippets` and install it.

## Supported languages (file extensions)
* Go (.go)

## Snippets

Below is a list of all available snippets and the triggers of each one.

### General
| Prefix  | Content |
| :------- | ------- |
| `vv`   | initialize variable `varName := value`|
| `ier`   | if error `if err != nil { myStatements }` |
| `ifok`   | if ok `if value,ok := myFunc; ok { myStatements } `|
| `fr`   | for range `for _, v := range values { myStatements }`|
| `frr`   | for range channel `for v := range channel { myStatements }`|
| `def`   | case default `default:` |
| `cl`   | close `close(closable)` |
| `fms`   | fmt Sprintf `fmt.Sprintf("%+v", args)` |
| `fme`   | fmt Errorf `fmt.Errorf("%+v", args)` |


### Types
| Prefix  | Content |
| :------- | ------- |
| `st`   | struct type <pre>type structName struct {<br/>}</pre>|
| `sf`   | struct field `fieldName string`|
| `stt`   | struct tag `` `json:"jsonFieldName"` ``|
| `ne`   | struct constructor method <pre>func NewFoo() *Foo{<br/>  return &Foo {<br/>  }<br/>}</pre>|
| `inte`   | Interface type <pre>type interfaceName interface {<br/>}|


### Collection manipulation
| Prefix  | Content |
| :------- | ------- |
| `sr`   | remove one element from slice `slice = append(slice[:index], slice[index+1:]...)` |
| `ap`   | append element to slice `slice = append(slice, element)` |
| `del`   | delete map element by key `delete(map, key)`|




### Return values
| Prefix  | Content |
| :------- | ------- |
| `rn`   | Return Nil `return nil`|
| `rne`   | Return Nil and err `return nil, err`|
| `re`   | Return err `return err`|


### Logging
| Prefix  | Content |
| :------- | ------- |
| `lo`   | log variable `log.Printf("%+v\n", varName)` |
| `le`   | log error `log.Printf("%+v\n", err)` |
| `lef`   | log error (when using logrus) `log.Errorf("%+v\n", err)` |
| `lf`   | log fatal `log.Fatal(err)` |
| `lff`   | log fatal `log.Fatalf("%+v\n", err)` |


### Error Handling
| Prefix  | Content |
| :------- | ------- |
| `es`   | errors with stack `errors.WithStack(err)`|
| `em`   | error with message `errors.WithMessage(err, message)`|
| `emf`   | error with messagef `errors.WithMessagef(err, format, args)`|
| `is`   | errors Is `if errors.Is(err, MyError) { myStatements }`|
| `as`   | errors As <pre>var e ErrorType<br/>errors<span>.</span>As(err, &e) {<br/>  myStatements<br/>}</pre> |


### Concurrency
| Prefix  | Content |
| :------- | ------- |
| `gofunc`   | anonymous go function `go func() { myStatements }` |
| `defunc`   | anonymous defer function `defer func { myStatements }`|
| `lock`   | sync.Mutex Lock and defer Unlock <pre>mu.Lock()<br/>defer mu.Unlock()</pre>|
| `nb` | non-blocking channel send <pre>select {<br/>case msg &lt;- msgChan:<br/>default:<br/>}</pre>|

### Testify Assert
| Prefix  | Content |
| :------- | ------- |
| `anil`   | assert nil `assert.Nil(t, actual)` |
| `annil`   | assert not nil `assert.NotNil(t, actual)` |
| `aeq`   | assert nil `assert.Equal(t, expected, actual)` |
| `anerr`   | assert nil `assert.NoError(t, err)` |

[code]: https://code.visualstudio.com/
[coffee]: https://buy.stripe.com/9AQ9DA6qq3Afbrq7ss


