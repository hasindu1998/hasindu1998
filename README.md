
<h1 align="center">Hi, I'm Hasindu Chanuka 👋</h1>

###

<h3 align="center">I'm an undergraduate IT student at SLIIT 👨‍💻, passionate about technology, software development, and creating innovative solutions. With a solid foundation in web development, including HTML, CSS, JavaScript, and PHP🌐<br> I’m continuously expanding my skills and working on exciting projects.<br><br>I'm always eager to learn new technologies and contribute to open-source projects, as well as collaborate on creative and impactful solutions.<br> <br>📂Check out my repositories to see what I'm working on!<br><br>Feel free to connect with me!</h3>

###

<div align="center">
  <a href="https://www.instagram.com/_.hasindu_98/" target="_blank">
    <img src="https://img.shields.io/static/v1?message=Instagram&logo=instagram&label=&color=E4405F&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="instagram logo"  />
  </a>
  <a href="https://www.linkedin.com/in/hasindu-chanuka-809a6a25b/" target="_blank">
    <img src="https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&label=&color=0077B5&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="linkedin logo"  />
  </a>
</div>

###

<div align="left">
  <img src="https://visitor-badge.laobi.icu/badge?page_id=hasindu1998.hasindu1998&"  />
</div>

###

<div align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="30" alt="javascript logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" height="30" alt="typescript logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" height="30" alt="react logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="30" alt="html5 logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" height="30" alt="css3 logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" height="30" alt="python logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/csharp/csharp-original.svg" height="30" alt="csharp logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg" height="30" alt="figma logo"  />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=ps" height="30" alt="adobephotoshop logo"  />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=ai" height="30" alt="adobeillustrator logo"  />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=mysql" height="30" alt="mysql logo"  />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=tailwind" height="30" alt="tailwindcss logo"  />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=bootstrap" height="30" alt="bootstrap logo"  />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=git" height="30" alt="git logo"  />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=github" height="30" alt="github logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg" height="30" alt="php logo"  />
</div>

###

<br clear="both">

<img src="https://raw.githubusercontent.com/hasindu1998/hasindu1998/output/snake.svg" alt="Snake animation" />

###

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=hasindu1998&hide_title=false&hide_rank=false&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=dracula&locale=en&hide_border=false" height="150" alt="stats graph"  />
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=hasindu1998&locale=en&hide_title=false&layout=compact&card_width=320&langs_count=5&theme=dracula&hide_border=false" height="150" alt="languages graph"  />
</div>

###
- 📫 How to reach me **chanukasankalpa456@gmail.com**

name: Generate snake animation

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"

  workflow_dispatch:

  push:
    branches:
    - master

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5

    steps:
      - name: generate snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: dist/snake.svg?palette=github-dark


      - name: push snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}


