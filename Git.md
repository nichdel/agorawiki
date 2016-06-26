Changes made via the website are currently anonymous, which could be inconvenient for ensuring ratification. Additionally, it's difficult to automate changes through the web interface.

Therefore, it can be convenient to post changes directly to the github repository. Changes made to the repository are merged in every hour, and always preferred over changes made to the wiki in case of conflicts.

Before anything else, tell me (nichdel@gmail.com) your github information so I can add you as a submitter and your content goes directly in.

First you need a copy of the repo:

    git clone https://github.com/nichdel/agorawiki.git

Find the file(s) you want in the new repository and edit as you please. Then, to send your update we'll make sure we have the newest versions of everything except the files we've changed, then push our own business upstream. Note that you could be overwriting someone else's work if they've also updated these files.

    git add FILE_YOU_CHANGED
    git commit -m "DESCRIBE YOUR CHANGE HERE"
    git pull --no-edit -X ours
    git push https://NAME:PASSWORD@github.com/nichdel/agorawiki.git