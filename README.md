# Hi there 👋

# Visit https://github.com/lowlighter/metrics#-documentation for full reference
name: Metrics
on:
  # Schedule updates (each hour)
  schedule: [{cron: "0 * * * *"}]
  # Lines below let you run workflow manually and on each commit
  workflow_dispatch:
  push: {branches: ["master", "main"]}
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - uses: lowlighter/metrics@latest
        with:
          # Your GitHub token
          # The following scopes are required:
          #  - public_access (default scope)
          # The following additional scopes may be required:
          #  - read:org      (for organization related metrics)
          #  - read:user     (for user related data)
          #  - read:packages (for some packages related data)
          #  - repo          (optional, if you want to include private repositories)
          token: ${{ secrets.METRICS_TOKEN }}

          # Options
          user: fallingmeteorite
          template: classic
          base: header, activity, community, repositories, metadata
          config_timezone: Asia/Shanghai

  
<p align="center">
  <img width="300px" src="https://count.getloli.com/get/@fallingmeteorite?theme=rule34"></img>
  <img width="300px" src="https://github-readme-stats.vercel.app/api/top-langs/?username=fallingmeteorite&layout=compact"></img>
  <img width="300px" src="https://github-readme-stats.vercel.app/api?username=fallingmeteorite"></img>
</p>


🍓 **About Me**

- 🔭 Main use: Python，C++
- 📫 E-mail: 2327667836@qq.com
- 👯 About me: 摸鱼快乐~
- 🌐 Languages: English, 中文

[![Readme Card](https://github-readme-activity-graph.vercel.app/graph?username=fallingmeteorite&theme=react-dark)](https://github-readme-activity-graph.vercel.app)






