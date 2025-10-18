# Caleb Yates
Hey!
I'm an enthusiastic programmer, who spends most of his free time integrating Rust crates together to build really cool things!
I work casually at a local programming company [MFDC](https://mfdc.io/) and contract for [Salt](salt.space), as well as on many side projects that have collectively taught me most of what I know today about programming.

## Schoolbox Styling
During high school (grade 10) I built a small chrome extension to change the colours of SchoolBox, an LMS our school used. It quickly grew in popularity, now it has over a hundred users spread across various schools in Ausrtalia and New Zealand.
Such a simple solution, but I designed it to be transparent and automatic, so once you've installed it, it will silently sync between devices and just keep working.
I wanted to mention this because it was the first time a project I had built directly impacted the lives of people I had never met before, and because it used a very-hacky method of integrating [Flutter](https://flutter.dev/) with the [JS chrome extension API](https://developer.chrome.com/docs/extensions/reference/api) that I still get Github issue emails from to this day ;)

## ChessBois
Around the same time, me and a couple other friends entered a competition called the [Mathematics and Statistics Research Competition (MSRC)](https://ms.unimelb.edu.au/engage/outreach/mathematics-and-statistics-research-challenge). We won the Queensland Prize, and are now [published](https://terra-docs.s3.us-east-2.amazonaws.com/IJHSR/Articles/volume7-issue3/IJHSR_2025_73_71.pdf), but my favourite part is the app I built which can be viewed in website form here: https://caleb-msrc-q11.netlify.app/. It is 100% Rust, uses a 3D game engine library called [Bevy](https://bevyengine.org/), and was an invaluable tool that has not been made before (to my knowledge).
I needed to know the maths behind what I was building, but the success of that paper taught me the potential benefits of combining that domain-specific knowledge with good programming skills, which is more than just the best of both worlds.

## YMap
And finally, this is a rather grandious idea of mine that I've started to build a few times now but have kept hitting walls in my programming understanding and time.
- The first motivating aspect is a notetaking app cloning MS OneNote, with the ability to own your own data. This means ideally you could self-host on a VPS for personal notetaking without needing to sign in to an organisation, or pay Microsoft for the rest of your life. Critically, I want to use my Apple Pen for drawing and *double tap* functionality, which isn't easy with `winit`.
- Beyond that, I wanted to build my own VCS (Version Control System) to replace `git` and `github`. The primary improvements are a requirement for cryptographic signing, and I believe in the decentralized web that Ethereum's implementation of cryptography is the best alternative to `gpg`. This means developers are primarily identified by their Ethereum wallet address. I'll call this hypothetical VCS `yit` for now
- But even remaking `git` can't solve hard branch merges, so I propose a new language called `The`. The key characteristics of `The` are:
  - It is a compiled language which deeply understands the computer it is targetting
  - All aspects of the languages assumptions are documented programmatically, and can be conveniently looked up by programmers
  - Programming in `The` stores only IR. There is no stable textual storage format. Therefore, a new ~~text~~ *IDE* editor must be built that deeply supports `The`, and users must customize their programming experience to make assumptions that they understand fluently
  - VCS is applied within the language, so that dichotamous branches turn into `The`-understood conditionals. Like having a runtime feature-flag for every branch, except at compile time. In `Rust` parlance, the closest equivalent to this would be an automatic `cargo` feature enabled for the current branch, which you could `#[cfg]` code based on.



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
