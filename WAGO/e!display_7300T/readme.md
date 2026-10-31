#About 
user / pass : user user  

user is not root, but permissions are such that user could become root.  
In my case, the device was requesting an ip over DHCP 
in the 192.168.77.X range.

#ssh
$ ssh user@192.168.77.176
Unable to negotiate with 192.168.77.176 port 22: no matching host key type found. Their offer: ssh-rsa,ssh-dss
$ ssh -o HostKeyAlgorithms=+ssh-rsa user@192.168.77.176


--> IN! evidently was at a factory reset. prompted to reset password on login.

Linux 3.6 kernel  
32-bit ARMv7 with NEON and VFPv3   
RAM ~512MB 
disk: ~2GB, 500MB root, ~1GB on fs_data

micro sd slot, 2 ethernet, 2 USB A, usb micro serice port  



<pre>
user@192.168.77.176's password: 
setterm: xterm-256color: unknown terminal type


WAGO Linux Terminal on e!DISPLAY-408A70.


Security message: please change your password!

Changing password for user
Old password: 
New password: 
Retype password: 
Password for user changed by user
user@e!DISPLAY-408A70:~ ls
logo.png
user@e!DISPLAY-408A70:~ w
-bash: w: command not found
user@e!DISPLAY-408A70:~ uname -a
Linux e!DISPLAY-408A70 3.6.11-psp2x-01.02.17_00-rt30 #1 Mon Nov 30 07:32:51 UTC 2015 armv7l GNU/Linux
user@e!DISPLAY-408A70:~ cat /etc/os-release 
NAME=PTXdist
VERSION="2013.03.0"
ID=ptxdist
VERSION_ID="2013.03.0"
PRETTY_NAME="PTXdist / WAGO-IO-IPC"
ANSI_COLOR="1;34"

PTXDIST_VERSION="2013.03.0"
PTXDIST_BSP_VENDOR="WAGO"
PTXDIST_BSP_NAME="IO-IPC"
PTXDIST_BSP_VERSION="IO-IPC-trunk"
PTXDIST_PLATFORM_NAME="perspecto-2"
PTXDIST_PLATFORM_VERSION="-trunk"
PTXDIST_BUILD_DATE="2015-12-14T11:24:59+0000"
user@e!DISPLAY-408A70:~ cat /proc/cpuinfo                                                                                         
Processor	: ARMv7 Processor rev 7 (v7l)
BogoMIPS	: 333.92
Features	: swp half thumb fastmult vfp edsp neon vfpv3 tls 
CPU implementer	: 0x41
CPU architecture: 7
CPU variant	: 0x1
CPU part	: 0xc08
CPU revision	: 7

Hardware	: MACH_PFC200_PERSPECTO_II
Revision	: 0020
Serial		: 0000000000000000
user@e!DISPLAY-408A70:~ free -m
             total         used         free       shared      buffers
