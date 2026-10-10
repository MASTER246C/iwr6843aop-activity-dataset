# Collection roadmap

## Phase 1: processed UART (planned)
Standalone IWR6843AOPEVM Rev G point/track outputs for sitting, standing and
walking, with original labels, quality checks and human final review. Zero
samples have been released.

## Phase 2: raw ADC (future option)
A separate compatible capture attachment and validated acquisition workflow
would be needed. No attachment has been selected or purchased by this project,
and no raw-ADC recording capability is supplied here. Keep raw ADC as a separate
modality linked by session IDs, firmware/configuration hashes, calibration,
timestamps and optional synchronized video metadata. More raw data does not by
itself establish better activity-classification accuracy.

Camera synchronization and AI-assisted review are future work, subject to consent
and human decisions. Choose suitable large-data hosting, access and versioned
checksummed manifests before releasing recordings; GitHub is the documentation
and provenance home, not a promise of unlimited dataset storage.
