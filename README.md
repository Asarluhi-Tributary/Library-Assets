# Library Assets

This repository stores the images used by Asarluhi's Library and Compendium on
Discord. The documents repository refers to these images by their path, so they
do not need to be copied into the document files.

## Where images go

- Put Library images in [`Library/v1`](Library/v1).
- Put Compendium images in [`Compendium/v1`](Compendium/v1).

Use short lowercase filenames with words separated by hyphens, such as
`genre-guides.png`. PNG is recommended for headers and other artwork that needs
transparency.

An image's location becomes its `assets://` reference in the documents
repository:

```text
Library/v1/genre-guides.png
assets://Library/v1/genre-guides.png

Compendium/v1/header-compendium.png
assets://Compendium/v1/header-compendium.png
```

Copy the matching `assets://` line into the `image` field of a collection or
genre file:

```yaml
image: assets://Library/v1/genre-guides.png
```

## Adding or replacing an image

1. Open or clone this repository with GitHub Desktop.
2. Copy the image into the correct `Library/v1` or `Compendium/v1` folder.
3. Give it a clear lowercase filename.
4. Commit and push the image through GitHub Desktop.
5. Add its `assets://` reference to the appropriate file in the
   [Library-Documents repository](https://github.com/Asarluhi-Tributary/Library-Documents).

Prefer adding a newly named file instead of overwriting an existing image.
Discord and other services may temporarily cache an older image that keeps the
same path. Do not delete an image until you have confirmed that no document
still refers to it.
