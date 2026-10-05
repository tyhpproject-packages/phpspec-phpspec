<!-- tyhp-readme:start -->
# tyhpdef/phpspec-phpspec

Tyhp type definitions for `phpspec/phpspec` `8.3.1`.

```bash
composer require --dev tyhpdef/phpspec-phpspec:8.3.1
```

This is a metapackage. Composer also installs `tyhpdef/phpspec-phpspec-impl` (type files).
Require **this** name, not `tyhpdef/phpspec-phpspec-impl`.

See https://tyhplang.com.

## Maintain `phpspec/phpspec`? Ship the types yourself

If you are a Packagist maintainer of `phpspec/phpspec`, you can take over these
types.

Copy `_tyhpdef/` from **`tyhpdef/phpspec-phpspec-impl`** (Apache-2.0; keep the `NOTICE`).
Then either:

1. **Bundle** the files in `phpspec/phpspec` and set `extra.tyhp.package` on
   that `composer.json`, plus
   `"replace": { "tyhpdef/phpspec-phpspec": "self.version" }`, or
2. **Publish a sibling** types package under your vendor, versioned with
   `phpspec/phpspec` (same `X.Y.Z`). Set `extra.tyhp.package` there,
   `require` `phpspec/phpspec` with a real constraint,
   `"replace": { "tyhpdef/phpspec-phpspec": "self.version" }`, and set
   `extra.tyhp.tyhpdef` on `phpspec/phpspec` to your sibling’s Composer name.

Ship that to Packagist first, then open an issue:

https://github.com/tyhpproject/tyhp-runtime-src/issues/new?template=tyhpdef-ownership.yml

We verify Packagist ownership and that the types parse and cover the PHP
API, then stop publishing community tags for those versions. We do not
transfer the `tyhpdef/phpspec-phpspec` Packagist name.

Full process: `TYHPDEF_OWNERSHIP.md` in
https://github.com/tyhpproject/tyhp-runtime-src
<!-- tyhp-readme:end -->
