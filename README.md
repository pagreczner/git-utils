## Some Utilities

### Git Extensions
Two git extenions that should make for easier adding of files to commit.

_Make sure you include these file in your PATH for them to be accesible._

#### git istatus
This method shows the modified files with an index next to their file location.  Works the same as `git status`.
__Usage__

```
> git istatus
Modified Files for Commit:
   1: src/my/file/one.java
   2: src/my/file/two.java
   3: src/my/three.java
   4: conf/main.conf
   5: README.md
```

#### git iadd
This method allows you to add by index (gotten from `git istatus`) the file associated at that index for commit. Works the same as `git add <file_name>`.

__Usage__

`git iadd <index>`

__Example__

```
> git istatus
Modified Files for Commit:
   1: src/my/file/one.java
   2: src/my/file/two.java
   3: src/my/three.java
   4: conf/main.conf
   5: README.md
   
# Add the file at index '2'
> git iadd 2

> git istatus
Modified Files for Commit:
   1: src/my/file/one.java
   2: src/my/three.java
   3: conf/main.conf
   4: README.md
   
# Add both files at index '2' and '4'
> git iadd 2,4
```
