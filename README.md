# Surf, a web browser

Forked from official https://surf.suckless.org.

This surf avoids key conflicts by command line instead of shortcuts.


## Thanks

- suckless.org e.V., München, Germany, who make softwares that suck less


## Usage

1. Open this surf as same as the official, like `surf your-url`.

2. Anytime browsing a webpage (including typing in input areas),

   type the leader key (`ctrl /` default) to invoke the command line.

   The leader key can be configed at compile-time now.

   A further patch is needed if you want to change it anytime.

3. Now you're on dmenu by default, enter a command,

   you should be back to step 2 then.


### Leader key

It is the first of `keys[]` in config.def.h:

```h
{ MODKEY, GDK_KEY_slash, spawn, SETPROP("_SURF_DO", "_SURF_DO") },
```

You can change `MODKEY` or `GDK_KEY_slash` as you like.

See developer.gnome.org/gdk3/stable/gdk3-Keyboard-Handling.html

Not used as a command below.


### Command format

usage: [mnemonic [arg]]

examples (`keys[]` in config.def.h):

- Do nothing: ` `
- Goto url: `g github.com`
- Find: `f some text on page`
- Find next: `n`
- Find last: `N`


## Used patches and tools

In terminal below have been 'patch < \*.diff'.

- surf.suckless.org/patches/unicode-in-dmenu


Below tools have been used.

- tools.suckless.org/x/sprop
