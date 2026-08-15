## p266 Release action

.github/scripts/bump.sh: Permission denied

### 1. Stage the changes
git add .

### 2. Set the executable permission for the shell script
git update-index --chmod=+x .github/scripts/bump.sh

### 3. Verify that the file mode is 100755
git ls-files --stage .github/scripts/bump.sh

### 4. Review the staged file mode change
git diff --cached --summary

### 5. Commit the changes
git commit -m "Fix release action"

### 6. Push the changes
git push

Important:
Do not run "git add ." again after step 2.
Otherwise, the file mode may be changed back to 100644 on Windows.