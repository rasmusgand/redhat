# Red Hat


- Boot into single user mode

Boot mode when computer starts up, edit.

```shell
mount -o remount,rw /sysroot
chroot /sysroot

echo "password"  | passwd --stdin root
touch /.autorelabel

reboot -f

```
- Change root password into something random.

```
# openssl rand -base64 15 | passwd --stdin root

```
