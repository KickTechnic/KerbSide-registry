# KerbSide council registry

The live council registry for the [KerbSide](https://github.com/KickTechnic/KerbSide) UK
bin-collection Android app. The app fetches `registry.json` from this repo's raw URL
(weekly, cached, with a bundled fallback), so **new councils and endpoint fixes ship as a
push to this repo — no app release**.

- `registry.json` — versioned document: `schemaVersion` gates the whole file; each tier-1
  council carries either a declarative JSON recipe or a vendor-platform config
  (`achieve` = Granicus/Firmstep self-service). Tier-3 entries are councils known but not
  yet supported.
- Source of truth lives in the KerbSide app repo (`registry/registry.json`, where it is
  also the app's bundled seed and is fixture-tested); this repo is the publish target.
  Do not edit here directly.

Collection data itself comes from each council's own public endpoints at runtime, on the
user's device. Nothing here contains personal data.
