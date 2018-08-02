C application that copies a file. The application should
receive the source file path, target file path and buffer size (in bytes) as command line
arguments. By default, the application does not overwrite an existing file, unless the -f option
was specified.

Examples
$ ./ex1
Invalid number of arguments
Usage:
ex1 [-f] SOURCE DEST BUFFER_SIZE
$ ./ex1 /etc/passwd /tmp/passwd
Invalid number of arguments
Usage:
ex1 [-f] SOURCE DEST BUFFER_SIZE
$ ./ex1 /etc/passwd /tmp/passwd 4096
File /etc/passwd was copied to /tmp/passwd
$ ./ex1 /etc/passwd /tmp/passwd 4096
Unable to open destination file for writing: File exists
$ ./ex1 -f /etc/passwd /tmp/passwd 4096
File /etc/passwd was copied to /tmp/passwd
$ ./ex1 -f /tmp/passwd /etc/passwd 4096
Unable to open destination file for writing: Permission denied
$ ./ex1 /etc/password /tmp/passwd 4096
Unable to open source file for reading: No such file or directory
