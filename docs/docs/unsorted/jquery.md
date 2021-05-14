        $('.contacts form[name="<?=$arResult["IBLOCK_CODE"]?>"]').validate({
            highlight: function( element ){
                $(element).parent().addClass('error');
            },
            unhighlight: function( element ){                       $("#person__check, #person__container").slideDown();

                        var body = $("html, body");
                        body.stop().animate({scrollTop: $("#person__container").offset().top}, 100, 'swing');
                        //isValid = true;
                $(element).parent().removeClass('error');
            },
            submitHandler: function( form ){
                var captcha = grecaptcha.getResponse();

                if( $('.contacts form[name="<?=$arResult["IBLOCK_CODE"]?>"]').valid() && captcha.length){
                    $(form).find('button[type="submit"]').attr("disabled", "disabled");
                    form.submit();
                }
            },
            errorPlacement: function( error, element ){
                error.insertBefore(element);
            }
        });


        $.ajax({
            url: '/ajax/basket/setOrder/',
            type: 'post',
            data: {
                orderData: orderData,
                orderComment: orderComment
            },
            success: function (response) {
                if (response) {

                } else {
                    alert(response.message);
                }
            },
            error: function (response) {
                //console.log(response);
            }
        });

indi.app.blocks.tickets = function () {
    var tickets = this;
    tickets.initDOM = function (domElement) {
        if (typeof domElement == 'undefined') {
            domElement = $('body');
        }
        // пошёл код
        //console.log(13);
    };
    //tickets.initDOM();
};
indi.app.blocks.tickets.exists = function () {
    return ( $('.p-training-booking').length > 0 );
};


    $('.modal-tickets').on('click', function(){

        var ID = $(this).data('id');

        $.get('/ajax/tickets/show/', {'ID': ID},
            function (response) {
                $('#tickets').modal('show');
                $('#tickets .modal-body').html(response);
                indi.app.blocks.tickets.initDOM();
            }
        );

        return false;
    });



    $.extend( $.validator.messages, {
        required: BX.message('JS_REQUIRED'),
        email: BX.message('JS_FORMAT'),
        equalTo: BX.message('JS_PASSWORD_COPY'),
        minlength: BX.message('JS_PASSWORD_LENGTH'),
        remote: BX.message('JS_ERROR')
    });


    $.validator.methods.email = function (value, element) {
        return this.optional(element) || /[a-z]+@[a-z]+\.[a-z]+/.test(value);
    }

    $.validator.addMethod(
        'regexp', function( value, element, regexp ){
            var re = new RegExp( regexp );
            return this.optional( element ) || re.test( value );
        },
        BX.message('JS_FORMAT')
    );

    $.validator.addMethod(
        'filesize', function( value, element, param ){
            return this.optional( element ) || ( element.files[0].size <= param )
        },
        BX.message('JS_FILE_SIZE')
    );

    $.validator.addMethod(
        'date', function( value, element, param ) {
            var status = false;
            if(!value || value.length <= 0){
                status = true;
            }
            else{
                var re = new RegExp('^([0-9]{2})(.)([0-9]{2})(.)([0-9]{4})$');
                var matches = re.exec(value);
                if(matches){
                    var composedDate = new Date(matches[5], (matches[3] - 1), matches[1]);
                    status = ((composedDate.getMonth() == (matches[3] - 1)) && (composedDate.getDate() == matches[1]) && (composedDate.getFullYear() == matches[5]));
                }
            }
            return status;
        }, BX.message('JS_DATE')
    );

    $.validator.addMethod(
        'datetime', function( value, element, param ) {
            var status = false;
            if(!value || value.length <= 0){
                status = true;
            }
            else{
                var re = new RegExp('^([0-9]{2})(.)([0-9]{2})(.)([0-9]{4}) ([0-9]{1,2}):([0-9]{1,2})$');
                var matches = re.exec(value);
                if(matches){
                    var composedDate = new Date(matches[5], (matches[3] - 1), matches[1], matches[6], matches[7]);
                    status = ((composedDate.getMonth() == (matches[3] - 1)) && (composedDate.getDate() == matches[1]) && (composedDate.getFullYear() == matches[5]) && (composedDate.getHours() == matches[6]) && (composedDate.getMinutes() == matches[7]));
                }
            }
            return status;
        }, BX.message('JS_DATETIME')
    );

    $.validator.addMethod(
        'extension', function(value, element, param){
            param = typeof param === 'string' ? param.replace(/,/g, '|') : 'png|jpe?g|gif';
            return this.optional(element) || value.match(new RegExp('.(' + param + ')$', 'i'));
        }, BX.message('JS_FILE_EXT')
    );

    $.validator.addMethod(
        'captcha', function( value, element, params ){
            return $.validator.methods.remote.call(this, value, element,{
                url: arScorpOptions['SITE_DIR'] + 'ajax/check-captcha.php',
                type: 'post',
                data:{
                    captcha_word: value,
                    captcha_sid: function(){
                        return $(element).closest('form').find('input[name="captcha_sid"]').val();
                    }
                }
            });
        },
        BX.message('JS_ERROR')
    );

    $.validator.addClassRules({
        'phone':{
            regexp: arScorpOptions['THEME']['VALIDATE_PHONE_MASK']
        },
        'confirm_password':{
            equalTo: 'input[name="REGISTER\[PASSWORD\]"]',
            minlength: 6
        },
        'password':{
            minlength: 6
        },
        'inputfile':{
            extension: arScorpOptions['THEME']['VALIDATE_FILE_EXT'],
            filesize: 5000000
        },
        'datetime':{
            datetime: ''
        },
        'captcha':{
            captcha: ''
        },
        'recaptcha':{
            recaptcha: ''
        },
        'processing_approval':{
            processing_approval: ''
        }
    });


    window.history.pushState(null, null, '/cart/');
    window.location.reload();

    $.ajax({
        type: "POST",
        url: "",
        data: 'html',
        dataType: 'html',
        success: function(res){
            $('.order-total__price').html($(res).find('.order-total__price').html());
            $('.shop_cart_items_full_price').html($(res).find('.shop_cart_items_full_price').html());
            $('.cart__total-price').html($(res).find('.cart__total-price').html());
        }
    });


    //добавление в корзину из карточки
    $('body').on('click', '.js-toBasket', function () {
        var form = $(this).closest('.js-block').find('form');
        if (form && $(this).data('id') > 0) {
            form.find('[name=id]').val(parseInt($(this).data('id')));
            addToBasket(form);
        } else {
            addToBasket(form);
        }
    });

