# PhpMyAdminInstaller

Simple script for install and configure PhpMyAdmin. The script download it specified version from [www.phpmyadmin.net/downloads/](https://www.phpmyadmin.net/downloads/) (multilanguage version).

## Usage

1. Copy the script to any directory on your server.

2. Declare main vars in script:

- **PMA_VERSION** - version of PhpMyAdmin (example: `PMA_VERSION="4.8.3"`) or `latest` (by default) for download latest stable version.
- **PMA_TEMP_DIR** - path to directory for temporary files (templates cache files). By default script create `tmp` directory in `/usr/share/phpmyadmin` with `777` permissions and set it as directory for temporary files. Be sure that PhpMyAdmin must have write access to directory if you change it. You may use php variables there (ex.: `PMA_TEMP_DIR="'/home/' . \$_SERVER['USER'] . '/tmp/'"`; `$` must be escaped by backslash).

3. Run the script:

```bash
bash pma-installer.sh
```

or

```bash
chmod +x pma-installer.sh
./pma-installer.sh
```

Notices:
- Installed versions from repositories must be removed before using script (recommended);
- There is no need to delete PhpMyAdmin installed with this script. Old versions will be saved in same directory;
- You must be root or user with sudo access.

## Changelog

- 2018.09.03 - 1.0.0 - released