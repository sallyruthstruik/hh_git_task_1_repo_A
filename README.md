Список команд:

git clone https://github.com/sallyruthstruik/hh_git_task_1_repo_A.git
cd hh_git_task_1_repo_A/
echo "file_A" > file_A
echo "file_B" > file_B
git add .
git commit
git checkout -b branch1
git push --all
cd ..
git clone hh_git_task_1_repo_A hh_git_task_1_repo_B
cd hh_git_task_1_repo_B
echo "file_C" > file_C
git add file_C 
git commit
git push origin branch1 
cd hh_git_task_1_repo_B/
git remote add repo_A https://github.com/sallyruthstruik/hh_git_task_1_repo_A.git
git remote add repo_B https://github.com/sallyruthstruik/hh_git_task_1_repo_B.git
git push repo_A --all
cd ../hh_git_task_1_repo_A
git pull origin branch1 
echo "Modified C from repo A" >> file_C 
git commit -a
git push
cd ../
cd hh_git_task_1_repo_B
echo "Modified C from repo B" >> file_C
git commit -a
git pull repo_A 
subl file_C 
git add file_C 
git status
git commit
git push repo_A --all 
git push repo_B --all
cd ../hh_git_task_1_repo_A/
git remote add repo_B https://github.com/sallyruthstruik/hh_git_task_1_repo_B.git
git pull repo_B branch1

