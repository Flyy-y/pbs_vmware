# PBS_VMware

## About
PBS_VMware goal is to create an interface between a [Proxmox Backup Server](https://www.proxmox.com/en/proxmox-backup-server) and a VMware Datastore managed by an ESXi host or VCenter Server, and be able to perform complete VM backup, from NAS (NFS) or SAN (FC / iSCSI)

*For yet, target supported versions will only be for VSphere 7 and Proxmox Backup Server 1.1+*

## Features

Nothing to flex about for now, project in still in early developpement phases !

## Roadmap

| Features | Available |
|--|--|
| Select targets VMs for backup using VCenter tags | ❌ |
| Backup a VM from SAN Datastore connected to a VCenter Server, from VMDK | ❌ |
| Restore backup to a new VM, using CLI as interface | ❌ |
| Backup a VM  by creating VMware snapshots as data source | ❌ |
| Backup a VM from NFS Datastore connected to a VCenter Server, from VMDK | ❌ |
| Backup a VM from SAN Datastore connected to an ESXi Host, from VMDK | ❌ |
| Backup a VM from NFS Datastore connected to an ESXi Host, from VMDK | ❌ |
| Backup from ZFS / BTRFS snapshots + VMware snapshots  | ❌ |


## Dependencies

Nothing here yet !

## Config file example

    [PBS]
    
    Hostname = pbs.example.com
    
    Username = example
    
    Password example
    
    Datastore = example
    
      
    
    [VMWARE]
    
    Hostname = esxi.example.com
    
    Username = example
    
    Password = example
    
    Tags = example-tag
    
      
    
    [VMWARE_DATASTORES]
    
    datastore1 = /dev/sdx
    
    datastore2 = nas.example.com:/NFS
