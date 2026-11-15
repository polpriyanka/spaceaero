---
layout: article
title: "Log 01: My first instrumented rocket flight"
date: 2026-11-14
number: 1
tags: [alpha iii, openrocket, flight data]
summary: "An Estes Alpha III with an onboard sensor on an A8-3 motor. OpenRocket predicted 312 ft; the real flight reached 287 ft (-8%), with clean, usable sensor data."
---

SpaceAero was already underway when Starship Flight 15 achieved the first tower catch of an orbital upper stage on November 14, 2026. Watching that flight reinforced why I started this project: real progress comes from measuring what actually happens and learning from the data.

SpaceAero is my high-school rocketry project. The goal is to design, build, fly, and log real flight data (altitude, acceleration, and recovery), then share the full process so other students can learn from it too.

## At a glance

| | |
|---|---|
| **Rocket** | Estes Alpha III with added payload bay |
| **Motor** | Estes A8-3 |
| **Mass (no motor)** | 48 g |
| **Stability** | ~2.1 calibers |
| **Predicted apogee** | 312 ft |
| **Actual apogee** | 287 ft (–8%) |
| **Cost of first setup** | $140 |

## Starting costs

Total spent for the first complete test setup: **$140**. This covered:

- Estes Alpha III rocket kit
- A8-3 motors and recovery wadding
- Basic altimeter and accelerometer
- Launch pad and controller

## Building the rocket

I chose the Estes Alpha III because it is simple and has enough space for a small sensor. Here is exactly what I did:

1. Assembled the rocket following the kit instructions.
2. Added a small payload bay and mounted the sensor with foam padding.
3. Weighed the finished rocket without a motor: **48 grams**.
4. Found the center of gravity: **14.2 cm from the nose tip**.
5. Checked stability in OpenRocket: approximately **2.1 calibers**.
6. Selected an A8-3 motor for a low, safe first flight.

## Simulation (OpenRocket)

Before flying, I ran a simulation in OpenRocket with these inputs:

- Rocket mass: 48 grams
- Center of gravity: 14.2 cm from nose tip
- Motor: Estes A8-3
- Launch conditions: sea-level atmosphere, zero wind

OpenRocket predicted:

- **Apogee:** 312 feet
- **Peak acceleration:** approximately 11–12 g
- **Time to apogee:** about 4.1 seconds

A separate hand calculation using the A8-3's published peak thrust suggested a higher peak acceleration of roughly 15 g.

## Flight day

At the field I:

1. Packed the parachute with recovery wadding.
2. Loaded the A8-3 motor and igniter.
3. Launched on a calm day.
4. Recovered the rocket after a short drift of about 40 meters.
5. Downloaded the flight data and compared it to the simulation.

## Flight results

| Measurement | OpenRocket prediction | Actual flight | Difference |
|---|---|---|---|
| Apogee | 312 ft | 287 ft | –25 ft (–8%) |
| Peak acceleration | ~11–12 g | 11.4 g | Matches |
| Time to apogee | ~4.1 s | 4.1 s | Match |

## Analysis

**Apogee.** The actual apogee was 25 feet (about 8%) lower than the OpenRocket prediction. This is normal for a first flight and can be explained by light wind causing slight weathercocking, small amounts of rail friction, and normal motor variation.

**Peak acceleration.** The peak acceleration of 11.4 g matched the OpenRocket prediction closely. The hand calculation had suggested around 15 g. The lower measured value is most likely due to the foam mounting slightly cushioning the sensor and the sampling rate possibly missing the true instantaneous peak.

**Overall.** The flight was clean. The parachute deployed near apogee, the rocket landed safely, and the sensor returned usable data.

## Next steps

For the next flight I will:

- Use a B6-4 motor for higher altitude and a longer data window.
- Try a firmer sensor mounting method.
- Work on reducing rail friction.
- Launch in the lightest wind possible.
- Calculate approximate velocity from the acceleration data.

## Why this project matters

Most student rocket projects only show the successful launches. The useful information is usually in the details and the differences between prediction and reality. SpaceAero exists to keep the full record: what I bought, what I built, what the numbers showed, and what I will change next.

**Long-term plan**

- **Year 1:** Reliable data logging and building experience, with NAR certification as a longer-term goal
- **Year 2:** A larger scratch-built rocket with a recoverable payload
- **Competitions:** The American Rocketry Challenge and NASA TechRise with the local CENJARS club

Starship Flight 15 showed what careful measurement can achieve at the highest level. SpaceAero is my attempt to apply the same approach at the high-school level: fly, measure, learn, and share the results.
