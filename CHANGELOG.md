## Release 0.3.0

## New features

* **Added `target_mapping` parameter in `resolve_reference` task** ([#1405](https://github.com/puppetlabs/bolt/issues/1405))

  The `resolve_reference` task has a new `target_mapping` parameter that accepts a hash of target attributes and the resource values to populate them with.

* **Added `state` parameter in the `resolve_reference` task** ([#1405](https://github.com/puppetlabs/bolt/issues/1405))

  The `statefile` parameter for the `resolve_reference` task has been replaced with a `state` parameter to maintain consistency among the other tasks and plans in the module.

### Bug fixes

* **Raise error when remote state cannot be loaded** ([#1436](https://github.com/puppetlabs/bolt/issues/1436))

  When attempting to load remote state from a non-existent state file, `terraform` would return a `nil` value which would be loaded into the inventory and cause Bolt to error. The `terraform` plugin now checks whether the attempt to load remote state returned any data and errors if it did not.

## Release 0.2.0

### Bug fixes

* **Expand `dir` path relative to Boltdir** ([#1162](https://github.com/puppetlabs/bolt/issues/1162))

  The `dir` option will now be expanded relative to the active Boltdir the user is running bolt with, instead of the current working directory they ran Bolt from. This is part of standardizing all configurable paths in Bolt to be relative to the Boltdir.

## Release 0.1.0

This is the initial release.
