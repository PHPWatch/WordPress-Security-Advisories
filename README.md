WordPress Security Advisories
==========================

Inspired [Roave/SecurityAdvisories](https://github.com/Roave/SecurityAdvisories), this package aims to provide rudimentary protection against installing known WordPress core packages, plugins, and themes. 

This package itself does not add any code changes to your WordPress site. This is not a plugin that you can install. 

To make use of this, add this package to your composer setup:

```bash
composer require phpwatch/wordpress-security-advisories --dev
```

After adding this package, if you try to `require` a package with a known vulnerability, it will be blocked. 
