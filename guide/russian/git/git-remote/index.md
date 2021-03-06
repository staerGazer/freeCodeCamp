---
title: Git Remote
localeTitle: Git Remote
---
## Git Remote

`git remote` команда `git remote` позволяет вам управлять удаленными репозиториями Git. Удаленные репозитории являются ссылками на другие репозитории Git, которые работают на одной и той же базе кода.

Ты можешь [тянуть из](https://guide.freecodecamp.org/git/git-pull/) а также [нажимать на](https://guide.freecodecamp.org/git/git-push/) удаленные репозитории.

Вы можете нажать или потянуть либо URL-адрес HTTPS, например `https://github.com/user/repo.git` , либо URL-адрес SSH, например `git@github.com:user/repo.git` .

Не беспокойтесь, каждый раз, когда вы нажимаете что-то, вам не нужно вводить весь URL. Git связывает удаленный URL с именем, и имя, которое большинство людей использует, является `origin` .

### Список всех настроенных удаленных репозиториев

```bash
git remote -v 
```

Эта команда перечисляет все удаленные репозитории рядом с их местоположением.

Удаленные репозитории называются по имени. Как отмечалось выше, основной репозиторий для проекта обычно называется `origin` .

Когда вы используете [git clone](https://guide.freecodecamp.org/git/git-clone/) получить копию репозитория Git устанавливает исходное местоположение в качестве _происхождения_ удаленного хранилища.

### Добавить удаленный репозиторий

Чтобы добавить удаленный репозиторий в свой проект, вы должны выполнить следующую команду:

```bash
git remote add REMOTE-NAME REMOTE-URL 
```

`REMOTE-URL` может быть либо HTTPS, либо SSH. URL-адрес GitHub можно найти, щелкнув раскрывающееся меню «Клонировать или загрузить» в вашем репозитории.

Например, если вы хотите добавить удаленный репозиторий и вызвать его `example` , вы должны запустить:

```bash
git remote add example https://example.org/my-repo.git 
```

### Обновление удаленного URL-адреса

Если URL-адрес удаленного репозитория изменяется, вы можете обновить его следующей командой, где `example` - имя пульта:

```bash
git remote set-url example https://example.org/my-new-repo.git 
```

### Удаление пультов

Удаление пультов производится следующим образом:

```bash
git remote rm REMOTE-NAME 
```

Вы можете подтвердить, что пульт удален, просмотрев список существующих пультов:

```bash
git remote -v 
```

### Дополнительная информация:

*   [Удаленная документация Git](https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes)