# Awesome Gitignore Templates

Create a file in your repository named .gitignore, Git uses it to determine which files and directories to ignore, before you make a commit. A .gitignore file should be committed into your repository, in order to share the ignore rules with any other users that clone the repository.

# Contents

-	[General Information](#general-information)
-	[Gitignore Pattern Format](#gitignore-pattern-format)
-	[Gitignore Files](#gitignore-files)
-	[Contribution](#contribution)
-	[License](#license)


## General Information

* [What is `.gitignore` file](https://help.github.com/articles/ignoring-files/)
* [Git - gitignore Documentation](https://git-scm.com/docs/gitignore)
* [How to create a gitignore file](https://help.github.com/articles/ignoring-files/)

## Gitignore Pattern Format

* A blank line matches no files, so it can serve as a separator for readability.
* A line starting with `#` serves as a comment.
* An optional prefix `!` which negates the pattern; any matching file excluded by a previous pattern will become included again. If a negated pattern matches, this will override lower precedence patterns sources.
* If the pattern ends with a slash, it is removed for the purpose of the following description, but it would only find a match with a directory. In other words, `foo/` will match a directory `foo` and paths underneath it, but will not match a regular file or a symbolic link `foo` (this is consistent with the way how pathspec works in general in git).
* If the pattern does not contain a slash `/`, git treats it as a shell glob pattern and checks for a match against the pathname relative to the location of the `.gitignore` file (relative to the toplevel of the work tree if not from a `.gitignore` file).
* Otherwise, git treats the pattern as a shell glob suitable for consumption by fnmatch(3) with the `FNM_PATHNAME` flag: wildcards in the pattern will not match a `/` in the pathname. For example, `Documentation/*.html` matches `Documentation/git.html` but not `Documentation/ppc/ppc.html` or `tools/perf/Documentation/perf.html`.
* A leading slash matches the beginning of the pathname. For example, `/*.c` matches `cat-file.c` but not `mozilla-sha1/sha1.c`.

## Gitignore Files
 

## Contribution

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request 😊 😇

## License
[CC0-1.0](/LICENSE)