## Olá, me chamo Lucas

- 🌱 Estudando Desenvolvimento Web 2022
- 💬 Contate me no email: lucasetf@gmail.com


<div align="center">
  <a href="https://github.com/Lcourse">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=Lcourse&show_icons=true&theme=dark&include_all_commits=true&count_private=true"/>
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Lcourse&layout=compact&langs_count=7&theme=dark"/>
</div>

  <div style="display: inline_block"><br>
  <img align="center" alt="Lcourse-HTML" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">
  <img align="center" alt="Lcourse-CSS" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg">
</div>
  
##
  
  <div>
  <a href="https://www.instagram.com/ourcourse/" target="_blank"><img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
 </div>
  
 
name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: Lcourse
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
  
