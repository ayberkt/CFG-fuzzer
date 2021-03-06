# CFG-randomizer

This is an implementation of a CFG _randomizer_ in Haskell. It takes the
representation of a CFG and randomly generates strings that would be accepted by
the CFG. In [`palindromes/Main.hs`][palindromes] there is a sample grammar that generates arithmetic expression. To run this:

```
$ stack build
$ stack install
$ for i in `seq 1 20`; do arithmetic; done
4 - 8
8
4
5
1 * 2 * 4 + 1 - 1 * 2 * 4
2
8
1 - 10
3
7 + 3 + 7 + 7 + 3
8 + 10
3
5 + 10
7 * 8 + 7 * 7 * 8
6
2
1
1 - 7 * 10 + 7 + 10 + 10 + 7
1
1
```

The nice thing is that the CFG implementation does not work with just `String`s but with all `Monoid` instances.

[palindromes]: https://github.com/ayberkt/CFG-randomizer/blob/master/palindromes/Main.hs
