# `libcxx-pretty-printers`

GDB Pretty Printers for `libc++` of Clang/LLVM.

## Example `~/.gdbinit`

```shell
$ cat ~/.gdbinit
set print pretty on
set print object on

# libc++ pretty printers
# See: https://github.com/koutheir/libcxx-pretty-printers
python
import sys
sys.path.insert(0, '/home/koutheir/libcxx-pretty-printers/src')
from libcxx.v1.printers import register_libcxx_printers
register_libcxx_printers(None)
end
```
