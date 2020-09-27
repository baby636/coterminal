<p align="center">
  <img src="https://raw.githubusercontent.com/relaxdiego/coterminal/main/logo.png">
</p>

<p align="center">
Share a terminal session with a co-worker.
</p>


Requirements
------------

I use this on Ubuntu. YMMV on other OS and distros.


Installation
------------

After cloning this repo, add its `bin/` subdirectory to your $PATH. For example:

```
export PATH=/path/to/this/repo's/bin:$PATH
```


Inviting Someone
----------------

If you want to give a co-worker access to your remote machine, SSH to it,
then run the following outside of any tmux or screen session:

```
coterminal-add <gh|lp>:<username>
```

Where gh stands for GitHub and lp stands for Launchpad and username is
your co-worker's username in GitHub or Launchpad. For example, if you
want to invite relaxdiego (GitHub) to your machine, run:

```
coterminal-add gh:relaxdiego
```


Afterwards, tell them to SSH to your machine via:

```
ssh <username>@<host>
```

Run `coterminal-add` multiple times if you want to add more co-workers
into the mix.


Read-only Mode
--------------

If you want to invite someone but only want them read-only access--That
is, they can't run commands on the shared terminal--just append `-r`:

```
coterminal-add gh:relaxdiego -r
```


Remove Someone
--------------

When you are done working with your co-workers, kick them out via:

```
coterminal-remove <username>
```
