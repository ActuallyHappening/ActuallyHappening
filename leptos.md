## Caleb's notes on Leptos
I've used leptos a couple times now, the first time earlier in its development, around 0.4-0.5, and back then I wasn't experienced enough to use it for anything too complicated.

Recently (2025) I started to build a basic ecommerce fullstack website in it, using `surrealdb` and leptos version 0.7. I laugh at where I began, no caching on database requests and not using `Transition` or `Suspense`, but manually dealing with the `LocalResource.value` Option.
Some notes:
- Understanding the reactivity system is really rewarding, understanding that everything is just `Effect::new` and `Signal::derive` under the hood yields a surprisingly simple mental model for when you need it
- Compile times are really slow, even with `--cfg erase_components` (which I looked for in the book under DX because I figured they would talk about something along those lines, and I was right to my pleasant surprise)
- USE ONLY ONE ERROR TYPE. This took me a while to understand why, but the "performance benefits" of using multiple error types is simply not an excuse to overcomplicate error handling, call your error `AppError` and export `AppResult<T>` in your prelude
- I found error handling, even after significant effort, was still annoying because Rust itself has no way of scoping usages of the question mark `?` operator, sometimes I even found myself using IIFE (immediately invoked function expressions), a trick from the JavaScript world I never though would be pure and useful to know!
  - Expanding on this, there was a bug with <ErrorBoundary /> that complicated things for me
  - Also, almost always to handle errors involved an inner closure like `let ui = move || -> AppResult<_> { fallible???.map(|d| view! { ... })}` that was a non-trivial amount of boilerplate to handle errors correctly
- The defaults for leptos were very bare bones, e.g. no default <Transition /> or <ErrorBoundary /> to warn you if you did something bad
- The developer experience using `cargo leptos` was OK, but compared to `dx serve` had a long ways to go
