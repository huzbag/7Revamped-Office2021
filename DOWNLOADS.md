# v0.7 packages

**Public downloads are pending.** This page describes the existing research packages; it does not provide a public download link yet. The current packages include readable scripts and third-party binaries. Public packaging and dependency notices need review before a more limited distribution can be offered.

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

GitHub **Code → Download ZIP** contains the public documentation and screenshot. It is not the prepared 305-file installer package. No installer download is concealed inside this repository.
