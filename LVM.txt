LVM is a tool for logical volume management which includes allocating disks, striping, mirroring and resizing logical volumes.
With LVM, a hard drive or set of hard drives is allocated to one or more physical volumes.
LVM physical volumes can be placed on other block devices which might span two or more disks.
The physical volumes are combined into logical volumes, with the exception of the /boot partition.
The /boot partition cannot be on a logical volume group because the boot loader cannot read it

LVM:
  1. It is logical volume manager.
  2. It is a device mapper framework that provides logical volume management for the Linux kernel.
  3. It is used for creating single logical volumes of multiple physical volumes for entire hard disk allowing for dynamic volume resizing.
  4. Most modern Linux distributions are LVM aware to point of being able to have their root file system on a logical volume.
  5. Performing consistent backups by taking snapshots of the logical volume.
  
1.pvs and pvdisplay
  To display Physical Volumes (PV) on a system you can issue the pvs command.
  To display more details about a PV, you can issue the pvdisplay command.

2.vgs
  To display basic information regarding a Volume Group on a Linux system you can issue the vgs command.
  
3.vgdisplay
  For a more detailed view of Volume Groups on a Linux system, you can use the command vgdisplay.

4.lvs
  To display Logical Volume (LV) information on a Linux system you can issue the lvs command.
  
5.lvdisplay
  For a more detailed display of Logical Volumes on a Linux system you can use the command lvdisplay.
  
6.lsblk
  To display partition types and disk information on a Linux system, you can use the lsblk command.
  
7.fdisk -l
  To display partition information on a Linux system, you can issue the fdisk -l command.
  If you issue the command "fdisk -l" without specifying a disk, then all disk information is displayed.

8.pvcreate
  To add a new disk into a system that is to be managed by LVM, you must use the command pvcreate.
  
9.pvremove
  To remove a Physical Volume from a system, you use the pvremove command.
  
10.pvs 
   Before the newly added disk can be used we use the pvcreate command. 
   The command pvs is used to show that it is not associated with any existing Volume Groups.

11.vgrename
   To rename an existing Volume Group, the vgrename command is used.
   
12.vgremove
   To remove a Volume Group, the command vgremove is used.

13.vgextend
   To add additional space to an existing Volume Group, the command vgextend is used.
   
14.vgreduce
   To remove storage from a Volume Group, the command vgreduce is used.
   
15.lvcreate 
   To create a Logical Volume on an existing Volume Group, the command lvcreate is used.

16.lvcreate -n lv01 -L1G vg01 
   The command will create a Logical Volume (LV) called lv01 with an allocation of 1GB from the Volume Group (VG) vg01