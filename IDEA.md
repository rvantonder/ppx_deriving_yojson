

When we have something like

```
type t = string
```

I want a yojson deriver that will serialize/deserialize against a concrete value, so, e.g.,

```
type x = string [@literal "hello"]
```

and when this is used in a record

```
type t =
   { message_type : x }
```

It will only parse when `x` matches `"hello"`.

Similar for

```
type x = int [@literal 0]
```
