name: Contribution Animation

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

permissions:
  contents: write

jobs:
  generate:
    runs-on: ubuntu-latest
    steps:
      - name: Generate contribution animation
        uses: Platane/snk@v3
        with:
          github_user_name: Chinmaysl29
          outputs: |
            dist/github-contribution-grid-snake.svg?color_snake=%23ff4fa3&color_dots=%230b0b0f%23251b25%235e2445%23b83270%23ff7abf

      - name: Publish animation
        uses: crazy-max/ghaction-github-pages@v4
        with:
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
