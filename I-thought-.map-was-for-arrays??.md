Yes, you're right. If you were to ask a JS developer what `.map` does, they'd probably give you their own definition of the [`Array.prototype.map` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map).

But what if I told you that `.map` is an implementation of a more abstract idea?

I will not get into the details (because they are completely unnecessary for the purposes of this discussion in all honesty), but one thing I do want to tell you about is that in the world of functional programming there's this thing called a Functor.

What's a Functor? A Functor is a "container" that can be mapped over.

So, what's an example of a Functor? ...... JS Array's are Functors! They are containers that can be mapped over. 

```
[1, 2, 3].map(num => `number is: ${num}`)
```

// map takes a Array<number> and turns it into a Array<string>
// or more formally: 
//   map<T, U>(arr: Array<T>, fn: (val: T) => U): Array<U>


`todo` ..finish this post