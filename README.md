iln
===

interactive ln: ln with additional features and interactive mode

Key features
------------

- Allow creation of backups when overwriting, or backup the new link when not.
  This behaves similarly to how package managers treat config files.
- Allow moving the target to the source if the target exists but the source isn't.
- Enhanced interactive mode to prompt both for overwriting, and for
  move-and-link-back.
- Add argument to convert absolute symbolic link paths to relative.

Usage
-----

```
iln [-fsMibvh] [-L|-P] source_file target_file
iln [-fsMibvh] [-L|-P] source_file... target_dir

ln options: (from the Single Unix Specification version 4)
  -f  Force existing destination pathnames to be removed to allow the link.
  -s  Create symbolic links instead of hard links. If the -s option is specified,
      the -L and -P options shall be silently ignored.
  -L  For each source_file operand that names a file of type symbolic link,
      create a (hard) link to the file referenced by the symbolic link.
  -P  For each source_file operand that names a file of type symbolic link,
      create a (hard) link to the symbolic link itself.

iln options:
  -b  Create backups of files when overwriting (-f or -i specified). If neither
      -f nor -i are specified, create backups of the links to be created.
  -i  Interactive mode. If the destination exists, prompt to overwrite. If the
      target_file exists, but the source_file does not, prompt to move target_file
      to source_file and link it back. (The -i option overrides any previous -f or
      -M options.)
  -M  Default to moving and linking back when appropriate (analagous to -f. If -i
      and -M are specified, prompt for overwrite but not for move).
  -r  Convert absolute paths to relative paths when creating symbolic links.
  -v  Increase verbosity: display the work being done.
  -h  Show this help and usage information.
```

Installation
------------

Place the script somewhere in your PATH.

TODO
----

See [TODO.md](TODO.md).
