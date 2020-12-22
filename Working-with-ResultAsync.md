`todo`

Early on in your usage / learning of `ResultAsync`, you may have realized that you can't create `async` functions that return `ResultAsync` values (a `async` function **always** returns a `Promise<T>`, where `Promise` is the native promise object).

Additionally, this doc should mention how Promises passed into `ResultAsync.fromPromise` should not `catch` the error. Rather, they should use the second argument to `fromPromise` in order to transform the error value into a known type `E`.

References:

- https://github.com/supermacro/neverthrow/issues/179
- https://github.com/supermacro/neverthrow/issues/191#issuecomment-749059246