# Task 3 - Grammars and Derivations

`<assign>` => `<id>` = `<expr>`\
`<id>` => A | B | C\
`<expr>` => `<id>` + `<expr>`\
| <`id>` * `<expr>`\
| (`<expr>`)\
| `<id>`\

## Example

```plaintext
  A = A * (B + (C * A))
```

```plaintext
      <assign>
      /      \
    <id> =  <expr>
    |       /     \
    A     <id> *  <expr>
            |     /    \
            A   <id> + <expr>
                  |    /    \
                  B  <id> *  <expr>
                      |         \
                      C         <id>
                                  |
                                  A
```
