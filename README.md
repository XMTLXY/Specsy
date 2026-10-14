# Specsy

A portable system information and device inventory tool for **Windows XP through Windows 11**.

Run Specsy on any PC to see its hardware and Windows details at a glance, then save the machine into an organised **Device List**. Keep one copy on a USB stick and build up an inventory of every computer you work on.

- One `.exe`. No installer, no runtimes, no admin rights, no internet.
- Works from read-only and removable drives.

## Download

Download **[Specsy.zip](https://github.com/XMTLXY/Specsy/releases/latest/download/Specsy.zip)** (latest release), unzip it and run `Specsy.exe`. That's all.

All versions are on the [Releases page](https://github.com/XMTLXY/Specsy/releases).

### v1.0.1 pre-release (experimental)

A test version is available on the [Releases page](https://github.com/XMTLXY/Specsy/releases) (marked *Pre-release*; the download above stays on the stable version). It adds:
- **Drivers tab**: every device and its driver, Device Manager-style, with problem devices flagged
- **Driver tools (experimental)**: install a driver from an .inf or a folder, find which device an .inf is for, and an **Install Queue** that runs driver installers one after another
- **Better CPU detection on Windows XP** (correct names and core counts for newer CPUs)
- **A portable folder layout**: `Specsy.exe` (launcher), `App\` (program files), `Drivers\` and `Device List\`

Driver installation is experimental. Test it on a machine you can restore first.

## Features

**About**: a "View basic information about your computer"-style summary.
- Windows logo and edition for the installed version, plus the PC maker's (OEM) logo
- Processor, installed RAM, graphics, motherboard and computer name
- Windows Experience Index scores on Vista, 7 and 8 (greyed out on other versions)

**Scan This PC**: the full spec list.
- OS name, version, build, service pack, architecture and install date
- System manufacturer and model, chassis type, battery
- CPU name, cores, threads and clock speed
- Each RAM stick (slot, capacity, speed)
- Disks (model, size, interface)
- Graphics (name, VRAM, driver version)
- Motherboard and BIOS
- Physical network adapters
- Suggests a category (Laptops / Desktops / Other) from the chassis type or battery, which you can change
- Optional nickname, and an optional human-readable `.txt` copy next to the JSON

**Saved Devices**: browse and manage everything you've saved.
- Folder tree of `Device List` → folders → devices; select a device to see its specs
- New folder, move to folder, rename and delete (with confirmation)

Press **Alt** for the menu bar (Help → About Specsy).

## How saving works

Devices are saved next to the exe:

```
Specsy.exe
Device List\
    Laptops\
    Desktops\
    Other\
    <your own folders>\
```

Each device is one JSON file named after its nickname or hostname. If a device with the same name already exists, you can overwrite it or keep a dated copy (`NAME_YYYY-MM-DD.json`).

## Credits

Vibecoded by **XMTLXY (Sylvia)**: https://github.com/XMTLXY

Windows logos are from the [Windows Logo Icon Set](https://www.rw-designer.com/icon-set/winlogos) (CC BY-SA). The logo artwork itself was made by Microsoft. Windows and the Windows logos are trademarks of Microsoft. Specsy is not affiliated with or endorsed by Microsoft.

## License

Specsy is released under the [MIT License](LICENSE). The Windows logos and the app icon artwork inside it are not covered by it; see the third-party section of `LICENSE`.
