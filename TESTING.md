# Tested results

The lab used VirtualBox. These results are specific to the listed packages and operating systems; they are not a claim that every Windows 7 configuration works.

| Windows 7 SP1 edition | Windows architecture | Package | Recorded outcome |
| --- | --- | --- | --- |
| Ultimate | x64 | Earlier manual method and v0.4 | Basic Word, Excel and PowerPoint checks passed |
| Professional | x64 | v0.4 | Basic application checks passed |
| Home Premium | x64 | v0.4, guided installer and v0.6 | Installation and basic application checks passed |
| Ultimate | x86 | R2 | Application checks passed, including a clean repeat |
| Home Premium | x86 | R2 and v0.6 | Installation and basic application checks passed |
| Ultimate | x64 | Candidate promoted unchanged to v0.7 | Manual installation reported successful by the researcher; detailed delayed application tests not recorded for this run |
| Home Premium | x86 | v0.7 candidate | Compiled checks and GUI handoff passed; full installation not repeated |

## What the detailed v0.6 checks covered

Clean Home Premium SP1 x86 and x64 installations completed architecture detection, prerequisites, deployment stages, restart/resume and original runtime verification. Word and Excel were left open for 180 seconds before editing/calculation, saving and reopening. PowerPoint was checked for saving, reopening and slideshow operation. Saved files were independently inspected.

These are earlier v0.6 results, not a replacement for a full v0.7 regression test.

## v0.7 checks and remaining work

The 305-file ZIP and ISO were compared file-by-file with the tested candidate. ZIP CRC verification passed. Compiled checks rejected damaged/missing files, invalid file lists, invalid application selections and invalid media. Architecture detection, media detection and readiness checks passed on Home Premium SP1 x86. The clean Ultimate x64 preparation also verified the package and architecture before manual testing.

PowerShell CLR crashes occurred during x86 lab work. One matched a standalone diagnostic script that did not load the new component; an earlier crash remains unattributed. This remains an open investigation.

Next checks: a complete v0.7 x86 deployment, repeatable delayed application checks for v0.7 on both architectures, restart reliability, and broader feature coverage. Professional x86 and physical-PC operation remain untested.

## v0.8 preview — 17 October 2026

The research uses the same English ProPlus2021Retail build **16.0.16327.20264**, with 32-bit Office applications on both Windows architectures.

| System | Publisher after correction | Access after correction |
| --- | --- | --- |
| Ultimate SP1 x64 | Reopened a two-page publication, edited, saved, exported PDF and closed | Reopened database, verified query total, opened form, exported report PDF and closed |
| Home Premium SP1 x86 | Same checks passed | Same checks passed |

The tested processes exited and event-log review found no new corresponding Publisher or Access crashes. Earlier five-minute editing/database tests passed before the correction, but closing failed. Those delayed checks must be repeated with the final package.

Word save/reopen, Excel calculation/save/reopen and PowerPoint save/reopen/slideshow regression actions passed on both systems. An x86 Excel background process remained after automation and needs investigation; passing functional checks does not prove every shutdown path is clean.

### New package checks

- The compiled component built successfully and loaded on both named Windows 7 systems.
- ZIP and ISO readback verified all 307 files and their manifests.
- Package checks rejected altered/missing files, invalid paths, malformed hashes and invalid manifests.
- All 31 nonempty selections of the five apps produced the expected installation choices.
- The new scripts parsed in Windows PowerShell 2 on x86 and x64, and the repair verified the correction already installed in the lab.

### Still pending

These application results came from existing research installations, not clean deployments of the v0.8 preview. Fresh installation, automatic repair application and rollback, restart/resume, repeated manual closing, delayed work after reboot and interface visual validation remain pending. The correction addresses the observed shutdown problem; it does not establish complete compatibility with newer Windows interfaces. Other editions, architectures and features are not implied by these two results.
