# EBS

- EBS are placed in a specific AZ, where they are automatically replicated. (Not to different AZ, but between SANs)
- cannot mount to multiple instances
- EC2 and EBS volume have to be in the same AZ
- can't modify standard volume, can change volume size and storage type on the fly

### Bootable:
- Magentic standard (bootable)
- GP2
- IO1

### Volume types

- GP2, general purpose SSD
    * 3 IOPS per GB with up to 10k IOPS, burst up to 3k IOPS
- Provisioned IOPS SSD (IO1)
    * I/O intensive
    * if you need >10k IOPS
    * provision up to 20k IOPS
- Throughput optimized HDD (ST1)
    * big data
    * data warehouses
    * Log processing
    * sequential data
    * cannot be a boot volume
- Cold HDD (SC1)
    * low cost
    * file server
    * cannot be a boot volume
- Magnetic (Standard)
    * bootable
    * lowest cost

### Snapshots

- snapshots exist on S3
- snapshots are point in time copies of volumes
- snapshots are incremental
- you can create AMIs from volumes and snapshots
- to move EC2 volume from one AZ/region to another - take a snap or an image, then copy it to the new region
- snaps of encrypted volumes are encrypted automatically
- volumes restored from encrypted snapshots are encrypted automatically
- you can share snapshots, but only unecrypted
    * snap can be shared with other AWS accounts or made public
- snapshot for root EBS volumes -> stop the instance before taking the snapshot

#### Snaps of RAID array

- stop app from writing to disk
- flush all caches to the disk
- take snap

How:
- freeze the filesystem
- unmount the RAID array
- shutting down EC2 instance

### Instance store

- Ephemeral storage
- can't stop. If the underlying host fails - will lose data
- EBS backed can be stopped
- Can reboot both