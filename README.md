# Llamafile debian utils package

## Why?

The [.llamafile files](https://github.com/Mozilla-Ocho/llamafile) operate using a bundle of files with the Llamafile main binary inside. Each binary version of Llamafile is important, as it may introduce new features, improvements, or bug fixes. When you update the Llamafile binary version, it's crucial to ensure that all bundles (with the models) (a.k.a .llamafile files) are updated accordingly, or you'll be using an old version in the bundle. To create these new bundles, you will need the latest utilities.

## What this deb pkg contains

This repository releases a Debian (.deb) package containing the latest utilities (extracted from the original binaries) required for creating llamafiles:

 * llamafile binary
 * zipalign binary
 * llamafile tokenize

## How to install it 

Search in the [release section](https://github.com/vicendominguez/llamafile-utils/releases) the deb pkg version you want. Example:

```
curl -Ls https://github.com/vicendominguez/llamafile-utils/releases/download/0.8.1/llamafile-utils_0.8.1_amd64.deb -o /tmp/llamafile-utils_0.8.1_amd64.deb 

sudo dpkg -i /tmp/llamafile-utils_0.8.1_amd64.deb && rm /tmp/llamafile-utils_0.8.1_amd64.deb
```

## Internals: How to create new deb version

 - create a tag here using `git tag` with the same [llamafile binaries version](https://github.com/Mozilla-Ocho/llamafile/releases)
 - `git push --tags` 

# The real and main project

 * [Llamafile](https://github.com/Mozilla-Ocho/llamafile)
