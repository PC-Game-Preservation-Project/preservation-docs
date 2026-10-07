# CD/DVD Disc Images & Copy Protection FAQ

This collection contains archival images of original PC CD-ROM and DVD-ROM releases. Some discs use copy protection that depends on information which cannot be stored in an ordinary disc image.

This FAQ explains the available image formats, what the **CP** column means, and what may be needed to run a copy-protected title.

## What type of disc image should I download?

All CDs in these collections are available in **BIN/CUE** format, and all DVDs are available in **ISO** format.

For most discs, this is all that is needed.

Some copy-protected discs require additional information that BIN/CUE or ISO cannot store. When this information has been preserved, an additional **CloneCD** or **MDS/MDF** image is also provided.

The important thing to remember is that an image can be a correct archival copy of the disc's normal data without necessarily containing everything needed to satisfy the original copy-protection system. BIN/CUE and ISO are the standard archival formats used here; the additional formats are provided when more information is needed for compatibility.

## What are BIN and CUE files?

A CD image normally consists of one or more **.bin** files and a **.cue** file.

The BIN file contains the actual contents of the CD. The CUE file describes how the tracks on the CD are arranged.

Think of the BIN files as the contents of the disc and the CUE file as the instructions that explain how those contents fit together.

Keep all of the BIN files and the CUE file together in the same folder.

## What is an ISO file?

An **ISO** is a single-file image commonly used for data DVDs.

All DVDs in these collections are provided as ISO images.

Windows can mount ISO files directly, but this does not mean that every copy-protected DVD will work from the ISO. Some protection systems check information about the original physical DVD that an ISO cannot contain.

## What is a CloneCD image?

A CloneCD image normally consists of three files:

**CCD + IMG + SUB**

The IMG file contains the main disc data, while the other files preserve additional information about the original CD.

CloneCD images are particularly useful for some older copy protections, such as early versions of **SecuROM**, which store important information outside the normal CD data represented by BIN/CUE.

Do not separate the files in a CloneCD image.

## What is an MDS/MDF image?

An MDS/MDF image normally consists of two files:

**MDS + MDF**

The MDF contains the disc data. The MDS contains additional information describing the original disc.

MDS/MDF is especially useful for protections that examine the physical layout of the original CD or DVD. This includes newer SecuROM releases, StarForce, TAGES, and SafeDisc-protected DVDs.

Keep the MDS and MDF files together and mount the **MDS** file.

## Why can't BIN/CUE or ISO contain everything?

Some copy protections deliberately examine characteristics of the original manufactured disc rather than simply checking its files.

Examples include unusual CD subchannel information, deliberately unreadable areas, duplicate sectors, physical sector positions, special DVD information, or even visible physical rings in the disc.

BIN/CUE and ISO were not designed to represent all of these features.

That does **not** mean the BIN/CUE or ISO is a bad dump. It simply means an additional format may be required if the goal is to run the software with its original copy protection intact.

## What does the CP column mean?

**CP** means **Copy Protection**.

The CP column provides a quick indication of whether the standard BIN/CUE or ISO image is expected to work with the original copy protection.

When the column contains a colored two-letter code:

- **Green** means the normal BIN/CUE or ISO image should work as-is when mounted in an appropriate virtual drive.
- **Red** means the normal BIN/CUE or ISO is still a valid archival image, but it is not expected to satisfy the original copy-protection check by itself.

Hover over the value in the **CP** column to display a tooltip showing the detected **copy-protection system and version** for that disc.

When the CP column contains a **disc-image download icon instead of a code**, an additional CloneCD or MDS/MDF image is available. This additional image should be used when attempting to run the software with its original copy protection.

The codes currently used are:

| Code | Protection |
|---|---|
| **LL** | LaserLok |
| **SD** | SafeDisc or SafeDisc Lite |
| **SR** | SecuROM or SecuROM Product Activation |
| **SF** | StarForce |
| **TG** | TAGES |
| **CP** | Another type of copy protection |

The generic **CP** code currently includes protections such as Bitpool, Bitpool & Rings, CD Lock, Rings, SolidShield, Steam, and other less common systems.

The tooltip provides the full protection name and version, so the two-letter code only needs to identify the general protection family.

## What should I download?

For an unprotected disc, download the normal BIN/CUE or ISO.

For a **green CP code**, start with the normal BIN/CUE or ISO.

For a **disc-image download icon**, use the linked CloneCD or MDS/MDF image when attempting to run the protected title.

For a **red CP code with no additional image available**, the normal image is still the archival copy, but the original copy protection may require the physical disc, a compatibility tool, or another workaround.

When more detail is needed, hover over the **CP** value to see the exact copy-protection type and version detected for that disc.

The color shown for the individual title should be considered more useful than the general chart below. Copy-protection systems changed over time, and publishers sometimes configured the same protection differently from one game to another.

