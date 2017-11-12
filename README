# crosstool-ng project for UEFI

## Configure:
```
ct-ng defconfig DEFCONFIG=configs/uefi_defconfig
ct-ng menuconfig
```
Now navigate to `C-Library` > `Target CFLAGS for newlib` and extend it like this to add the required directories to the include path:
`-I /home/builduser/edk2/MdePkg/Include -I /home/builduser/edk2/MdePkg/Include/Arm`


`/home/builduser/edk2` is the path to your EDK2 directory.

## Compile:
`ct-ng build`
