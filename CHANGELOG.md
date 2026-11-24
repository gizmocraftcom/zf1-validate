# Changelog

## 2.0.0

Fork of `diablomedia/zendframework1-validate`, published as `gizmocraft/zendframework1-validate`.

### Breaking changes

- Requires PHP `>=8.5`. Tested on PHP 8.5 and 8.6.
- Package renamed from `diablomedia/zendframework1-validate` to `gizmocraft/zendframework1-validate`. It now requires `gizmocraft/zendframework1-exception` `^2.0.0`, `gizmocraft/zendframework1-config` `^3.0.0`, `gizmocraft/zendframework1-loader` `^2.0.0`, `gizmocraft/zendframework1-registry` `^2.0.0`, `gizmocraft/zendframework1-date` `^2.0.0`, `gizmocraft/zendframework1-filter` `^2.0.0`, `gizmocraft/zendframework1-locale` `^2.0.0` and `gizmocraft/zendframework1-translate` `^2.0.0`. The `suggest` entries for the optional `validate-db`, `validate-ldap`, `validate-file` and `validate-sitemap` packages use the new vendor.

### Other changes

- No public signature changes.
- `Zend_Validate_Date` no longer passes a `null` format to `strpos()`/`strtoupper()` when only a locale is set (deprecated since PHP 8.1, raised on every validation with a locale and an unparsable value). Behaviour is unchanged.
- Dev dependencies upgraded (PHPUnit 13, PHPStan 2.3, php-cs-fixer 3.95, GrumPHP 2.27). Dropped `composer-require-checker`, which has no release for PHP 8.6.
- Tests migrated to PHPUnit 13 attributes. `Zend_Validate_EmailAddressTest::testInstanceWithOldOptions` now restores its error handler.
- Removed one obsolete PHPStan ignore pattern.
- CI runs PHP 8.5 and 8.6.
