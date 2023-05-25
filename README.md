## Install Python Package

```bash
pip3 install moteus_gui
```

## Power Supply

Input range is 10-44V.

Peak phase current is 100A.

## Calibration

With motor controller powered and CAN connected to USB adapter, run 

```bash
py -m moteus.moteus_tool --target 1 --calibrate
```

## Launch GUI

```bash
py -m moteus_gui.tview --devices=1
```
