# Bo
**Bo** is a flavour of the MediaWiki [Chameleon skin](https://www.mediawiki.org/wiki/Skin:Chameleon) specially crafted for [Amereida](http://www.amereida.cl) and later for [Casiopea](http://wiki.ead.pucv.cl), which have separate layouts.

**Bo** is named after the poet **Efraín Tomás Bó**.

## Installation

You can install **Bo** using [Composer](https://getcomposer.org/).

On the root of your MediaWiki installation, run:

```
COMPOSER=composer.local.json composer require --no-update eadpucv/bo-skin:^2

composer update eadpucv/bo-skin --no-dev -o
```

This will also install the [Chameleon skin](https://www.mediawiki.org/wiki/Skin:Chameleon) and other required packages.

For making it work you need to modify your  "LocalSettings.php" as follows:

```php
# - LOAD SKIN
wfLoadSkin( 'chameleon' );

# -- BO SETTINGS
## --------------------------------------------- layout --------------------------------------------
$egChameleonLayoutFile= "$IP/skins/bo/layouts/layout-2022.xml";

## --------------------------------------------- theme  --------------------------------------------
$egChameleonThemeFile  = "$IP/skins/bo/scss/bo-riables.scss";

## --------------------------------------------- bo     ---------------------------------------------
$egChameleonExternalStyleModules = [
  $IP . '/skins/bo/scss/bo.scss' => 'afterFunctions'
];
```
