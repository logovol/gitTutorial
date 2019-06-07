#Лабораторная работа №1
##1.2.1.   Запрос OPTIONS
###Отправьте запрос на http://mail.ru, http://ya.ru, www.rambler.ru, https://www.google.ru, https://github.com/,   www.apple.com/.
http://mail.ru – Status: 200 OK; Time:163 ms; Size:282.08 KB

    Server →nginx/1.14.1
    Date →Mon, 03 Jun 2019 15:06:20 GMT
    Content-Type →text/html; charset=utf-8
    Transfer-Encoding →chunked
    Connection →keep-alive
    Cache-Control →no-cache,no-store,must-revalidate
    Pragma →no-cache
    Expires →Sun, 03 Jun 2018 15:06:20 GMT
    Last-Modified →Mon, 03 Jun 2019 18:06:20 GMT
    Content-Security-Policy →default-src mail.ru *.mail.ru *.imgsmail.ru *.mradx.net *.serving-sys.com *.moatads.com    *.doubleverify.com *.adsafeprotected.com; script-src 'unsafe-inline' 'unsafe-eval' mail.ru *.mail.ru *.imgsmail.ru *.mradx.net *.odnoklassniki.ru ok.ru *.doubleverify.com *.dvtps.com *.doubleclick.net *.googletagservices.com *.googlesyndication.com *.googleadservices.com *.moatads.com *.adlooxtracking.com *.adsafeprotected.com *.serving-sys.com; img-src data: blob: *; style-src 'unsafe-inline' 'unsafe-eval' blob: *.mail.ru *.imgsmail.ru *.mradx.net; font-src data: blob: https: *.mail.ru *.imgsmail.ru *.mradx.net; frame-src mail.ru *.mail.ru *.mradx.net *.doubleverify.com *.doubleclick.net ok.ru *.ok.ru; child-src mail.ru *.mail.ru *.mradx.net *.doubleverify.com *.doubleclick.net ok.ru *.ok.ru; report-uri https://cspreport.mail.ru/splash;
    X-Frame-Options →SAMEORIGIN
    X-XSS-Protection →1; mode=block; report=https://cspreport.mail.ru/xxssprotection
    X-Content-Type-Options →nosniff
    Strict-Transport-Security →max-age=16070400
    Content-Encoding →gzip

http://ya.ru/ - Status: 403 Forbidden; Time:71 ms; Size:12.32 KB

    Date →Mon, 03 Jun 2019 15:07:05 GMT
    Content-Type →text/html; charset=utf-8
    ETag →W/"5cf12719-3077"
    Content-Encoding →gzip
    X-Content-Type-Options →nosniff
    Transfer-Encoding →chunked

http://www.rambler.ru/ - Status: 403 Forbidden; Time:163 ms; Size:11.22 KB

    Server →nginx
    Date →Mon, 03 Jun 2019 15:07:33 GMT
    Content-Type →text/html; charset=utf-8
    Transfer-Encoding →chunked
    Connection →keep-alive
    Keep-Alive →timeout=50
    Last-Modified →Wed, 29 May 2019 11:01:34 GMT
    Vary →Accept-Encoding
    ETag →W/"5cee668e-2ae9"
    Content-Encoding →gzip
    X-Cache →REVALIDATED

Обработан правильно https://www.google.ru/ - Status: 405 Method Not Allowed; Time:84 ms; Size:1.81 KB

    Allow →GET, HEAD
    Date →Mon, 03 Jun 2019 15:08:09 GMT
    Content-Type →text/html; charset=UTF-8
    Server →gws
    Content-Length →1592
    X-XSS-Protection →0
    X-Frame-Options →SAMEORIGIN
    Alt-Svc →quic=":443"; ma=2592000; v="46,44,43,39"

