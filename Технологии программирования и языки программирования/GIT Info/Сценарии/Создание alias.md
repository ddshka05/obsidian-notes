## Cоздание простых алиазов

Для создания постоянного алиаза, доступного на всех локальных и удаленных репозиториях, необходимо воспользоваться [[git config]].

	 git config --global alias.<короткое-имя> "<полная-команда>"

Для создания локального алиаза, доступного только для локального репозитория:

	 git config --local alias.<короткое-имя> "<полная-команда>"

#### Где хранятся:

Алиасы автоматически сохраняются в конфигурационном файле:

- **Глобальные** (для всех репозиториев):  
    `~/.gitconfig` (Linux/macOS) или `%UserProfile%\.gitconfig` (Windows)
- **Локальные** (только для текущего репозитория):  
    `.git/config`

Для прочтения содержимого алиазов можно воспользоваться командой [[git cat-file]] по отношению к `/gitconfig`(глобальные алиазы) или `config` (локальные алиазы)

Либо можно через [[git config]] можно получить все алиазы 

	git config --get-regexp alias

***Пример содержимого:***
![[Pasted image 20250423193448.png]]

#### Редактирование алиазов

Лучше всего редактировать алиазы вручную посредством [[git config]].

	git config --global --edit  # Откроет .gitconfig в редакторе

#### Удаление алиаза

Используем [[git config]]:

	git config --global --unset alias.название
	Пример:
	git config --global --unset alias.st

#### Перенос алиасов на другой компьютер

Для переноса необходимо просто скопировать файл .gitconfig
	
	cp ~/.gitconfig ~/backup.gitconfig
#### Полезные алиазы

Для упрощения работы я использую такие алиазы

	git config --global alias.st "status -s"
	git config --global alias.ci "commit"
	git config --global alias.co "checkout"
	git config --global alias.br "branch"
	git config --global alias.unstage "reset HEAD --"
	git config --global alias.last "log -1 HEAD"

## Создание сложных алиазов

Используются функции [[Git Bash или просто Bash]] или если мы на линукте, то просто bash

