# 04 — Detector feedback design (fictional software project, April)

The controller's intended design is to update `residual_history` whenever an anomaly detector raises an alarm and to read that history before applying feedback correction.

The plan also requires an integration test that confirms the **controller state changed**, not merely that the detector emitted an alarm. The plan itself is not evidence that the wiring was deployed.
