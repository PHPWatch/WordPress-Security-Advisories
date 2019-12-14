WordPress Security Advisories
==========================

Inspired [Roave/SecurityAdvisories](https://github.com/Roave/SecurityAdvisories), this package aims to provide rudimentary protection against installing known WordPress core packages, plugins, and themes. 

This is a **metapackage**, which means it does not add any functional code to your application. This file is purely a JSON file that contains a list of package _conflicts_, which instructs composer to block installation of known vulnerable packages. 

To make use of this, add this package to your composer setup:

```bash
composer require --dev phpwatch/wordpress-security-advisories:dev-master
```

After adding this package, if you try to `require` a package with a known vulnerability, it will be blocked. 


## Additing new packages

Please send a PR. Please see the rules for the WordPress core package when writing your own `conflict` rules.
Packages need to be in alphabetical order. The first two lines are reserved for WordPress core, followed by plugins, and themes at the end. An intentional new line is used to separate core, plugins, and themes.

I intend to keep this list for packages hosted in wordpress.org (thus, available at `wpackagist`). For commercial plugins and themes hosted elsewhere, I suggest you offer your own update endpoints. 

## Coordinated security releases

If you would like to release a security vulnerability for your plugin, and would like to coordinate an update to the list, please _do not_ create a PR/issue. Instead, please contact me with details mentioned in [SECURITY.md](SECURITY.md) file.

## Credits

This package is maintained by [@Ayesh](https://github.com/Ayesh), for [PHP.Watch](https://php.watch).