# Copy Protection Reference

In the table below, **Standard Image** means the BIN/CUE supplied for a CD or the ISO supplied for a DVD.

**Yes** means the standard image will generally contain what the protection needs. **Sometimes** means it depends on the title, protection version, and virtual-drive software. **No** means another image format or compatibility method is normally required.

| Protection | Version or type | Standard image normally enough to run? | Preferred additional image | Can the standard CD image normally be burned and retain the protection? | Notes |
|---|---|---|---|---|---|
| **Bitpool** | Standard | Sometimes | Usually none | Sometimes | Bitpool relies on deliberately unusual or error-containing CD sectors. A normal burn program may repair those sectors while writing. RAW-capable writing may be required. |
| **Bitpool & Rings** | Combined protection | No | No universally reliable replacement | No | The physical ring is the limiting factor. |
| **CD Lock** | Standard | Usually | Usually none | Usually | Most CD Lock discs can be represented as a normal CD image, although unusual track layouts and oversized or dummy files can complicate copying. |
| **LaserLok** | Various versions | Sometimes | CloneCD when available | Not reliably | LaserLok combines software checks with deliberately difficult-to-read areas and, in some versions, physical mastering features. |
| **Rings / Ring PROTECH** | Physical-ring protection | No | No exact replacement in ordinary image formats | No | The original disc contains a physical ring or no-signal area that a normal CD-R cannot reproduce. |
| **SafeDisc** | 1.x CD | Sometimes | CloneCD may help | Sometimes | Early SafeDisc primarily uses deliberately unreadable or error sectors. RAW-capable hardware and software gives the best chance when writing a physical copy. |
| **SafeDisc** | 2.x-4.x CD | Sometimes | CloneCD may help | Sometimes; highly writer-dependent | SafeDisc 2 introduced additional so-called "weak sectors," making physical copies much more dependent on the CD writer. |
| **SafeDisc Lite** | CD | Sometimes | CloneCD may help | Sometimes | A lighter SafeDisc variant using fewer deliberately bad sectors. |
| **SafeDisc** | DVD | **No** | **MDS/MDF** | No from ISO alone | SafeDisc DVDs use information outside the ISO image. A working preservation image requires additional MDS information. |
| **SecuROM** | Before approximately 4.76 | **No** | **CloneCD** | No from BIN/CUE alone | Older SecuROM uses special CD subchannel information that BIN/CUE does not contain. |
| **SecuROM** | Approx. 4.76 through 4.x | No / Sometimes | CloneCD **or** MDS/MDF | Usually no from BIN/CUE | This is a transition period: some releases use the older method while others use physical-position information. |
| **SecuROM** | 5.x and later disc-check versions | **No** | **MDS/MDF** | No | These releases normally check the physical positioning of data on the original disc. |
| **SecuROM** | DVD disc-check versions | **No** | **MDS/MDF** | No from ISO | SecuROM-protected DVDs use the physical-position method. |
| **SecuROM PA** | Product Activation | Usually | None unless another disc check is also present | Yes as installation media | The important protection is activation rather than the physical image format. Activation availability is a separate issue. |
| **SolidShield** | v1 combined with TAGES | **No** | **MDS/MDF** | No from the standard image | The TAGES portion requires the special image. |
| **SolidShield** | Activation-based v1/v2 | Usually | None | Yes as installation media | The disc itself can normally be imaged conventionally; activation is the separate restriction. |
| **StarForce** | Disc-based versions | **No** | **MDS/MDF** | No | StarForce can authenticate the physical geometry of the original CD or DVD. |
| **Steam** | Steam client/account DRM | **Yes** | None | Yes as installation media | The disc is normally just installation media. Steam itself performs the ownership or account check. |
| **TAGES** | Disc-check version | **No** | **MDS/MDF** | No from BIN/CUE | TAGES uses "twin sectors": two physically different sectors that appear to have the same address. A special image is needed to represent this. |
| **TAGES** | Activation version | Usually | None | Yes as installation media | The disc image itself is conventional; activation is the limiting factor rather than the image format. |

## Can I convert a BIN/CUE or ISO into CloneCD or MDS/MDF?

The file format can be converted, but doing so will **not restore information that was never present in the original image**.

For example, converting an ISO to MDS/MDF does not recreate the physical-disc measurements required by StarForce or newer SecuROM.

Likewise, converting BIN/CUE into CloneCD format does not create missing SecuROM subchannel information.

When a separate CloneCD or MDS/MDF download is provided, it was created from the original disc specifically to preserve the additional information.

## Can I burn the BIN/CUE back to a CD-R?

For an ordinary unprotected CD, generally yes.

Copy-protected CDs are more complicated. Some protections intentionally rely on malformed sectors, unreadable areas, unusual track layouts, or physical features that normal burning software will correct or cannot reproduce at all.

