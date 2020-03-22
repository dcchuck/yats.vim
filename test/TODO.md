Wrote test expecting it to fail in vader, but it passed!

Removed the following form typescript.vim
```
  if s:IsInMultilineComment(v:lnum, 1) && !s:IsLineComment(v:lnum, 1)
    return cindent(v:lnum)
  endif
```

The result? I still got the `* `, but it was not indented - so the syntax to create that must be elsewhere

* Why can we not get the tests to fail? My running the command manually (the vim opening with the vimrc), I do not see the comment triggering like I want it to

* Removing the cindent line does make the test fail
* For both typescriptreact and typescript...
