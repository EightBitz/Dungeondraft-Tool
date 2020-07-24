# EightBitz's Dungeondraft Tools

What follows is a brief description of what this is and what it does, but please read [the full documentation](https://gitlab.com/EightBitz/dungeondraft-tools/-/blob/master/EightBitz's%20Dungeondraft%20Tools.pdf) as it contains important details.

## Getting Started

To use this program, download the following files from this repository, and put them all in the same folder:

* [DDTools.exe](https://gitlab.com/EightBitz/dungeondraft-tools/-/blob/master/DDTools.exe)
* [Newtonsoft.Json.dll](https://gitlab.com/EightBitz/dungeondraft-tools/-/blob/master/Newtonsoft.Json.dll)
* [dungeondraft-pack.exe](https://gitlab.com/EightBitz/dungeondraft-tools/-/blob/master/dungeondraft-pack.exe)
* [dungeondraft-unpack.exe](https://gitlab.com/EightBitz/dungeondraft-tools/-/blob/master/dungeondraft-pack.exe)

If you want to convert files to .webp format, you will also need to download and install [ImageMagick for Windows](https://imagemagick.org/script/download.php#windows).

You don't need anything from the Source folder unless you want to peek under the hood and look at the code. For those who do, this was written in Visual Basic .NET using Visual Studio 2019, Community Edition.

## What Does it Do?

This program offers six tools to facilitate creating and managing custom asset packs for Dungeondraft.

* Tag assets
* Convert Assets
* Convert Packs
* Copy Assets
* Pack Assets
* Unpack Assets

### Tag Assets

For people who want to create their own custom asset packs, the Tag Assets tool will create a properly
formatted default.dungeondraft_tags file. This is the file that Dungeondraft uses to determine which
assets in the object library are associated with which tags.

### Convert Assets

The Convert Assets tool will convert supported image formats in selected folders to .webp format.
.webp offers lossless compression, so the files on disk end up being smaller. That being said, this will not
save resources in Dungeondraft, as when .webp files are loaded into memory, they are uncompressed.
I added this function at the suggestion of someone on the Dungeondraft Discord server. Whether or not
you find it ultimately beneficial, I will leave to you.

### Convert Packs

This works similar to the Convert Assets tool, except it works on files that are already packed. This tool
calls dungeondraft-unpack.exe to unpack selected files, then it calls ImageMagick to convert assets to
webp, then it repacks the converted asset folders.

### Copy Assets

This tool is primarily designed to copy Campaign Cartographer 3 Plus (CC3+) assets into a
textures\objects and/or textures\portals folder structure for Dungeondraft. This tool will work for other
assets as well, but Campaign Cartographer has two important naming conventions that this tool uses to
manage how it copies assets.

### Pack Assets

This tool will create .dungeondraft_pack files from selected asset folders.

### Unpack Assets

This tool will unpack .dungeondraft_pack files.
This tool will unpack .dungeondraft_pack files.