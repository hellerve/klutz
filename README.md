# klutz

**Disclaimer: Proof-of-concept software! Probably does not work most of the time.**

klutz compiles zepto modules to Clojure namespaces.
Named `klutz` because `clotz` is not a pun.

## Usage

Don't. If you insist, you can call `zepto klutz.zp <input-file>`. This will
print the rendered Clojure namespace to the standard output, which you can
then redirect to a file and load with Clojure.

## To Do

- [ ] Small integers
- [ ] Complex numbers
- [ ] Byte vectors (currently compiled to `(into-array Byte/TYPE (map byte [<contents>]))`, but
      that is suboptimal - I think - and won't work if quoted)
- [ ] Standard library/Core function translation (as in, transforming the names of the functions
      in zepto's standard library to functions from `clojure.core`)

<hr/>

Have fun!