Mem:        507176       114924       392252            0            0
-/+ buffers:             114924       392252
Swap:            0            0            0
user@e!DISPLAY-408A70:~ df -h 
Filesystem                Size      Used Available Use% Mounted on
ubi0:ubi_rootfs1        403.1M    112.6M    290.5M  28% /
devtmpfs                247.6M         0    247.6M   0% /dev
none                    247.6M      5.6M    242.0M   2% /tmp
none                    247.6M         0    247.6M   0% /media
none                      4.0M     88.0K      3.9M   2% /var/log
none                    247.6M     32.0K    247.6M   0% /var/run
none                    247.6M         0    247.6M   0% /var/lock
none                    247.6M         0    247.6M   0% /var/tmp
tmpfs                   247.6M         0    247.6M   0% /dev
/dev/ubi0_3              58.4M     28.0K     58.4M   0% /home
user@e!DISPLAY-408A70:~ sudo -l
User user may run the following commands on this host:
    (root) NOPASSWD: /sbin/ifup, (root) /sbin/ifdown, (root) /bin/date, (root) /sbin/hwclock, (root) /usr/bin/sed, (root)
    /etc/init.d/keymap, (root) /usr/sbin/setreset, (root) /bin/kill, (root) /sbin/bootpc, (root) /sbin/bootpc-startup, (root)
    /sbin/route, (root) /sbin/ifconfig, (root) /bin/ip, (root) /usr/sbin/ntpclient, (root) /usr/sbin/cp_cfcard, (root)
    /usr/sbin/update_boot, (root) /usr/sbin/update_mbr_grub, (root) /usr/sbin/update_fw, (root) /usr/sbin/create_home_int, (root)
    /usr/sbin/sfdisk, (root) /sbin/mke2fs, (root) /usr/sbin/telnetd, (root) /sbin/utelnetd, (root) /usr/sbin/pure-ftpd, (root)
    /sbin/e2fsck, (root) /usr/sbin/loadkbushex, (root) /usr/sbin/loadkbushex.sh, (root) /usr/sbin/ethtool, (root)
    /etc/config-tools/start_reboot, (root) /usr/bin/ipkg, (root) /etc/config-tools/firmware_backup, (root)
    /etc/config-tools/firmware_restore, (root) /bin/rm, (root) /etc/config-tools/change_bootflag, (root)
    /etc/config-tools/get_device_data, (root) /etc/config-tools/config_snmp, (root) /etc/config-tools/fat_format, (root)
    /etc/config-tools/switch_bootloader, (root) /etc/config-tools/config_interfaces, (root) /etc/config-tools/change_hostname,
    (root) /etc/config-tools/config_default_gateway, (root) /etc/config-tools/edit_dns_server, (root)
    /etc/config-tools/config_port, (root) /etc/config-tools/change_rts_config, (root) /etc/config-tools/copy_firmware_image,
    (root) /etc/config-tools/config_RS232, (root) /etc/config-tools/filesystem_check, (root) /etc/config-tools/restart_webserver,
    (root) /etc/config-tools/change_video_mode, (root) /etc/config-tools/config_mousepointer, (root)
    /etc/config-tools/config_touchscreen, (root) /etc/config-tools/change_keyboard_layout, (root)
    /etc/config-tools/change_screen_state, (root) /etc/config-tools/config_clock_display_mode, (root)
    /etc/config-tools/config_sntp, (root) /etc/config-tools/config_webserver, (root) /etc/config-tools/get_wbm_diaglist, (root)
    /etc/config-tools/pbdp_config, (root) /etc/config-tools/config_tftp, (root) /etc/config-tools/config_ssh, (root)
    /etc/config-tools/get_typelabel_value, (root) /etc/config-tools/config_ethernet, (root)
    /etc/config-tools/get_run_stop_switch_value, (root) /etc/config-tools/get_coupler_details, (root)
    /etc/config-tools/config_linux_user, (root) /etc/config-tools/get_user_info, (root) /etc/config-tools/set_dsa_mode, (root)
    /etc/config-tools/get_firmware_restore_packages, (root) /etc/config-tools/config_plc, (root) /etc/config-tools/config_clock,
    (root) /etc/config-tools/firewall, (root) /etc/config-tools/get_filesystem_data, (root) /etc/config-tools/modbus_config,
    (root) /etc/config-tools/config_switch
