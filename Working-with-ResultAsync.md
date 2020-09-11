Early on in your usage / learning of `ResultAsync`, you may have realized that you can't create `async` functions that return `ResultAsync` values (a `async` function **always** returns a `Promise<T>`, where `Promise` is the native promise object).

`todo`
