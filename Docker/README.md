## Docker
Цель задания – научиться работаться с dockerfile и собирать посредством него docker контейнер.

Задание:
Необходимо сделать dockerfile для получения рабочего контейнера.
1.	В качестве основы, берём образ continuumio/miniconda3:latest
2.	Добавляем и делаем рабочей папкой /app 
3.	Создаём простой sh файл с названием 1.sh, который должен выдавать надпись “Helloy Netology”.
4.	Надо скопировать этот файл внутрь контейнера и выдать ему права на исполнение.
5.	Запустить установку пакетов python mlflow boto3 pymysql.
6.	В конце запустить на вывод файл 1.sh.
7.	После чего собрать через docker build контейнер с тегом netology-ml:netology-ml

Как оформить ДЗ?
Домашнее задание выполните в файле readme.md в github репозитории. В личном кабинете отправьте на проверку ссылку на .md-файл в вашем репозитории.
- приложить полученный dockerfile
- лог выполнения сборки

Также вы можете выполнить задание в Google Docs и отправить в личном кабинете на проверку ссылку на ваш документ. Название файла Google Docs должно содержать номер лекции и фамилию студента. Пример названия: "1.2. Docker — Товаркин Мананаж" Перед тем как выслать ссылку, убедитесь, что ее содержимое не является приватным (открыто на комментирование всем, у кого есть ссылка). Если необходимо прикрепить дополнительные ссылки, просто добавьте их в свой Google Docs.

Любые вопросы по решению задач задавайте в чате Slack.

Результатом выполнения задания должны быть:
ЗЫ  - Не удаляйте images, он может понадобиться в следующих ДЗ.