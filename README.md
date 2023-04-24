# Репозиторий для **pull request**
* В своём аккаунте на GitHub создать копию репозитория **"AndreyBulgakov19/SCV_Git_PR"** с помощью кнопки **"Fork"**.
---
* Клонировать копию репозитория на локальный компьютер.
---
* Создать новую ветку.
---
* Добавить файл с инструкцией в новую ветку.
---
* Дополнить инструкцию разделами по работе с удалёнными репозиториями, pull request.
---
* Зафиксировать изменения (коммиты).
---
* Отправить изменения на GitHub.
---
* На сайте GitHub выполнить **Pull request**.
---
# Работа с Git и GitHub 

## 1. Поверка наличия установленного Git  
В терминале выполнить комманду *git version*
Если Git установлен, появится сообщение с информацией о версии программы. Иначе будет сообщение об ошибке. 

## 2. Установка Git 
Загружаем последнюю версию Git c cайта https://git-scm.com/downloads. 
Устанавливаем с настройками по умолчанию.

## 3. Настройка Git 
При первом использовании Git необходимо представиться. Для этого нужно ввести в терминале две команды: 
```
git config --global user.name "Ваше имя на английском"
``` 
## 4. Инициализация репозитория 
Получить репозиторий можно двумя способами. 
1. В терминале перейти к папке, в которой хотим создать репозиторий. Выполняем команду: 
``` 
git init 
``` 
В исходной папке появится скрытая папка *git* 
2. Клонировать существующий репозиторий Git из любого места. Сделать это можно с помощью команды: 
``` 
git clone <aдрес репозитория> 
``` 

## 5. Запись изменений в репозитории. 
* Для создания в терминале нового коммита вводим: 
``` 
git commit -m "название заголовка, который добавили" 
``` 
* Чтобы получить информацию от git о его текущем статусе вводим: 
``` 
git status  
```
* Для добавления файла или файлов к следующему коммиту вводим: 
``` 
git add <имя файла> 
``` 
* Если мы хотим увидеть разницу между текущим файлом и закоммиченным файлом (сохраненным), вводим: 
``` 
git diff 
``` 

## 6. Просмотр истории коммитов. 
* Если понадобилось просмотреть историю изменений коммитов, то вводим: 
```
git log 
``` 
* Также похожяю программа, но с добавлением -h используется для просмотра всех комманд Git: 
``` 
git log -h 
``` 

## 7. Перемещение между сохранениями. 
Для переходов между коммитами используется команда (нужный коммит мы увидим после введения предварительно **git log**): 
``` 
git chekout <7мизначный код, можно ввести первые 4 знака> 
``` 
Мы перешли в тот коммит, который нужен.
Если же нам необходимо к последней версии коммита, то вводим: 
``` 
git switch 
``` 

## 8. Игнорирование файлов.
Для того, чтобы исключить из отлеживания опеределенные файлы или папки, необходимо создать там файл ***.gitignore*** и записать в него их названия или шаблоны, соответствующие таким файлам или папкам. 

## 9. Создание веток в Git.
По умолчанию имя основной ветки в Git - *master*. 
Создать ветку можно командой: 
``` 
git branch <имя новой ветки> 
``` 
Cписок веток в репозитории можно смотреть с помощью команды `git branch` 
Текущая ветка будет отмечена звездочкой: **\*master** 

## 10. Слияние веток и разрешение конфликтов. 
для слияния выбранной ветки с текущей нужно выполнить команду: 
``` 
git merge <название выбранной ветки> 
``` 
Если была изменена одна и та же часть файла в обеих ветках, то может возникнуть конфликт, который потребует участия пользователя. 
VSCode предлагает варианты разрешения.  
В этой ситуации мы можем выбрать 3 варианта: 
* 1. Выбрать изменения, сделанные в *основной* ветке 
* 2. Выбрать изменения, сделанные во *второстепенной* ветке 
* 3. Оставить *оба* изменения.
После выбора варианта, необходимо выполнить команду `git commit -am "Разрешили конфликт"`. 

## 11. Удаление веток. 
Чтобы удалить ветку, которую не нужно более, необходимо в основной ветке выполнить команду: 
``` 
git branch -d <название ветки> 
```
Если данную команду вызывать во второстепенной ветке - будет ошибка и ветка не удалиться. Поэтому стоит уточниться с помощью команды git branch в основной ли Вы ветке находитесь. 

## Работа с удаленными репозиториями. 
Для начала работы с удаленными репозиториями, нужно:
1. Создали аккаунт на GitHub.com 
2. Создать локальный репозиторий 
3. "Подружить" ваш локальный и удаленный репозиторий. GitHub при создании нового репозитория подскажет как это сделать. 
4. Возможно, нужно будет авторизоваться на удаленном репозитории. 

### Работа со своим удаленным репозиторием.
При работе со своего аккаунта в GitHub удаленным репозиторием, создаем *new repository*, кликая на **+** в верхнем правом углу. Даем имя и сохраняем. Далее в **VSCode** в локальном репозитории в терминале вводим `git clone <cсылка на удаленный репозиторий>`. 

Вводим необходимую информацию. После окончания всех записей вводим в терминале команду `git commit -am "Добавили информацию"`. 

Для получения изменений и слияния с локальной версией вводим команду 
``` 
git pull 
``` 
Для отправления локальной версии репозитория на внешний/удаленный 
``` 
git push 
``` 
Далее в GitHub видим наш репозиторий. При необходимости можно ввести информацию в GitHub, коммит расположен чуть ниже. Вводим в коммит что мы сделали и сохраняем. 

### Работа с чужим удаленным репозиторием. 
Найдя нужный нам репозиторий в GitHub, мы кликаем на кнопку **FORK**, делая ответвление этого репозитория к себе в аккаунт. 
Далее копируем ссылку данного репозитория и в **VSCode** пишем команду: 
```
git clone <копируем ссылку>
``` 
Далее создаем папку для репозитория 
``` 
git cd название_репозитория_скопированного 
``` 
Для добавления своей информации создаем ветку `git branch название_ветки` и переходим на нее `git checkout название_ветки`. 
В данной ветке добавляем информацию, далее команда `git commit -am "Информируем что сделали"`. 
А после `git push`. 
Далее переходим в GitHub и следуем за зелеными кнопками, начиная с pull request. 

При скачивании из GitHub репозитория сам GitHub может дать варианты команд, которые Вам нужны. Поэтому следуем за командами по GitHub. 
Таким образом, можно внести свои изменения в репозиторий. А автор уже сам решит будет ли он эту информацию оставлять.