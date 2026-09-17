GitFlow Setup – HelloApp

This project demonstrates a basic GitFlow workflow using Git and GitHub.

Workflow

main
 │
 ├── release/v1.0.0 → v1.0.0
 │
 └── hotfix/v1.0.1 → v1.0.1
          │
          └──→ develop

develop
 │
 └── feature/UC1-printHello

Commands Used

Setup

git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git clone <repository-url>
cd HelloApp
git flow init

Feature

git flow feature start UC1-printHello
git add .
git commit -m "feature(UC1): print message"
git flow feature finish UC1-printHello
git push origin develop

Release

git flow release start v1.0.0
git flow release finish v1.0.0
git push origin main
git push origin develop
git push origin --tags

Hotfix

git flow hotfix start v1.0.1
git add .
git commit -m "hotfix: critical fix"
git flow hotfix finish v1.0.1
git push origin main
git push origin develop
git push origin --tags

Verification

git status
git branch
git tag
git log --oneline --graph --all --decorate

Final Result

Feature UC1-printHello merged into develop

Release v1.0.0 created and merged into main

Hotfix v1.0.1 merged into main and develop

Tags v1.0.0 and v1.0.1 created

Feature, release, and hotfix branches deleted after finishing
