# goejs

provider a powerful template by using ejs. But you should **very careful to using it in a high traffic business**.


## Usage

```go
e := NewDefaultOttoEngine()
got, _ := e.Exec("hello, <%= name %>!", map[string]interface{}{"name": "goejs"}, &contract.Option{
	Debug: true,
})
fmt.Println(got) // hello, goejs!
```

goja exists error, use otto first.

## diff with ejs

- not support include, partials
- keep `<%_`, `_%>`
- not use strict
- remove opts.scope
- remove opts.async
- remove opts.client
- remove opts.destructuredLocals

## best Scene

- admin page
- config template 
- dev tool

## more ejs syntax

https://ejs.co/#docs

## Thanks

- [ejs](https://github.com/mde/ejs/)
- [otto](https://github.com/robertkrimen/otto)