# TODO – needforheat-presence-detector-firmware

Open work for this repository, distilled from the old NeedForHeat Trello board, including the discussions on the cards (paraphrased and regrouped) and from the 2026 maintenance review.

Items that touch several repositories are written out in full in one *lead* repository; the others list them with a link (→). Keep the details up to date in the lead repository only.

## Now: needed to run at home this winter

- [ ] → Release workflow without the Windesheim signing key — see [needforheat-generic-firmware](https://github.com/energiegedrag-nl/needforheat-generic-firmware/blob/main/TODO.md#unsigned) *(Trello #480)*

## Soon: robustness and correctness

- [ ] <a id="btstab"></a>**Stable Bluetooth presence detection.** Research and fix the instability of Bluetooth presence detection. On the old P1 gateway, ESP-NOW and Bluetooth presence detection seemed to interfere with TLS certificate checks (shared Wi-Fi mutex); check the mbedTLS threading settings and mutex use. Also affects: needforheat-living-room-module-firmware, needforheat-p1-reader-firmware. *(Trello #222, #769)*
- [ ] <a id="pdbuild"></a>**Presence detector builds again with generic v3.3.0+.** PR #5 fails to link: the `sdkconfig` must enable Bluetooth Classic (and the A2DP/GAP parts the presence detection uses). Then move it to v3.4.0 with the buffer partition. Also affects: needforheat-generic-firmware.
- [ ] → Upgrade to ESP-IDF 5.5 (WPA3, Wi-Fi 6) — see [needforheat-generic-firmware](https://github.com/energiegedrag-nl/needforheat-generic-firmware/blob/main/TODO.md#idf) *(Trello #806)*
- [ ] → Let generic and device-specific code share buttons — see [needforheat-generic-firmware](https://github.com/energiegedrag-nl/needforheat-generic-firmware/blob/main/TODO.md#buttons) *(Trello #833)*
- [ ] → Use the ESP-IDF certificate bundle — see [needforheat-generic-firmware](https://github.com/energiegedrag-nl/needforheat-generic-firmware/blob/main/TODO.md#crtbundle)

## Later: features and ideas

- [ ] <a id="room"></a>**Room-level presence.** Use RSSI and several detectors per home (see ESPresense, Bermuda). *(Trello #323)*
- [ ] <a id="pddocs"></a>**Presence detection documentation.** Update the configuration docs for the new onboarding, and fix the `nvs.bin` instructions for Windows (`%IDF_PATH%`). Also affects: needforheat-generic-firmware. *(Trello #821, #697)*
- [ ] → E-ink screen glitches — see [needforheat-generic-firmware](https://github.com/energiegedrag-nl/needforheat-generic-firmware/blob/main/TODO.md#einkfix) *(Trello #860, #862, #870, #686, #996, #822, #363)*
- [ ] → All device-type settings in platformio.ini — see [needforheat-generic-firmware](https://github.com/energiegedrag-nl/needforheat-generic-firmware/blob/main/TODO.md#config) *(Trello #695, #510)*
- [ ] → Presence detection on hardware other than the CoreInk — see [needforheat-generic-firmware](https://github.com/energiegedrag-nl/needforheat-generic-firmware/blob/main/TODO.md#presence-other) *(Trello #829)*
- [ ] → Finish the rename from Twomes to NeedForHeat — see [needforheat-generic-firmware](https://github.com/energiegedrag-nl/needforheat-generic-firmware/blob/main/TODO.md#rename) *(Trello #1030)*
- [ ] → CONTRIBUTING.md with the branching workflow — see [needforheat-generic-firmware](https://github.com/energiegedrag-nl/needforheat-generic-firmware/blob/main/TODO.md#contrib) *(Trello #394, #1032)*
- [ ] → Register phones for presence detection — see [needforheat-server-api](https://github.com/energiegedrag-nl/needforheat-server-api/blob/main/TODO.md#bt) *(Trello #104, #117, #863, #576)*
- [ ] → Fix links and errors in device manuals — see [needforheat-manuals](https://github.com/energiegedrag-nl/needforheat-manuals/blob/prd/TODO.md#manlinks) *(Trello #718, #995, #719)*
