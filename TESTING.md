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
