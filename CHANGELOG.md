# Changelog

## 2026-10-16 — Mounting, schema and camera status

- Supersedes the 2026-10-10 mounting entry below. The 2.00 m / 15-degree selection is historical. Mount height is configurable and must be measured; 4 ft (1.2192 m) to the flat top of the bracket is a historical project reference, not a default or calibration. README and COLLECTION.md now summarize and link Radar Studio's [MOUNTING.md](https://github.com/MASTER246C/radar-studio-chromebook/blob/main/MOUNTING.md) instead of repeating it.
- SCHEMA.md links the real original-radar-dataset v1 JSON Schema and its field mapping in the recorder repository. Exports use integer microseconds. SCHEMA.md remains the planned release schema.
- Camera tooling: Radar Studio v0.9.0-preview.4 and later include optional local camera recording and experimental pose-assisted review, and the recorder can convert a verified recording and review into a dataset file. Synchronization is human-matched, not independently verified; model output is never ground truth. These tools are not validated.
- Add `tools/check_links.py` and CI that checks relative Markdown links on every push and pull request.
- Still 0 released samples. Dataset terms remain pending.

## 2026-10-11 — Hosted Radar Studio launch

- Linked the public hosted viewer for desktop/ChromeOS Chrome with Web Serial; local versioned downloads remain available.
- Clarified matching firmware/configuration, browser-local recording/export and unchanged source-available/no-resale terms.
- Hosting does not broaden hardware/demo compatibility, firmware acceptance or dataset-publication permission. Existing release tags, artifacts, licenses and notices are unchanged; release manifests continue to describe their frozen packages.


## 2026-10-10 — Mounting standard documentation

- Selected the 2.00 m floor-to-flat-mount-TOP reference, excluding screws, with a final 15-degree downward tilt for the experimental activity setup.
- Antenna-center height remains 2.00 m plus the measured signed vertical offset after tilt; the positive offset in the photographed arrangement has no verified numeric value yet.
- Physical adjustment/calibration is planned, not completed. No optimal-accuracy claim, code change or guessed firmware configuration.
- Documentation-only update. Existing release tags, ZIPs, code and configurations remain unchanged; historical release manifests describe their frozen release snapshots, not these later documentation edits.

## 2026-10-10 — Project beginning
- Created public documentation-only scaffold for IWR6843AOPEVM Rev G activity data.
- Planned sitting/standing/walking collection, quality review and held-out sessions.
- Added proposed metadata/annotation schema and future camera/AI review roadmap.
- Released zero capture files. Final dataset terms and attribution remain pending.
- Planned sit-to-stand and motion-onset events on a separate annotation axis, with boundaries, operational definitions and uncertainty; no events collected.
