### header
```php
<?
use \Bitrix\Main\Localization\Loc;
use \Bitrix\Main\Application;
use \Bitrix\Main\Page\Asset;

Loc::loadMessages(__FILE__);

$asset = Asset::getInstance();

$asset->addCss(SITE_TEMPLATE_PATH . '/css/bootstrap.min.css');

$asset->addJs(SITE_TEMPLATE_PATH . '/js/jquery-3.3.1.min.js');

$front = CSite::InDir('/index.php');
$uri = explode('/', $APPLICATION->GetCurPage());
?>
<!doctype html>
<html lang="<?=LANGUAGE_ID?>">
<head>
    <title><?$APPLICATION->ShowTitle()?></title>

    <? $APPLICATION->ShowMeta("keywords", false, false); ?>
    <? $APPLICATION->ShowMeta("description", false, false); ?>
    <? $APPLICATION->ShowMeta("robots", false, false);?>

    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, user-scalable=yes, initial-scale=1.0" />
    <meta name="skype_toolbar" content="skype_toolbar_parser_compatible" />
    <meta name="format-detection" content="telephone=no, address=no" />

    <?
    $APPLICATION->ShowCSS();

    $APPLICATION->ShowHeadStrings();
    $APPLICATION->ShowHeadScripts();
    ?>
    <script src="https://api-maps.yandex.ru/2.1/?lang=ru_RU" type="text/javascript"></script>

    <link rel="shortcut icon" href="<?= SITE_TEMPLATE_PATH?>/favicon.ico" type="image/x-icon" />
</head>
<? $APPLICATION->ShowPanel()?>
<body>
<div class="wrapper">

    <header class="row">
        <div class='container header'>
            <div class='col-md-3 col-sm-5 col-xs-1 logo-wrap'>
                <? if ($front) { ?>
                <span class='top-logo' title='Офис рядом с домом'>Кристалл</span>
                <? } else { ?>
                <a href="/" title=""><span class='top-logo' title='Офис рядом с домом'>Кристалл</span></a>
                <? } ?>
            </div>
            <div class='col-md-9 col-sm-7 col-xs-11 menu-wrap'>
                <nav class="navbar navbar-default">
                    <div class="container-fluid">
                        <div class="navbar-header">
                            <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#navbar-main">
                                <span></span><span></span><span></span>
                            </button>
                        </div>
                        <div class="collapse navbar-collapse navbar-main" id="navbar-main">
                            <ul class="nav navbar-nav">
                                <?$APPLICATION->IncludeComponent(
                                    'bitrix:menu',
                                    'top',
                                    array(
                                        'ROOT_MENU_TYPE' => 'top',
                                        'MAX_LEVEL' => '1',
                                        'USE_EXT' => 'N',
                                        'DELAY' => 'N',
                                        'ALLOW_MULTI_SELECT' => 'N',
                                        'MENU_CACHE_TYPE' => 'A',
                                        'MENU_CACHE_TIME' => 0,
                                        'MENU_CACHE_USE_GROUPS' => 'N',
                                        'MENU_CACHE_GET_VARS' => array(),
                                    )
                                )?>
                            </ul>
                        </div>
                    </div>
                </nav>
            </div>
        </div>
        <div class='container top-address-row'>
            <div class='top-address'>
                <? $APPLICATION->IncludeFile('/includes/topaddress.php', array(), array('MODE' => 'html'));?>
            </div>
        </div>
    </header><!-- .header-->

    <main class="content main-content">
```

### footer
```php
<?
if(!defined('B_PROLOG_INCLUDED') || B_PROLOG_INCLUDED !== true)
    die();
?>
</main><!-- .content -->

</div><!-- .wrapper -->

<footer class="row footer">
    <div class='container'>
        <div class='col-md-6 col-sm-6 pull-right'>
            <div class='ft-address'>
                <? $APPLICATION->IncludeFile('/includes/address.php', array(), array('MODE' => 'html'));?>
            </div>
        </div>
        <div class='col-md-6 col-sm-6 pull-left'>
            <div class='ft-copyr'>
                <p><? $APPLICATION->IncludeFile('/includes/copyright.php', array(), array('MODE' => 'html'));?></p>
                <p class="studio"><? $APPLICATION->IncludeFile('/includes/developer.php', array(), array('MODE' => 'html'));?></p>
            </div>
        </div>
    </div>

</footer><!-- .footer -->

</body>
</html>
```