user@e!DISPLAY-408A70:~ cat /proc/mtd                                                                                             
dev:    size   erasesize  name
mtd0: 00400000 00020000 "raw_linux1"
mtd1: 00400000 00020000 "raw_linux2"
mtd2: 3cd40000 00020000 "fs_data"
user@e!DISPLAY-408A70:~ ls -l /lib/libc* /lib/ld*
-rwxr-xr-x    1 root     root        130228 Dec 14  2015 /lib/ld-2.16.so
lrwxrwxrwx    1 root     root            10 Dec 14  2015 /lib/ld-linux.so.3 -> ld-2.16.so
-rwxr-xr-x    1 root     root       1184912 Dec 14  2015 /lib/libc-2.16.so
-rwxr-xr-x    1 root     root         30172 Dec 14  2015 /lib/libcrypt-2.16.so
lrwxrwxrwx    1 root     root            16 Dec 14  2015 /lib/libcrypt.so.1 -> libcrypt-2.16.so
lrwxrwxrwx    1 root     root            12 Dec 14  2015 /lib/libc.so.6 -> libc-2.16.so
user@e!DISPLAY-408A70:~ ps aux 
USER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root         1  0.1  0.1   2600   632 ?        Ss   07:08   0:06 init      
root         2  0.0  0.0      0     0 ?        S    07:08   0:00 [kthreadd]
root         3  0.0  0.0      0     0 ?        S    07:08   0:00 [ksoftirqd/0]
root         5  0.0  0.0      0     0 ?        S<   07:08   0:00 [kworker/0:0H]
root         6  0.0  0.0      0     0 ?        S    07:08   0:00 [kworker/u:0]
root         7  0.0  0.0      0     0 ?        S<   07:08   0:00 [kworker/u:0H]
root         8  0.0  0.0      0     0 ?        S<   07:08   0:00 [khelper]
root         9  0.0  0.0      0     0 ?        S    07:08   0:00 [kdevtmpfs]
root        10  0.0  0.0      0     0 ?        S    07:08   0:00 [kworker/u:1]
root        28  1.7  0.0      0     0 ?        S    07:08   0:57 [kworker/0:1]
root       263  0.0  0.0      0     0 ?        S    07:08   0:00 [bdi-default]
root       265  0.0  0.0      0     0 ?        S<   07:08   0:00 [kblockd]
root       409  0.0  0.0      0     0 ?        S    07:08   0:00 [khubd]
root       528  0.0  0.0      0     0 ?        S<   07:08   0:00 [rpciod]
root       536  0.0  0.0      0     0 ?        S    07:08   0:00 [khungtaskd]
root       537  0.0  0.0      0     0 ?        S    07:08   0:00 [kswapd0]
root       538  0.0  0.0      0     0 ?        S    07:08   0:00 [fsnotify_mark]
root       539  0.0  0.0      0     0 ?        S<   07:08   0:00 [nfsiod]
root       543  0.0  0.0      0     0 ?        S<   07:08   0:00 [crypto]
root      1095  0.0  0.0      0     0 ?        S<   07:08   0:00 [OMAP UART1]
root      1097  0.0  0.0      0     0 ?        S<   07:08   0:00 [OMAP UART2]
root      1099  0.0  0.0      0     0 ?        S<   07:08   0:00 [OMAP UART3]
root      1176  0.0  0.0      0     0 ?        S    07:08   0:00 [ubi_bgt0d]
root      1180  0.0  0.0      0     0 ?        S    07:08   0:00 [spi1]
root      1183  0.0  0.0      0     0 ?        S    07:08   0:00 [spi2]
root      1185  0.0  0.0      0     0 ?        S    07:08   0:00 [spi3]
root      1187  0.0  0.0      0     0 ?        S    07:08   0:00 [spi4]
root      1223  0.0  0.0      0     0 ?        S    07:08   0:00 [irq/125-ads7846]
root      1242  0.0  0.0      0     0 ?        S    07:08   0:00 [irq/194-mmc0]
root      1272  0.0  0.0      0     0 ?        S<   07:08   0:00 [deferwq]
root      1276  0.0  0.0      0     0 ?        S    07:08   0:00 [kworker/gpiokey]
root      1293  0.0  0.0      0     0 ?        S    07:08   0:00 [ubifs_bgt0_0]
root      1325  0.0  0.1   2040   872 ?        Ss   07:08   0:01 /sbin/udevd --daemon --debug
root      1387  0.0  0.1   2036   660 ?        S    07:08   0:00 /sbin/udevd --daemon --debug
root      1392  0.0  0.1   2036   644 ?        S    07:08   0:00 /sbin/udevd --daemon --debug
root      1401  0.0  0.0      0     0 ?        S    07:08   0:00 [flush-ubifs_0_0]
root      1496  0.0  0.1   2600   596 ?        Ss   07:08   0:00 /usr/sbin/crond
www       1531  0.0  0.3   5120  1728 ?        S    07:08   0:02 /usr/sbin/lighttpd -f /etc/lighttpd/lighttpd.conf
www       1533  0.0  0.4   9168  2380 ?        Ss   07:08   0:00 /usr/bin/php-cgi
www       1538  0.0  0.4   9168  2380 ?        Ss   07:08   0:00 /usr/bin/php-cgi
root      1543  0.0  0.1   3668   556 ?        S    07:08   0:00 supervising syslog-ng
root      1544  0.0  0.3   4224  1860 ?        Ss   07:08   0:01 /sbin/syslog-ng
www       1545  0.0  0.5   9680  2748 ?        S    07:08   0:00 /usr/bin/php-cgi
www       1546  0.0  0.2   9168  1020 ?        S    07:08   0:00 /usr/bin/php-cgi
root      1549  0.0  0.0   2600   396 ?        Ss   07:08   0:00 /usr/sbin/inetd
103       1566  0.0  0.1   2376   808 ?        Ss   07:08   0:00 /usr/bin/dbus-daemon --system
root      1590  0.0  0.0   2100   500 ?        Ss   07:08   0:00 /usr/sbin/dropbear -p 22 -m
root      1621  0.0  0.4   8360  2336 ?        Sl   07:08   0:00 /bin/ledserverd
root      1629  0.0  0.3   6904  1572 ?        S    07:08   0:00 /usr/bin/logforward
root      1644  0.0  0.5   4856  2876 ?        Ss   07:08   0:01 /usr/sbin/ipwatchd -c /etc/ipwatchd.conf
root      1652  0.0  0.0      0     0 ?        S    07:08   0:00 [ubifs_bgt0_3]
root      1659  0.0  0.0   1620   372 ?        Ss   07:08   0:00 /usr/bin/tempd
root      1692  0.0  0.0      0     0 ?        S    07:09   0:02 [irq/190-si1142]
root      1698  0.0  0.0      0     0 ?        S    07:09   0:00 [irq/272-qt1070]
root      1736  0.0  0.2   2604  1116 ?        S    07:09   0:00 /bin/sh /usr/bin/startx -- -nocursor
root      1737  0.0  0.1   2604   660 ttyO2    Ss+  07:09   0:00 /sbin/getty -L 115200 ttyO2 xterm
root      1738  0.0  0.1   2924   760 ?        S    07:09   0:00 xinit /usr/bin/pekwm -- /usr/bin/X :0 -nolisten tcp -nocursor
root      1739  0.1  1.4  15680  7192 tty2     S<s+ 07:09   0:06 /usr/bin/X :0 -nolisten tcp -nocursor
root      1742  0.0  0.6   6548  3264 ?        S    07:09   0:00 /usr/bin/pekwm
root      1755  0.0  0.2  21372  1044 ?        Sl   07:09   0:00 statemonitor
root      1771  1.2 11.4 153636 57872 ?        Sl   07:09   0:40 /usr/bin/webkit_browser -cache http://127.0.0.1/app
root      1775  0.0  0.0   1524   268 ?        Ss   07:09   0:00 poll_gpio_keys
root      1776  0.0  0.1  20504   832 ?        Sl   07:09   0:02 brightness_control
root      1876  0.0  0.0   2600   412 ?        Ss   07:21   0:00 /sbin/udhcpc -i br0 -h e!DISPLAY-408A70 -V 762-3000 -p /var/run/ud
root      1904  0.0  0.1   2180   872 ?        Ss   07:34   0:00 /usr/sbin/dropbear -p 22 -m
user      1905  0.0  0.3   4888  1668 pts/0    Ss   07:34   0:00 -bash
root      1949  0.0  0.0      0     0 ?        S    07:49   0:00 [kworker/0:2]
root      2005  0.1  0.0      0     0 ?        S    08:00   0:00 [kworker/0:0]
user      2012  0.0  0.2   4204  1088 pts/0    R+   08:03   0:00 ps aux
user@e!DISPLAY-408A70:~ top
'xterm-256color': unknown terminal type.
user@e!DISPLAY-408A70:~ htop
Error opening terminal: xterm-256color.
user@e!DISPLAY-408A70:~ top 
'xterm-256color': unknown terminal type.
user@e!DISPLAY-408A70:~ lshw
-bash: lshw: command not found
user@e!DISPLAY-408A70:~ ps w
  PID TTY      STAT   TIME COMMAND
 1905 pts/0    Ss     0:00 -bash
 2021 pts/0    R+     0:00 ps w
