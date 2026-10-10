# Proposed collection and quality plan

**Mount reference height: 2.00 meters from floor to the flat TOP of the tripod mount, excluding screws.**

This is the selected experimental activity-collection setup, with a final **15-degree downward tilt**. The mount reference is not the antenna/chip-center height. After setting the final tilt, measure the signed **vertical** offset from the mount-top reference plane to the antenna/chip center:

**Antenna-center height = 2.00 m + measured signed vertical chip-center offset.**

The chip is above the mount in the current photographed arrangement, so its offset is positive, but its numeric value is still unknown. Do not guess it or substitute 2.00 m for chip height. The owner plans to adjust the setup when ready to load the software; that adjustment and calibration have not yet been completed. This is a repeatable experimental standard, not a universal optimum or a proven most-accurate setting. Verify and record the actual geometry before collection; no firmware `sensorPosition` or other configuration value is inferred here.

Status: planning only; zero recordings released. First collection uses processed
UART from the IWR6843AOPEVM Rev G. Do not confuse UART packets/point clouds with
raw ADC samples, firmware BIN files or synthetic demonstrations.

## Before a session
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
