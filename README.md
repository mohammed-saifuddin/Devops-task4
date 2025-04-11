
# DevOps Project – Task 4: Version-Controlled DevOps Workflow

📌 Objective
To manage a DevOps project using Git and GitHub, following industry-standard version control practices including branching, pull requests, tagging, and documentation.


 🛠 Tools Used
- Git
- GitHub

 🌿 Branching Strategy

- main: Production-ready code  
- dev: Active development branch  
- feature/*: Feature-specific branches (e.g., feature/docker-setup)

All features should be developed in feature/* branches and merged via Pull Requests into dev, then from dev into main.

 📋 How to Contribute (Git Workflow)

Initialize repo
git init

First commit
echo "# DevOps Project" > README.md
git add .
git commit -m "Initial commit"

 Add remote and push to GitHub
git remote add origin https://github.com/<your-username>/devops-project.git
git branch -M main
git push -u origin main

 Create branches
git checkout -b dev
git push -u origin dev

git checkout -b feature/your-feature-name
 Make changes, then:
git add .
git commit -m "Add your feature"
git push -u origin feature/your-feature-name

 Merge via PR on GitHub
 After merging dev to main:
git checkout main
git pull origin dev
git push origin main

 Add .gitignore
echo "*.log" >> .gitignore
git add .gitignore
git commit -m "Add .gitignore"
git push

 Tag a version
git tag -a v1.0 -m "Initial release"
git push origin v1.0
 


🧾 Versioning

Git tags are used to track project releases:  
git tag -a v1.0 -m "Initial project setup"  
git push origin v1.0  


 📄 Documentation

All tasks and processes are documented inside the `documentation/` directory:
- featurestag.md: Task logs
- branching.md: Git flow explanation

