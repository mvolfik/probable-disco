This is a bug reproduction repo.

Install dependencies with `yarn`, then `yarn build`.

```
$ cat build/test/index.html
<meta http-equiv="refresh" content="0;url=/test/">
```

`yarn preview` apparently does something special, so the bug doesn't occur, but when you serve with `cd build/; python3 -m http.server` and visit `localhost:8000/test/`, you get infinite redirection loop.
