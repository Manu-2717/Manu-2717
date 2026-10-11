# Hey, I'm Meyank 👋

<img src="assets/hello.svg" alt="Meyank — building useful things with computer vision, AI, and open source" width="100%">

I build tools that make complicated workflows easier to use. Right now I'm learning computer vision in public through [Kornia](https://github.com/kornia/kornia), exploring Rust and PyO3 in [Kornia-rs](https://github.com/kornia/kornia-rs), and building my own AI and data tools.

[See my projects](#featured-projects) · [See my open source work](#open-source) · [Visit my portfolio](https://meyank-portfolio.vercel.app/)

## Featured projects

> ### 🔐 [DropVault](https://github.com/Manu-2717/Dropvault)
> **Save something now. Find it by meaning later.** A browser extension and local dashboard for capturing links, notes, and files, then searching them with embeddings. It also extracts text from images and PDFs.
>
> `React` · `FastAPI` · `PyTorch` · `Chrome extension` &nbsp; [Explore the code →](https://github.com/Manu-2717/Dropvault)

> ### 🧭 [CampusPilot](https://github.com/Manu-2717/CampusPilot)
> **Teach a browser task once; reuse the workflow.** CampusPilot navigates a college portal, saves the steps that worked, and repairs them when a selector goes stale.
>
> `React` · `TypeScript` · `FastAPI` · `SQLite` &nbsp; [Explore the code →](https://github.com/Manu-2717/CampusPilot)

> ### 🧩 [FlowWeaver](https://github.com/Manu-2717/flow-weaver)
> **Build data preparation pipelines visually.** A node canvas for cleaning, transforming, and inspecting datasets, with reusable processing nodes and execution feedback.
>
> `Python` · `FastAPI` · `React Flow` · `Polars` &nbsp; [Explore the code →](https://github.com/Manu-2717/flow-weaver)

<details>
<summary><strong>What I learned building these</strong></summary>

- **DropVault:** connecting a browser extension, a web app, and local semantic search into one workflow.
- **CampusPilot:** keeping browser automation repeatable by saving and validating each learned step.
- **FlowWeaver:** designing data tools around reusable operations and clear execution feedback.

</details>

## Open source

I've been working through real bugs in Kornia's augmentation code and learning how to turn a reproduction into a focused test and reviewable fix.

- **Merged:** [Align empty mask and image shapes](https://github.com/kornia/kornia/pull/5706) when an always-applied augmentation changes an empty batch's size.
- **Merged:** [Replace generic exceptions with specific errors](https://github.com/kornia/kornia/pull/5686) so callers can tell invalid inputs apart.
- **Open for review:** [Keep skipped augmentation inputs unchanged](https://github.com/kornia/kornia/pull/5732), including their gradients.

<details>
<summary><strong>What I'm exploring next</strong></summary>

I'm reading through Kornia-rs's Rust and Python bindings, especially how PyO3 turns Rust errors into useful Python exceptions. I'm also continuing to learn how computer vision libraries test numerical and edge-case behavior.

</details>

---

If one of these projects is useful to you, I'd like to hear about it. You can find more of my work on my [portfolio](https://meyank-portfolio.vercel.app/) or browse my [repositories](https://github.com/Manu-2717?tab=repositories).
