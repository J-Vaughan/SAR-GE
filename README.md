# SAR-GE

SAR-GE is a plan for a satellite using an SAR (Synthetic Aperture Radar) to
surveil Greenhouse Emissions over the entire domain of Canada. This project is
for Spacecraft Design I (AERO 3841) at Carleton University, and the defined
project variables are listed in the [Requirements](#Requirements) section.

> IMPORTANT: If you are currently taking AERO 3841, you are *not* permitted to
> use any part of this project to help you, for risk of academic misconduct.

This repository is meant to showcase my analysis and writing skills.

## Mission Statement

From the project guidelines written by Professor T. Kaya, the main goal of this
mission is to monitor gas and oil pipelines from space. The payload is a SAR
consuming an average power of 350 W with a mass of 200 kg, housed in a
1 m by 0.5 m by 0.5 m (presumably) rectangular housing. The required resolution
is 5 m, and the ground swath width is 100 km. The coverage area per image is
100 x 100 km^2, and the whole country (Canada) needs to be imaged within
14 days. The master Earth station is the Gatineau Satellite Ground Station, with
Prince Albert station as a backup. The useful lifetime is 5 years, and the time
to deployment is 3 years.

# Requirements

The requirements listed in this section have been prescribed by the project
document.

## Communications
- The communications package must include the following data in addition to the
  payload data:
  | Data | Bits |
  | ---- | ---- |
  | Error Detection | 3 b per image size in bytes |
  | Latitude | 32 b per image |
  | Longitude | 32 b per image |
  | Altitude | 32 b per image |
  | Time | 64 b per image |
  | Synchronization | 24 b per image |
- Housekeeping data is sampled 100 times per minute with 16 bits
  per sample.

## Power
- Payload average power of 350 W.

## ADCS
- 1 degree accuracy for each of the three axes, and 0.1 degree accuracy for
  attitude determination.

## GNS
- Orbit should be maintained within 5 km of accuracy.

## Thermal
- Upper temperature limit of 50 degrees celsius, lower limit of -5 degrees, with
  a 5 degree margin on both values.
- Payload to be maintained at 20 degrees celsius with variation of less than
  1 degree on either side.
