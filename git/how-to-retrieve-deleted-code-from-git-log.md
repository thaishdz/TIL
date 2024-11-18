
# TIL : It's not necessary to preserve the code by commenting it, because you can use `git log` to search for the piece of code you need.

### Example

You want to search a piece of code that called `PutCursorAt`

```sh
git log --oneline -G "PutCursorAt"
```

It very quickly spits out the commits that contain code that matches the `PutCursorAt` pattern (read more about `-G` option here):

```sh
> git log --oneline -G "PutCursorAt"

36ee67ec Use Write to drop PutCursorAt logic
ac07e7b3 Update cursor to follow moved down statement
79f1bb43 Update cursor to follow moved up statement
(END)

```
Narrowed down to 3 commits. Not bad. In fact, commit `36ee67ec` seems to be the one I was looking for.

>[!NOTE]
> `git log -G` is your way to find code across the whole git history of the project. The `--oneline` option is here to make the output slim and to the point.

#### Need to find the commit where we got rid of your “daily emails” feature? 

```sh
git log --oneline -G "daily-email"
```

#### Do you remember the name of the deleted file, but you are not sure where it was located?

```sh
git log --oneline -- **/dailyEmail.ts
```

👉 Click here for more : [Delete unused code 📰](https://understandlegacycode.com/blog/delete-unused-code/#how-to-retrieve-deleted-code-from-git-logs)
