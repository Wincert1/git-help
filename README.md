# Git Help
## **How we work with git**

У нас 2 ветки:
- **master** - Рабочая версия бота с автодеплоем
- **dev** - Копия ветки master для разработки

### Оглавление
1. [Если еще нет проекта](#Если-еще-нет-проекта)
2. [Основные команды](#Основные-команды)
3. [Краткое описание работы над любой задачей](#вкратце-опишу-процесс-разработки-над-любой-новой-задачей-даже-мелкой)
4. [Подробное описание процесса](#теперь-подробно-весь-процесс)

### Если еще нет проекта

### Основные команды

### Вкратце опишу процесс разработки над любой новой задачей (даже мелкой):
- Получаем последнюю версию ветки dev;
- На ее основе создаем новую ветку под текущую задачу;
- Работаем;
- Закончили - делаем коммит;
- Получаем последнюю версию ветки dev;
- Мерджим свою ветку в dev решая возникшие конфликты;
- Пушим на сервер;
- Ответсвенный проверяет, тестирует. Если все хорошо сливает ветку dev в master - так все изменеия попадают на рабочий сервер через автодеплой.


### Теперь подробно весь процесс:
#### 1. Когда приступаем к работе над git новым дефектом / функционалом, переключаемся на ветку dev и получаем ее последнюю версию:

- git checkout dev
- git pull origin dev     (origin - Название удаленного репозитория, dev - ветка)

#### 2. Допустим нужно пофиксить баг в функционале "Спасибо". Создаем новую ветку из dev:

- git checkout -b Thanks-bug-fix      (Создает ветку на основе текущей и переключает на нее)
