### command to view:
https://cs.csis.work:4455



Steps:
<ol>
<li> press fork button in gitea </li>
<li> Repository settings in top right corner add ssh key pub </li>
<li> git clone https://cs.csis.work:4455/luterw/Example.git</li>
<li> git remote add upstream _gitea@cs.csis.work:OrgOne/Example.git</li>
<li> git branch doc-branch</li>
<li> git switch doc-branch</li>
    git add . </li>
<li> git push --set-upstream origin doc-branch</li>
<li> in gitea again.. </li>
<li> git pull upstream main</li>
  <li> if merge conflicts, solve</li>
<li>git pull upstream main</li>
</ol>
