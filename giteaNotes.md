### command to view:
https://cs.csis.work:4455



Steps:
<ul>
<li> press fork button in gitea </li>
<li> Repository settings in top right corner add ssh key pub </li>
<li> `git clone https://cs.csis.work:4455/luterw/Example.git`</li>
<li> `git remote add upstream _gitea@cs.csis.work:OrgOne/Example.git`</li>
<li> `git branch doc-branch`</li>
<li> `git switch doc-branch`</li>
    <li> `git add . `</li>
<li>`git commit `</li>
<li> `git push --set-upstream origin doc-branch`</li>
<li> in gitea again.. --pull request against orig repo</li>
<li> `git pull upstream main`</li>
  <li> if merge conflicts, solve -- not done PR</li>
    <li> `git pull upstream main --rebase` li>
    <li> merge conflicts -- already PR </li>
    <li> `git pull upstream main --rebase` </li>
    <li> fix the file</li>
    <li> git add </li>
    <li> git rebase -- continue </li>
    <li> git push --force (WE DONT NORMALLY WANT TO DO THIS BUT WORKING OUT OF SAME FILE) </li>
<li>git pull upstream main</li>
</ul>
