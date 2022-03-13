# Руководство по git

1. Сохраняете проект себе на компьютер (знаки "<" и ">" вводить не нужно, ссылка на репозиторий нашего проекта - https://github.com/rianriant/individual_task_2.git ):\
   `git clone <project http-link>`
   ***
2. Создаете ответвление проекта, в котором вы будете работать:\
   `git branch <your_branch_name>`
   ***
3. Переходите на эту ветку (после этого возвращаться на основную ветку, которая называется `master` не понадобится):\
   `git checkout <your_branch_name>`
   ***
4. Работа теперь будет происходить так: из сделанных вами изменения вы будете как бы выращивать снежный ком. После внесения изменений, вы можете добавить их в свой слепок командой `git add .`. Потом надо будет сказать гиту : "так, я уверен в своих изменениях, давай их сохраним у тебя под определенным именем, а дальше я буду катать новый комок изменений"; для этого надо будет использовать команду `git commit 'название набора изменений, которые вы хотите сохранить"`. Теперь можете отправить изменения, которые гит зафиксировал при команде `git commit` в наше общее хранилище в интернете, на репозиторий:\
   \
    _свою ветку вы пока создали только у себя на компьютере, давайте создадим её и у нас на сервере такой командой:_\
    `git push --set-upstream origin <your_branch_name>`\
    \
    Теперь можем загрузить на неё свои изменения:\
    `git push`\
    \
    То, что вы внесли в слепока командой `git add .`, но не зафиксировали командой `git commit` не будет отправленно на сервер.
   Изменения, которые вы загрузите на сервер будут касаться только вашей ветки: я их проверю и соединю с главной веткой `master`.

   ***

5. Предположим, я изменил ветку `master`, теперь наш проект обновился на сервере, но у вас на компьютерах он остался прежним. Что делать, чтобы ваша локальная версия тоже обновилась? Надо вернуться на ветку `master`, обновить её командой `git pull`, затем перейти в свою свобственную ветку командой `git checkout <your_branch_name>`, а потом перекачать, слить полученные изменения с ветки `master` в ветку, на которую вы только что пересели вот этой командой : `git merge master`

---
