# The ideal abstraction
**There is no ideal abstraction, except the absence of one to provide the flexibillity of chosing your own.** (my own quote)

That said, the abstractions i would 100% invest my time, energy and money into are as follows:
- Rust
- WebGPU
- docs.rs/tracing
- URL links, e.g. https://ymap.dev/thing/isinternal

## URLs as data
Using URLs as data is an absolutely underrated mechanism.
Firstly, they are the perfect blend of human readability (UTF-8), typeability, yet precision and exactness.
They naturally have a global namespace, and if desired you can trivially create your own namespaces.
But the most important property they have is that they are universally supported *as a data*, as in, in their meta form. All programs that support UTF-8 support natively transacting URLs, but more importantly many programs automatically handle them in a desirable way, i.e. clicking them in terminals.
URLs have global meaning (in theory), anybody anywhere if they trust their network and the URL domain they are connecting to, can access the URLs backing information. Having a commit hash doesn't tell somebody the git repo their talking about, on the contrary, or even that the random hash of data is even related to git.
Supporting URLs supports many usecases

## My ideal abstraction
In the end, even Christianity doesn't give us an ideal abstraction. The the question becomes: what qualities do you want of future abstractions?

- Temporal relevance, i.e. showing timestamps that don't become obselete if screenshotted and viewed at a later date
  - This means building UIs that don't lose information by screenshotting them
- Action data / UI independence, i.e. having logic and UI untangled
  - This makes automating and testing the logic behind an application easier (not trivial)
- Tracability, having logs that partially or explicitely link back to the source code
  - This helps debugging, even in release builds exposing line numbers isn't a security vulnerabilty
  - This also allows for holistic understanding, traces should be a trusted and reliable system, so reading traces should give you a solid understanding of the workings of code
  - To practically facilitate this, it would be great in Rust for a `std2` crate to be released that automatically traces all systemcalls with high-level interpretations (performance wise, most of this would be disabled by default). Ideally, by patching std you could get traces of most file reads and network calls to truly understand how a program behaves
- OS-level appreciation, meaning using RedoxOS where things don't "just work" and your forced to understand the hardware and many layers of software involved
  - RedoxOS is 100% Rust which is why I'm interested in it
- Statically linking everything, OpenSSL included
  - Dynamically linking is a thing of the past in terms of the problem it solved, which was to save storage space
  - Statically linking avoid you needing to validate your consuming an un-compromised library at runtime
  - Statically linking forces you to constantly rebuild your project as your deps update.
    This is perhaps its biggest downside, your tiny CLI project which linked against a yesterday-compromosed OpenSSL version will never update faster than your OS currently
- Stability without stagnation, rebuilding your projects regularly (daily hopefully)
  - This is a hard but objective goal, updating minor versions and running tests when minor versions of dependencies change is very important from a security standpoint and a good practise
  - Stability is hard to do properly, automated tooling is very important here
- Running programs is always better than "declarativeness"
  - Hot take, programs can be written declaratively and there is always a blur between running a program and resolving configuration options
  - In general serializability and declarativity are seperate and inequal concepts, configuration can be serializable without being declarative, think IR
  - Hooks shouldn't rely on anything to do with the system except a very *very* small hole, say a command to build and run a Rust project that takes a stdin and pipes stdout like `cargo run pre_commit_hook`.
    This hole should be a rust project on the stable channel where the version of stable used is `msrv`ed to something determined by the version of the project itself, to force updates and allow modern scripts to be reasonably backwards compatible
