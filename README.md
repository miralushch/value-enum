# value-enum

Macro for generating enums associated with values.

## Example

```Rust
use value_enum::value_enum;

value_enum!(
  #[derive(Clone, Copy, PartialEq, Eq, Debug)]
  enum Abc: char {
    A = 'a',
    B = 'b',
    C = 'c',
  }
);

assert_eq!(
  char::from(Abc::A),
  'a'
);
assert_eq!(
  Abc::try_from('b'),
  Ok(Abc::B)
);
```
