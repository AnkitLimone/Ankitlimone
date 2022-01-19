<h1 align="center"> Connect Me </h1>
<p align="center" style="display: flex;
justify-content: center; align-items: center;"> 
    <a href="https://github.com/AnkitLimone" target="_blank" style="font-size: 40px;
    display: flex;background-color: white; justify-content: center; align-items: center; width: 40px; height: 40px; border-radius: 5px;
    margin: 5px; text-decoration:none;">
        <img  src="./github-sign.png" width="90px" height="90px" />
    </a> 
    <a href="mailto:ankitlimone16@gmail.com" target="_blank"
    style="font-size: 40px;background-color: white; display: flex; justify-content: center; align-items: center; width: 60px; height: 60px; border-radius: 5px;text-decoration:none;margin: 5px;">
        <img  src="./google.png" width="90px" height="90px"/>
    </a>
    <a href="https://www.linkedin.com/in/ankit-limone-381206180?originalSubdomain=in" target="blank"
    style="font-size: 40px;background-color: white; display: flex; justify-content: center; align-items: center; width: 60px; height: 60px; border-radius: 5px;text-decoration:none;margin: 5px;">
        <img  src="./linkedin.png" width="90px" height="90px"/>
    </a>
    <a href="https://www.instagram.com/ak_demonimmortal/" target="_blank"
    style="font-size: 40px;background-color: white; display: flex; justify-content: center; align-items: center; width: 60px; height: 60px; border-radius: 5px;text-decoration:none;margin: 5px;">
        <img  src="./instagram.png" width="90px" height="90px"/>
    </a>
    <a href="https://api.whatsapp.com/send?phone=+917354193408" target="_blank"
    style="font-size: 40px;background-color: white; display: flex; justify-content: center; align-items: center; width: 60px; height: 60px; border-radius: 5px;text-decoration:none;margin: 5px;">
        <img  src="./whatsapp.png" width="90px" height="90px"/>
    </a>
<p]>
<br/>
    
    
    
<p>
    <img align="top" src="https://github-readme-stats.vercel.app/api/top-langs/?username=AnkitLimone&theme=radical&count_private=true&show_icons=true"
    alt="AnkitLimone"/>
        <img align="top" src="https://github-readme-stats.vercel.app/api?username=AnkitLimone&layout=compact&hide=html&theme=radical&count_private=true&show_icons=true"
    alt="AnkitLimone"/>
    </p>
    
    
    name: GitHub-Profile-3D-Contrib

on:
  schedule: # 03:00 JST == 18:00 UTC
    - cron: "0 18 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    name: generate-github-profile-3d-contrib
    steps:
      - uses: actions/checkout@v2
      - uses: Ankitlimone/github-profile-3d-contrib@0.4.0
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          USERNAME: ${{ github.repository_owner }}
      - name: Commit & Push
        run: |
          git config user.name github-actions
          git config user.email github-actions@github.com
          git add -A .
          git commit -m "generated"
          git push
