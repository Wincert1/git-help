# Памятка по работе с Git
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
Переходим в папку с проектами и клонируем проект:<br>
`git clone https://github.com/Wincert1/git-help.git git-help`<br>
Где **https://github.com/Wincert1/git-help.git** - удаленный репозиторий с проектом,<br>
**git-help** - папка с проектом


### Основные команды
`git remote -v` - Список удаленных репозиториев
`git branch` - Список локальных веток (текущая ветка отмечена звездочкой)
`git checkout dev` - Переключиться на ветку dev
`git checkout -b new-issue` - Создает новую ветку (new-issue) из текущей и переключается на нее
`git status` - Показывает измененения в файлах текущей ветки
`git add file.php` - Добавляет файл к текущей ветки.<br> 
IDE-шки как правило спрашивают нужно ли добавлять новые файлы автоматически, тогда эта команда не требуется. Но если этого нет, то все новые файлы нужно добавлять этой командой, иначе они не появятся в коммите.



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
1. Когда приступаем к работе над git новым дефектом / функционалом, переключаемся на ветку dev и получаем ее последнюю версию:

`git checkout dev`<br>
`git pull origin dev`<br>
(origin - Название удаленного репозитория, dev - ветка)

2. Допустим нужно пофиксить баг в функционале "Спасибо". Создаем новую ветку из dev:

`git checkout -b Thanks-bug-fix`<br>
(Создает ветку на основе текущей и переключает на нее)
