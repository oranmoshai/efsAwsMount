# Ansible Role: efsAwsMount

Create mount folder  
Install nfs-utils/nfs-common  
Write to /etc/fstab efs path  
Mount  

## Example Playbook
vars:  

  efsFolderList:  
      - { folderPath: "/opt/efs", folderOwner: "root", folderGroup: "root", folderMode: "0644" , fileSystemId: "fs-xxxx"}  
  awsRegion: us-east-1  
  mountState: mounted  

roles:  
    - efsAwsMount

    mount options:
    present (default)
    absent
    mounted
    unmounted


## Dependencies

Curl installed.
