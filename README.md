iln
===

interactive ln: ln with enhanced interactive mode and support for creation of backups

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
````

See [TODO.md](TODO.md) for the task list.
