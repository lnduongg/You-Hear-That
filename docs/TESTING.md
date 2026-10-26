# Testing & Performance — What Is Verified and What Is Not

## Documented Functional Checks

The 2026 graduation report (section 5.3) records six successful black-box checks:

| Check | Documented result |
|---|---|
| Change CCTV viewpoint | Passed |
| Toggle an interactable lamp | Passed |
| Guide camper across a waypoint route | Passed |
| Collect a key | Passed |
| Trigger camera interference at elevated Time Pressure | Passed |
| Trigger the Secret Ending conditions | Passed |

These six cases are **not** a complete automated regression suite and do not prove that all combinations of choices or all endings were tested exhaustively.

## Performance Capture from Graduation Report

![Unity Profiler screenshot from the graduation report](../media/profiler.png)

*Figure 5-6: profiler screenshot reported in the thesis; this is not a new benchmark.*

## Reported Performance

The graduation report (section 5.4) describes testing on an Acer Nitro 5 with RTX 3050 Laptop GPU using Unity Profiler. Its stated observations are:

- **60–75 FPS** during typical gameplay
- Dips to roughly **55 FPS** when switching viewpoints rapidly
- Approximately **1.2 GB RAM** reported in testing

This is a report of observations, not an independently reproducible benchmark or a measured before/after improvement. Build type, resolution, quality presets, profiler overhead, and detailed sampling conditions should be documented in a future repeatable benchmark.

## Known Limitations

- The graduation report identifies the lack of voice acting and limited visual sophistication of the low-poly art direction.
- Source review suggests opportunities to improve error handling, action dispatch, and separation of responsibilities.
- No independently verified player-retention, downloads, sales, or commercial metrics are available.

## Suggested Next QA Pass

1. Test all intended Good / Bad / Secret ending paths with written steps.
2. Test fast camera switching, missing objects, and scene restarts.
3. Collect Profiler screenshots with version, build configuration, resolution, and hardware noted.
4. Test a standalone Windows build outside the Unity Editor.
