# virtualbox and vagrant home setting

## VirtualBox home directory.
`"C:\Program Files\Oracle\VirtualBox\VBoxManage.exe" setproperty machinefolder "C:\VMs"`
## Vagrant home directory for downloadad boxes.
`REG ADD HKCU\Environment /v VAGRANT_HOME /t REG_SZ /d "C:\VMs\vagrant.d"`
## Upgrade to new powershell version > 2.0,otherwise vagrant may stuck [download and install](https://www.microsoft.com/en-us/download/details.aspx?id=40855)
## Scp files from vm using private keys
`scp -P 2222  -i "D:/vms/vagrant.d/insecure_private_key" core@127.0.0.1:/home/core/working/pipeline-1.2.0/prediction.ml/jvm.tar.gz .`