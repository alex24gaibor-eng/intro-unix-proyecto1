#Research questions:

1. What is LUKS, and what is its relationship with dm-crypt in the Linux kernel? Explain the role of the device mapper in the encryption process.
LUKS (Linux Unified Key Setup) is a standard for disk encryption in Linux, according to Boutnaru (2025); it works on top of the dm-crypt, that’s a"transparent disk encryption subsystem in the Linux kernel...implemented as a device mapper target" (Dm-crypt - ArchWiki, n.d.). In the encryption process, the device mapper acts as the foundational framework for mapping physical block devices to virtual ones, as explained in Boutnaru’s (2025) blog ‘The Linux Concept Journey — dm (Device Mapper).

2. What is the difference between full disk encryption (FDE) and filesystem-level encryption? Mention two advantages and two limitations of each.
FDE encrypts the whole disk, including the operating system, referencing Bitdefender (2025), while  file-level encryption protects only specific files or directoriesvrefering to Content Studio (2023). FDE provides complete protection and is transparent to users, but offers no protection when the system is running, offering less flexibility. In contrast, a filesystem-level encryption supports multiple users with different keys and has a selective protection of data, is also more complex to configure and in the long-run may not fully protect metadata.

3. What is LVM and what are its three abstraction layers (PV, VG, LV)? What advantages does LVM offer compared to traditional partitioning in a server environment?
	The Logical Volume Manager (LVM) is a “tool for logical volume management which includes allocating disks, striping, mirroring and resizing logical volumes.” (Red Hat, n.d.).It has three layers:  PV (Phyiscal Volume), contains physical disks/partitions, VG (Volume Group) is a pool of storage created from PVs, and LV (Logical Volume) are the virtual partitioned crated from a VG, referencing simplyblock (n.d.). LVM offers superior flexibility, easier storage expansion, high scalability and the creation of snapshots for backups, according to Fedora Discussion (2019).

4. Explain what happens during the boot process of a system with LUKS + LVM: at what point is the decryption password requested and what role does GRUB play in this process?
	During boot, GRUB (GRand Unified Bootloader) loads the Linux kernel and initramfs (Lenovo, 2023). Then, in the initramfs stage, the system requests the LUKS decryption passphrase to unlock the encrypted disk, according to Debian GNU/Linux Installation Guide (n.d.). Once the user provides the correct passphrase, LVM activates the LVs, and the system continues booting normally.

#Screenshot List – Section 1

1.1 Start of the Debian installation process (Graphical Install mode).

1.2 Partitioning configuration using the option “use entire disk and set up encrypted LVM”.

1.3 Creation of logical volumes (/, swap, /home).

1.4 Disk encryption setup with LUKS (passphrase creation).

1.5 User creation and hostname configuration.

1.6 Completion of the installation and software selection.

1.7 System boot asking for the passphrase to unlock the encrypted disk.

1.8 System verification using commands:

lsblk
sudo pvs
sudo vgs
sudo lvs
sudo cryptsetup status sda5_crypt

