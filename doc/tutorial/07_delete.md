## Delete a backup

This tutorial will show you how to delete a backup from [**pgmoneta**](https://github.com/pgmoneta/pgmoneta).

### Preface

This tutorial assumes that you have an installation of PostgreSQL 13+ and [**pgmoneta**](https://github.com/pgmoneta/pgmoneta).

See [Install pgmoneta](https://github.com/pgmoneta/pgmoneta/blob/main/doc/tutorial/01_install.md)
for more detail.

### Delete the oldest backup

```
pgmoneta-cli -c pgmoneta.conf delete primary oldest
```

will delete the oldest backup on `[primary]`.

Note that currently delete will fail if the backup has an incremental backup child that depends on it.
We will support incremental backup deletion in later releases.

(`pgmoneta` user)
