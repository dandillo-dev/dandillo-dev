<div align="center">

<!-- Animated typing terminal — replaces the static whoami block -->
<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=18&duration=2800&pause=1400&color=A9B1D6&center=true&vCenter=true&width=600&height=140&lines=%E2%94%8C%E2%94%80%E2%94%80(lofi_driver%40nightshift)-%5B~%2Freality%5D;%E2%94%94%E2%94%80%24+whoami;lofi_driver;%E3%80%94+Dandillo+%E3%80%95;Compiling+dreams+into+reality...+no+errors+yet.;Crafting+things+nobody+asked+for+but+somehow+needed." alt="typing-svg" />

<br>

<!-- thin animated divider, monochrome, matches dark terminal palette -->
<img width="100%" height="4" src="https://capsule-render.vercel.app/api?type=rect&color=1a1b26&height=3&section=header" />

<br><br>

<!-- cycling status line -->
<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=14&duration=2600&pause=1200&color=6B7089&center=true&vCenter=true&width=520&lines=status%3A+probably+building+something+weird...;origin%3A+Third+Rock+from+the+Sun;mood%3A+rainy+terminal+sounds+at+2%3A13+AM;system%3A+idle+%7C+listening+to+lofi" alt="status-svg" />

<br><br>

<pre>~/access_points</pre>

<a href="https://dandillo.netlify.app/">terminal</a>
‎ ‎ ✦ ‎ ‎
<a href="https://lofidriver.netlify.app/">space</a>

<br><br>

<img width="100%" height="3" src="https://capsule-render.vercel.app/api?type=rect&color=1a1b26&height=3&section=header" />

</div>

<br>

## ~/system_stats

<div align="center">

<!-- single restrained widget: animated contribution snake, monochrome -->
<img src="https://raw.githubusercontent.com/Dandillo/Dandillo/output/github-contribution-grid-snake-dark.svg" alt="contribution snake" />

</div>

<sub align="center">

**setup note (one-time):** the snake needs a GitHub Action to generate itself — it isn't a drop-in image link like the typing SVGs above. Add this as `.github/workflows/snake.yml` in your `dandillo-dev/dandillo-dev` repo:

</sub>

```yaml
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
```

<div align="center">
<sub>after the action runs once, the image URL above will resolve — swap <code>Dandillo</code> in the raw.githubusercontent.com path if your repo/org name differs.</sub>
</div>

