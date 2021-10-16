# Инструкция по работе с Git

## Что такое Git?

**Git** - одна из реализаций распределённых систем контроля версий. Позволяет контролировать версионность файлов как локально, так и на удалённом сервере. Самая популярная на данный момент.

*это система помогающая отслеживать и управлять версиями файлов. Особенно сильно помогает при коллективной разработке. Гораздо удобнее чем пересылка по голубиной =) почте или ручное использования отдельных папок (так как хранит только изменения, а не полные версии фаилов)*

## Подготовка репозитория

## Создание "сохранений"
Создать "сохранения" они же фиксации или коммиты, мы можем с помощью команды *git commit*. Для этого необходимо написать команду *git commit-m <сообщение к коммиту>* сообщение к коммиту писать **ОБЯЗАТЕЛЬНО**. Все файлы должны быть добавлены в коммит с помощью команды *git add*. Если файлы не добавлены то можно использовать флаг *-a* и команда преобретёт вид *git commit -a -m <сообщение к коммиту>*.

## Журнал изменений

## Перемещение между "сохранениями"
Для переключения между "сохранениями"(коммитами) необходимо использовать команду *git checkout <номер коммита для перекючения>*. Номер коммита берётся из истории коммитов и на него произойдёт переключение.

Комманды *git reset* и *git revert* позволит отменять изменения. Команда *git revert* возвращает к указанному коммиту, создавая новый коммит, а команда *git reset* возвращает к указанному коммиту и затирает историю изменений до указанного коммита. Применяется это следующим образом: *git revert <норме коммита>* или *git reset --hard <номер коммита>*.

## Ветки в Git

## Слияние веток и решение конфликтов

## Удаление веток