# command

tar

---

## Description

- The Linux ‘**tar**’ stands for tape archive.
- It is used to create archive and extract the archive files.
- `tar` command in Linux is one of the important command which provides archiving functionality in Linux.
- We can use Linux tar command to create compressed or uncompressed archive files and also maintain and modify them.

---

## Syntax

```bash
$ tar [options] [archive-file] [file or directory to be archived]
```

---

## Options/Flags

- ### -cvf

  Creating an uncompressed tar archive using option `-cvf`. This command creates a tar file called _file.tar_ which is the archive of all _.c_ files in current directory.

  ```bash
  $ tar cvf file.tar *.c
  ```

- ### -xvf
  Extracting files from archive using option `-xvf`. This command extracts files from archives.
  ```bash
  $ tar xvf file.tar
  ```
- ### -z

  gzip compression on the tar archive, using option `-z`. This command creates a tar file called _file.tar.gz_ which is the archive of _.c_ files.

  ```bash
  $ tar -zcvf file.tar.gz *.c
  ```

  Extracting a gzip tar archive _\*.tar.gz_ using option `-xvzf`. This command extracts files from tar archived _file.tar.gz_ files.

  ```bash
  $ tar -zxvf file.tar.gz
  ```

- ### -j

  Creating compressed tar archive file in Linux using option `-j`. This command compresses and creates archive file less than the size of the gzip. Both compress and decompress takes more time than gzip.

  ```bash
  $ tar cvfj file.tar.tbz example.cpp
  ```

- ### -C
  Untar single tar file or specified directory in Linux. This command will Untar a file in current directory or in a specified directory using `-C` option.
  ```bash
  $ tar xvfj file.tar -C [path of file in directoy]
  ```
- ### -c
  Check size of existing _tar_, _tar.gz_, _tar.tbz_ file in Linux. The above command will display the size of archive file in Kilobytes(KB).
  ```bash
  $ tar czf file.tar | wc -c
  ```

---

## Exit Status

- **0** (EXIT_SUCCESS): The operation completed successfully without any errors.
- **1** (EXIT_FAILURE): General error, indicating some unspecified problem with the tar command.
- **2**: Fatal error. This might indicate issues like incorrect command-line options, improper usage, or inability to access the archive or files.
- **4**: Warning exit code. This might indicate issues like some files changed while tar was archiving them.
- **6**: archive extraction error. It might occur if there are issues during the extraction process, such as insufficient permissions, corrupted archives, or unrecognized archive formats.
- **8**: Inconsistent archive errors. This could occur when the archive is found to be inconsistent or corrupted.

---

## Author

- John Gilmore
- some other contributors as part of the GNU project.

---

## Copyright

BSD tar: BSD-2-Clause <br>
GNU tar: GPL-3.0-or-later <br>
pdtar: Public domain<br>
Plan 9: MIT<br>
star: CDDL-1.0

---
    
