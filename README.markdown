# autocommit

Script to watch a git repository for changes, then commit and push them
automatically.

I use this to back up the notes I keep in [nvAlt][nv] (even
though I also sync them to [Simplenote][sn]).

[nv]: https://brettterpstra.com/projects/nvalt/
[sn]: https://simplenote.com


## Usage

    autogit [-h] [-b branch] [-r remote] [-s sleep] source_dir [repo_dir]

* `source_dir`

    the directory to watch

* `repo_dir`

    optional second directory to act as a git repository that `source_dir` is
    copied to if the source is not itself a git repository

* -h

    print help

* -b *branch*

    use *branch* as the remote branch to push to. Defaults to `main`.

* -r *remote*

    use *remote* as the remote target to push to. Defaults to `origin`.

* -s *seconds*

    sleep for *seconds* before trying to copy/commit. Defaults to 10.
    Set to 0 if not desired.

    Using this allows multiple changes happening in short succession to
    be bundled into one commit. For example, an application that changes
    multiple files as part of a save operation, but takes a few seconds
    before complete.
