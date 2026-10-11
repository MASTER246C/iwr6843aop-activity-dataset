# Proposed collection and quality plan

**Mount height is configurable. Current user-reported reference: 4 feet (1.2192 m) from floor to the flat TOP of the bracket, excluding screws.**

The chip center is above that reference in the photographed arrangement. Its signed vertical offset is **estimated at +0.003175 to +0.00635 m**, giving an **estimated antenna-height interval of 1.222375–1.22555 m**. The midpoint is about **1.224 m**; it is not a calibrated measurement. **Actual downward tilt is unconfirmed.** Measure the final geometry after setting the physical tilt, and preserve the uncertainty in capture metadata.

**Antenna-center height = measured mount-top reference height + measured signed vertical chip-center offset after final tilt.** The mount reference is not the chip height. Do not guess the offset, replace it with zero, or apply an extra cosine to an already vertical offset. Verify point and track coordinate conventions separately before applying a transform; do not infer a firmware `sensorPosition` or claim calibrated angles from these estimates.

The earlier **2.00 m / 15-degree** arrangement was a planned experimental reference and remains in historical examples and frozen releases. It is **not the current setup, a mandatory height, a universal optimum or a proven most-accurate setting**. Earlier underside-to-board-bottom measurements are not used for the chip-center offset. Physical calibration remains unverified.

Status: planning only; zero recordings released. First collection uses processed
UART from the IWR6843AOPEVM Rev G. Do not confuse UART packets/point clouds with
raw ADC samples, firmware BIN files or synthetic demonstrations.

## Before a session
- For original JSON firmware, first follow the [matching viewer's acceptance procedure](https://github.com/MASTER246C/radar-studio-chromebook/blob/main/QUICKSTART.md): verify control status, configure measured geometry and pair both ports without RF. Save the capture JSON and both raw JSONL lanes, then **stop here for review of the initial no-RF receipts**. Startup, configuration and pairing do not implicitly start RF. Only after review and separate authorization should a later manual 1–5 second sensing take be considered. These hardware checks do not authorize public release.
- Record board revision, firmware identifier/hash, exact CFG hash, output protocol,
  baud rates, frame period and viewer/export version. Obtain TI files officially;
  vendor binaries/configuration contents are not included in this repository.
- Record mounting height, orientation, sensor coordinates, room/environment and
  relevant obstructions. Keep a documented calibration procedure and its result;
  do not call measurements calibrated solely because metadata is present.
- Obtain informed participant permission for collection, public distribution and
  intended downstream use. Keep identities, signed forms and contact details
  privately; public records use non-identifying participant/session IDs.
- Record whether others could enter the sensing area. Pause or exclude captures
  involving unconsenting bystanders. Public radar data is not automatically anonymous.

## Labels and quality
Define sitting, standing and walking operationally before collection, including
transition boundaries, stationary pauses and ambiguous intervals. Preserve the
original operator label. Mark transitions/unknowns explicitly rather than forcing
all frames into three classes. Review packet loss, timing gaps, truncation,
clipping, parser errors, activity boundaries and configuration consistency.
Document exclusions without silently erasing original annotations.

## Splits
Split by complete session and participant where feasible, not random adjacent
frames. Keep overlapping windows and duplicated/derived recordings in one split.
Reserve held-out sessions/participants before model selection. Report the actual
split manifest and limitations; no split or benchmark exists yet.

## Future camera-assisted review (not implemented)
If explicitly consented, synchronized video may support annotation. Record camera
settings, file hashes, time offset/drift, synchronization method and uncertainty,
extrinsic calibration and coordinate conventions. Preserve the captured label,
AI proposal/model version/confidence and disagreement flags. A human reviewer
accepts/corrects/rejects each relevant annotation with time and reason. Never
substitute model confidence for ground truth. Private review video need not be
published; public video requires a separate consent/privacy clearance.
