# Commonmeta

A metadata standard for scholarly metadata, available via its [website](https://docs.commonmeta.org).

## Documentation

The documentation in `docs/` is built with [Hugo](https://gohugo.io) (extended, v0.147 or later)
and the [Hextra](https://imfing.github.io/hextra/) theme, loaded as a Hugo module (requires Go).

```sh
cd docs
hugo server   # preview at http://localhost:1313
hugo --minify # build into docs/public
```

Pushes to `main` are deployed to GitHub Pages by `.github/workflows/pages.yml`.

## JSON Schema

The canonical Commonmeta JSON Schema is maintained in
[commonmeta-schema](https://codeberg.org/front-matter/commonmeta-schema) and served from
`https://commonmeta.org/commonmeta_v1.0.json`. The documentation keeps a copy of each version in
`docs/static/`, so pre-1.0 versions remain available at `https://docs.commonmeta.org/commonmeta_v0.15.json`
etc. The schema reference page is generated from the version set in `params.schemaVersion` in
`docs/hugo.yaml`. To update the schema, copy the new file from `commonmeta-schema/schemas/` into
`docs/static/`.

## License

This project is licensed under the [MIT License](https://github.com/commonmeta/commonmeta/blob/main/LICENSE).
