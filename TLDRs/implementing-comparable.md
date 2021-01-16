# TL;DR - Implementing Comparable`<T>`

- you can't instantiate an interface
- interfaces allow us to write polymorphic code
- many pre-existing classes implement Comparable`<T>`
- Comparable only forces you to write one method: `int compareTo(T t)`
- `compareTo` must:
  - return a negative int if this comes before other
  - return a positive int if this comes after other
  - return 0 otherwise
- if your natural order involves numbers, the easiest way to do an ascending compareTo is `return this.field - other.field`
  - to go descending, just flip it: `other.field - this.field`