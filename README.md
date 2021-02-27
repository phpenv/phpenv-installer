# phpenv-installer

Install [phpenv](https://github.com/phpenv/phpenv) +
[php-build](https://github.com/php-build/php-build) (and
other plugins), updating all of them when you want to!

## Installation

It's the standard way: installs `phpenv` in $HOME/.phpenv (default
$PHPENV_ROOT value).

```shell
curl -L https://raw.githubusercontent.com/phpenv/phpenv-installer/master/bin/phpenv-installer \
    | bash
```

The script will then instruct you to edit your shell initialization files.

### Optional: Installation in other directory (i.e. system-wide)

If you prefer to install `phpenv` in other directory (i.e
`$HOME/myphpenv`), or perhaps system-wide (i.e. `/usr/local/bin/phpenv`),
it's easy: just set $PHPENV_ROOT before the installer command:

```shell
# $HOME/myphpenv
curl -L https://raw.githubusercontent.com/phpenv/phpenv-installer/master/bin/phpenv-installer \
    | PHPENV_ROOT=$HOME/myphpenv bash
```

```shell
# /usr/local/bin/phpenv
curl -L https://raw.githubusercontent.com/phpenv/phpenv-installer/master/bin/phpenv-installer \
    | PHPENV_ROOT=/usr/local/bin/phpenv bash
```

> Note: depends on the path, you will need superuser (sudo)
permission. You may also want to `sudo chown -R /usr/local/bin/phpenv` so that you can run the phpenv utilities as a regular user. Feel free to ask if you need some help!

## Updating

```shell
phpenv update
```

## Plugins installed by default

- [php-build/php-build](https://github.com/php-build/php-build): allows `phpenv install`
- [madumlao/phpenv-aliases](https://github.com/madumlao/phpenv-aliases): provides aliases for php versions
- [ngyuki/phpenv-composer](https://github.com/ngyuki/phpenv-composer): automatically installs composer script for php version

## Uninstallation

```shell
rm -rf $(phpenv root)
```

<hr>

Inspired by [rbenv-installer](https://github.com/fesplugas/rbenv-installer) and [pyenv-installer](https://github.com/yyuu/pyenv-installer)
