# configs
configs



/etc/init/[..].conf
# multibuilder daemon
description     "multibuilder daemon. Configurable server for building static files. Should NOT be used in production."

start on runlevel [2345]
stop on runlevel [!2345]

setuid nizhi
setgid morda

umask 0002

exec node /usr/share/multibuilder/main.js

respawn
respawn limit 15 15

console log
