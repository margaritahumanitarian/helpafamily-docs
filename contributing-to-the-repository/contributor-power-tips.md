---
description: Power tips for contributing to the project
---

# Contributor Power Tips

### Link Your PR to Your Issue

When you submit a PR, link it to the related issue. See [GitHub's instructions for manually linking PRs to issues](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue#manually-linking-a-pull-request-to-an-issue).

### Auto-Close Your Issue Via Commit Message

Put "Fixes \#123" or "Resolves \#456" into any commit message that's part of your PR. That will auto-close the related issue when the PR is merged. 

See [this StackOverflow answer](https://stackoverflow.com/a/23024034/271697) for more info.

### Minimize File Sizes

If your PR adds any graphics or other non-code files to the project, do your best to keep the files as small as possible. More info:

* [How SVG Optimization Can Help In Improving Website Speed?](https://imagekit.io/blog/svg-optimization-improves-website-speed/)
* [Weighing SVG Animation Techniques \(with Benchmarks\)](https://css-tricks.com/weighing-svg-animation-techniques-benchmarks/)
* [How to Optimize Images for Web and Performance](https://kinsta.com/blog/optimize-images-for-web/)

### Use Yarn to Install Packages

If you ever need to install a new dependency into the project, install it via `yarn add` instead of `npm install`. This will update the project's `package.json` and `yarn.lock` files.



