# Бот для  знакомств Вконтакте

## Основная информация и  и возможности
Бот представляет из себя программу, написаннуюна языке Python. Будучи запущенной на любом какомпьютере с выходом в интернет, она позволяет в автоматичском режиме предлагать пользователю подходящих кандидатов для знакомства. Кандидаты предлагаются по следующим критериям:
* Возраст кандидата совпадает с возрастом пользователя, +/- 3 года
* Пол предлагаемого кандидата противоположен полу пользователя
* Город кандидата совпадает с городом пользователя

Всю информацию о пользователе Бот собирает автоматически из профиля самого пользователя.

## Установка и начало работы
### Необходимые условия для корректной работы программы:
+ Должен быть установлен интерпритатор Python
+ Установлена СУБД PostgreSQL
+ Должны быть указаны корректные ключи доступа, а именно:
  - ключ доступа сообщества, от имени которого будет отвечать бот
  - ключ доступа с правами доступа пользователя. Для выполнения поиска кандидата и подбора фотографий
  - по умолчанию, ключи хранятся в корневой папке программы в файле new_token.ini в переменных *key_oauth* - для ключа группы и *vk_access_token* - для ключа пользователя
+ Должны быть установлены все зависимости из файла requirements.txt
### Начало работы
* Т.к. Бот активно использует базу данных, то для начала работы необходимо её создать на компьтере, где запускается Бот. По умолчанию имя базы данных - Vkinder.
* Необходимо создать нужные таблицы, в которые бот записывает нужную информацию в процессе своей работы.
* Запустить основной файл программы - main.py
* *Подробную информацию по работе с базами данных смотрите в соответствующем разделе*
## Использование бота
Чтобы начать пользоваться ботом, нужно:
* зайти в сообщество в соцсети Вконтакте, на работу с которым настроен Бот. По умолчанию это: [группа, где живет бот](https://vk.com/public187269980)
* перейти к диалогу с сообществом, нажав кнопку **Сообщение**
* ввести любое сообщение или нажать предложенную кнопку, бот подсскажет что дальше делать и что он умеет.
* воспользоваться возможностями бота и найти для себя подходящую кандидатуру для знакомства.

## Что умеет Бот
Команды, которые можно отправлять Боту,путем ввода сообщения вручную с клавиатуры или нажимая соответствующте кнопки
* **Начать** - команда, которая выведет приветственное сообщение и подскажет список доступных команд.
* **Предложить кандидата** - основная команда Бота. В ответ на нее бот вернет вам кандидата, подскажет как его зовут, даст ссылку на его профиль, покажет 3 его самых популярных фотографии из профиля.
* **В избранное** - добавит текущего кандидата в избранное.
* **В черный список** - добавит текущего кандидата в черный список.
* **Список избранных** - выведет список понравившихся вам кандидатов, которых вы успели добавить в избранное. 