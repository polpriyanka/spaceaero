---
layout: article
title: "Log 01 — My First Instrumented Rocket Flight"
date: 2026-11-14
permalink: /logs/01-first-instrumented-flight/
summary: "Building an Estes Alpha III with an onboard sensor board, simulating it in OpenRocket, and comparing the prediction to real flight data."
---

## Why I started SpaceAero

In November 2026, SpaceX's Starship Flight 15 made history when the upper stage returned from orbit and was successfully caught by the launch tower. Watching that flight made one idea clear to me: real progress in rocketry comes from measuring what actually happens and learning from the data. That is why I started SpaceAero.

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

I decided to document everything from the beginning, including cost. The total for the first complete test setup was **$140**, which covered:

- Estes Alpha III rocket kit
- A8-3 motors and recovery wadding
- Basic altimeter and accelerometer board
- Launch pad and controller

## Building the rocket

I chose the Estes Alpha III because it is simple and has enough space for a small sensor board. Here's exactly what I did:

1. Assembled the rocket following the kit instructions.
2. Added a small payload bay and mounted the sensor board with foam padding.
3. Weighed the finished rocket without a motor: **48 grams**.
4. Found the center of gravity: **14.2 cm from the nose tip**.
5. Checked stability in OpenRocket: approximately **2.1 calibers**.
6. Selected an A8-3 motor for a low, safe first flight.

## Simulation (OpenRocket)

Before flying, I ran a simulation in OpenRocket with these inputs:

- Rocket mass: 48 grams
- Center of gravity: 14.2 cm from nose tip
- Motor: Estes A8-3
- Launch conditions: sea-level atmosphere, zero wind (ideal case)

OpenRocket predicted:

- **Apogee:** 312 feet
- **Peak acceleration:** approximately 11–12 g
- **Time to apogee:** about 4.1 seconds

I recorded the 312-foot prediction in my notebook the night before the flight.

## Flight day

At the field I:

1. Packed the parachute with recovery wadding.
2. Loaded the A8-3 motor and igniter.
3. Launched on a calm day.
4. Recovered the rocket after a short drift of about 40 meters.
5. Downloaded the flight data and compared it to the simulation.

## Flight results

| Measurement | OpenRocket prediction | Real flight | Difference |
|---|---|---|---|
| Apogee | 312 ft | 287 ft | –25 ft (–8%) |
| Peak acceleration | ~11–12 g | 11.4 g | Very close |
| Time to apogee | ~4.1 s | 4.1 s | Match |

The real altitude was 25 feet lower than the simulation, about 8% less than predicted.

## Why the difference happened

Several real-world factors usually make a rocket fly a little lower than a perfect simulation:

- **Wind:** light wind can cause slight weathercocking, so some energy goes sideways instead of straight up.
- **Launch rod friction:** the rod creates a small amount of friction that simulations often ignore.
- **Motor variation:** no two motors are exactly identical; small variations in total impulse are normal.
- **Construction:** tiny differences in glue, alignment, or paint also affect performance.

On this flight the day was mostly calm, but a very light breeze was present. Combined with normal rail friction and motor variation, an 8% difference is realistic for a first test.

## What the data told me

- The peak acceleration of 11.4 g matched the published A8-3 thrust curve, showing the motor performed normally.
- The parachute deployed near apogee and the rocket landed safely.
- The sensor board survived and produced clean, usable data, which was the main goal of this flight.

## Next steps

For the next flight I will:

- Use a B6-4 motor for higher altitude and a longer data window.
- Work on reducing rail friction.
- Launch in the lightest wind possible.
- Extract approximate velocity from the accelerometer data.
