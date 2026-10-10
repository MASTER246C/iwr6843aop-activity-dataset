# IWR6843AOP Activity Dataset

**Mount reference height: 2.00 meters from floor to the flat TOP of the tripod mount, excluding screws.**

This is the selected experimental activity-collection setup, with a final **15-degree downward tilt**. The mount reference is not the antenna/chip-center height. After setting the final tilt, measure the signed **vertical** offset from the mount-top reference plane to the antenna/chip center:

**Antenna-center height = 2.00 m + measured signed vertical chip-center offset.**

The chip is above the mount in the current photographed arrangement, so its offset is positive, but its numeric value is still unknown. Do not guess it or substitute 2.00 m for chip height. The owner plans to adjust the setup when ready to load the software; that adjustment and calibration have not yet been completed. This is a repeatable experimental standard, not a universal optimum or a proven most-accurate setting. Verify and record the actual geometry before collection; no firmware `sensorPosition` or other configuration value is inferred here.

**JUST BEGINNING — 0 released samples. Planning scaffold only.**

Planned sitting, standing, and walking motion-signature dataset for the
**Texas Instruments IWR6843AOPEVM (IWR6843AOP), Rev G**. Initial collection
is board-only processed UART output, not raw ADC capture. No trained model,
benchmark, accuracy result or completed collection pipeline is supplied.

## Current status

This repository currently contains planning and documentation only. No capture
files or dataset have been released. Sample counts, capture specifications,
quality checks, and download links will be added only when verified.

## Intended reuse policy

The intended policy will allow research, teaching, commercial AI training, and
selling trained models or services, with persistent credit to the dataset creator
in dataset notices, training records, and model documentation or service credits.
It will not require a credit on every model prediction or answer, or an unsupported
claim that a particular output came from a particular recording.

The final dataset license or use agreement has not yet been adopted. This
statement of intent is not a license grant for unreleased captures. Final terms
and attribution details will accompany any approved dataset release.

## Attribution information

The release will identify the dataset creator, dataset name, version, canonical
source URL, and applicable terms. Downstream dataset copies and model provenance
records should preserve those details. Proposed credit, pending confirmation before the first data release:
“Christopher Kalkowski — IWR6843AOP Activity Dataset”, with the exact version,
canonical URL and final terms. This is a proposed citation, not an adopted grant.

## Release documentation to be added

- Hardware and firmware configuration, radar settings, and capture procedure
- Activity labels, annotation method, sample counts, and capture duration
- Processing steps, file formats, units, and quality checks
- Participant permissions and appropriate privacy review for actual captures
- Known limitations and a documented train/test split method
- Versioned file manifest and checksums

## Separate from the software

This dataset project is separate from [Radar Studio Chromebook](https://github.com/MASTER246C/radar-studio-chromebook). Its future dataset
terms do not change the software's source-available no-resale license. Texas
Instruments software, firmware, SDKs, and other third-party materials remain
subject to their own terms; no rights to them are granted here.

## Documentation

- [Phased collection and hosting roadmap](ROADMAP.md)
- [Collection and quality plan](COLLECTION.md)
- [Proposed record schema](SCHEMA.md)
- [Dataset status and limitations](DATASET_CARD.md)
- [Release checklist](RELEASE_CHECKLIST.md)

Future synchronized camera/radar capture and AI-assisted annotation are roadmap
ideas only. Human review makes the final label decision; AI confidence is not
ground truth. Videos require separate participant permission and privacy review
before any public release. No camera or AI pipeline is implemented here.

## Help validate future labels

See [CONTRIBUTING.md](CONTRIBUTING.md) to volunteer through a GitHub issue.
Accepted human-review contributions can receive opt-in GitHub credit; anonymous
participation is also available. [Acknowledgments](ACKNOWLEDGMENTS.md).

## Related repositories

- [Radar Studio: visualizer and easy-to-run package](https://github.com/MASTER246C/radar-studio-chromebook)
- [Activity Recorder: reusable collection component](https://github.com/MASTER246C/iwr6843aop-activity-recorder)
- [This activity dataset](https://github.com/MASTER246C/iwr6843aop-activity-dataset)

The recorder repository now contains experimental reusable modules and synthetic tests. This dataset still contains no captures; module tests do not establish real-world activity accuracy.

## Submit recordings for review

The activity recorder is the collection tool; the [activity dataset repository](https://github.com/MASTER246C/iwr6843aop-activity-dataset) is for recordings Chris has reviewed and accepted. Contact **dataset@swarmcord.com** first with a short, non-sensitive summary. This owner-provided address has not been delivery-tested here. Do not attach unreviewed personal video or sensitive recordings to a public issue; arrange an appropriate private transfer and permissions first.

Include the export schema/version and firmware path (original JSONL versus TI-compatible capture), file hashes, session IDs, human-observed labels and event boundaries, quality flags, exact configuration/firmware identity, measured or explicitly uncertain mounting/timing metadata, collection context and consent/reuse scope. Keep original labels separate from AI proposals and final human decisions. Do not invent calibration, ground truth or participant permissions.

Chris reviews submissions and adds accepted recordings to the dataset himself. Nothing is uploaded or published automatically. Large recordings need an agreed storage/transfer location; GitHub is not unlimited storage. Accepted review contributions may receive opt-in name/handle credit; anonymous credit is available. Public inclusion and future reuse remain subject to review and final dataset terms.
