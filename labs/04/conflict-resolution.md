# Version Control Software
## What happened
I created a merge conflict by editing the same line(s) in `bio.md` on both `main` and the `feature-facts` branch.

## How I saw the conflict
When running `git merge feature-facts` on `main`, Git reported a conflict and paused the merge.

## How I resolved it
I opened `bio.md`, found the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`), and manually combined the changes into the final text. Then I removed the markers.

## Final outcome
I successfully merged the two branches.
