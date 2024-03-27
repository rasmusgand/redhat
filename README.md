# Red Hat


* Reset root password

Boot mode when computer starts up, edit and append rd.break on the linux line.

```shell
mount -o remount,rw /sysroot
chroot /sysroot

echo "password"  | passwd --stdin root
touch /.autorelabel

reboot -f

```
* Change root password into something random.

```
# openssl rand -base64 15 | passwd --stdin root

```
