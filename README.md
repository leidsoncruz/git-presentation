# Fixup command

In Git, the `fixup` and `squash` commands are used during an interactive rebase to combine or amend commits. The `fixup` command is specifically used to mark a commit as a fix for an earlier commit. Here's how you can use `git commit fixup`:

## Steps to Use `git commit fixup`:

1. Create a Regular Commit:

Make regular commits as you work on your changes.

```bash
git add <file>
git commit -m "Implement feature XYZ"
```

2. Create a Fixup Commit:

When you identify a commit that needs fixing, create a fixup commit using the `git commit fixup` command. This commit will be associated with the commit you want to fix.

```bash
git add <file>
git commit --fixup=<SHA-of-commit-to-fix>
```
Replace <SHA-of-commit-to-fix> with the SHA-1 hash of the commit that you want to fix.

3. Perform an Interactive Rebase:

Perform an interactive rebase to reorder, combine, or amend commits.

```bash
git rebase -i HEAD~n 
```
Replace n with the number of commits you want to include in the rebase or with the remote branch. An editor will open with a list of commits.

4. Auto-Squash Fixup Commits:
If you used `git commit --fixup`, Git recognizes these commits during the rebase. In the interactive rebase editor, you'll see lines like:

```bash
pick abc123 Commit message
fixup def456 Fixup! Commit message
```
Save and exit the editor.

5. Complete the Rebase:

After saving the changes, Git will apply the rebase, combining the fixup commit with the original commit. If there are no conflicts, the rebase will complete.

## Challenge

The openapi file has two errors. These errors are crashing our application and our clients. 

- The status code of the creation response is wrong. It should be 201 instead of 200.

```bash
+++ b/openapi.json
@@ -27,7 +27,7 @@
           }
         },
         "responses": {
-          "200": {
+          "201": {
             "description": "User created successfully"
           }
         }
```
- The status code of the error response for getting a user is wrong. It should be 404 instead of 500.

```bash
@@ -60,7 +60,7 @@
               }
             }
           },
-          "500": {
+          "404": {
             "description": "User not found",
             "content": {
               "application/json": {
```

Use the fixup command to fix the incorrect commit.
