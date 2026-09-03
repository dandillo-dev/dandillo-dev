<div align="center">

### dandillo.exe

```diff
+ lofi_driver / Dandillo
+ Compiling dreams into reality... no errors yet.
+ Crafting things nobody asked for but somehow needed.
  status: probably building something weird...
  origin: third rock from the sun
  mood: rainy terminal sounds at 2:13 AM
```

**[terminal](https://dandillo.netlify.app/)** ‎ ‧ ‎ **[space](https://lofidriver.netlify.app/)**

</div>

## system_stats

<div align="center">

<img src="https://raw.githubusercontent.com/Dandillo/Dandillo/output/github-contribution-grid-snake-dark.svg" alt="contribution snake" />

</div>

<details>
<summary>snake widget setup (one-time)</summary>

Add `.github/workflows/snake.yml` in your `dandillo-dev/dandillo-dev` repo:

\`\`\`yaml
name: generate snake

on:
  schedule:
    - cron: "0 */6 * * *"
  workflow_dispatch:
  push:
    branches:
      - main

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
      - uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
\`\`\`

Swap `Dandillo` in the image path above if your repo/org name differs. The image won't render until this runs once.

</details>

