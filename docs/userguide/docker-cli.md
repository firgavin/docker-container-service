#Docker CLI
Once you prepare your docker client as described in the user guide's [Quick Start](./user-guide.md##Quick Start) you can use the [Docker CLI](https://docs.docker.com/engine/reference/commandline/cli/). We support docker 1.10.3 and above. 


All the commands to manage your containers are supported. But they are limited to containers that belonging to the tenant specified in your config.json file.  For instance, ps will only list containers belonging to the specified tenant.

These docker cli commands are supported:

- attach
- create (see flag restrictions below)
- diff
- exec
- inspect
- kill
- logs
- network connect ?
- network create ?
- network disconnect ?
- network inspect ?
- network ls ?
- network rm ?
- pause
- port
- ps
- pull
- rename
- restart
- rm
- rmi
- run (see flag restrictions below)
- search
- start
- stats
- stop
- top
- unpause
- version
- volume create  (note: only the default driver is currently supported)
- volume inspect
- volume ls
- volume rm
- wait

These docker run flags are supported, but there may be some restrictions:

- a, attach
- d, detach
- e, env  (note affinity and constraints are suppoted) dock
- entrypint
- expose
- hostname
- help
- i, interactive
- l, label
- m (must be less than or equal to the default tenant quota)
- memory-reservation (must be less than or equal to the default tenant quota)
- memory-swap (must be less than or equal to the default tenant quota)
- memory-swappiness ?
- name
- net  ?
- oom-kill-disable ?
- P, publish-all
- p, --publish (external host port not allowed)
- restart ?
- rm
- stop-signal
- t, tty
- v, volume ((local host directory not allowed)
- volumes-from
- w, workdir

There docker run and create flags are not supported:

- add-hosts
- blkio-weight
- cpu-shares
- cap-add
- cap-drop
- cgroup-parent
- cidfile
- cpu-period
- cpu-quota
- cpuset-cpus
- cpuset-mems
- device
- disable-content-trust
- dns ?
- dns-opt ?
- dns-search ? 
- env-file ?
- group-add
- ipc
- kernel-memory
- label-file
- log-driver
- log-opt
- lxc-conf
- mac-address
- net ?
- oom-kill-disable
- pid
- privileged
- read-only
- restart ?
- security-opt
- sig-proxy
- u, user 
- ulimit
- uts



These docker cli commands are not supported:

- daemon
- buid
- commit
- cp
- events
- export
- history
- images
- import
- info
- load
- login
- logout
- network connect ?
- network create ?
- network disconnect ?
- network inspect ?
- network ls ?
- network rm ?
- push
- save
- tag