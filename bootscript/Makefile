ETCDIR		:= /etc
EXTDIR		:= ${DESTDIR}${ETCDIR}
MODE		:= 754
DIRMODE		:= 755
CONFMODE	:= 644

install-bootscripts: create-dirs
	install -m ${CONFMODE} clfs/rc.d/init.d/functions ${EXTDIR}/rc.d/init.d/
	install -m ${MODE} clfs/rc.d/startup         ${EXTDIR}/rc.d/
	install -m ${MODE} clfs/rc.d/shutdown        ${EXTDIR}/rc.d/
	install -m ${MODE} clfs/rc.d/init.d/syslog   ${EXTDIR}/rc.d/init.d/
	ln -sf ../init.d/syslog ${EXTDIR}/rc.d/start/S05syslog
	ln -sf ../init.d/syslog ${EXTDIR}/rc.d/stop/K99syslog

all: install-bootscripts install-dropbear install-netplug

create-dirs:
	install -d -m ${DIRMODE} ${EXTDIR}/rc.d/init.d
	install -d -m ${DIRMODE} ${EXTDIR}/rc.d/start
	install -d -m ${DIRMODE} ${EXTDIR}/rc.d/stop

install-dropbear: create-dirs
	install -m ${MODE} clfs/rc.d/init.d/sshd   ${EXTDIR}/rc.d/init.d/
	ln -sf ../init.d/sshd ${EXTDIR}/rc.d/start/S30sshd
	ln -sf ../init.d/sshd ${EXTDIR}/rc.d/stop/K30sshd

install-netplug: create-dirs
	install -m ${MODE} clfs/rc.d/init.d/netplugd   ${EXTDIR}/rc.d/init.d/
	ln -sf ../init.d/netplugd ${EXTDIR}/rc.d/start/S10netplugd
	ln -sf ../init.d/netplugd ${EXTDIR}/rc.d/stop/K90netplugd

.PHONY: all create-dirs install-bootscripts install-dropbear install-netplug
