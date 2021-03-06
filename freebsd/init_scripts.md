# Notes on creating init scripts for FreeBSD.

## References
[System Startup](https://www.freebsd.org/doc/en/articles/linux-users/startup.html)
[Practical rc.d scripting](https://www.freebsd.org/doc/en/articles/rc-scripting/)
[FreeNAS jails - Starting installed software](http://doc.freenas.org/9.3/freenas_jails.html#starting-installed-software)


## Example: carbon-cache
```
#!/bin/sh
#
# $FreeBSD: releng/9.3/etc/rc.d/carbon-cache 263970 2014-03-31 14:39:56Z des $
#

# PROVIDE: carbon-cache
# REQUIRE: FILESYSTEMS
# KEYWORD: shutdown


name="carbon-cache"
rcvar="carbon-cache_enable"
prg="/usr/local/bin/carbon-cache.py"
pidfile="/var/run/carbon-cache.pid"
configfile="/usr/local/etc/carbon/carbon.conf"
cmd="$prg --config $configfile --pidfile $pidfile"

# /usr/local/bin/carbon-cache.py --config /usr/local/etc/carbon/carbon.conf --pidfile /var/run/carbon-cache.pid

. /etc/rc.subr

start() {
  $cmd start
}
stop(){
  $cmd stop
}

status(){
  $cmd status
}

case $1 in
  start)
        start
        ;;
  stop)
        stop
        ;;
  restart)
        stop
        start
        ;;
  status)
        status
        ;;
  *)
        echo "Usage: ${0} {start|stop|restart|status}"
esac

load_rc_config $name
# run_rc_command "$1"
```
