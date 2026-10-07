# File Naming Scheme

## General Format

```text
Name (Variant) (Platform) (Year) (Version) (Alt) (Region) (Languages) (Publisher) (Series) (Format) (Disk) [Flag1] [Flag2] ...
```

All fields except **Name** are optional. Parentheses and square brackets shown in the format are part of the filename.

## Fields

| Field | Description |
|---|---|
| **Name** | Software title. |
| **Variant** | Title variant, edition, display mode, or system-specific release. Examples include EGA, VGA, 16 Color, Enhanced, Tandy, and PCjr. |
| **Platform** | Hardware platform, operating environment, or boot/runtime type required by the release. Examples include Booter, C64, IBM PC, Win3.1, and Win2.1. |
| **Year** | Release date for this specific image or release, not necessarily the copyright year. Dates may be written as `YYYY`, `YYYY-MM`, or `YYYY-MM-DD`. More specific dates are used when needed to distinguish between multiple releases. |
| **Version** | Version, revision, or release number. |
| **Alt** | Literal tag indicating an alternate release. This appears as `(Alt)`. |
| **Region** | Region of release. Examples include Europe, UK, France, Germany, Spain, Italy, etc. USA is the default and is not shown unless needed to distinguish a release. |
| **Languages** | Language or languages included in the release. Two-letter codes are used. English is the default and is not shown for USA or other English-language regions. When the region and language identify the same release, only the language is shown. For example, a German release in German is shown as `(De)`, not `(Germany) (De)`. A French/German release is shown as `(Fr, De)` when the regions and languages match. English is shown as `(En)` only when it is part of a non-English-region release. |
| **Publisher** | Regional publisher or publisher credited for this release. |
| **Series** | Publication, magazine, budget line, compilation, or other series associated with the release. |
| **Format** | Disk format or formats included in the archive. Examples include 160K, 180K, 320K, 360K, 720K, 1.2M, and 1.44M. Archives containing multiple disk formats show all applicable formats separated by plus signs, such as `1.2M+360K`. |
| **Disk** | Disk number, disk name, or disk role. Examples include Disk 1, Disk 2, Program, Data, Install, and Play. |
| **Flags** | One or more status flags enclosed in square brackets. Examples include `[!]`, `[M]`, and `[cp]`. |

## Image Flags

| Flag | Name | Description |
|---|---|---|
| `[!]` | **Verified** | The image is verified from two or more matching dumps, or all sectors in the corresponding flux set report as unmodified. |
| `[M]` | **Modified** | The image contains one or more modifications. |
| `[F]` | **Fixed** | Modifications were removed from the image. |
| `[cp]` | **Copy Protected** | The original disk is copy protected. |
| `[cr]` | **Cracked** | Key disk protection has been removed from the image. |

## Flux Set Flags

| Flag | Name | Description |
|---|---|---|
| `[!]` | **Verified** | The flux set is verified from two or more matching dumps, or all sectors report as unmodified. |
| `[M]` | **Modified** | One or more sectors have been modified. |
| `[MW]` | **Modified by Windows** | Modifications appear to have been made by Windows, such as changes to the OEM Name, directory entry created dates, or directory entry last-accessed dates. |
| `[U]` | **Unmodified** | Tracks were written using sector-level duplication and appear to be unmodified. |
| `[MR]` | **Modifications reverted** | Modifications on the disk were reverted to factory defaults prior to dumping. |
| `[B]` | **Bad Sectors** | One or more sectors are bad. |
| `[BU]` | **Bad Sectors in Unallocated Space** | Bad sectors are present only in unallocated regions of the disk. |
| `[INC]` | **Incomplete** | One or more flux sets is missing. |
| `[w]` | **Weak Sectors** | One or more sectors are weak and may not be readable by some tools. |
| `[cp]` | **Copy Protected** | The original disk is copy protected. |
