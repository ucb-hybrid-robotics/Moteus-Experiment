## Install Python Package

```bash
pip3 install moteus_gui
```

## Power Supply

Input range is 10-44V. We are using 24V during the calibration process.

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

## Calibration Procedure

This is a typical calibration log

```bash
PS D:\OneDrive\School\HybridRobotics\Humanoid-IROS\actuator\Experiment\Moteus-Experiment> py -m moteus.moteus_tool --target 2 --calibrate
This will move the motor, ensure it can spin freely!
Starting calibration process
Testing 1.067V for resistance
Using 1.067 V for resistance and inductance calibration
Calculating winding resistance
0.534V - 2.467A
0.640V - 2.952A
0.747V - 3.533A
0.907V - 4.359A
1.067V - 4.972A
Calibrating - 
Storing encoder config
Calculating motor inductance
Calculated inductance: 0.00011903529854725936H
Calculated kp/ki: 0.07479208388678756/131.0572332975816
Calculating Kv rating
Testing 2.288V for Kv
0.000V - -0.023Hz
0.572V - 1.778Hz
1.144V - 3.711Hz
1.716V - 4.605Hz
2.288V - 7.455Hz
v_per_hz (pre-gearbox)=0.3215791691231419
Saving to persistent storage
Calibration complete
REPORT: moteus-cal-ADcAQDdTUA0gMjlC-20230526T030418.129018.log
------------------------
{
  "timestamp": "2023-05-26 03:04:18.129018",
  "device_info": {
    "serial_number": "ADcAQDdTUA0gMjlC",
    "model": "800",
    "git_hash": "75df0139aaf6e76f207dffae17b81b39f3d5d5ce",
    "git_dirty": false,
    "git_timestamp": 1659188141,
    "uuid": "01e6abe2-0c78-4b1e-a79c-4d2a4f80e8a5"
  },
  "calibration": {
    "invert": false,
    "phase_invert": false,
    "poles": 28,
    "offset": [
      1.5652600064153666,
      1.3883951507290604,
      1.2072252436773028,
      1.0509661706995692,
      0.9177183824042237,
      0.8202072490342932,
      0.7747363114286897,
      0.7492939507598004,
      0.7550369796533937,
      0.7945241737666235,
      0.8529132578612275,
      0.9362921741543154,
      1.03056123066945,
      1.1028329430500625,
      1.1594264888705939,
      1.2439228576111598,
      1.3180994552809155,
      1.3548719713307757,
      1.3993363842668267,
      1.4518845686697603,
      1.5015688533123086,
      1.5555311695638974,
      1.5858247837346882,
      1.595408547656177,
      1.625050159804666,
      1.648972221027813,
      1.6192384374873325,
      1.5662856822961368,
      1.4925649472954747,
      1.4245941658475656,
      1.3514964271208485,
      1.2409192248542351,
      1.1264153038914544,
      1.044734669578014,
      0.988137063252903,
      0.9723835665422832,
      0.9644320486077641,
      0.9935721152450767,
      1.0991078780072778,
      1.2539163614019992,
      1.4237384714052592,
      1.6239483744671979,
      1.877481324391759,
      2.1471581348981466,
      2.3910477651472553,
      2.6046965992267124,
      2.8210677328602594,
      2.9976030061088417,
      3.115618248358252,
      3.197071861193824,
      3.268008936823502,
      3.288704916573813,
      3.2635137469008395,
      3.225952811381029,
      3.1534133008207315,
      3.0654669625523674,
      2.970338497974395,
      2.8273023442269793,
      2.6897250282825405,
      2.5210452691729626,
      2.3485754305507966,
      2.1582537424756882,
      1.957505721993239,
      1.7761816481789967
    ]
  "winding_resistance": 0.2085840650725785,
  "inductance": 0.00011903529854725936,
  "pid_dq_kp": 0.07479208388678756,
  "pid_dq_ki": 131.0572332975816,
  "torque_bw_hz": 100.0,
  "encoder_filter_bw_hz": 200.0,
  "encoder_filter_kp": 2513.2741228718346,
  "encoder_filter_ki": 1579136.7041742974,
  "v_per_hz": 0.3215791691231419,
  "kv": 93.28962470362046,
  "unwrapped_position_scale": 1.0
}
```
