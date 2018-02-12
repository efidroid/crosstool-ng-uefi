# crosstool-ng project for UEFI

## Configure:
```
ct-ng defconfig DEFCONFIG=configs/uefi_[GCCARCH]_defconfig
ct-ng menuconfig
```
Now navigate to `C-Library` > `Target CFLAGS for newlib` and extend it like this to add the required directories to the include path:
`-I /home/builduser/edk2/MdePkg/Include -I /home/builduser/edk2/MdePkg/Include/[EDKARCH] -I /home/builduser/EFIDroidLKLPkg/UEFIThreads/Include`

`/home/builduser/edk2` is the path to your EDK2 directory.

`GCCARCH`: See `configs/` for a list of supported values

`EDKARCH`: Supported values:
* Arm
* X64



## Compile:
`ct-ng build`
