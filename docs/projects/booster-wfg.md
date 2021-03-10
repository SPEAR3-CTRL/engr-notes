# Booster RF Waveform Generator

## Overview

The SPEAR3 booster is powered by a 5-cell standing wave cavity at 358.54 MHz. The middle cell is coupled to a rectangular waveguide through a short coaxial line and coupling loop, which can be manually rotated to adjust the coupling to the cavity. Each cell has a fixed frequency tuner, and the two end cells have movable tuners with motors that can be adjusted during operation. Each cell has additionally a coaxial probe with a coupling loop to instrument the field amplitude. As the frequency of the SPEAR3 RF drifts over time, the booster cavity tuners need to be periodically adjusted to keep the cavity driven on resonance. We are developing a feedback system to keep the cavity on resonance by adjusting the two movable tuners. In this Engineering Note the design of the tuners feedback systems is described, as well as experimental results from a test implementation in Matlab.

## PV list

### PVs in the current booster waveform generator

PV | Description | Channel
-- | ----------- | -------
inj:BOO_RF$POWER_AS | Waveform setpoint |
inj:BOO_RF$POWER_MIN_AS | Waveform offset |
inj:BOO_RF$POWER_MAX_AS | Waveform amplitude |
inj:BOO_RF$PHASE_AS | Waveform delay |
inj:BOO_RF$WAVEFORM_DS | Type of waveform |

### PVs watched by the BOO-RF-WFG soft IOC

PV | Description | Channel
-- | ----------- | -------
inj:BOO_DC$CURR_AM | White circuit current
inj:BOO_AC$VOLT_AM | White circuit voltage

### PVs planned for the BOO-RF-WFG soft IOC

PV | Description | Channel
-- | ----------- | -------
BOO-RF-WFG:WavSetpt | Waveform setpoint |
BOO-RF-WFG:WavRdbk | Waveform readback from the waveform generator |
BOO-RF-WFG:Amp | Waveform amplitude |
BOO-RF-WFG:Offset | Waveform offset |
BOO-RF-WFG:Delay | Delay of the waveform relative to the TTL signal |
BOO-RF-WFG:WavType | Type of waveform |
BOO-RF-WFG:WhiteCircCurrLo | Lower limit of the white circuit current (mA) |
BOO-RF-WFG:WhiteCircCurrHi | Upper limit of the white circuit current (mA) |
BOO-RF-WFG:WhiteCircVoltLo | Lower limit of the white circuit voltage (mV) |
BOO-RF-WFG:WhiteCircVoltHi | Upper limit of the white circuit voltage (mV) |
