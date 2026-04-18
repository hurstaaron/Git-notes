# git log --oneline
--  gives me the log of commits made locally regardless of push status
    Ex: 9465116 (HEAD -> main, origin/main, origin/HEAD) Initial commit
# git remote -v
--  points to the URL for fetching and pushing
# origin 
--  is the nickname my PC gives the GitHub copy of my repo
# git add .
-- packages changes made locally for push to GitHub (box packed but not ready to ship)
# git commit -m "message"
-- labels the changes (seals the box and puts the shipping label on it)
# git push
-- send the local changes to GitHub (the only command that talks to the internet)