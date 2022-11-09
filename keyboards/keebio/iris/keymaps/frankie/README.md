# Frankie's Changes

Before running anything:

- Open `QMK MSYS` from the start menu
- `cd source/qmk_firmware/`

## Build Firmware

- `qmk compile -kb keebio/iris/rev6a -km frankie`

## Flash Firmware

- Have a spare keyboard plugged in or the on-screen keyboard open
- Press the physical RESET button on the underside of the PCB

```term
dfu-programmer.exe atmega32u4 erase --force
dfu-programmer.exe atmega32u4 flash --force ./keebio_iris_rev6a_frankie.hex
dfu-programmer.exe atmega32u4 reset
```

## Debugging

- `qmk doctor`
