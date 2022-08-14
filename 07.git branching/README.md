1. Create master and development branch with only readme file
2. Now based on the new requirement creating new feature from development branch.
3. checkout the feature branch and doing some changes to it and push the changes into the feature/f1 remote branch.
```
git checkout -b feature/f1 origin/feature/f1 
git add filename
git commit -m "f1 feature"
git push
```
4. Development team raise the pull request from origin/feature/f1 to development branch to merge the changes into the development branch.
5. After merging the code azure pipeline will start the build and deploy the changes into the test environment.
6. Testing team started test case execution in test environment.
7. Then the DevOps team creates a release branch (release/v1.0.1) from the development branch.
8. Testing team reported some bugs in newly deployed changes in test environment.
9. Dev team checkout (release/v1.0.1) branch locally and do the changes directrly into release branch.
10. when the changes pushed into remote release branch then dev team raise the pull request from release branch to development branch.
11. After merging the changes into development branch start the deployment from to test environment and point the development branch as a source.
12. Testing team started test case execution in test environment.
13. If no bugs reported, QA team provide the sign-off.
14. After sign-off raise the pull request from release branch (release/v1.0.1) to master branch.
15. And create tag after merging into master branch.
16. Finally start the deployment into production environment from master branch.
17. after the deployment into production environment if any bugs occured create hotfix branch from master and checkout hotfix branch
18. fix the changes into hotfix branch and merge the changes into master branch 
