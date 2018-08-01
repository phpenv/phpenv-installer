# phpenv-installer

Install [madumlao/phpenv](https://github.com/madumlao/phpenv) +
[php-build/php-build](https://github.com/php-build/php-build) (and
other plugins), updating all of them when you want to!

## Installation

It's the standard way: installs `phpenv` in $HOME/.phpenv (default
$PHPENV_ROOT value).

```shell
curl -L http://git.io/phpenv-installer \
    | bash
```

### Optional: Installation in other directory (i.e. system-wide)

If you prefer to install `phpenv` in other directory (i.e
`$HOME/myphpenv`), or perhaps system-wide (i.e. `/usr/local/bin/phpenv`),
it's easy: just set $PHPENV_ROOT before the installer command:

```shell
# $HOME/myphpenv
curl -L http://git.io/phpenv-installer \
    | PHPENV_ROOT=$HOME/myphpenv bash
```

```shell
# /usr/local/bin/phpenv
curl -L http://git.io/phpenv-installer \
    | PHPENV_ROOT=/usr/local/bin/phpenv bash
```

> Note: depends on the path, you will need superuser (sudo)
permission. Feel free to ask if you need some help!

## Updating

```shell
phpenv update
```

## Uninstallation

```shell
rm -rf $(phpenv root)
```

<hr>

Inspired by [rbenv-installer](https://github.com/fesplugas/rbenv-installer) and [pyenv-installer](https://github.com/yyuu/pyenv-installer)
