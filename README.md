Here we will define the syntax and semantics of `dpath`, which is
the path traversal format for [`dmap`](https://github.com/dapphub/dmap).

It describes the existing dpath definition as well as a future-proof
way of extending it. At the moment, this just means reserving all special
characters, but we will define some as private use area so you can start
experimenting with your own extensions right away.

Besides the two that are defined already, we list a few runes
for which we already have specific use cases.

```
dpath ::= step*
step  ::= rune name
rune  ::= ':' | '.'
name  ::= [a-z]
```

Definitions:

- `.` `dot`
- `:` `lock`

Reserved glyphs:

```
dquery:   !?@#$()
reserved: everything else
```