https://github.com/ - Status: 404 Not Found; Time:209 ms; Size:1.55 KB

    Date →Mon, 03 Jun 2019 15:08:47 GMT
    Content-Type →text/html; charset=utf-8
    Content-Length →0
    Server →GitHub.com
    Status →404 Not Found
    X-Request-Id →b12ab3d7-9d6e-4ec3-98aa-2af70f92cc5d
    Strict-Transport-Security →max-age=31536000; includeSubdomains; preload
    X-Frame-Options →deny
    X-Content-Type-Options →nosniff
    X-XSS-Protection →1; mode=block
    Referrer-Policy →origin-when-cross-origin, strict-origin-when-cross-origin
    Expect-CT →max-age=2592000, report-uri="https://api.github.com/_private/browser/errors"
    Content-Security-Policy →default-src 'none'; base-uri 'self'; block-all-mixed-content; connect-src 'self' uploads.github.com www.githubstatus.com collector.githubapp.com api.github.com www.google-analytics.com github-cloud.s3.amazonaws.com github-production-repository-file-5c1aeb.s3.amazonaws.com github-production-upload-manifest-file-7fdce7.s3.amazonaws.com github-production-user-asset-6210df.s3.amazonaws.com; font-src github.githubassets.com; form-action 'self' github.com gist.github.com; frame-ancestors 'none'; frame-src render.githubusercontent.com; img-src 'self' data: github.githubassets.com media.githubusercontent.com camo.githubusercontent.com identicons.github.com collector.githubapp.com avatars0.githubusercontent.com avatars1.githubusercontent.com avatars2.githubusercontent.com avatars3.githubusercontent.com github-cloud.s3.amazonaws.com; manifest-src 'self'; media-src 'none'; script-src github.githubassets.com; style-src 'unsafe-inline' github.githubassets.com
    X-GitHub-Request-Id →C8B8:C994:22A756F:35505E6:5CF537FF

http://www.apple.com/ - Status: 200 OK; Time:257 ms; Size:9.1 KB

    Server →Apache
    Content-Type →text/html; charset=UTF-8
    X-Frame-Options →SAMEORIGIN
    Strict-Transport-Security →max-age=31536000; includeSubDomains
    X-Content-Type-Options →nosniff
    X-Xss-Protection →1; mode=block
    Vary →Accept-Encoding
    Content-Encoding →gzip
    Cache-Control →max-age=274
    Expires →Mon, 03 Jun 2019 15:13:45 GMT
    Date →Mon, 03 Jun 2019 15:09:11 GMT
    Content-Length →8885
    Connection →keep-alive
###Для чего используется запрос OPTIONS? Какие коды ответов приходят при этом запросе? Какие сайты правильно обработали запрос и вернули ожидаемые данные?
    OPTIONS используется для определения возможностей веб-сервера или параметров соединения для конкретного ресурса. В ответ серверу следует включить в заголовок Allow со списком поддерживаемых методов. Также в заголовке ответа может включаться информация о поддерживаемых расширениях.
    Коды ответа: 200 OK - запрос успешно обработан. Если клиентом были запрошены какие-либо данные, то они находятся в заголовке и/или теле сообщения. Появился в HTTP/1.0.
    403 Forbidden - сервер понял запрос, но он отказывается его выполнять из-за ограничений в доступе для клиента к указанному ресурсу. Иными словами, клиент не уполномочен совершать операции с запрошенным ресурсом. Если для доступа к ресурсу требуется аутентификация средствами HTTP, то сервер вернёт ответ 401, или 407 при использовании прокси. В противном случае ограничения были заданы администратором сервера или разработчиком веб-приложения и могут быть любыми в зависимости от возможностей используемого программного обеспечения. В любом случае клиенту следует сообщить причины отказа в обработке запроса.
    405 Method Not Allowed - указанный клиентом метод нельзя применить к текущему ресурсу. В ответе сервер должен указать доступные методы в заголовке Allow, разделив их запятой. Эту ошибку сервер должен возвращать, если метод ему известен, но он не применим именно к указанному в запросе ресурсу, если же указанный метод не применим на всём сервере, то клиенту нужно вернуть код 501 (Not Implemented).
##1.2.2.   Запрос HEAD
vk.com

    Server →Internet Information Services
    Date →Mon, 03 Jun 2019 13:44:04 GMT
    Content-Length →0
    Connection →keep-alive
    X-Frontend →front623305
    Access-Control-Expose-Headers →X-Frontend

