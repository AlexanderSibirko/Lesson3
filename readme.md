# Инструкция по работе с Git

## Что такое Git?

**Git** - одна из реализаций распределённых систем контроля версий. Позволяет контролировать версионность файлов как локально, так и на удалённом сервере. Самая популярная на данный момент.

*это система помогающая отслеживать и управлять версиями файлов. Особенно сильно помогает при коллективной разработке. Гораздо удобнее чем пересылка по голубиной =) почте или ручное использования отдельных папок (хранит только изменения, а не полные версии фаилов что существенно экономит "место")*

Скачать **Git** можно по ссылке [сайт Git](https://git-scm.com/).

## Подготовка репозитория

**Репозиторий** - это папка в которая поддерживает версионирование фаилов. Для того что-бы превраить папку в **репозиторий** необходимо находять в папке использовать команду *git init*.

## Создание "сохранений"

Создать "сохранения" они же фиксации или коммиты, мы можем с помощью команды *git commit*. Для этого необходимо написать команду *git commit-m <сообщение к коммиту>* сообщение к коммиту писать **ОБЯЗАТЕЛЬНО**. Все файлы должны быть добавлены в коммит с помощью команды *git add*. Если файлы не добавлены то можно использовать флаг *-a* и команда преобретёт вид *git commit -a -m <сообщение к коммиту>*.

## Журнал изменений

Для того чтобы увидеть журнал изменений необходимо ввести команду *git log*. ![Пример git log](GitLog.png)
Существуют дополнительные флаги для более удобного просмотра журнала изменений. Наример команда *git log --onelinе* показывает сокращенную информацию по изменениям в одну строку. ![Пример git log --oneline](GitLogOneLine.png)

## Перемещение между "сохранениями"

Для переключения между "сохранениями"(коммитами) необходимо использовать команду *git checkout <номер коммита для перекючения>*. Номер коммита берётся из истории коммитов и на него произойдёт переключение.

Комманды *git reset* и *git revert* позволит отменять изменения. Команда *git revert* возвращает к указанному коммиту, создавая новый коммит, а команда *git reset* возвращает к указанному коммиту и затирает историю изменений до указанного коммита. Применяется это следующим образом: *git revert <норме коммита>* или *git reset --hard <номер коммита>*.

## Ветки в Git

**Ветка** - это черновик изменений создаваемый, для того чтобы не "испортить" чистовую рабочую версию, пока работа над измененим не закончена полностью. Для того чтобы создать новую **ветку** используется команда *git branch <имя ветки>*.


Чтобы просмотреть список существующих **веток** нужно просто ввести команду *git branch*

 ![Пример git branch](GitBranch.png)

Для переключения между ветками используется команда как и для переключения между "сохранениями", только вместо <номера сохранения> используется <имя ветки>.
Пример: *git checkout <имя ветки>*,  

## Слияние веток и решение конфликтов

Для слияния веток используется команда *git merge <имя ветки>*, при этом просиходит "вливание" всех изменений из указаннов ветки в текущую.

При возникновении конфликта, изменения "вливания" затрагивают то что было изменено в основной ветке с момента отсоединия ветви, необходимо вручном режиме выбрать что оставить и произвести вручную "коммит".

![Пример конфликта](GitMergeConflict.png)

После слияния веток мы можем увидеть историю принятых изменений с некоторой визуализацией использую команду *git log --graph*

![Пример git log --graph](GitLogGraph.png)

## Удаление веток

Удаление ветки после того как она больше не нужна, например её слияния с основной веткой. Нужно ввести команду *git branch -d <имя ветки>*.

## Работа с удалённым репозитерием

Для того чтобы связать локальный репозиторий с удаленным нужно их "подружить" через команду *git remote add <name> {url}*. После чего **необходимо** задать основную ветку при помощи команды *git branch -M <имя ветки>*.

## Отправка или принятие изменений из/в удалённый репозиторий 
