## Caleb Yates
Hey!
I'm an enthusiastic programmer, who spends most of his free time integrating Rust crates together to build really cool things!
I've worked part time at a local programming company [MFDC](https://mfdc.io/), for myself in a growing [partnership](https://www.jordanyatesdirect.com/about#About%20Us), and on many side projects that have collectively taught me most of what I know today about programming.

## Schoolbox Styling
In Grade 10 i built a small chrome extension to change the colours of SchoolBox, a LMS our school used. It quickly grew in popularity, now it has about 143 users.
Such a simple solution, but I designed it to be transparent and automatic, so once you've installed it, it will silently sync between devices and just keep working.
![image](https://github.com/user-attachments/assets/bbc372e0-4882-43be-8a5f-86e4f7963257)


## JYD
I'm building a really cool 100% Rust ecommerce website from scratch.
I really enjoy building things without any tutorials, it forces you to solve already known problems and really makes you appreciate your solutions.
I've noticed that my solutions to many existing problems have matched 'industry standard' almost exactly, it is very satisfying to listen to other devs talk about problems in the companies codebase that I solved myself just the other week.

Building it in 100% Rust means I have had to seriously challenge myself, as when I first began many important projects were still starting out.
I'm keeping the source code closed-source for the moment, because I don't want other people to naively benifit from the many hours of effort by just copy-pasting my work!
But I can say the tech stack I'm using:
- [Leptos](https://leptos.dev/), a strongly-typed fine-grained reactivity isomorphic web framework; Integrating with its reactivity implementation has taught me a lot about how reactivity is implemented in other frameworks (such as VueJS and React) beacuse it is done in a strongly-typed manner, and is no nonsense about error (panics, not loosey-goosey JS errors, will happen if you do something wrong)
- [SurrealDB)(https://surrealdb.com/), a 100% Rust database implementation; I've absolutely abused this libraries epic live updating features even when [internal bugs surface](https://github.com/surrealdb/surrealdb/issues/4921#issuecomment-2754496703), and I've designed my own in-house integration between surrealdb and leptos so that the UI with fine-grained reactivity updates on WebSocket-pushed database updates!
- [Nushell](https://www.nushell.sh/), a really good shell implementation in Rust; This shell takes the best of shell scripting and add structured datatypes, which is the only way I'll ever write scripts again
- [BinaryLane](https://www.binarylane.com.au) for self hosting, using simple-hosting solutions is for people with no time on their hands ;)

<!--
**ActuallyHappening/ActuallyHappening** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