www.apple.com

    Server →Apache
    X-Frame-Options →SAMEORIGIN
    X-Xss-Protection →1; mode=block
    Accept-Ranges →bytes
    X-Content-Type-Options →nosniff
    Content-Type →text/html; charset=UTF-8
    Strict-Transport-Security →max-age=31536000; includeSubDomains
    Content-Encoding →gzip
    Cache-Control →max-age=177
    Expires →Mon, 03 Jun 2019 13:46:42 GMT
    Date →Mon, 03 Jun 2019 13:43:45 GMT
    Connection →keep-alive
    Vary →Accept-Encoding

www.msn.com

    Content-Length →16188
    Content-Type →text/html; charset=utf-8
    Content-Encoding →gzip
    Expires →-1
    Vary →User-Agent
    Set-Cookie →PreferencesMsn=eyJIb21lUGFnZSI6eyJTdHJpcGVzIjpbXSwiTWVTdHJpcGVNb2R1bGVzIjpbXSwiTWFya2V0Q29uZmlndXJhdGlvbiI6eyJNYXJrZXQiOiJydS1ydSIsIlN1cHByZXNzUHJvbXB0IjpmYWxzZSwiUHJlZmVycmVkTGFuZ3VhZ2VDb2RlIjoicnUtcnUiLCJDb3VudHJ5Q29kZSI6IlJVIn19LCJFeHBpcnlUaW1lIjo2MzcyNjc4ODYwMDI5Mjc2NjgsIlZlcnNpb24iOjF90; domain=msn.com; expires=Wed, 03-Jun-2020 13:43:20 GMT; path=/; HttpOnly
    Set-Cookie →marketPref=ru-ru; domain=msn.com; expires=Wed, 03-Jun-2020 13:43:20 GMT; path=/; HttpOnly
    Access-Control-Allow-Origin →*
    X-AspNetMvc-Version →5.2
    X-AppVersion →20190530_16172718
    X-Activity-Id →4fca6938-d65a-4b37-b9e5-e23d2a41c52e
    X-Az →{did:9a9a6dcc560c4a5a958f3f1a2bcb24f4, rid: 96, sn: eastus-prod-hp, dt: 2019-06-03T11:06:09.3885689Z, bt: 2019-05-31T00:31:01.5245166Z}
    X-UA-Compatible →IE=Edge;chrome=1
    X-Content-Type-Options →nosniff
    X-FRAME-OPTIONS →SAMEORIGIN
    X-Powered-By →ASP.NET
    Access-Control-Allow-Methods →HEAD,GET,OPTIONS
    X-XSS-Protection →1
    X-MSEdge-Ref →Ref A: 4FCA6938D65A4B37B9E5E23D2A41C52E Ref B: PRG01EDGE0417 Ref C: 2019-06-03T13:43:20Z
    Date →Mon, 03 Jun 2019 13:43:19 GMT
###Для чего нужен запрос HEAD? Какой сайт прислал ожидаемый ответ?
HEAD запрашивает заголовки, идентичные тем, что возвращаются, если указанный ресурс будет запрошен с помощью HTTP-метода GET. Такой запрос может быть выполнен перед загрузкой большого ресурса, например, для экономии пропускной способности.
HTTP метод HEAD работает точно так же, как и метод GET, с той лишь разницей, что сервер в ответ не посылает тело HTTP сообщения. Все заголовки ответа при запросе клиента с использованием метода HEAD идентичны тем заголовкам, которые бы были, если бы использовался метод GET. Обычно HTTP метод HEAD используется для получения метаинформации об объекте без пересылки тела HTTP сообщения. Метод HEAD часто используется для тестирования HTTP соединений и достижимости узлов и ресурсов, так как нет необходимости гонять по сети содержимое, тестирование HTTP методом HEAD производится гораздо быстрее.

Все прислали ожидаемые ответы
##1.2.3.   Запросы GET и POST. Что они вернули? Что содержится в теле ответа?
yandex.ru
GET
В теле ответа содержится ресурс.

    <!DOCTYPE html>
    <html class="i-ua_js_no i-ua_css_standart i-ua_browser_unknown i-ua_browser_desktop document_streamnow-tabs_yes i-ua_platform_other" lang="ru">
    <head xmlns:og="http://ogp.me/ns#">
        <meta http-equiv=Content-Type content="text/html;charset=UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <title>Яндекс</title>
        <link rel="shortcut icon" href="//yastatic.net/iconostasis/_/8lFaTHLDzmsEZz-5XaQg9iTWZGE.png">
        <link rel="apple-touch-icon" href="//yastatic.net/iconostasis/_/5mdPq4V7ghRgzBvMkCaTzd2fjYg.png" sizes="76x76">
        <link rel="apple-touch-icon" href="//yastatic.net/iconostasis/_/s-hGoCQMUosTziuARBks08IUxmc.png" sizes="120x120">
POST

    403 Forbidden
    <!DOCTYPE HTML>
    <html lang="ru">
    <head>
        <meta http-equiv="Content-Type" content="text/html;charset=UTF-8">
        <title>Яндекс</title>
        <link rel="shortcut icon" href="">
        <style type="text/css">
    body, div, ul, table, tr, td, form, input {
    margin: 0;
    padding: 0
    }

    body {
    font: .8em Arial, sans-serif;
    color: #000;
    background: #fff;
    }
Google.com
GET

    <!doctype html><html itemscope="" itemtype="http://schema.org/WebPage" lang="ru"><head><meta content="&#1055;&#1086;&#1080;&#1089;&#1082; &#1080;&#1085;&#1092;&#1086;&#1088;&#1084;&#1072;&#1094;&#1080;&#1080; &#1074; &#1080;&#1085;&#1090;&#1077;&#1088;&#1085;&#1077;&#1090;&#1077;: &#1074;&#1077;&#1073; &#1089;&#1090;&#1088;&#1072;&#1085;&#1080;&#1094;&#1099;, &#1082;&#1072;&#1088;&#1090;&#1080;&#1085;&#1082;&#1080;, &#1074;&#1080;&#1076;&#1077;&#1086; &#1080; &#1084;&#1085;&#1086;&#1075;&#1086;&#1077; &#1076;&#1088;&#1091;&#1075;&#1086;&#1077;." name="description"><meta content="noodp" name="robots"><meta content="text/html; charset=UTF-8" http-equiv="Content-Type"><meta content="/images/branding/googleg/1

