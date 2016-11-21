# klutz

**Disclaimer: Proof-of-concept software! Probably does not work most of the time.
  It also depends on the bugfixes of the zepto standard module `compiler/ast` that
  will be in the upcoming version of zepto (`v0.9.7`, if you are reading from the future)**

klutz compiles zepto modules to Clojure namespaces.
Named `klutz` because `clotz` is not a pun.

## Usage

Don't. If you insist, you can call `zepto klutz.zp <input-file>`. This will
print the rendered Clojure namespace to the standard output, which you can
then redirect to a file and load with Clojure.

## To Do

- [ ] Complex numbers (using them throws an error for now)
- [ ] Byte vectors (currently compiled to `(into-array Byte/TYPE (map byte [<contents>]))`, but
      that is suboptimal - I think - and won't work if quoted)
- [ ] Small integers (currently compiled to `(long <number>)`, has the same problems as above; this
      is probably a theoretical problem, however, as regular zepto has no literals for these numbers)
- [ ] Standard library/Core function translation (as in, transforming the names of the functions
      in zepto's standard library to functions from `clojure.core` - there is already a minimal
      structure in `translations.zp`)

<hr/>

Have fun!
