# 7Revamped

### Office 2021 on Windows 7 — a compatibility research project by @Bwinex

I started with a practical question: could Word and Excel from Office 2021 run on Windows 7? The project grew into **7Revamped for Office 2021**, a guided installer for 32-bit and 64-bit Windows 7 SP1, with PowerPoint added along the way.

My aim is to make the setup easier to follow and document what works, what fails, and what still needs testing. This repository documents the research, installation experience and tested results.

![7Revamped installer running on Windows 7](assets/installer-windows7.png)

*Installer interface on Windows 7 Home Premium SP1, 32-bit. An open installer window demonstrates the interface; application results are recorded separately below.*

**[Package information](DOWNLOADS.md)** · **[Research story](RESEARCH.md)** · **[Tested results](TESTING.md)** · **[Installation walkthrough](INSTALLATION.md)** · **[v0.7 changes](CHANGELOG.md)** · **[Credits](CREDITS.md)**

## What it does

- Lets you choose Word, Excel and PowerPoint.
- Detects 32-bit or 64-bit Windows and selects matching preparation components.
- Checks installation files and the Office media drive.
- Saves installation progress and guides you through restarts.

Office applications install in **32-bit on either Windows architecture**. The research uses Windows 7 **SP1** and the English **ProPlus2021Retail build 16.0.16327.20264**. Other Office builds and languages are not interchangeable with the tested setup.

## Tested Office configuration

| Item | Research configuration |
| --- | --- |
| Office product | Office Professional Plus 2021 Retail (`ProPlus2021Retail`) |
| Office build | **16.0.16327.20264** |
| Media language | English (`en-us`) |
| Media used in the lab | `ProPlus2021Retail.img` |
| Applications | Word, Excel and PowerPoint |
| Application architecture | 32-bit Office on both x86 and x64 Windows |
| Windows baseline | Windows 7 with Service Pack 1 |
| Lab environment | VirtualBox virtual machines |

A filename alone does not identify a compatible image. The edition, language and build must match. An image renamed to `ProPlus2021Retail.img` is not necessarily the media used in this research.

## What success means here

The project goes beyond reaching an installer completion screen. Earlier detailed checks included creating documents, calculating formulas, saving and reopening files, and running a presentation. Word and Excel were also checked after remaining open for several minutes. These checks cover basic use, not every feature or workload.

Across the research, basic application checks passed on Ultimate and Home Premium in both Windows architectures, and Professional x64. The [test matrix](TESTING.md) identifies the package used for each result; an earlier successful test is not automatically a v0.7 certification.

## Current milestone: v0.7

v0.7 adds a compiled welcome launcher, compiled readiness checks and clearer interface wording. I completed a manual installation on Windows 7 Ultimate SP1 x64 and reported that it worked. That run does not yet have the same detailed delayed-edit, save and reopen record as earlier tests. The full [test matrix](TESTING.md) separates versions and evidence levels.

## Downloads

- **[Download v0.7 ZIP](https://github.com/huzbag/7Revamped-Office2021/releases/download/v0.7/7Revamped-Office2021-v0.7.zip)** — extract before opening.
- **[Download v0.7 ISO](https://github.com/huzbag/7Revamped-Office2021/releases/download/v0.7/7Revamped-Office2021-v0.7.iso)** — mount as a virtual DVD.

[Release notes and checksums](https://github.com/huzbag/7Revamped-Office2021/releases/tag/v0.7) · [Package guide](DOWNLOADS.md)

Both archives contain the same 305 kit files. Supply your own matching Office image separately. The kit contains supporting scripts and bundled components; it does not include a complete Office or Windows installation image, activation tools or a product key. Compiled components and scripts remain inspectable.

GitHub's **Code → Download ZIP** downloads repository documentation, not the prepared installer. Use the release links above, then follow the [installation walkthrough](INSTALLATION.md).

## Research milestones

| Stage | Main change |
| --- | --- |
| Initial experiments | Established the Office 2021 target and investigated setup and delayed application failures |
| v0.4 | Improved setup preparation for the observed installation failure |
| x86 R2 | Developed and repeated the route for 32-bit Windows |
| v0.6 | Combined x86 and x64 preparation into one guided installer |
| v0.7 | Added a compiled entry point, compiled checks and clearer interface wording |

[Read the change history](CHANGELOG.md) for the evidence and limitations behind these milestones.

## Installation at a glance

**Prepare Windows 7 SP1 → extract or mount the kit → mount matching Office media → choose apps → follow setup and restarts → test your files.**

The ZIP is convenient for a normal PC; the ISO can be mounted as a virtual DVD. Both represent the same kit. The Office installation image is supplied separately. See the [full walkthrough](INSTALLATION.md).

## Known limits

This is independent compatibility research, not a Microsoft-supported Office configuration. Optional PowerPoint AI helpers are disabled, and some newer touch/WinRT features remain unavailable or unvalidated. Physical PCs, other hypervisors, printers, add-ins, large documents and every Office feature have not been covered by the recorded tests.

Normal Office licensing requirements still apply. The project does not activate Office.

## Share feedback

Use [Issues](https://github.com/huzbag/7Revamped-Office2021/issues) to share questions, ideas or a reproducible problem. Include Windows edition, SP1 status, 32/64-bit architecture, kit version, application and steps taken. Remove personal information from screenshots and logs; do not post product keys or passwords.

Project direction and hands-on testing: **@Bwinex**. External compatibility work is credited in [CREDITS.md](CREDITS.md).
