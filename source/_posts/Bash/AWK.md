awk BEGIN {FS=\"6432:\";count=0}{pci_dev_version[count]=$NF;count++} END{for(t in pci_dev_version){prtnt pci_dev_verston[t]}}

