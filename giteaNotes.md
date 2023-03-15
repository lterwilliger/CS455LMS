### command to view:
https://cs.csis.work:4455



Steps:
<ul>
<li> press fork button in gitea </li>
<li> Repository settings in top right corner add ssh key pub </li>
<li> 
    
             git clone https://cs.csis.work:4455/luterw/Example.git
</li>
<li> 
    
             git remote add upstream _gitea@cs.csis.work:OrgOne/Example.git
</li>
<li> 
    
             git branch doc-branch`</li>
<li> 
    
             git switch doc-branch
</li>
Make your changes now then...
<li> 
    
             git add . 
</li>
<li>
    
             git commit 
</li>
<li> 
    
             git push --set-upstream origin doc-branch
</li>
in gitea again.. -- create pull request against orig repo
<li> 
    
             git pull upstream main
</li>
if merge conflicts, solve 

<li> 
    
             git pull upstream main --rebase
</li>
fix the file... 
<li> 
    
             git add <filename> 
</li>
<li> 
    
             git rebase --continue 
</li>
<li> 
    merge conflicts -- ONLY for already existing PR 
</li>
<li> 
    
             git push --force    (WE DONT NORMALLY WANT TO DO THIS BUT WORKING OUT OF SAME FILE) 
</li>
No PR -- do PR now
Fix main branch -- 
<li>
             git switch main
             git pull upstream main
</li>
</ul>
