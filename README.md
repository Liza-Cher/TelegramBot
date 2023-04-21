# TelegramBot
Написать и протестировать Telegram-бота, в котором будет реализован следующий функционал:

Бот возвращает цену на определённое количество валюты (евро, доллар или рубль).

При написании бота необходимо использовать библиотеку pytelegrambotapi.

Человек должен отправить сообщение боту в следующем виде <имя валюты цену которой он хочет узнать> <имя валюты в которой надо узнать цену первой валюты> <количество первой валюты>.

При вводе команды /start или /help пользователю выводятся инструкции по применению бота.
При вводе команды /values должна выводиться информация о всех доступных валютах в читаемом виде.

Для взятия курса валют необходимо использовать API и отправлять к нему запросы с помощью библиотеки Requests.
Для парсинга полученных ответов использовать библиотеку JSON.

При ошибке пользователя (например, введена неправильная или несуществующая валюта или неправильно введено число) вызывать собственно написанное исключение APIException с текстом пояснения ошибки.

Текст любой ошибки с указанием типа ошибки должен отправляться пользователю в сообщения.

Для отправки запросов к API описать класс со статическим методом get_price(), который принимает три аргумента: название валюты, на которую надо узнать стоимость — это base, имя валюты, в которой будет указана стоимость — это quote, количество переводимой валюты — это amount, которое должно возвращаться в указанной пользователем сумме.
Токен telegramm-бота хранить в специальном конфиг-файле (можно использовать config.py ).

Все классы спрятать в файле extensions.py.
