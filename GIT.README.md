### Start de travail

```bash 
git checkout main
git pull origin main
git checkout -b R-20102025-customization
```
# ... work ...
```bash 
git add .
git commit -m "customization 1 application"
git push origin R-20102025-customization
```
# ... Once main is up-to-date and stable ...
```bash 
git checkout main
git branch -d R-20102025-customization # safe delete (refuse if unmerged)
git branch -D R-20102025-customization # force delete (use if you're sure)
git push origin --delete R-20102025-customization
git fetch -p
git branch
```
