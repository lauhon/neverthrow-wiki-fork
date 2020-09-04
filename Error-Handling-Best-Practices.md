This document outlines patterns and best practices for working in a system that doesn't ever throw exceptions.

### Distinguish between "Expected Errors" and "Unexpected, or Irrecoverable Errors"

talk about panics in Rust.


### Wrap 3rd party code to localize exceptions

The JavaScript community has agreed on the convention of throwing exceptions. As such, when interfacing with third party libraries it's imperative that you wrap third-party code in `try / catch` blocks.

### Synchronous Example:

`todo`

#### Async Example:

```typescript
import { ResultAsync } from 'neverthrow'

const getBookById = (id: string): ResultAsync<BookList, HTTPError> => ResultAsync.fromPromise(
  axios.get(`${BOOK_SERVICE_BASE_URL}/books/${id}`),
  (error: unknown) => {
    return intoHttpError(error)
  }
)
```