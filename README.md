﻿#Инструкция:

Данный скрипт позволяет настроить таргетинг без редиректа на определенное гео
и с определенных устройств. Также он сверяет ip пользователя с базой ip-адресов
модеров FB. Пользователям, которые пройдут проверку по гео, ip, и типу девайса,
будет выводится один сайт с папки "bad_site", а всем остальным с папки	"good_site".

#Как настроить?
						      
1. Раскидать ленды по папкам:
	"good_site" - в эту папку нужно закинуть чистый сайт чтоб модер не волновался.
	"bad_site"  - ну ты понял)) тут твой ленд с чернухой.

2. Выбрать настройки:
	Откройте файл "settings.php" и заполните код нужной страны в поле "country_code",
	согласно ISO: https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2
	Например, 
		
		'country_code' => "US",
	
	означает, что всем пользователям, которые из США, будет показыватся ленд
	с чернухой, а всем остальным - белый ленд из папки "good_site".
	
	Дальше выберите настройки таргетинга проставляя true или false напротив
	соответствующих параметров.Например,
	
		'Mobile' => false,
		'Tablet' => false,
		'Desktop' => true,

	означает, что bad_site будет виден только на ПК, а на мобильных устройствах
	и таблетах будет виден good_site.
