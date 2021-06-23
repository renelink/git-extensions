# git review extension

The git review extensions support you when you want to review code.

## git review-rebase

The `review-rebase` can be invoked with a commit id, branch, tag or any other ref. It does an interactive rebase in the background while setting all commits to `edit`. This causes git to stop at each commit. Thus you can take a look at the actual working directory and see what happened. Then it asks you if you want to continue or not. If you continue it continues the rebase and thus sets the working directory to the next commit.

The `review-rebase` is useful if you want to show someone how you implemented code or how you refactored it.

Example:

    $ git review-rebase 11032840
    Stopped at 92fdf7a2...  Moved classes to another package.
    Continue [Y/n]? y
    Stopped at b1f21430...  Extracted interfaces
    Continue [Y/n]? y
    Stopped at 5663aefc...  Replaced implementations
    Continue [Y/n]? y
    Stopped at 2aa94231...  Added tests.
    Continue [Y/n]? y