## Find a package containing a missing system file that software depends on
https://stackoverflow.com/a/23021454/1707636
> error while loading shared libraries: libXi.so.6: cannot open shared object file: No such file or directory
```shell
$ sudo apt-get install apt-file && apt-file update

$ apt-file search libXi.so.6
libxi6: /usr/lib/x86_64-linux-gnu/libXi.so.6
libxi6: /usr/lib/x86_64-linux-gnu/libXi.so.6.1.0
libxi6-dbg: /usr/lib/debug/usr/lib/x86_64-linux-gnu/libXi.so.6.1.0

$ sudo apt-get install libxi6
```
