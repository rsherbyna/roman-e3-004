# Базовый курс веб-разработки [![Build Status](https://travis-ci.com/Maximumstart-basic-course/roman-e3-004.svg?branch=master)](https://travis-ci.com/Maximumstart-basic-course/roman-e3-004)

* Студент:  `Roman Shcherbyna`.
* План занятий: [нате](https://docs.google.com/document/d/1e6PG06nszODebSn5DsqBsG6AujbXoKmqj1drDsoQElM/edit?usp=sharing).
* Требования к выпускному проекту: [тут](https://docs.google.com/document/d/16VOU_viRMtN2wBW6nv_2rGkjsI8PiBILPVwKOMp-vMs/edit?usp=sharing).
* Основные репозитории: [здесь](https://github.com/Maximumstart-basic-course).
* Репозиторий с домашними заданиями: [там](https://github.com/MaximumStart/essential-course).

---

Не удаляй и ничего не меняй в файлах: `.eslintrc`, `.gitignore`, `package.json`, `package-lock.json`.

Если есть необходимость размещать какие-то свои личные файлы, то в корню локального репозитория есть специальная папка `Personal`, которая не индексируется и не прилетает на проверку.

---

# Что делать, если потерялся конфиг гита?

## 1. Создай SSH-ключ, если еще этого не делал

Для этого в `Git BASH` или в терминале запусти команду:

```bash
ssh-keygen
```

Нажимай `Enter` до появления графического ключа. 

После чего, в домашней папке (для того, чтобы узнать расположение домашней папки, в `Git BASH` введи символ `~` и нажми `Enter`) найди папку `.ssh`, а в ней файл `id_rsa.pub`. Открой его в любом текстовом редакторе и полностью скопируй его содержимое.

Зайди на GitHub -> Settings -> SSH and GPG keys -> New SSH key. В поле __Title__ введи любое название, а в поле __Key__ вставь содержимое файла `id_rsa.pub`.

## 2. Представься

Укажи свой логин на Github и email, которые потом будут записываться в каждый коммит. Делается это с помощью команд:

```bash
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```

# Что делать, если все ок?

## 1. Найди свой репозиторий и форкни его

На [странице курса](https://github.com/Maximumstart-basic-course) найди свой репозиторий, перейди в него и нажми кнопку `Fork`. Все дальнейшее обучение будет проходить непосредственно в форкнутом репозитории.

## 2. Клонируй репозиторий себе на компьютер

Найди форкнутый репозиторий у себя в аккаунте, нажми в нем на кнопку `Clone or download`, выбери `Use SSH` и скопируй ссылку. На рабочем столе или в любой другой папке откройте `Git BASH` и введи следующую команду:

```bash
git clone <ссылка_из_гитхаба>
```

## 3. Установи линтер

Установи [Node.js](https://nodejs.org/), после чего открой папку или перейди в нее из консоли командой:

```bash
cd <название репозитория>
```

Установи все необходимые для работы файлы командой: 

```bash
npm i
```

## 4. Поправь .gitignore

Открой файл `.gitignore` в корне проекта и в первых двух строках убери знак октоторпа "#". После этого на GitHub не будут отправляться папки __node_modules__, __Personal__ и сам файл __.gitignore__.

## 5. Создай ветку и измени файл README.md

Для создания новой ветки введи команду:

```bash
git checkout -b first-task
```

В этом курсе мы для выполнения каждого задания будем создавать отдельную ветку, а потом будем вливать ее в основной репозиторий.

Сейчас ты находишься в ветке `first-task`, убедиться в этом можно, используя команду:

```bash
git status
```

В ответе должна быть строка:

```bash
On branch first-task
```

В этом файле пока еще нет информации о тебе, вместо нее ты видишь надписи `undefined`. Заполни эту информацию, чтобы нам было удобнее работать с тобой. Все остальное оставь без изменений.

## 6. Отправь все файлы в свой форк на Гитхаб

Для этого в своей рабочей папке запусти `Git BASH` и выполни команду

```bash
git add README.md
```

чтобы проиндексировать файл. После чего выполни:

```bash
git commit -m 'Изменила Readme'
```

Консоль подскажет что-то вида:

```
[master c75f147] Изменила Readme
 1 file changed, 26 insertions(+), 1 deletion(-)
 rewrite README.md (100%)
```

Отправь свой коммит на Гитхаб командой:

```bash
git push origin first-task
```

Тут очень важно указать ветку, которая отправляется, потому что сейчас у нас есть две ветки -- `master` и `first-task`. В `master` никаких изменений нет, а в `first-task` ми обновили файл `README.md`

## 7. Отправь все файлы в свой форк на Гитхаб

Убедитесь, что в репозитории появился свежий коммит и нажмите на кнопку `New pull request`, на появившейся странице нажмите `Create pull request`, оставьте комментарий для наставника и сообщите о готовом к проверке домашнем задании в Телеграм. В течение нескольких часов задание проверят и сольют с главным репозиторием.

## 8. Сообщи ментору

После создания pull request'a, сообщи ментору о том, что задание готово к проверке.

# Критерии оценивания

1. В конце курса студенты проходят компьютерное тестирование, которое включает все вопросы курса ‒ Bash, Git, адаптивная верстка, Bootstrap 4, Javascript (ES-2015). __Минимальный проходной балл ‒ 70%__.

2. После тестирования студенты проходят письменный контроль, который состоит из 10 случайно выбранных экзаменационных вопросов по JavaScript. __Необходимо правильно ответить минимум на 6 из 10 заданий (среди них минимум 2 задачи)__.

3. После тестового и письменного контроля студент __обязательно проходит устное собеседование__ по всем темам курса.

4. Если студент успешно одолевает все препятствия, он получает .psd-файл выпускного проекта и список требований к нему. На сдачу готового проекта выделяется 14 дней, все даты и требования будут объявлены заранее.

# Как синхронизировать основной и локальный репозитории?

1. Добавляем адрес основного репозитория, если еще этого не сделали:

```bash
git remote add main <адрес основого репозитория>
```

2. Переходим в **master**, если еще не там:

```bash
git checkout master
```

3. Получаем ветки из основного репозитория:

```bash
git fetch main
```

4. Сливаем наш основной репозиторий с локальным:

```bash
git merge main/master
```

# Как тестировать мой код?

Мы задали определенный правила, исполнение которых и проверяет линтер в автоматическом режиме. Роль ментора при этом не теряется, однако, если код не проходит проверку линтером, то и ментор его не примет.

Если не знаешь значения какой-то ошибки, то просто загугли. Все эти правила хорошо задокументированы.

Для прохождения теста введи команду:

```bash
npm test или npm t
```

Некоторые ошибки линтер предложит исправить автоматически. Для этого запусти команду:

```bash
npm run eslint:fix
```