POST 405 Method Not Allowed

    <!DOCTYPE html>
    <html lang=en>
    <meta charset=utf-8>
    <meta name=viewport content="initial-scale=1, minimum-scale=1, width=device-width">
    <title>Error 405 (Method Not Allowed)!!1</title>
    <style>
    *{margin:0;padding:0}html,code{font:15px/22px arial,sans-serif}html{background:#fff;color:#222;padding:15px}body{margin:7% auto 0;max-width:390px;min-height:180px;padding:30px 0 15px}* > body{background:url(//www.google.com/images/errors/robot.png) 100% 5px no-repeat;padding-right:205px}p{margin:11px 0 22px;overflow:hidden}ins{color:#777;text-decoration:none}a img{border:0}@media screen and (max-width:772px){body{background:none;margin-top:0;max-width:none;padding-right:0}}#logo{background:url(//www.google.com/images/branding/googlelogo/1x/googlelogo_color_150x54dp.png) no-repeat;margin-left:-5px}@media only screen and (min-resolution:192dpi){#logo{background:url(//www.google.com/images/branding/googlelogo/2x/googlelogo_color_150x54dp.png) no-repeat 0% 0%/100% 100%;-moz-border-image:url(//www.google.com/images/branding/googlelogo/2x/googlelogo_color_150x54dp.png) 0}}@media only screen and (-webkit-min-device-pixel-ratio:2){#logo{background:url(//www.google.com/images/branding/googlelogo/2x/googlelogo_color_150x54dp.png) no-repeat;-webkit-background-size:100% 100%}}#logo{display:inline-block;height:54px;width:150px}

Apple.com
GET

    <!DOCTYPE html>
    <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en-US" lang="en-US" prefix="og: http://ogp.me/ns#" class="no-js" data-layout-name="wwdc">
    <head>
        <script src="/metrics/target/scripts/1.0/at.js" type="text/javascript" charset="utf-8"></script>
        <script>
			window.AB = window.AB || {};
			window.AB.isAbTestActive = true;
		</script>

POST

    <!DOCTYPE html>
    <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en-US" lang="en-US" prefix="og: http://ogp.me/ns#" class="no-js" data-layout-name="wwdc">
    <head>
        <script src="/metrics/target/scripts/1.0/at.js" type="text/javascript" charset="utf-8"></script>
        <script>
			window.AB = window.AB || {};
			window.AB.isAbTestActive = true;
		</script>
        <meta charset="utf-8" />
        <link rel="canonical" href="https://www.apple.com/" />
        <link rel="alternate" href="https://www.apple.com/" hreflang="en-US" />
        <link rel="alternate" href="https://www.apple.com/ae-ar/" hreflang="ar-AE" />
        <link rel="alternate" href="https://www.apple.com/ae/" hreflang="en-AE" />

####Описание:
GET используется для запроса содержимого указанного ресурса. С помощью метода GET можно также начать какой-либо процесс. В этом случае в тело ответного сообщения следует включить информацию о ходе выполнения процесса.
POST применяется для передачи пользовательских данных заданному ресурсу. Например, в блогах посетители обычно могут вводить свои комментарии к записям в HTML-форму, после чего они передаются серверу методом POST и он помещает их на страницу. При этом передаваемые данные (в примере с блогами — текст комментария) включаются в тело запроса. Аналогично с помощью метода POST обычно загружаются файлы на сервер.
##1.3.2.1.        Получите список всех факультетов МГТУ им. Н.Э.Баумана.
- Получим access_token на сайте vk.com (инструкция https://www.youtube.com/watch?v=2eiPf-DfZBE)
- Вернем список стран (метод database.getCountries)

Синтакис запроса: https://api.vk.com/method/METHOD_NAME?PARAMETERS&access_token=ACCESS_TOKEN&v=V
https://api.vk.com/method/database.getCountries?need_all=1&offset=140&count=20&access_token=ТОКЕНf&v=5.92

    {"response":{"count":234,"items":[{"id":146,"title":"Оман"},{"id":147,"title":"Остров Мэн"},{"id":148,"title":"Остров Норфолк"},{"id":149,"title":"Острова Кайман"},{"id":150,"title":"Острова Кука"},{"id":151,"title":"Острова Теркс и Кайкос"},{"id":152,"title":"Пакистан"},{"id":153,"title":"Палау"},{"id":154,"title":"Палестинская автономия"},{"id":155,"title":"Панама"},{"id":156,"title":"Папуа — Новая Гвинея"},{"id":157,"title":"Парагвай"},{"id":158,"title":"Перу"},{"id":159,"title":"Питкерн"},{"id":160,"title":"Польша"},{"id":161,"title":"Португалия"},{"id":162,"title":"Пуэрто-Рико"},{"id":163,"title":"Реюньон"},{"id":1,"title":"Россия"},{"id":164,"title":"Руанда"}]}}

- Вернем список высших учебных заведений (метод database.getUniversities)

https://api.vk.com/method/database.getUniversities?q=%D0%9C%D0%93%D0%A2%D0%A3&country_id=1&city=1&access_token=ТОКЕН&v=5.92

    {"response":{"count":48,"items":[{"id":248,"title":"МГТУ им. Косыгина (бывш. МГТА им. Косыгина, МТИ)"},{"id":249,"title":"МГТУ ГА"},{"id":250,"title":"МГТУ им. Н. Э. Баумана"},{"id":252,"title":"МГТУ «Станкин»"},{"id":613,"title":"МГТУ им. Г. И. Носова"},{"id":616,"title":"МГТУ\r\n"},{"id":629,"title":"МГТУ\r\n"},{"id":1077,"title":"МГТУ «МАМИ» (уч. подразделение)"},{"id":1838,"title":"МГТУ"},{"id":2168,"title":"КФ МГТУ им. Баумана"},{"id":2942,"title":"МГТУ ГА"},{"id":4536,"title":"МГТУ им. Н. Э. Баумана"},{"id":4685,"title":"МГТУ им. Баумана"},{"id":4873,"title":"МГТУ им. Н.Э. Баумана"},{"id":5051,"title":"МГТУ"},{"id":5114,"title":"МГТУ"},{"id":7840,"title":"МГТУ"},{"id":9989,"title":"МГТУ «МАМИ» (ЛФ)"},{"id":10243,"title":"МГТУГА"},{"id":10422,"title":"МГТУ МАМИ"},{"id":14131,"title":"МГТУ им.Баумана"},{"id":14262,"title":"МГТУ МПК"},{"id":15053,"title":"МГТУ им. Баумана"},{"id":15611,"title":"МГТУ им. Н. Э. Баумана"},{"id":17074,"title":"МГТУ (МФ)"},{"id":17574,"title":"МГТУ им. Баумана"},{"id":24107,"title":"МГТУ"},{"id":29673,"title":"МГТУ им. Г.И. Носова"},{"id":29805,"title":"мгту"},{"id":31118,"title":"МГТУ (АФ)"},{"id":31462,"title":"МГТУ им. Н.Э.Баумана"},{"id":31589,"title":"МГТУ им. Косыгина"},{"id":36162,"title":"МГТУ имени Баумана"},{"id":41361,"title":"Филиал МГТУ"},{"id":51854,"title":"МГТУ «МАМИ» (представительство)"},{"id":81090,"title":"МГТУ им.Косыгина"},{"id":96782,"title":"МГТУ ГА (РФ)"},{"id":100929,"title":"ИФ МГТУ ГА"},{"id":102899,"title":"МГТУ «МАМИ» (ДФ)"},{"id":105346,"title":"МГТУ «МАМИ» (представительство)"},{"id":117132,"title":"МГТУ им. Г. И. Носова (БФ)"},{"id":126815,"title":"ЕТИ МГТУ «Станкин»"},{"id":137961,"title":"МГТУ им. Г. И. Носова (СФ)"},{"id":158445,"title":"колледж МГТУ"},{"id":169759,"title":"ИСОТ МГТУ им. Баумана (бывш. МИПК МГТУ им. Баумана)"},{"id":278964,"title":"МГТУ ГА"},{"id":354636,"title":"колледж МГТУ"},{"id":1190337,"title":"МФ МГТУ им. Баумана"}]}}

- Вернем список факультетов (метод database.getFaculties)

https://api.vk.com/method/database.getFaculties?university_id=250&ТОКЕН&v=5.92

    {"response":{"count":20,"items":[{"id":1031,"title":"Аэрокосмический факультет"},{"id":1032,"title":"Факультет инженерного бизнеса и менеджмента"},{"id":1033,"title":"Факультет информатики и систем управления"},{"id":1034,"title":"Факультет машиностроительных технологий"},{"id":1035,"title":"Факультет оптико-электронного приборостроения"},{"id":1036,"title":"Приборостроительный факультет"},{"id":1037,"title":"Радиотехнический факультет"},{"id":1038,"title":"Факультет радиоэлектроники и лазерной техники"},{"id":1039,"title":"Факультет ракетно-космической техники"},{"id":1040,"title":"Факультет робототехники и комплексной автоматизации"},{"id":1041,"title":"Факультет специального машиностроения"},{"id":1042,"title":"Факультет фундаментальных наук"},{"id":1043,"title":"Факультет энергомашиностроения"},{"id":1044,"title":"Кафедра юриспруденции, интеллектуальной собственности и судебной экспертизы"},{"id":1803,"title":"Факультет биомедицинской техники"},{"id":1804,"title":"Факультет социально-гуманитарных наук"},{"id":56430,"title":"Факультет лингвистики"},{"id":56431,"title":"Физкультурно-оздоровительный факультет"},{"id":2071503,"title":"Головной учебно-исследовательский и методический центр (ГУИМЦ)"},{"id":2183736,"title":"Факультет военного обучения (Военный институт)"}]}}

##1.3.2.2. Получите свою аватарку.
- Вернем аватарку (метод users.get)

https://api.vk.com/method/users.get?user_ids=logovol&photo_id&access_token=b9e3cf869f6feaf12da761a0140f9e09c9618bfb3a121ae9fe9d23774c59a6a026f77e2523d8ada36b10f&v=5.92

    {
    "response": [
        {
            "id": 43391845,
            "first_name": "Павел",
            "last_name": "Лях",
            "is_closed": false,
            "can_access_closed": true
        }
    ]
    }

##1.3.2.3. Ответьте на вопросы: какой код ответа присылается от api? Что содержит тело ответа? В каком формате и какой кодировке содержатся данные? Какой веб-сервер отвечает на запросы? Какая версия протокола HTTP используется?
- Код ответа 200 OK.
- Запрошенную информацию.
- В формате JSON, кодировка UTF-8.
- Internet Information Services
- HTTP 1.1

##1.3.3.1. Отправьте запись на стену любому пользователю/группе и убедитесь, что она пришла.
- Отправим сообщение на стену (метод wall.post)

https://api.vk.com/method/wall.post?owner_id=43391845&message=test%20api&access_token=ТОКЕН&v=5.92

![](C:\Git\gitTutorial.pic.png)

##1.3.3.2. Ответьте на вопрос: каким образом передаются данные от пользователя к серверу в POST-запросах?

    В рамках POST запроса произвольное количество данных любого типа может быть отправлено на сервер в теле сообщения запроса. Поля заголовка в POST-запросе обычно указывают на тип содержимого.

#2. Серверное приложение
1.

    // создание объекта http
    const http = require('http');

    const html = `
    <!doctype>
    <html>
        <head>
            <meta charset="utf-8">
            <tittle>Message from server</title>
            <link rel="stylesheet" href="app.css">
        </head>
            
        <body>
            <h1>Message from server</h1>
            <button>Press</button>
            
            <script src="app.js"></script>
        </body>
    </html>`;
    const css = `
    body {
        margin: 0;
        padding: 0;
        text-align: center;
    }   
    h1 {
        background-color: #43853d;
        color: white;
        padding: .5em;
        font-family: 'Consolas'
    }`;
    const js = `
        const button = document.querySelector('button');
        button.addEventListener('click', event => alert('Working'));
    `;


    // создание сервера у объекта http
    http.createServer((req, res) => {
    /*console.log(req.url);
    console.log(req.method);
    console.log(req.headers);*/
    
    switch (req.url){
        case '/':
            res.writeHead(200, { 'Content-Type': 'text/html' });
            res.end(html);
        case '/app.css':
            res.writeHead(200, { 'Content-Type': 'text/css' });
            res.end(css);
        case '/app.js':
            res.writeHead(200, { 'Content-Type': 'text/javascript' });
            res.end(js);

        default:
            res.writeHead(404, { 'Content-Type': 'text/plain' });
            res.end('404 Not found');
    }
    
    }).listen(3000, () => console.log('Server is working'));

2.

    var list = [];

    const express = require("express");
    const bodyParser = require("body-parser");

    const app = express();  
    // парсер для данных
    app.use(bodyParser.urlencoded({ extended: true }));
    app.use(bodyParser.json());

    // определяем обработчик для маршрута "/"
    app.get("/", function(request, response){
    response.send(list);
    });

    app.post("/", function(req, res) {
    list.push(req.body);
    res.send(req.body); 
    });
    app.delete("/", function(req, res) {
    list.pop();
    res.json("<h2>Удалил</h2>");
    });
    app.put("/", function(req, res) {
    list.splice(req.body.index,1);
    res.send("<h2>PUT запрос</h2>");
    });
    app.options("/", function(req, res) {
    res.setHeader('Allow', 'GET, POST, DELETE, PUT, OPTIONS')
    res.json({ response: "This is OPTIONS"});
    });

    app.listen(3000);


















