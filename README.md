libcxx-pretty-printers
======================

GDB Pretty Printers for libc++ of Clang/LLVM

My .gdbinit
======================

```
$ cat ~/.gdbinit
set print pretty on
set print object on

handle SIGUSR1 nostop noprint
handle SIGUSR2 nostop noprint

set directories /home/davenger/src/ClickHouse

##################
# C++ pretty printers from https://github.com/koutheir/libcxx-pretty-printers
##################
python
import sys
sys.path.insert(0, '/home/davenger/src/libcxx-pretty-printers/src')
from libcxx.v1.printers import register_libcxx_printers
register_libcxx_printers (None)
end
```
