# fwtool.py #

A python tool to unpack Sony camera firmware images, ported from [nex-hack's fwtool](http://www.personal-view.com/faqs/sony-hack/fwtool).

## Special features ###
* **3rd gen firmware images are supported**
* Known file system images are extracted

## Usage ##
### Unpack a firmware image ###
    python fwtool.py unpack -f Update_ILCE_V100.exe -o outDir

The following files are accepted as input (*-f* flag):
* A Windows firmware updater executable (.exe file)
* The *FirmwareData.dat* file extracted from an updater
* A firmware dump created by running `dd if=/dev/nflasha of=dump.dat` on the camera

### Decode Backup.bin ###
    python fwtool.py print_backup -f Backup.bin

This will list all properties defined in Backup.bin, the settings file used on Sony cameras. In firmware updates, you can find different variants this file in the *0110_backup* directory.
