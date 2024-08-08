```
type MyType struct { // ... } 

func (m MyType) SomeMethod() { // ... } 

var _ SomeInterface = (*MyType)(nil)
```

この場合は、`_ SomeInterface = (*MyType)(nil)`は、`MyType`型が`SomeInterface`を満たしていることを示している。

# 参考
- [Ensuring Go interface satisfaction at compile-time | by Jason | Stupid Gopher Tricks | Medium](https://medium.com/stupid-gopher-tricks/ensuring-go-interface-satisfaction-at-compile-time-1ed158e8fa17)
- [Compile time checks to ensure your type satisfies an interface #golang #quicktip | by Mat Ryer | Medium](https://medium.com/@matryer/golang-tip-compile-time-checks-to-ensure-your-type-satisfies-an-interface-c167afed3aae)
- [Model and query hooks](https://bun.uptrace.dev/guide/hooks.html#introduction)