$(function ()
{


});


function windowSize(){
    if ($(window).width() <= '995'){
        $('#shelf').show(10);
    } else {
        $('#shelf').hide(10);
    }
}
$(window).load(windowSize); // при загрузке
$(window).resize(windowSize); // при изменении размеров
// или "два-в-одном", вместо двух последних строк:
$(window).on('load resize',windowSize);


<div id="banner-insta">
  <div class="container">
    <h2>Instagram Feed</h2>
    <div class="owl-carousel owl-theme" id="banner-insta-target">Loading...</div>
  </div>
</div>
var instabanner = $('#banner-insta-target');
if(instabanner.length){
  // assemble unique URL every hour so content is always fresh
  var d = new Date();
  var hrs = d.getHours();
  var day = d.getDate();

  $.get( "/sites/default/files/cef/instagram/feed.json?"+day+hrs, function( data ) {

    instabanner.html(''); // remove Loading.. placeholder text
    var ouputHtml ="";
    var limit = 10;

    // loop over instagram posts and build output
    for (var i = 0; i < limit; i++) {
      var post = data.data[i];
      ouputHtml += '<div class="insta-post"><a href="'+post.link+'" class="bk-image" style="background-image:url('+post.images.standard_resolution.url+')" alt="'+post.caption.text+'">';
      ouputHtml += '</a></div>';
    }

    // Take the output and inject it into the page
    // then have owlCarousel turn it into a carousel
    instabanner.html( ouputHtml ).owlCarousel({
        autoPlay: 3000, //Set AutoPlay to 3 seconds
    });
  });//end get
}//end if




        function request() {
            var response;
            if (response == true) {
                // This makes it unable to send a new request
                // unless you get response from last request
                response = false;
                var req = $.ajax({
                    type: "POST",
                    url: "/local/components/webway/site_elements/templates/session_modal/session.ajax.php",
                    data: {data: "GET_SESSION_TIME"}
                });
                req.done(function () {
                    console.log("Request successful!");
                    // This makes it able to send new request on the next interval
                    response = true;
                });
            }
            setTimeout(request(),1000);
        }

        request();


