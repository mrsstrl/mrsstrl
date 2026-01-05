<h1 align="center"> Hello! Servus! Salut! こんにちは!</h1>

![Kawaii Kitty](https://media.giphy.com/media/3kRa3yvntxlFm/giphy.gif)

![Keyboard Cat](https://media4.giphy.com/media/LHZyixOnHwDDy/giphy.gif?cid=ecf05e478w1sghr06tfu8ltnbxcaa41t71wv3sxi9lxxjmxu&ep=v1_gifs_search&rid=giphy.gif&ct=g)

![GitHub Streak](https://streak-stats.demolab.com/?user=mrsstrl)    

![GitHub stats](https://github-readme-stats.vercel.app/api?username=mrsstrl&show_icons=true&theme=ambient_gradient)

![Contributions](https://ssr-contributions-svg.vercel.app/_/mrsstrl?chart=3dbar&gap=0.6&scale=2&gradient=true&flatten=1&animation=wave&animation_duration=3&animation_delay=0.03&animation_amplitude=24&animation_frequency=0.1&animation_wave_center=19_3&format=svg&weeks=40)
  
![mrsstrl](https://count.getloli.com/get/@mrsstrl?theme=rule34)

name: Update Space Shooter Game

on:
  schedule:
    - cron: '0 0 * * *'  # Daily at midnight UTC
  workflow_dispatch:

permissions:
  contents: write

jobs:
  update-game:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: czl9707/gh-space-shooter@v1
        with:
          github-token: ${{ secrets.GITHUB_TOKEN }}
          output-path: 'game.gif'
          strategy: 'random'