user@e!DISPLAY-408A70:~ ls -ld /etc/*http* /etc/*nginx* /etc/*lighttpd* /etc/*boa* \
 >  /var/www /srv/www /www /home/* 2>/dev/null
drwxr-xr-x    2 root     root          1216 Dec 30  2016 /etc/lighttpd
drwxr-xr-x    2 root     root          1216 Dec 30  2016 /etc/lighttpd
drwxr--r--    2 admin    admin          232 Dec 14  2015 /home/admin
-rwxr-xr-x    1 root     root           802 Dec 14  2015 /home/index.html
drwx------    2 root     root           232 Aug 15  2016 /home/log
drwxr--r--    3 user     user           368 Apr  8 08:03 /home/user
-rwxr-xr-x    1 root     root           270 Dec 14  2015 /home/webview_style.css
drwxr-xr-x    5 root     root           488 Dec 14  2015 /var/www
user@e!DISPLAY-408A70:~ cat /etc/inittab
#
# /etc/inittab
#

# devkit-ti-am3517-pac200

console::sysinit:/etc/init.d/rcS
console::respawn:/sbin/getty -L 115200 ttyO2 xterm

# Stuff to do before rebooting
#::ctrlaltdel:/sbin/reboot
#::shutdown:/bin/umount -a -r
::shutdown:/etc/init.d/shutdown


user@e!DISPLAY-408A70:~ ls -l /etc/init.d/
-rwxr-xr-x    1 root     root           193 Dec 14  2015 auto_firmware_restore
-rwxr-xr-x    1 root     root          1779 Dec 14  2015 basyskom
-rwxr-xr-x    1 root     root          2061 Dec 14  2015 cpsd2intern
-rwxr-xr-x    1 root     root            96 Dec 14  2015 crond
-rwxr-xr-x    1 root     root          1637 Dec 14  2015 dbus
-rwxr-xr-x    1 root     root           181 Dec 14  2015 determine_hostname
-rwxr-xr-x    1 root     root          3188 Dec 14  2015 dropbear
-rwxr-xr-x    1 root     root           853 Dec 14  2015 finalize_root
-rwx------    1 root     root          2208 Dec 14  2015 firewall
-rwxr-xr-x    1 root     root          1258 Dec 14  2015 inetd
-rwxr-xr-x    1 root     root          2984 Dec 14  2015 ipwatchd
-rwxr-xr-x    1 root     root           558 Dec 14  2015 ledserver
-rwxr-xr-x    1 root     root           769 Dec 14  2015 lighttpd
-rwxr-xr-x    1 root     root           262 Dec 14  2015 logforward
-rwxr-xr-x    1 root     root           542 Dec 14  2015 logsystemstart
-rwxr-xr-x    1 root     root           625 Dec 14  2015 modules
-rwxr-xr-x    1 root     root          1385 Dec 14  2015 mounthd2
-rwxr-xr-x    1 root     root          1022 Dec 14  2015 net-snmpd
-rwxr-xr-x    1 root     root           358 Dec 14  2015 net-snmptrapd
-rwxr-xr-x    1 root     root          6678 Dec 14  2015 networking
-rwxr-xr-x    1 root     root          2986 Dec 14  2015 networking-finish
-rwxr-xr-x    1 root     root           407 Dec 14  2015 nfsd
-rwxr-xr-x    1 root     root          5469 Dec 14  2015 ntpclient
-rwxr-xr-x    1 root     root           322 Dec 14  2015 omsdaemon
-rwxr-xr-x    1 root     root            97 Dec 14  2015 portmapd
-rwxr-xr-x    1 root     root          2403 Dec 14  2015 pureftpd
-rwxr-xr-x    1 root     root           520 Dec 14  2015 rc-once
-rwxr-xr-x    1 root     root           379 Dec 14  2015 rcS
-rwxr-xr-x    1 root     root           210 Dec 14  2015 remountrw
-rwxr-xr-x    1 root     root           901 Dec 14  2015 rt-set-bandwidth
-rwxr-xr-x    1 root     root           832 Dec 14  2015 shutdown
-rwxr-xr-x    1 root     root           987 Dec 14  2015 ssl_post
-rwxr-xr-x    1 root     root           350 Dec 14  2015 start_panel
-rwxr-xr-x    1 root     root           431 Dec 14  2015 sysctl
-rwxr-xr-x    1 root     root          1758 Dec 14  2015 syslog-ng
-rwxr-xr-x    1 root     root           543 Dec 14  2015 telnetd
-rwxr-xr-x    1 root     root           616 Dec 14  2015 tempd
-rwxr-xr-x    1 root     root           729 Dec 14  2015 touchcal
-rwxr-xr-x    1 root     root          1970 Dec 14  2015 udev
user@e!DISPLAY-408A70:~ ls -l /etc/rc*.d/ /etc/rc.local /etc/init.d/rcS 2>/dev/null
-rwxr-xr-x    1 root     root           379 Dec 14  2015 /etc/init.d/rcS

/etc/rc.d/:
lrwxrwxrwx    1 root     root            14 Dec 14  2015 S00_udev -> ../init.d/udev
lrwxrwxrwx    1 root     root            19 Dec 14  2015 S01_mountrw -> ../init.d/remountrw
lrwxrwxrwx    1 root     root            20 Dec 14  2015 S01_networking -> ../init.d/networking
lrwxrwxrwx    1 root     root            17 Dec 14  2015 S01rc-once -> ../init.d/rc-once
lrwxrwxrwx    1 root     root            28 Dec 14  2015 S02_determine_hostname -> ../init.d/determine_hostname
lrwxrwxrwx    1 root     root            31 Dec 14  2015 S04_auto_firmware_restore -> ../init.d/auto_firmware_restore
lrwxrwxrwx    1 root     root            24 Dec 14  2015 S05_logsystemstart -> ../init.d/logsystemstart
lrwxrwxrwx    1 root     root            15 Dec 14  2015 S10_crond -> ../init.d/crond
lrwxrwxrwx    1 root     root            18 Dec 14  2015 S10_lighttpd -> ../init.d/lighttpd
lrwxrwxrwx    1 root     root            19 Dec 14  2015 S10syslog-ng -> ../init.d/syslog-ng
lrwxrwxrwx    1 root     root            15 Dec 14  2015 S11_inetd -> ../init.d/inetd
lrwxrwxrwx    1 root     root            14 Dec 14  2015 S12_dbus -> ../init.d/dbus
lrwxrwxrwx    1 root     root            18 Dec 14  2015 S16dropbear -> ../init.d/dropbear
lrwxrwxrwx    1 root     root            16 Dec 14  2015 S17sysctl -> ../init.d/sysctl
lrwxrwxrwx    1 root     root            19 Dec 14  2015 S20_ledserver -> ../init.d/ledserver
lrwxrwxrwx    1 root     root            20 Dec 14  2015 S21_logforward -> ../init.d/logforward
lrwxrwxrwx    1 root     root            27 Dec 14  2015 S21_networking-finish -> ../init.d/networking-finish
lrwxrwxrwx    1 root     root            18 Dec 14  2015 S22_ipwatchd -> ../init.d/ipwatchd
lrwxrwxrwx    1 root     root            18 Dec 14  2015 S48_mounthd2 -> ../init.d/mounthd2
lrwxrwxrwx    1 root     root            15 Dec 14  2015 S87_tempd -> ../init.d/tempd
lrwxrwxrwx    1 root     root            18 Dec 14  2015 S88touchcal -> ../init.d/touchcal
lrwxrwxrwx    1 root     root            17 Dec 14  2015 S90_modules -> ../init.d/modules
lrwxrwxrwx    1 root     root            26 Dec 14  2015 S92_rt-set-bandwidth -> ../init.d/rt-set-bandwidth
lrwxrwxrwx    1 root     root            23 Dec 14  2015 S99_finalize_root -> ../init.d/finalize_root
lrwxrwxrwx    1 root     root            18 Dec 14  2015 S99_ssl_post -> ../init.d/ssl_post
lrwxrwxrwx    1 root     root            21 Dec 14  2015 S99_start_panel -> ../init.d/start_panel

/etc/rc.once.d/:
-rwxr-xr-x    1 root     root            48 Dec 14  2015 initial_plclist_generation.sh
-rwxr-xr-x    1 root     root           292 Dec 14  2015 machine-id
user@e!DISPLAY-408A70:~ grep -inE 'http|web|browser|qt|touch|fb|display|perspecto' \
 >  /etc/init.d/* 2>/dev/null
/etc/init.d/basyskom:4:export QT_QPA_EGLFS_HIDECURSOR=1
/etc/init.d/basyskom:5:export QT_TSLIB_TOUCHMODE=1
/etc/init.d/basyskom:6:export QT_IM_MODULE=Maliit
/etc/init.d/basyskom:7:#export http_proxy="http://proxy:port"
/etc/init.d/basyskom:15:	export DISPLAY=:0
/etc/init.d/basyskom:20:export QT_QPA_PLATFORM=$PLATFORM
/etc/init.d/basyskom:31:	logger "launching browser"
/etc/init.d/basyskom:32:	/usr/examples/webkitwidgets/browser/browser -plugin Tslib:/dev/input/event0 -platform $PLATFORM &
/etc/init.d/basyskom:40:	killall browser 
/etc/init.d/basyskom:50:	echo "0" > /sys/class/graphics/fbcon/cursor_blink 
/etc/init.d/basyskom:64:			modprobe omaplfb
/etc/init.d/lighttpd:4:# lighttpd
/etc/init.d/lighttpd:8:PREFIX="lighttpd: "
/etc/init.d/lighttpd:9:LIGHTTPD="/usr/sbin/lighttpd"
/etc/init.d/lighttpd:10:LIGHTTPD_CONF="/etc/lighttpd/lighttpd.conf"
/etc/init.d/lighttpd:17:		if [ \! -d /var/log/lighttpd ]; then
/etc/init.d/lighttpd:18:			mkdir -p /var/log/lighttpd
/etc/init.d/lighttpd:19:			chown www:www /var/log/lighttpd
/etc/init.d/lighttpd:22:		if start-stop-daemon --start --quiet --oknodo --exec ${LIGHTTPD} -- -f ${LIGHTTPD_CONF}; then
/etc/init.d/lighttpd:32:		if start-stop-daemon --stop --quiet --oknodo --exec ${LIGHTTPD}; then
/etc/init.d/ntpclient:4:# For further info to ntpclient see http://doolittle.icarus.com/ntpclient/HOWTO
/etc/init.d/ssl_post:5:# Required-Start:    lighttpd, pureftpd
/etc/init.d/ssl_post:6:# Required-Stop:     lighttpd, pureftpd
/etc/init.d/ssl_post:11:# Short-Description: Fire events start/stop for http, https, ftp and ftps demons.
/etc/init.d/tempd:10:#LIGHTTPD_CONF="/etc/lighttpd/lighttpd.conf"
/etc/init.d/touchcal:3:# Script-name: touchcal
/etc/init.d/touchcal:5:# starting touch calibration at boottime
/etc/init.d/touchcal:15:      if [ -e /etc/specific/display.conf ]; then
/etc/init.d/touchcal:16:        CALIBONBOOT=`getconfvalue /etc/specific/display.conf calibonboot -l`  
/etc/init.d/udev:38:	# set display brightness to maximum
/etc/init.d/udev:39:	setup_display 255
user@e!DISPLAY-408A70:~ dmesg | grep -iE 'machine|board|omap|am33|cpu|nand|mmc|sdhci|usb|ether|mdio|phy|touch|input|i2c|spi|lcd|framebuffer'                        
[    0.000000] Booting Linux on physical CPU 0
[    0.000000] CPU: ARMv7 Processor [411fc087] revision 7 (ARMv7), cr=10c53c7d
[    0.000000] CPU: PIPT / VIPT nonaliasing data cache, VIPT nonaliasing instruction cache
[    0.000000] Machine: MACH_PFC200_PERSPECTO_II
[    0.000000] pcpu-alloc: s0 r0 d32768 u32768 alloc=1*32768
[    0.000000] pcpu-alloc: [0] 0 
[    0.000000] Kernel command line: rw ubi.mtd=2 rootfstype=ubifs root=ubi0:ubi_rootfs1  pac_boot_id=0x40 bootversion=01.01.06_01 devconf=0x8008 macaddr=00:30:DE:40:8A:70 systeminfo=0x0001 vram=4M,0x8f400000 omapfb.vram=0:4M@0x8f400000
[    0.000000] OMAP clockevent source: GPTIMER1 at 32768 Hz
[    0.000000] OMAP clocksource: 32k_counter at 32499 Hz
[    0.055601] CPU: Testing write buffer coherency: ok
[    0.217637] OMAP GPIO hardware version 2.5
[    0.225883] omap_mux_init: Add partition: #1: core, flags: 0
[    0.229299] _omap_mux_get_by_name: Could not find signal uart4_rx.uart4_rx
[    0.242038] gpmc_nand_data->dev_ready is enabled!
[    0.242499] nand-xx: init successful: cs mapped to 0x28000000.
[    0.459367]  usbhs_omap: alias fck already exists
[    0.474783] omap_mux_init: Add partition: #2: core, flags: 0
[    0.488999]  omap-mcbsp.2: alias fck already exists
[    0.489738]  omap-mcbsp.3: alias fck already exists
[    0.492076] OMAP DMA hardware revision 4.0
[    0.596695] omap-dma-engine omap-dma-engine: OMAP DMA engine driver
[    0.601741] usbcore: registered new interface driver usbfs
[    0.602172] usbcore: registered new interface driver hub
[    0.602664] usbcore: registered new device driver usb
[    0.604357] omap_i2c omap_i2c.1: bus 1 rev1.3.12 at 400 kHz
[    0.611311] omap_i2c omap_i2c.2: bus 2 rev1.3.12 at 400 kHz
[    0.613618] omap_i2c omap_i2c.3: bus 3 rev1.3.12 at 400 kHz
[    0.674389] usbhs_omap usbhs_omap: xclk60mhsp1_ck set parentfailed error:-22
[    0.698083] OMAP DSS rev 2.0
[    0.699744] omapdss supply vdds_dsi not found, using dummy regulator
[    0.943690] omap_uart.1: ttyO1 at MMIO 0x4806c000 (irq = 73) is a OMAP UART1
[    0.944890] omap_uart.2: ttyO2 at MMIO 0x49020000 (irq = 74) is a OMAP UART2
[    0.945875] omap_uart.3: ttyO3 at MMIO 0x4809e000 (irq = 84) is a OMAP UART3
[    0.984922] enabling NAND BCH ecc with 8-bit correction
[    0.985753] NAND device: Manufacturer ID: 0x01, Chip ID: 0xd3 (AMD S34ML08G1), page size: 2048, OOB size: 64
[    0.986461] Creating 3 MTD partitions on "omap2-nand.0":
[    2.596049] UBI: physical eraseblock size:   131072 bytes (128 KiB)
[    6.407520] omap2_mcspi omap2_mcspi.1: registered master spi1
[    6.407827] omap-dma-engine omap-dma-engine: allocating channel for 36
[    6.407920] omap-dma-engine omap-dma-engine: allocating channel for 35
[    6.407981] spi spi1.0: setup: speed 750000, sample leading edge, clk normal
[    6.408012] spi spi1.0: setup mode 0, 8 bits/w, 1000000 Hz max --> 0
[    6.408443] omap2_mcspi omap2_mcspi.1: registered child spi1.0
[    6.409120] omap2_mcspi omap2_mcspi.2: registered master spi2
[    6.409827] omap2_mcspi omap2_mcspi.3: registered master spi3
[    6.410566] omap2_mcspi omap2_mcspi.4: registered master spi4
[    6.410843] omap-dma-engine omap-dma-engine: allocating channel for 71
[    6.410904] omap-dma-engine omap-dma-engine: allocating channel for 70
[    6.410966] spi spi4.0: setup: speed 1500000, sample leading edge, clk normal
[    6.410997] spi spi4.0: setup mode 0, 8 bits/w, 1500000 Hz max --> 0
[    6.411397] omap2_mcspi omap2_mcspi.4: registered child spi4.0
[    6.414412] libphy: Fixed MDIO Bus: probed
[    6.417982] libphy: GPIO Bitbanged MDIO: probed
[    6.423336] ehci_hcd: USB 2.0 'Enhanced' Host Controller (EHCI) Driver
[    6.423520] ehci-omap.0 supply hsusb0 not found, using dummy regulator
[    6.423828] ehci-omap ehci-omap.0: OMAP-EHCI Host Controller
[    6.423920] ehci-omap ehci-omap.0: new USB bus registered, assigned bus number 1
[    7.459737] ehci-omap ehci-omap.0: irq 77, io mem 0x48064800
[    7.475060] ehci-omap ehci-omap.0: USB 2.0 started, EHCI 1.00
[    7.475306] usb usb1: New USB device found, idVendor=1d6b, idProduct=0002
[    7.475368] usb usb1: New USB device strings: Mfr=3, Product=2, SerialNumber=1
[    7.475399] usb usb1: Product: OMAP-EHCI Host Controller
[    7.475460] usb usb1: Manufacturer: Linux 3.6.11-psp2x-01.02.17_00-rt30 ehci_hcd
[    7.475491] usb usb1: SerialNumber: ehci-omap.0
[    7.477122] hub 1-0:1.0: USB hub found
[    7.478076] Initializing USB Mass Storage driver...
[    7.478630] usbcore: registered new interface driver usb-storage
[    7.478691] USB Mass Storage support registered.
[    7.478722] musb-hdrc: version 6.0, ?dma?, otg (peripheral+host)
[    7.480722] usbcore: registered new interface driver synaptics_usb
[    7.480907] ads7846 spi1.0: setup: speed 750000, sample leading edge, clk normal
[    7.480968] ads7846 spi1.0: setup mode 0, 8 bits/w, 1000000 Hz max --> 0
[    7.481030] spi1.0 supply vcc not found, using dummy regulator
[    7.482107] ads7846 spi1.0: touchscreen, irq 125
[    7.483368] input: ADS7846 Touchscreen as /devices/platform/omap2_mcspi.1/spi_master/spi1/spi1.0/input/input0
[    7.485368] usbcore: registered new interface driver usbtouchscreen
[    7.485830] usbcore: registered new interface driver pixcir_hid_tangoc
[    7.490753] i2c /dev entries driver
[    7.496815] omap_wdt: OMAP Watchdog Timer Rev 0x31: initial timeout 60 sec
[    7.498292] omap_hsmmc omap_hsmmc.0: Failed to get debounce clk
[    7.498415] omap-dma-engine omap-dma-engine: allocating channel for 62
[    7.498476] omap-dma-engine omap-dma-engine: allocating channel for 61
[    7.548109] usbcore: registered new interface driver usbhid
[    7.548170] usbhid: USB HID core driver
[    7.556386] pfc200-audio pfc200-audio:  tlv320aic23-hifi <-> omap-mcbsp.3 mapping ok
[    7.563340]     input device check on
[    7.798178] usb 1-1: new high-speed USB device number 2 using ehci-omap
[    7.857626] input: PAC-Operating-Mode-Switch as /devices/platform/gpio-keys.1/input/input1
[    7.877042] libphy: dsa slave: probed
[    8.014954] usb 1-1: New USB device found, idVendor=0424, idProduct=2514
[    8.015015] usb 1-1: New USB device strings: Mfr=0, Product=0, SerialNumber=0
[    8.022492] hub 1-1:1.0: USB hub found
[    8.306224] usb 1-1.3: new low-speed USB device number 3 using ehci-omap
[    8.428874] usb 1-1.3: New USB device found, idVendor=04f3, idProduct=152e
[    8.429028] usb 1-1.3: New USB device strings: Mfr=1, Product=2, SerialNumber=0
[    8.429028] usb 1-1.3: Product: Gaming KB
[    8.429059] usb 1-1.3: Manufacturer: Gaming KB
[    8.455767] input: Gaming KB Gaming KB as /devices/platform/usbhs_omap/ehci-omap.0/usb1/1-1/1-1.3/1-1.3:1.0/input/input2
[    8.457644] hid-generic 0003:04F3:152E.0001: input: USB HID v1.11 Keyboard [Gaming KB Gaming KB] on usb-ehci-omap.0-1.3/input0
[    8.481430] input: Gaming KB Gaming KB as /devices/platform/usbhs_omap/ehci-omap.0/usb1/1-1/1-1.3/1-1.3:1.1/input/input3
[    8.482291] hid-generic 0003:04F3:152E.0002: input: USB HID v1.11 Keyboard [Gaming KB Gaming KB] on usb-ehci-omap.0-1.3/input1
[   14.919874] net eth0: attached PHY driver [Generic PHY] (mii_bus:phy_addr=fixed-0:01, id=1)
[   15.876242] libphy: gpio-1:00:01 - Link is Down
[   15.953106] libphy: gpio-1:00:02 - Link is Down
[   16.913689] libphy: fixed-0:01 - Link is Up - 100/Full
[   17.953075] libphy: gpio-1:00:02 - Link is Up - 100/Full
[   40.766238] input: SI114X_Sensor as /devices/platform/omap_i2c.3/i2c-3/3-005a/input/input4
[   40.785962] sysfs_create_group successful /sys/bus/i2c/devices/3-005a 
[   41.302224] input: AT42QT1070 QTouch Sensor as /devices/platform/omap_i2c.3/i2c-3/3-001b/input/input5
[   41.894765] omap_uart omap_uart.2: Initializing Modbus driver
[   41.894827] omap_uart omap_uart.2: Baudrate = 9600, TO_15 = 2862500ns, TO_35 = 5152500ns
[   41.896335] omap_uart omap_uart.2: Baudrate = 115200, TO_15 = 845000ns, TO_35 = 1845000ns
user@e!DISPLAY-408A70:~ 

</pre>
