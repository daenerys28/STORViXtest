# STORViXtest

## How to install Hyper V with PowerShell

First open your PowerShell ISE as an admin and implement:

`PS C:\WINDOWS\system32> Get-WindowsOptionalFeature -online -FeatureName *hyper-v* | select DisplayName, FeatureName`

Choose the Microsoft-Hyper-V-All

`PS C:\WINDOWS\system32> Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V-All`

And import the Hyper-V Moule

`PS C:\WINDOWS\system32> Import-Module Hyper-V`

Now you can blablablabla a new VHD and Name it

`PS C:\WINDOWS\system32> New-VM -NewVHDPath C:\HyperVvm\STORViXtest.vhdx -NewVHDSizeBytes 10GB -Generation 2 -MemoryStartupBytes 1073741824 -Name STORViXtest -SwitchName "Default Switch"`


### How to 


## How to remove VM

First Remove the VM

`PS C:\WINDOWS\system32> Remove-VM -Name "STORViXtest" -Force`


Then remove the item path

`PS C:\WINDOWS\system32> Remove-Item -Path C:\HyperVvm\STORViXtest.vhdx`
