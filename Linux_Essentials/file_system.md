# The Filesystem

Well, you can always distinguish file in two independent distinctions :
    - shareable vs unshareable
    - variable vs static.

"Shareable" files are those files that can be stored on one host and used on others as well. For example, the files in the user home directories are all shareable while device lock files aren't.

"Static" files are those files that doesn't change a lot unless "admin" intervenes, these files include binaries, libraries, documentations.


Here is an example of a FHS-compliant layout showing which parts of the filesystem are typically shareable and which are not:

| Type     | Shareable                      | Unshareable                    |
|----------|--------------------------------|--------------------------------|
| static   | `/usr`<br>`/opt`               | `/etc`<br>`/boot`              |
| variable | `/var/mail`<br>`/var/spool/news` | `/var/run`<br>`/var/lock`      |


