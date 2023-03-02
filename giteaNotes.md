### command to view:
https://cs.csis.work:4455



Steps:
1.) press fork button in gitea 
2.) Repository settings in top right corner add ssh key pub 
3.) git clone https://cs.csis.work:4455/luterw/Example.git
4.) git remote add upstream _gitea@cs.csis.work:OrgOne/Example.git
5.) git branch doc-branch
6.) git switch doc-branch
    git add . 
8.) git push --set-upstream origin doc-branch
9.) in gitea again.. 
10.) git pull upstream main
  11.) if merge conflicts, solve
12.)git pull upstream main
13.) 
