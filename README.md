## Hi hi, I'm Mario 👋

<img alt="GitHub commit activity" src="https://img.shields.io/github/commit-activity/w/marioyeahdude/marioyeahdude">


:zap: ACTIVIDAD RECIENTE

name: Update README

on:
  schedule:
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    name: Update Profile README

    steps:
      - uses: actions/checkout@v4.2.2
      
      - uses: Readme-Workflows/recent-activity@v2.4.1
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
