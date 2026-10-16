# How the project developed

## Starting point

I wanted Office 2021 itself on Windows 7, rather than substituting an older Office version. Word and Excel were the original targets; PowerPoint became a separate compatibility challenge.

## Installation was only the first hurdle

Early attempts reached application windows but later failed. The work had to cover setup preparation, compatibility dependencies, service behavior and delayed application checks. A successful launch was not enough.

One recurring setup result was exit code 17002. Preparing the required integration and protection components before the streaming stage produced a zero-exit setup sequence on the tested baseline. That result is specific to the observed failure: it does not make 17002 a universally solved error.

## Stability and PowerPoint

Delayed Word and Excel failures led to work around the licensing service starting when needed. The installer exposes that choice to the person running it. Normal activation remains separate.

PowerPoint needed additional compatibility handling. Basic presentation operations passed in earlier tests, but optional AI helpers and parts of newer Windows functionality remain outside the validated scope.

## From manual steps to a guided installer

The manual method became a staged kit, then a guided installer with application selection and saved progress. Separate 32-bit Windows experiments led to a combined package that chooses the appropriate Windows components automatically.

v0.7 adds a compiled welcome screen and compiled checks while preserving the installation stages. Compilation does not make a program impossible to inspect, and some supporting scripts remain readable.

## Publisher and Access

The next experiments expanded the application list. Publisher could edit and export a publication, and Access could work with related tables, forms and reports, but both failed when closing. This made shutdown testing an explicit part of the research.

Tracing the failure led to a compatibility-layer cleanup problem. A targeted correction passed the recorded close tests on Ultimate SP1 x64 and Home Premium SP1 x86. The v0.8 preview brings that correction and the additional app choices into the installer; complete package validation is the next step. VxKex remains the external compatibility dependency credited in this project.

## What comes next

I want to strengthen repeatable testing before broadening compatibility claims. The next priorities are clean v0.8 deployments, automatic repair and rollback checks, repeated post-restart application tests, clearer troubleshooting, dependency review and feedback on the installation experience. Research into other applications may follow later; Office 2021 is the current scope.
