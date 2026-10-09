# NES Clone to Bluetooth

A hardware-reuse project exploring whether a wireless retro game-stick controller can be adapted to work as a Bluetooth game controller with an iPhone and the Delta emulator.

The goal is to keep the original controller's NES-style buttons and feel instead of replacing it with a different controller.

> **Status:** Early research / planning. The controller has not been opened or tested yet, and no working Bluetooth conversion has been demonstrated.

## Project goals

- [ ] Open the controller and photograph both sides of the PCB.
- [ ] Identify the radio chip, microcontroller, and other important components.
- [ ] Investigate how the controller's original wireless connection works, even though the original USB receiver is not available.
- [ ] Decide whether the original electronics can be reused or whether a different input-reading approach is needed.
- [ ] Test a suitable ESP32 development board for Bluetooth gamepad support.
- [ ] Build a bridge from the controller's button inputs to a Bluetooth gamepad, if the hardware makes that practical.
- [ ] Pair with an iPhone and test the controls in Delta.

## Hardware

### Existing

- Wireless NES-style controller from a **Babibubary Extreme Mini Game Box / Retro Game Stick 2.1** kit.
- iPhone running Delta (intended test device).

### Planned

- ESP32 development board (exact model not chosen yet).
- Any additional radio or interface hardware identified during research.

**Important:** The original USB receiver is not available, so the original wireless link may be harder to investigate directly. An ESP32's Bluetooth capability does not automatically let it receive every proprietary 2.4 GHz controller signal. The controller's chips and circuitry need to be identified first. The project may require additional hardware or a different approach.

## How it might work

1. Inspect the controller's PCB and identify its chips.
2. Determine what signals are available inside the controller when buttons are pressed.
3. Investigate whether the original radio hardware or protocol can be reused without the receiver.
4. Choose a practical way to read the button inputs.
5. Send the inputs to the iPhone using a Bluetooth gamepad implementation supported by iOS.

This is an investigation, not a confirmed design. The steps may change as new information is discovered.

## Research notes

Record findings here as the project develops:

- **Controller model:** Babibubary Extreme Mini Game Box / Retro Game Stick 2.1 kit.
- **Original USB receiver:** Not available.
- **PCB inspection:** Not started.
- **Radio protocol:** Unknown.
- **Bluetooth implementation:** Not chosen.
- **Delta compatibility:** Not tested.

## Experiments

For each experiment, write down:

- **Date**
- **Question:** What are you trying to find out?
- **Setup:** Hardware, wiring, software, and tools used.
- **Steps:** What you did.
- **Result:** What happened, including failures.
- **Conclusion:** What you learned and what to try next.

Failed experiments are useful documentation too. Keep observations separate from guesses, and don't mark a feature complete until it has actually been tested.

## Development log

Add dated entries as real progress happens. Example:

```text
### YYYY-MM-DD — First PCB inspection
- Goal:
- Observations:
- Photos / measurements:
- Result:
- Next step:
```

## Safety

Disconnect the controller's battery or power source before soldering or making wiring changes. Avoid shorting battery contacts, and verify power and ground before connecting an ESP32.

## License

The project code is intended to be released under the MIT License. See [LICENSE](LICENSE) if the license file is present. Hardware designs, photos, and documentation may need separate licensing if they are added later.
