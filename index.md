## linux挂载:mount,umount

linux挂载mount,卸载umount,不常用，一般都是通过网络上传

### 常用命令


```markdown
mount 查看已经挂载的设备

vim /etc/fstab linux 自动挂载的文件

mount -a 自动挂载

mount -t文件系统 -o特殊选项 设备文件名 挂载点

-t :ext3,ext4,iso9660 

-o :exec 允许执行可执行文件,默认

vi hello.sh

#! /bin/bash
echo "hello cangls"
chmod 755 hello.sh
./hello.sh


mount -o remount,noexec /home/

./hello.sh

whoami

mount -o remount.exec /home/

./hello.sh

mkdir /mnt/cdrom/ 建立挂载点

ls /

mount -t iso9660 /dev/sr0 /mnt/cdrom 挂载光盘

mount -t /dev/sr0 /mnt/cdrom

cd /mnt/cdrom

ls

umount 设备文件名或挂载点

umount /dev/sr0

umount /mnt/cdrom/ 设备正忙（在光盘目录下）
ls
pwd

5.挂载u盘

ls /dev 系统自动挂载

sdb1 第二块硬盘

fdisk -l 分区命令,查看u盘设备文件名

mount -t vfat /dev/sdb1 /mnt/usb/
linux默认不支持ntfs文件系统

ntfs-3g
```
