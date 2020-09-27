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

* -l *seconds*

    use I<seconds> as the latency for fswatch (how long between batches of
    notifications). Default is 4.0. Larger values are useful when multiple
    sizeable files are changed as part of a single operation (eg saving
    binary files).

* -r *remote*

    use *remote* as the remote target to push to. Defaults to `origin`.

* -v

    be more verbose about file changes, even when they are ignored
