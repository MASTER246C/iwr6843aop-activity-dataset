# Proposed collection and quality plan

**Mount height is configurable.** Radar Studio pre-fills editable 1219 mm / 0° starting values that must be measured and confirmed before use; they are not a default calibration, and 4 ft (1.2192 m) to the flat top of the bracket is a historical project reference. See [MOUNTING.md](https://github.com/MASTER246C/radar-studio-chromebook/blob/main/MOUNTING.md) for antenna height and its uncertainty. For every collection, measure the final geometry after setting the physical tilt, and record the measurements and their uncertainty in capture metadata.

Status: planning only; zero recordings released. First collection uses processed
UART from the IWR6843AOPEVM Rev G. Do not confuse UART packets/point clouds with
raw ADC samples, firmware BIN files or synthetic demonstrations.

## Before a session
- For original JSON firmware, first follow the [matching viewer's acceptance procedure](https://github.com/MASTER246C/radar-studio-chromebook/blob/main/QUICKSTART.md): verify control status, configure measured geometry and pair both ports without RF. Save the capture JSON and both raw JSONL lanes, then **stop here for review of the initial no-RF receipts**. Startup, configuration and pairing do not implicitly start RF. Only after review and separate authorization should a later manual 1–5 second sensing take, or the exact 0.3.2-rc1 continuous workflow (build `87589b2c32638ae119334c72`), be considered. These hardware checks do not authorize public release.
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

## Camera-assisted review (experimental)
Radar Studio v0.9.0-preview.4 and later include optional local browser camera
recording and an experimental MediaPipe pose-assisted label review page
(`camera-review.html`); see its
[camera workflow](https://github.com/MASTER246C/radar-studio-chromebook/blob/main/CAMERA_WORKFLOW.md).
The recorder's `original_training/camera_import.py` converts a verified recording
folder and review into an original-radar-dataset file. These tools are not
validated, and no camera-assisted sample has been admitted or released.

Use camera recording only with explicit consent for video. Record camera
settings, file hashes, time offset/drift, synchronization method and
uncertainty, extrinsic calibration and coordinate conventions. Synchronization comes from human-matched
events; it is not independently verified. Timestamps and pose landmarks do not
establish radar/camera spatial calibration. Preserve the captured label, AI
proposal/model version/confidence and disagreement flags. A human reviewer
accepts/corrects/rejects each relevant annotation with time and reason. Never
substitute model output or confidence for ground truth. Private review video need
not be published; public video requires a separate consent/privacy clearance.
