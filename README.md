- 👋 Hi, I’m @prince. 
- 👀 
  I'm a passionate BTech CSE student eager to learn about the upcoming technologies and contribute to innovative projects. Feel free to connect with me on LinkedIn
<!---
param20h/param20h is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
![Paramjit's GitHub stats](https://github-readme-stats.vercel.app/api?username=param20h&show_icons=true&theme=radical)
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=param20h&layout=compact)
name: Update GFG Stats

on:
  schedule:
    - cron: '0 0 * * *'  # Runs daily at midnight
  workflow_dispatch:

jobs:
  update-readme:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Setup Python
        uses: actions/setup-python@v2
        with:
          python-version: '3.x'
      - name: Install Dependencies
        run: pip install beautifulsoup4 requests
      - name: Update README with GFG Stats
        run: python your_script.py  # Replace with your actual script name
      - name: Commit changes
        run: |
          git config --local user.email "action@github.com"
          git config --local user.name "GitHub Action"
          git add README.md
          git commit -m "Update GFG Stats"
          git push


[![Twitter](https://img.shields.io/twitter/follow/param20h?style=social)](https://twitter.com/param20h)
[![LinkedIn](https://img.shields.io/badge/-Paramjit%20Singh-blue?style=flat-square&logo=linkedin&logoColor=white&link=https://www.linkedin.com/in/param20h/)](https://www.linkedin.com/in/param20h/)
