# NeedForHeat Presence Detector example

This is a [template project](https://github.com/energiegedrag-nl/needforheat-presence-detector-firmware/generate) that can be used to create firmware for measurement devices that use the [twomes-generic-esp-firmware](https://github.com/energiegedrag-nl/needforheat-generic-firmware) library.

> **Own deployment.** This repository is maintained by [energiegedrag-nl](https://github.com/energiegedrag-nl) and deployed under `energiegedrag.nl`. To run your own instance, replace `energiegedrag-nl` by your GitHub organisation and `energiegedrag.nl` by your domain (hosts used: `api.<domain>`, `manuals.<domain>`), consistently in configuration and build settings.

## Table of contents
* [General info](#general-info)
* [Measurements](#measurements)
* [Deploying](#deploying)
* [Developing](#developing) 
* [Supported devices](#supported-devices)
* [Features](#features)
* [Status](#status)
* [License](#license)
* [Citation](#citation)
* [Credits](#credits)

## General info
The NeedForHeat Presence Detector primarily serves as an example and template repository how to create firmware that uses the [twomes-generic-esp-firmware](https://github.com/energiegedrag-nl/needforheat-generic-firmware) library. Nevertheless, it can be used in  measurement campaigns that require occupancy detection using Bluetooth name requests.

## Measurements

A NeedForHeat Presence Detector measurement device, in addition to [generic data sent by any NeedForHeat measurement device](https://github.com/energiegedrag-nl/needforheat-generic-firmware#readme), sends data about the following property via the [NeedForHeat API](https://github.com/energiegedrag-nl/needforheat-server-api) to a NeedForHeat server:

| Sensor    | Property       | Unit | [Printf format](https://en.wikipedia.org/wiki/Printf_format_string) | Default measurement interval \[h:mm:ss\] | Description                                                |
| --------- | -------------- | ---- | ------------------------------------------------------------------- | ---------------------------------------- | ---------------------------------------------------------- |
| Bluetooth | `occupancy__p` | [-]  | %u                                                                  | 0:10:00                                  | number of smartphones responding to Bluetooth name request |

## Deploying
To deploy this software, see the [deploying section in the twomes-generic-esp-firmware library documentation](https://github.com/energiegedrag-nl/needforheat-generic-firmware/blob/main/docs/deploying/prerequisites.md). The firmware needed can be found as a [release from this repository](https://github.com/energiegedrag-nl/needforheat-presence-detector-firmware/releases).

## Developing
To develop software for, or based on this software, see the [developing section in the twomes-generic-esp-firmware library documentation](https://github.com/energiegedrag-nl/needforheat-generic-firmware/blob/main/docs/starting/prerequisites.md)

## Supported devices
This example was tested on:
- [M5Stack CoreInk](https://github.com/m5stack/M5-CoreInk)

This example still needs to be tested n:
- [LilyGO TTGO T7 Mini32 V1.3 ESP32](https://github.com/LilyGO/ESP32-MINI-32-V1.3)

## Features
The example features all generic firmware tasks.

Ready:
* Generic firmware tasks using the [twomes-generic-esp-firmware](https://github.com/energiegedrag-nl/needforheat-generic-firmware) library, including presence detection based on Bluetooth name requests.

## Status
Project is: _in progress_

## License
This software is available under the [Apache 2.0 license](./LICENSE), Copyright 2022 [Research group Energy Transition, Windesheim University of Applied Sciences](https://windesheim.nl/energietransitie) 

## Citation

If you use this repository in your research or work, please cite the following pre-print, which describes the overall NeedForHeat DataGear system of which this repository is a part:

> Ter Hofte, H., & van Ravenzwaaij, N. (2025). *NeedForHeat DataGear: An Open Monitoring System to Accelerate the Residential Heating Transition*. arXiv preprint arXiv:2509.06927. https://doi.org/10.48550/arXiv.2509.06927

**Note:** This is a pre-print submitted on 8 Sep 2025 and has not yet been peer-reviewed. For the full paper, see [https://arxiv.org/abs/2509.06927](https://arxiv.org/abs/2509.06927).

## Credits
Author:
* Henri ter Hofte · [@henriterhofte](https://github.com/henriterhofte)

This repository continues [energietransitie/needforheat-presence-detector-firmware](https://github.com/energietransitie/needforheat-presence-detector-firmware), made by the Research group Energy Transition at Windesheim University of Applied Sciences.
Thanks to the authors and contributors of the original:
* Nick van Ravenzwaaij · [@n-vr](https://github.com/n-vr)

We use and gratefully acknowlegde the efforts of the makers of the following source code and libraries:
* [ESP-IDF](https://github.com/espressif/esp-idf), by Espressif Systems, licensed under [Apache License 2.0](https://github.com/espressif/esp-idf/blob/9d34a1cd42f6f63b3c699c3fe8ec7216dd56f36a/LICENSE)
* [twomes-generic-esp-firmware](https://github.com/energiegedrag-nl/needforheat-generic-firmware), by [Research group Energy Transition, Windesheim University of Applied Sciences](https://windesheim.nl/energietransitie), licensed under [Apache License 2.0](https://github.com/energiegedrag-nl/needforheat-generic-firmware/blob/main/LICENSE.md)

### AI assistance

Since November 2026, parts of the maintenance of this repository have been done with [Claude Code](https://claude.com/claude-code) (Anthropic), under the author's direction and review. Commits made this way carry a `Co-Authored-By: Claude …` trailer. The author remains responsible for all content.
