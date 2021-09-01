# Tmux

Note: Your custom prefix is `CTRL + a` and not the default `CTRL + b`.  
> CTRL + b is hard to hit and strains my fingers b/c of how far apart those keys are.

## Installation instructions for tmux-resurrection

tmux-resurrection helps save you tmux sessions.  
To use `prefix + CTRL - s` to save `prefix + CTRL - r` to restore.  
> prefix by default is CTRL + b  
> NOTE THAT YOUR prefix is CTRL + a

If you accidently saved over a session no worries.  
You can go to ~/.tmux/resurrect and recover the session.  
last is a symbolic link to the lastest session saved in a txt file.  
You can then delete the txt file that last points to.  
The run `ln -s <filename.txt> last` and tmux-resurrection will restore from that.

Go to [tmux-resurrect](https://github.com/tmux-plugins/tmux-resurrect)

```
git clone https://github.com/tmux-plugins/tmux-resurrect ~/clone/path
```

example

```
git clone https://github.com/tmux-plugins/tmux-resurrect ~/.config/tmux-resurrect
```

Add line to bottom of `.tmux.conf`.

```
run-shell ~/clone/path/resurrect.tmux
```

You already have this in .tmux so you can skip this step.
