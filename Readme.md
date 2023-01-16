# Инструкция по работе с Git.

## Что такое Git ?.

***Git*** Самая популярная реализация распределенной системы контроля версий (Версионность поддерживается и на сервере, и у каждого клиента). Самой распространенной реализацией ***Git*** является (*GitHub*) [https://github.com].

## Подготовка репозитория
Для создания репозитория используется комманда *git init*. Для этого необходимо открыть в терминале папку с будущим репозиторием и написать команду *git init*. 


### Создание "коммита"

Для создания новой фиксации (коммита) используется команда *git commit*. Для этого в терминале с папкой- репозиторием пишем *git commit -m "<Сообщение к коммиту>*. Сообщение к коммиту писать ***Обязательно!!!*** 

### Добавление файлов к коммитам ###

Для добавления файлов к коммиту используется команда *git add*. Используется она следующим образом: в терминале с папкой репозиторием пишем *git add<название файла>*. 



## Журнал изменений.

Для просмотра истории измененний используется команда *git log*. Для этого в терминале с папкой-репозиторием необходимо написать команду *git log*.

## Перемешение между Коммитами.
Для перемещения на другую фиксацию (коммит) используется команда *git checkout*. Для этого необходимо, как показано в прошлом пункте, в журнале изменений найти необходимый коммит и его хеш (номер),после чего в терминале с папкой-репозиторием надо написать *git checkout<хеш коммита>*.
После выполнения этой команды мы попадаем в состояние **detached head**, в котором никакие следующие коммиты сохранятся не будут. Для выхода из этого состояния необходимо написать команду *git checkout master*.

## Ветвление в Git.
Для создания веток в *Git* необходимо написать в терминале команду *git branch*,Для этого в терминале с папкой репозиторием необходимо написать команду *git branch<название ветки>
## Perekluchenie между ветками в Git/
Для того чтобы узнать в какой ветке вы находитесь используется команда *git branch*, для этого в терминале необходимо написать команду *git branch*.

Для переключения между ветками в *Git* используется команда *git checkout*, Для этого в терминале с папкой репозиторием необходимо написать команду *git checkout<название ветки>*

## Слияние веток и разрешение конфликтов.
Для слияния веток в *Git* Используется команда *git merge *, для этого в терминале необходимо сначала перейти в  ветку (например : *Master*) Для этого используется команда *git checkout master*, затем написать команду *git merge<название ветки>*.*** (Команда *merge* вызывается из той ветки куда вы хотите слить изменения!!!!) ***
Разрешение конфликтов при слиянии веток. Для получения финальной версии необходимо либо выбрать вариант вручную: *(Для этого необходимо удалить строки <<<<HEAD И строку ===== после необходимо в терминале набрать команду *git add* и команду *git commit -m "коментарий", Либо воспользоватся встроеным механизмом VSC.

## Удаление веток.
Для того чтобы удалить ветку в *Git* используется команда *git branch -d*,для этого необходимо в терминале прописать команду *git branch -d<название ветки>*.