For that reason, **being able to mount an image successfully does not necessarily mean that the same image can be burned to a CD-R and still pass the original protection check**.

SafeDisc in particular can be highly dependent on the CD writer, while ring-based protections and protections based on physical disc geometry generally cannot be recreated accurately on ordinary recordable media.

# Virtual Drive Software

A **virtual drive** makes a disc-image file appear to Windows as though a real CD or DVD has been inserted.

An important distinction is that **supporting an image format is not the same thing as supporting its copy protection**. A program may successfully open an MDS file, for example, but still fail to reproduce the particular physical-disc behavior that the game is checking.

| Virtual drive | BIN/CUE | ISO | CloneCD | MDS/MDF | Best use |
|---|---:|---:|---:|---:|---|
| **DAEMON Tools** | Yes | Yes | Yes | **Yes** | One of the better choices for copy-protected images, especially MDS/MDF. |
| **Alcohol 52% / 120%** | Yes | Yes | Yes | **Yes** | Another strong choice for protected images, particularly MDS/MDF and protections based on physical-disc measurements. |
| **WinCDEmu** | Yes | Yes | Yes | Yes | Excellent free general-purpose mounting software, but being able to open the format does not guarantee that advanced copy protection will work. |
| **Virtual CloneDrive** | Basic BIN support | Yes | **Yes** | No | A good free choice for ordinary images and CloneCD images. |
| **PowerISO** | Yes | Yes | Yes | Yes | Can open and mount a large number of image formats, but recognizing a format does not necessarily mean advanced copy-protection behavior will be reproduced. |
| **Windows built-in ISO mounting** | No | **Yes** | No | No | Fine for ordinary DVDs and ISO images with no special copy-protection requirements. |

For a protected image supplied as **MDS/MDF**, **DAEMON Tools** or **Alcohol** are generally the best places to start.

# Why won't some old games run on Windows 10 or Windows 11 even with the correct image?

There are two separate problems:

1. **Can Windows see a disc that passes the copy-protection check?**
2. **Can the old copy-protection software itself still run on modern Windows?**

Solving the first problem does not necessarily solve the second.

SafeDisc is a particularly common example. Many SafeDisc games use an old driver called **secdrv.sys** that modern Windows blocks for security reasons. As a result, an original SafeDisc CD can fail on Windows 10 or Windows 11 even though there is nothing wrong with the disc.

Community compatibility projects now exist for several of these older systems.

## SafeDiscShim

**SafeDiscShim** is an open-source compatibility tool for SafeDisc games on modern Windows.

Instead of reinstalling the old SafeDisc driver, it intercepts the game's requests to that driver and supplies the expected responses. Its normal mode still expects the original disc or a suitable mounted image.

[SafeDiscShim on GitHub](https://github.com/RibShark/SafeDiscShim)

## SafeDiscLoader2

**SafeDiscLoader2** is another open-source compatibility project. It supports SafeDisc versions **2.0 through 4.9** and is intended specifically to make SafeDisc-protected games work on modern Windows.

Unlike SafeDiscShim's original-disc-oriented approach, SafeDiscLoader2 can handle the SafeDisc check itself and therefore does not necessarily require the protected disc to remain mounted.

[SafeDiscLoader2 on GitHub](https://github.com/nckstwrt/SafeDiscLoader2)

## SecuROMLoader

**SecuROMLoader** is an open-source compatibility project for SecuROM-protected games.

It supports multiple generations of SecuROM and is intended to allow older legally owned games to run on modern versions of Windows without depending on the original obsolete DRM environment.

[SecuROMLoader on GitHub](https://github.com/nckstwrt/SecuROMLoader)

Because compatibility varies between SecuROM versions and individual games, check the project's tested-game list and documentation if a title does not work immediately.

## DiscCheckEmu

**DiscCheckEmu** is a more general open-source compatibility tool for games that perform simpler CD/DVD checks.

It does **not** directly replace active protections such as SafeDisc or SecuROM, but it can handle ordinary disc checks and several passive protection systems, including **Bitpool**.

[DiscCheckEmu on GitHub](https://github.com/Luca1991/DiscCheckEmu)

Pre-made configurations for supported games are available from the project's companion DCEConfigs repository.

## Which method should I try first?

For the simplest experience, follow the **CP column** in the collection.

If it is **green**, try mounting the normal BIN/CUE or ISO.

If an additional-image icon is present, use the supplied CloneCD or MDS/MDF image with an appropriate virtual drive.

If the image mounts correctly but an old SafeDisc or SecuROM title still refuses to start under Windows 10 or Windows 11, the problem may be the obsolete DRM software rather than the disc image. At that point, one of the compatibility projects above may be useful.

For the exact protection type and version used by an individual disc, hover over its **CP** value.

No single virtual drive or compatibility tool works with every title, because these copy-protection systems changed substantially during their lifetimes.