$(document).ready(function() {
    setInterval(function() {
        $.get('/local/components/webway/page_elements/templates/session_modal/session.ajax.php',
            function (response) {
                if (response == 'show') {
                    $('#refreshPage').modal('show');
                }
            }
        );
    }, 1000 * 10 * 1);


    $(".modal button").click(function() {
        window.location.reload();
    });
});



        $.ajax({
	        url: arScorpOptions['SITE_DIR'] + 'ajax/basket_items.php',
	        type: 'POST',
	        beforeSend: function(){
		        $buyBlock.addClass('loading');
	        },
	        complete: function(){
		        $buyBlock.removeClass('loading');
	        },
	        success: function(html){
		        $buyBlock.removeClass('in');

		        $('.ajax_basket').html(html);
		        $('.basket_top .items').scrollTop(scrollTop);

		        if(!getCurUri){
			        setTimeout(function(){
				        $('.basket_top .dropdown').addClass('expanded');
			        }, basketShowDelay);

			        setTimeout(function(){
				        $('.basket_top .dropdown').removeClass('expanded');
			        }, basketHideDelay);
		        }
	        }
        });





        $("#applicationForRepair").validate({
	        submitHandler: function(form) {
		        var form = $('#applicationForRepair');
		        var security = $('#email').val();

		        if (security) {
			        $('#applicationForRepair-success').modal('show');
			        form[0].reset();
		        } else {
			        var formData = $(this).serializeArray();

			        $.ajax({
				        url: '/ajax/tech/addPosts/',
				        type: 'POST',
				        data: {
					        data: formData
				        },
				        success: function (response) {
					        if (response) {
						        $('#repairApplicationModal').modal('hide');
						        $('#applicationForRepair-success').modal('show');
						        form[0].reset();
					        } else {
						        alert(response.message);
					        }
				        },
				        error: function (response) {
					        console.log(response);
				        }
			        });
		        }
	        }
        });


        $('.edit-personal-data').find('[type="submit"]').text('Сохранение...');


        var items = [];
        $('.custom-control-input.del').each(function(i) {
	        if ($(this).prop('checked') == true) {
		        items[i] = $(this).attr('id');
	        }

        });


        $("#sendsay_form").validate({
	        rules: {
		        _member_email: {
			        required: true,
			        email: true
		        },
	        },
	        messages: {
		        _member_email: {
			        required: "",
			        email: ""
		        }
	        },
	        submitHandler: function(form) {
		        var loading = new indi.ui.loading('body');
		        form.submit();
	        }
        });



        $(document).ready(function(){
	        $('body').removeClass('loading').addClass('load');
	        $('input').keyup(function(){
		        if($(this).val() != '') {
			        $(this).addClass('hasContent');
		        } else {
			        $(this).removeClass('hasContent');
		        }
	        })

	        $('form').submit(function(e){

		        var name = $('form input[name=Name]');
		        var email = $('form input[name=Email]');
		        var err = [];

		        if(name.val() == '') {
			        name.addClass('error');
			        name.siblings('.input-error').text('Обязательное поле');
			        $('.js-errorbox, .js-error-req').show();
			        err.push('name');
		        } else {
			        name.removeClass('error');
			        name.siblings('.input-error').text('');
			        $('.js-errorbox, .js-error-req').hide();
		        }

		        if(email.val() == '') {
			        email.addClass('error')
			        email.siblings('.input-error').text('Обязательное поле');
			        $('.js-errorbox, .js-error-req').show();
			        err.push('email');
		        } else {
			        if(!validateEmail(email.val())){
				        email.addClass('error')
				        email.siblings('.input-error').text('Некорректный email');
				        $('.js-errorbox, .js-error-email').show();
				        err.push('validate');
			        } else {
				        email.removeClass('error');
				        email.siblings('.input-error').text('');
				        $('.js-errorbox, .js-error-email').hide();
			        }
		        }

		        if(err.length > 0) { return false; } else { $('form').trigger('reset'); $('input').removeClass('hasContent'); $('.js-successbox').show(); }

		        yaCounter46658895.reachGoal('formSend');

		        var request = {
			        "action" : "login",
			        "login" : "x_146641902159406",
			        "sublogin" : "tilda",
			        "passwd" : "wr*R|O;6T!"
		        }

		        $.ajax({
			        url: 'https://api.sendsay.ru/clu180',
			        type: 'post',
			        data: "apiversion=100&json=1&request=" + encodeURIComponent($.toJSON(request)),
			        success: function(r) {

				        var obj = $.parseJSON(r);
				        var session = obj.session;

				        var request1 = {
					        "action" : "member.set",
					        "email" : email.val(),
					        "if_exists": "overwrite",
					        "newbie.confirm" : "1",
					        "newbie.letter.confirm" : "63",
					        "return_fresh_obj" : "1",
					        "obj" : {
						        "a58" : {
							        "q25" : email.val(),
							        "q379" : name.val()
						        },
						        "-group" : {
							        "p443": "1"
						        }
					        },
					        "session" : session
				        }

				        $.ajax({
					        url: 'https://api.sendsay.ru/clu180',
					        type: 'post',
					        data: "apiversion=100&json=1&request=" + encodeURIComponent($.toJSON(request1)),
					        success: function(r1) {
						        console.log(r1)
					        }
				        })
			        }
		        });

		        e.preventDefault();
	        })
        })

        function validateEmail(email) {
	        var re = /^(([^<>()\[\]\\.,;:\s@"]+(\.[^<>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
	        return re.test(email);
        }


        /*
		* динамический таймер в акциях
		* */
        if ($('.actions-add-js').length > 0){
	        $('.action-date-lost').each(function() {
		        var actId = $(this).attr('id');
		        var activeTo = $(this).data('active-to');
		        $.post('/ajax/action/setFormattedDateLost/', {'activeTo': activeTo}, function (data) {
			        $('#'+actId).show(600).html(data.data);
		        });

	        });
        }

        $.get(
	        '/ajax/form/feedback/',
	        function(response) {
		        $('#super-form').html(response);
	        }
        );

        if($('input.driver_item:checked').length == chbcount) {
	        $(this).closest('table').find('thead td input[type=checkbox]').prop('checked', true).trigger('refresh');
        }  else {
	        $(this).closest('table').find('thead td input[type=checkbox]').prop('checked', false).trigger('refresh');
        }


        $("#add_field_area") . on("click", "#add_block", function() {

	        var
		        contract = $("[name='USER_CONTRACT[]']") . html();
	        var
		        role = $("[name='USER_ROLE[]']") . html();

	        $(".append-block") . append('<div class="form_el clearfix" id="clone_field_area"><select name="USER_CONTRACT[]">' + contract + '</select> <select name="USER_ROLE[]">' + role + '</select></div>');

	        $("#clone_field_area select") . styler();

	        return false;
        });

        indi . app . blocks . registration = function() {
	        $("body") . on("change", "#COUNTRY", function() {
		        var
			        loading = new indi . ui . loading('body');
		        var
			        val = $(this) . val();
		        var
			        form = $(this) . closest("form");
		        var
			        formData = new FormData($(form)[0]);
		        formData . delete("register_submit_button");
		        $.ajax({
			        type: 'POST',
			        processData: false,
			        contentType: false,
			        data: formData,
			        success: function(response){
				        var
					        cities = $(response) . find(".js-city");
				        var
					        citiesHTML = cities . html();
				        $(".js-city") . html(citiesHTML);
				        loading . hide();
			        }
		        });
	        });
        }


        $('#class_list option:selected').click(function(){
	        var value = $(this).val() || $(this).text();
	        console.log(value);
        });
        $('#class_list').change(function () {

	        var UF_XML_ID = $(this).val();

	        alert (s);
	        console.log(1);

	        return false;
        });
        }


        $.getJSON('/local/json/cars.json', function(incomingData) {}

        $('input[id^=zagran_seriya_]').inputmask('99 9999999');

        $('.desigion__content .buy').off('click');

        // отобраение нескольких точек на карте
        <script type="text/javascript">

	        function initYmaps() {
	        <?if ($arResult['MAN_FILIAL']['MAP']) {?>
			        var myMap = new ymaps.Map("map2", {
				        center: [<?=$arResult['MAN_FILIAL']['MAP'];?>],
			        zoom: 14
		        });
			        myMap.controls.add(new ymaps.control.SmallZoomControl());

		        <?foreach ($arResult['FILIALS'] as $arOffice) {?>
			        (function (points, id) {
				        var myPlacemark = new ymaps.Placemark(points, {}, {
					        iconImageHref: '<?=SITE_TEMPLATE_PATH;?>/img/map-icon.png',
					        iconImageSize: [82, 50]
				        });
				        myPlacemark.events.add('click', function () {
					        $('.contacts-block__item-' + id).show().siblings('[class^="contacts-block__item"]:visible').hide();
				        });
				        myMap.geoObjects.add(myPlacemark);
			        })([<?=$arOffice['MAP'];?>], <?=$arOffice['ID'];?>);
		        <? } ?>
		        <? } ?>
	        }
	        </script>

        var percent = $('option:selected', this).attr('data-percent');


        $('input.numberFormat').inputmask("decimal", {
	        digits: 0,
	        digitsOptional: false,
	        radixPoint: "",
	        integerDigits: 10,
	        rightAlign: false,
	        groupSeparator: " ",
	        autoGroup: true,
	        allowPlus: false,
	        allowMinus: false,
	        clearMaskOnLostFocus: false,
	        removeMaskOnSubmit: true,
	        autoUnmask: true,
	        onUnMask: function(maskedValue, unmaskedValue) {
		        var x = maskedValue.split(',');
		        return x[0].replace(/\s/g,'');
	        }
        });


        $('input[data-structure="age"]').on("keyup", function(event) {
	        var node = $(this);
	        var id = node.attr("id");
	        var val = parseInt(node.val());

	        console.log(val);
	        /*
					var type_doc = 'Паспорт (серия и номер)';
					if (val < 14) {
						type_doc = 'Cвидетельство о рождении (серия и номер)';
					}
					$('#pass' + index).prev().text(type_doc);

					if (val < 14) {
						//Св-во о рождении
						$('#pass' + index).inputmask('a{1,3}-a{2} 9{6}');
					} else {
						//Паспорт
						$('#pass' + index).inputmask('99-99 999999');
					}*/
        });


        $("body").on("click", ".action-btn_client", function(event) {

	        event.preventDefault();
	        event.stopImmediatePropagation();

	        let id = $(this).data('id'),
		        data = '';

	        $.ajax({
		        type : 'GET',
		        url : '/redactor/travel/?id=' + id,
		        dataType: 'html',
		        data: data,
		        success : function(msg) {
			        let html = $('<div>' + msg + '</div>').find('#form-message').html();

			        let form = $(html).find('input').serialize();

			        $.ajax({
				        type : 'POST',
				        url : ajax_url,
				        dataType: 'json',
				        data: 'AJAX=Y&' + form + '&METHOD=DEV&ID=' + id,
				        success : function(data) {
					        if (data == 'ok') {
						        alert ('Полис отправлен клиенту');
					        } else {
						        alert ('Ошибка при отправке');
					        }
					        $('.card-action_test').text('Отправить тестовое');
				        },
			        });

		        },
	        });

        });



        function paydate_check(date){
	        var ajax = $.ajax({
		        type: 'POST',
		        url: ajax_url,
		        dataType: 'json',
		        data: $("#form-desigion").serialize() + '&PAYDATE=Y&BEGINDATE=' + date + '&UID=' + uid,
	        });
	        return ajax;
        };


        var ajax = paydate_check(date);
        ajax.done(function(data){
	        console.log(data.result);
	        if (data.result==false) {
		        $('#date_policy_start').addClass("is-invalid");
		        nfield = $('#date_policy_start').parent().children(".invalid-feedback").html('Неправильно введена дата');
		        //if (nfield.hasClass("invalid-feedback") == true) {
		        //    nfield.html('Дата начала должна быть не ранее '+ date_d);
		        //};
	        } else {
		        $('#step1').slideUp();
		        $('#step2').slideDown();
		        $('.buy.choose').slideDown();
		        $('.desigion__item-nav div').removeClass('current');
		        $(".desigion__item-nav div[data-step=2]").addClass('current');
		        $(".desigion__item-nav div[data-step=1]").addClass('past');
	        }
	        goToNav();
        });


        $('body').on('change', '#BANK_ID', function() {
	        var fixedpercent = $('option:selected', this).attr('data-fixedpercent');
	        console.log(fixedpercent);
	        $('.percent-block').hide();
	        $('#PERCENT').val('');
	        if (fixedpercent == 0) {
		        $('.percent-block').show();
	        }
        });



        <script>

        $(function () {
	        function getCookie(name) {
		        var cookie = " " + document.cookie;
		        var search = " " + name + "=";
		        var setStr = null;
		        var offset = 0;
		        var end = 0;
		        if (cookie.length > 0) {
			        offset = cookie.indexOf(search);
			        if (offset != -1) {
				        offset += search.length;
				        end = cookie.indexOf(";", offset)
				        if (end == -1) {
					        end = cookie.length;
				        }
				        setStr = unescape(cookie.substring(offset, end));
			        }
		        }
		        return(setStr);
	        }

	        //запись города в куки
	        document.cookie='BITRIX_SM_CITY_NAME=<?=$arResult["PROPERTIES"]["CITY"]['FOUND_CODE']?>; path=/;';

	        $.ajax({
		        url: "/ajax/sessionstart.php",
		        data: {city: getCookie('BITRIX_SM_CITY_NAME')},
		        success: function(data){

		        }
	        });
        });
        </script>




        /**
         * загрузим файл в tmp-директорию
         */
        $(document).on('change', '.js-work-file', function () {
	        var form = document.getElementById('post_form');
	        var formData;
	        formData = new FormData(form);

	        formData.append('file', $('input[type=file]')[0]['value']);
	        $.ajax({
		        url: '/local/components/webway/upload.ajax.php',
		        type: 'POST',
		        data: formData,
		        processData: false,
		        contentType: false,
		        success: function (data) {
			        //some action;
		        }
	        });
        });


        <form method="post" action="" enctype="multipart/form-data" name="post_form" id="post_form">

	        <input type="file" class="js-work-file" name="file_source" size="40"  onchange='$("#upload-file-info").html($(this).val());'>







<script type="text/javascript">
    $(function(){
        $("#fst").on("change", function(){
// AJAX-запрос
            $.ajax({
                url: "select.php?id=" + $('#fst').val()
            })
                .done(function(data){
                    $('#snd').html(data);
                    $("#snd").prop("disabled", false);
                });
        });
    });
</script>


// Назначаем обработчики, только после полной загрузки документа
$(function(){
// Обработчик нажатия на кнопку submit
    $('input[type=submit]').on('click', function(e){
// Предотвращаем обычное поведение элемента
        e.preventDefault();
// Формируем JSON из полей формы
        var json = {
            name: $('input[name=name]').val(),
            family: $('input[name=family]').val()
        }
// Отправляем асинхронный POST-запрос по адресу,
// указанному в атрибуте action формы
        $.ajax({
            url: $('form').prop('action'),
            method: 'POST',
            data: 'json=' + JSON.stringify(json)
        })
        // В случае успешного получения ответа от сервера
            .done(function(msg){
// Заменяем надпись Здравствуйте в поле p#is-hello
                $('#js-hello').html(msg);
            });
    });
});


<?php
// Преобразуем JSON-данные в массив
    $arr = json_decode($_POST['json'], true);
// Объединяем содержимое в строку
$name = trim(implode(" ", $arr));
$result = "Здравствуйте";
if(!empty($name))
    $result .= ", $name";
$result .= "!";
// Отдаем результат
echo htmlspecialchars($result);
?>

<script type="text/javascript">
// Назначить обработчики события click
// после загрузки документа
    $(function() {
        $(document).on("click", "input[type='button'][value!='+']", remove_field);
        $(document).on("click", "input[type='button'][value!='-']", add_field);
    });
// Обработчик для кнопки +
function add_field(){
// Добавляем новое поле в конец
    $("p:last").clone().insertAfter("p:last");
}
// Обработчик для кнопки -
function remove_field(){
    console.log($(this));
// Удаляем последнее поле
    $("p:last").remove();
}
</script>
</head>
<body>
<form enctype='multipart/form-data' method="post">
    <p><input type="file" name="filename[]" />
    <input type="button" value="+">
    <input type="button" value="-"></p>
    <div><input type="submit" value="Загрузить"></div>
    </form>
    </body>

    <script type="text/javascript">
// Назначить обработчики события click
// после загрузки документа
    $(function(){
        $("#id").on("click", function(){
            $('#info').load("time.php");
        })
    });
</script>


$(document).ready(function(){
    $("#submit-id").on("click", function(){
// Проверяем корректность заполнения полей
        if($.trim($("#nickname").val()) === "")
        {
            alert('Пожалуйста, заполните поле "Автор"');
            return false;
        }
        if($.trim($("#content").val()) === "")
        {
            alert('Пожалуйста, заполните поле "Сообщение"');
            return false;
        }
// Блокируем кнопку отправки
        $("#submit-id").prop("disabled", true);
// AJAX-запрос
        $.ajax({
            url: "addcom.php",
            method: 'post',
            data: {nickname: $("#nickname").val(),
                content: $("#content").val()}
        }).done(function(data){
// Успешное получение ответа
            $("#info").html(data);
            $("#submit-id").prop("disabled", false);
        });
    })

    <script type="text/javascript">
        $(function(){
            $("input[type=checkbox]").on("click", function(){
                $.post(
                    "check.php",
                    {id: $(this).prop("id"),
                        status: $(this).prop("checked")}
                );
            });
        });
    </script>



    