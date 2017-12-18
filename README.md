# WooCommerce Git Hooks

Collection of WooCommerce core git hooks.

## Installation

```bash
composer require woocommerce/woocommerce-git-hooks
```

## Usage

Include the follow lines into the project's `composer.json`:

```
    "scripts": {
        "pre-update-cmd": "WooCommerce\\GitHooks\\Hooks::preHooks",
        "pre-install-cmd": "WooCommerce\\GitHooks\\Hooks::preHooks",
        "post-update-cmd": "WooCommerce\\GitHooks\\Hooks::postHooks",
        "post-install-cmd": "WooCommerce\\GitHooks\\Hooks::postHooks"
    }
```

### Manual setup (optional)

By default should already run all commands from composer `scripts` when installed, but if necessary run it manually is possible with the follow commands:

```bash
composer run-script pre-update-cmd
composer run-script post-update-cmd
```

## Release history

- 2017-12-18 - 1.0.5 - Fixed how check for `phpcs.xml.dist`.
- 2017-12-18 - 1.0.4 - Auto detects `phpcs.xml` or `phpcs.xml.dist` by default. No longer accepts `phpcs.ruleset.xml`.
- 2017-11-09 - 1.0.3 - Removed list of ignored directories.
- 2017-09-27 - 1.0.2 - Uses `phpcs.ruleset.xml` instead of `dev.ruleset.xml`.
- 2017-07-20 - 1.0.1 - Ignore 3rd party libraries and legacy code.
- 2017-06-26 - 1.0.0 - Initial release.

## Sources

Inspired by:

- <https://github.com/juizmill/git-hooks>
- <https://github.com/smgladkovskiy/phpcs-git-pre-commit>
