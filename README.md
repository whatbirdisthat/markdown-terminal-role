# markdown-terminal-role
Read markdown files on terminal using pandoc and lynx

Initially I was going to make this a fancy ansible (fancible) thingf.

Maybe I still will. For now, here's how a human can do it.

## Linux:

```bash
apt install pandoc lynx
```

## Mac

```bash
brew install pandoc lynx
```

> Then put this on the end of some file like `~/.bashrc` (or `~/.bash_profile` on your mac)

```bash
md() {
  pandoc $1 | lynx -stdin
}
```

Then either source your bashrc and you will have a new "builtin" (not really but yknow) called `md` which will take the first argument and try to load it up.

## FAQ

*Q* Shouldn't this be a *Gist* ?
*A* Yeah probably (but it *was* going to be an ansible thing so I could automate all the things)

*Q* Are you going to ansiblize this so you can automate all the things
*A* Yeah probably - unless you feel like PR'ing and **you** can do it!

*Q* Can I just steal all this and forget where I got it from?
*A* Feel free - I can't remember how I got it ... probably StackOverflow though, to be honest :)

