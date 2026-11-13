# Photochrom images (IIIF level 0 thumbnails)

Static thumbnails of the **Photochrom Collection of the Zentralbibliothek Zürich**, served with
GitHub Pages as a IIIF Image API 2.1 service at compliance **level 0** (no image server, only
pre-computed sizes). They are used by the Photochrom research environment:
https://github.com/eliaskreyenbuehl/photochrom

## Source and rights

- Dataset: Photochrom Collection of the Zentralbibliothek Zürich, Zenodo, version 1.1,
  https://doi.org/10.5281/zenodo.24141227
- Images: **Public Domain Mark 1.0**. Metadata of the dataset: CC0.
- Made from the 800 px previews in the dataset (`images-legacy-preview.zip`,
  `images-recatalogued-preview.zip`) with `scripts/build_thumbs_iiif.py` from the code repository.
- For full resolution use the dataset on Zenodo, or e-rara.ch for recatalogued records.

## Layout

```
iiif/<id>/info.json                      IIIF Image API 2.1 info, level 0, lists the available sizes
iiif/<id>/full/300,/0/default.jpg        thumbnail, 300 px wide
```

`<id>` is the image file name in the dataset without extension (field `img` in the code
repository's `data/catalog.json`). The "full" image of this service is the 800 px preview;
only the sizes listed in `info.json` are served.

Example: `https://eliaskreyenbuehl.github.io/photochrom-images/iiif/<id>/full/300,/0/default.jpg`
