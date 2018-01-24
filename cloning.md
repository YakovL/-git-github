So if we found a nice repo and we want to get its contents we may go (in an appropriate folder):

    git init
    git remote add official https://github.com/cowboy/php-simple-proxy.git
    git pull official master

Now "official" is not a conventional name for a repo. Instead, usually one of the following names are used: `origin` or `upstream`.
The latter is a preferrable name when the repo is an actively updated central repo (not our fork). If it's our fork or we don't expect it
to get updated (a bold assumption) or we're not going to make any changes of our own (why limit ourselves?), naming it `origin` is fine.
Note that we're pulling only the `master` branch here while we may fetch all of them instead:

    git fetch --all
    git pull official master

There's a shortcut:

    git clone https://github.com/cowboy/php-simple-proxy.git

which names the repo `origin` and fetches all the branches.

Once we have pulled/cloned the repo, we may want to change something. It's always a good idea to create a separate branch for this:

    git checkout -b tweaking

and do stuff there.

Finally, if we want to make some pull requests via GitHub/(GitLab/..?), we should fork the repo there first, pull/clone our fork and
work with it. This can be done later, but to use name `origin` for it, we shouldn't use this name for the main repo (use `upstream`).
