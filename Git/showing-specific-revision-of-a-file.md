---
title: Showing a Specific Revision Of a File
type: howto
---

To display the contents of a file at a given revision in Git, run the following command:

    $ git show <revision>:<filename>

For example, to view the version of "README.md” on the `dev` branch:

    $ git show dev:README.md

There is an alternative form of this command that will show the changes applied to that file as part of the commit:

    $ git show <revision> -- <filename>

This can be used alongside the log command to work out what happened to a file that was deleted.

First, view the history of the file.  You are interested in the ID before the commit that deleted the file: attempting to run `git show` using the deletion commit ID it will result in nothing being shown.

    $ git log -- file/that/was/deleted
    commit abc123
    Author: The Deleter <deleter@example.com>
    Date:   XXX
    
        Deleted this file.  Ha ha ha!
    
    commit beforeCommit
    Author: File Changer <changer@example.com>
    Date:   XXX
    
        Added a new file at file/that/was/deleted

Then, use `git show` to view the version before it was deleted:

    $ git show beforeCommit:file/that/was/deleted
