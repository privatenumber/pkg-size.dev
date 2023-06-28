<p align="center">
	<br>
	<img src=".github/logo.svg" width="400px">
	<br>
	<br>
</p>

This repository serves as a place to file bug reports and feature requests for [pkg-size.dev].

If you found the website useful, your donation/sponsorship would be greatly appreciated! Issues from sponsors will be prioritized for support.


Currently, the project is in early stages of development and closed-source. But it may be open-sourced here in the future.

## About

The goal of [pkg-size.dev] is to make it easier for curious developers like you to explore the npm ecosystem. It allows you to browse projects in your dependency tree, discover new packages, and learn about their creators. Ultimately, it aims to foster a greater appreciation for the npm ecosystem.

#### For package users, pkg-size.dev helps you:

- Uncover hidden dependencies and understand why they're installed.
- Maintain control over your `node_modules` by being mindful of what you're installing and its impact on size.
- Optimize web app performance by choosing smaller and optimized ESM packages.
- Compare and evaluate similar packages to identify the best fit for your specific needs.
- Discover the authors, developlment, and funding behind packages.

#### For package authors, pkg-size.dev helps you:
- Evaluate installation bottlenecks to improve speed. Particularly important for CLI tools loaded with npx.
- Ensure seamless downloads even in unideal conditions such as slow internet or low storage.
- Minimize dependencies to reduce risks like breaking changes or malicious code.


## FAQ

### Why care about package sizes?

Because they take up a lot of space on your disk. Even small packages can add up quickly. Try [calculating the total size of all the `node_modules`](https://stackoverflow.com/a/55928999/911407) on your disk.

When analyzing them, you may find some packages include unnecessary code and impact your app's performance.

> If you're interested in minimizing how much space `node_modules` consumes, check out [pnpm](https://pnpm.io). Not only do you regain a ton of disk space, it's also a huge DX improvement!

### What was this project inspired by?
Major thanks to [Package Phobia](https://packagephobia.com) & [Bundlephobia](https://bundlephobia.com).

I used to use both services often, but I always wished to see the their results on a single page. I also wanted more insights. For example: What dependencies do the packages install? And what are the bottlenecks?

I thought of making that tool serveral times but I was conflicted by the idea of server maintenance and costs, until I discovered [WebContainers](https://webcontainers.io).

### How does the website work?

This website operates entirely in your browser, from installing npm packages to bundling them.

At its core, the tool is built on [WebContainers](https://webcontainers.io)—a technology by [StackBlitz](https://stackblitz.com) that allows Node.js to run in-browser—, to run npm and install packages directly in your browser. It then analyzes the `node_modules` directory to gain insights into the installed packages and their stats. [esbuild WASM](https://esbuild.github.io/getting-started/#wasm) is used to bundle the package.

The website is static (doesn't require a backend) and hosted on Vercel.


[pkg-size.dev]: https://pkg-size.dev
