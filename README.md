# xbar-low-power-mode-tool
A quick xbar tool to better manage Low Power Mode on Mac books.

## What's xbar?

[This is xbar!](https://xbarapp.com/)

## Important installation note

This tool makes use of the `pmset` command, which needs to be called with `sudo`. `sudo` commands require the user to enter a password, which is a problem for automated bash scripts. 

So, you need to alter your sudo config such that you don't need to enter a password for `sudo pmset` commands. You do that by editing your `sudoers` file by calling `sudo visudo` (which will edit that file with vim and check for mistakes to make sure you don't mess the config up).

You want to add a line like this to your sudoers file.

```
yourusername ALL = (ALL) NOPASSWD: /usr/bin/pmset
```

For more info on this:

- https://www.garron.me/en/linux/visudo-command-sudoers-file-sudo-default-editor.html
- https://www.unixtutorial.org/how-to-use-visudo/
- https://www.sudo.ws/docs/man/1.8.13/visudo.man
