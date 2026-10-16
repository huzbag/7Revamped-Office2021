# Packages

## v0.8 preview

The preview adds optional Publisher and Access selection and the tested closing-crash correction. **Use a backed-up test system. Full fresh installation, automatic repair/rollback and restart validation of this package remain pending.** Existing v0.7 downloads stay available below.

**[Download preview ZIP](https://github.com/huzbag/7Revamped-Office2021/releases/download/v0.8-preview.1/7Revamped-Office2021-v0.8-candidate.zip)** · **[Download preview ISO](https://github.com/huzbag/7Revamped-Office2021/releases/download/v0.8-preview.1/7Revamped-Office2021-v0.8-candidate.iso)** · **[Preview release notes](https://github.com/huzbag/7Revamped-Office2021/releases/tag/v0.8-preview.1)**

| Format | Filename | Size |
| --- | --- | --- |
| ZIP | `7Revamped-Office2021-v0.8-candidate.zip` | 164,983,408 bytes |
| ISO | `7Revamped-Office2021-v0.8-candidate.iso` | 294,467,584 bytes |

Both contain the same 307 files. The `candidate` filename identifies the preview; it has not been renamed or rebuilt for publication. File hashes and archive readback passed. These checks verify packaging, not a complete Office deployment.

Preview ZIP SHA256: `130dcdea782bad76e75d1cfe6727f8998fa45b4f9ffaeca7f61af4c302a00d8d`

Preview ISO SHA256: `b34e185bcae4f4736fc511be291c886535236b1ca442b019e037bab1af8fa777`

The release includes both checksum files and verification reports. See [preview validation](TESTING.md#v08-preview--17-october-2026). The packages include readable supporting scripts and bundled components; they are not a way to conceal every implementation detail.

## v0.7 packages

**[Download ZIP](https://github.com/huzbag/7Revamped-Office2021/releases/download/v0.7/7Revamped-Office2021-v0.7.zip)** · **[Download ISO](https://github.com/huzbag/7Revamped-Office2021/releases/download/v0.7/7Revamped-Office2021-v0.7.iso)** · **[All release assets](https://github.com/huzbag/7Revamped-Office2021/releases/tag/v0.7)**

These are the existing v0.7 research packages, published without changes to their contents. They include readable supporting scripts and third-party components. Public availability does not establish additional runtime validation or grant rights beyond the applicable terms of each component.

## ZIP or ISO?

| Format | Filename | Size | How it is used |
| --- | --- | --- | --- |
| ZIP | `7Revamped-Office2021-v0.7.zip` | 164,981,196 bytes (157.34 MiB) | Extract the entire archive, then open `7Revamped.exe` from the extracted folder |
| ISO | `7Revamped-Office2021-v0.7.iso` | 294,459,392 bytes (280.82 MiB) | Mount as a virtual DVD, then open the launcher from that drive |

Both contain the same 305 kit files. The ISO is the **7Revamped kit disc**, not the Office installation image. Neither package includes the complete Office image or a Windows installation image. This does not mean the packages contain no Microsoft components.

## Package integrity

These SHA256 values identify the existing v0.7 artifacts. A matching hash confirms byte identity with that artifact, not universal compatibility or software safety.

**ZIP**
```text
0db65a0d82a7953f372cc97cb5a3d7432d0d29ea36818eb3816f21cd460f98bd
```

**ISO**
```text
f697d051fdf820903283c4eee23c2a6cbe89096f34cf0806e24b7f7ae43a8153
```

The ZIP passed CRC checks. Every file in both archives was compared with the frozen v0.7 candidate. See [TESTING.md](TESTING.md) for runtime evidence and limits.

## Separate Office media

The tested media is English Office Professional Plus 2021 Retail (`ProPlus2021Retail`), build **16.0.16327.20264**. The lab used an `.img` file. Supply a legitimately obtained matching image and retain normal Office licensing. The kit does not activate Office or provide a product key.

## About the repository ZIP

GitHub **Code → Download ZIP** contains the public documentation and screenshot. It is not a prepared installer package. Use the prepared release assets linked above for installation.
