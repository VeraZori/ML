# ML
Итоговый проект
Итоговый проект курса "Машинное обучение в бизнесе"

Стек:

ML: sklearn, pandas, numpy API: flask

Задача: предсказать по описанию новости фейковая или реальная. Бинарная классификация

Используемые признаки:

title (text)
text (text)

Преобразования признаков: tfidf

Модель: logreg

Клонируем репозиторий и создаем образ
$ git clone https://github.com/vera/GB_docker_flask_example.git
$ cd GB_docker_flask_example
$ docker build -t vera/gb_docker_flask_example .
Запускаем контейнер
Здесь Вам нужно создать каталог локально и сохранить туда предобученную модель (<your_local_path_to_pretrained_models> нужно заменить на полный путь к этому каталогу)

$ docker run -d -p 8180:8180 -p 8181:8181 -v <your_local_path_to_pretrained_models>:/app/app/models/gb_docker_flask_example
Переходим на localhost:8181
