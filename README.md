# First Project

---

Создан с *целью* **освоения** `git`

VCS (Version control system)
SCM (Source control management)

## Настройка git
```bash
$ git config --global user.name "User Namovich"
# имя или ник нужно написать латиницей и в кавычках

$ git config --global user.email username@yandex.ru
# здесь нужно указать свой настоящий email
```
Все глобальные настройки git хранятся в `.gitconfig`
```bash
cat ~/.gitconfig
```
или
```bash
git config --list
```

## Начало работы
Инициализация репозитория
```bash
git init
```
Разгитить папку
```bash
rm -rf .git # удалили подпапку .git
```
Посмотреть статус
```bash
git status
```
Добавить файлы в индекс
```bash
git add --all
git add -A # то же самое
git add .
git add file-name
```
Сохранение
```bash
git commit -m 'Мой первый коммит'
```
>[!info] `create mode 100644 readme.txt`
>100644 - обычный файл
>100755 - исполняемый файл
>120000 - файлы-ссылки и Linux

Посмотреть историю коммитов
```bash
git log
```
или в более сжатом виде
```bash
git log --oneline
```

## Связываем локальный репозиторий с удаленным
connect to remote repository on GitHub
```bash
git remote add origin git@github.com:sannjka/first-project.git
git branch -M main
git push -u origin main
```
Скопировать публичный ключ
```bash
pbcopy < ~/.ssh/id_rsa.pub
```
Проверить подключение
```bash
ssh -T git@github.com
```
Проверить, что репозитории связаны
```bash
git remote -v
```
Отправить изменения в удаленный репозиторий
```bash
git push -u origin main
```
>[!info] В первый раз нужно выполнить команду с ключом `-u`, чтобы связать локальную ветку с одноименной удаленной. В дальнейшем можно просто писать `git push`


