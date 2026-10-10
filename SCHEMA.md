# Proposed schema (not a released data format)

All fields below are design requirements pending a real capture/export audit.
No example row represents an actual participant or recording. Use explicit null
or unavailable reasons rather than invented measurements. Units and coordinate
conventions must be declared per release.

## Session metadata
- schema_version, dataset_version, session_id, pseudonymous_participant_id
- board_model, board_revision, firmware_name, firmware_sha256, cfg_sha256
- protocol_profile, parser_version, capture_tool_version, UART baud rates
- start_time_basis (prefer relative public time), frame_period_s, duration_s
- mounting_height_m, sensor_orientation, coordinate_frame, environment_summary
- calibration_method, calibration_result, calibration_time_relative
- consent_scope_reference (non-identifying), public_release_review_status

## Recording manifest
- recording_id, session_id, relative_path, media_type, byte_size, sha256
- processed_uart_or_decoded_format, units, coordinate_frame, timestamp_basis
- frame_count, missing_or_invalid_frame_count, quality_flags, exclusion_reason
- split_assignment, derivation_parent_ids, processing_steps and software versions

## Annotation history
- annotation_id, recording_id, interval_start_s, interval_end_s
- captured_label (original immutable operator annotation)
- ai_proposed_label, ai_confidence, ai_model_name, ai_model_version (optional)
- review_flag, disagreement_flag, ambiguity_reason
- human_review_status, human_final_label, reviewer_pseudonym, reviewed_at
- decision_reason, prior_annotation_id, annotation_version

Permitted activity vocabulary starts with sitting, standing, walking, transition,
unknown. A final human label is populated only after human review. Keep prior
annotations append-only; corrections reference earlier versions. Automated
proposals and captured labels remain separately accessible.

## Optional future synchronized video
- video_relative_path or private_reference, video_sha256, frame_rate_hz
- radar_to_video_time_offset_s, drift_estimate, synchronization_method,
  synchronization_uncertainty_s
- extrinsic_transform, transform_direction, coordinate_frames,
  calibration_method/version/residuals
- video_consent_scope, privacy_review_status, public_video_release_approved

These fields do not imply a camera pipeline exists or authorize a video upload.
Do not publish private reference values, participant identities, exact private
locations, signed consent forms or unnecessary absolute timestamps.
