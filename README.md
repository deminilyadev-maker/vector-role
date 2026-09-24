# Домашнее задание

**Студент:** Демин Илья Викторович\
**Репозиторий:**
[vector-role](https://github.com/deminilyadev-maker/vector-role)

------------------------------------------------------------------------

# Molecule

## 1. Запуск существующего сценария

Выполнен запуск существующего Molecule-сценария из задания.

Результат выполнения:

[![Ubuntu Xenial
test](https://github.com/deminilyadev-maker/vector-role/blob/main/screenshots/Ubuntu_xenial_test.png)](https://github.com/deminilyadev-maker/vector-role/blob/main/screenshots/Ubuntu_xenial_test.png)

[Ubuntu_xenial_test.png](https://github.com/deminilyadev-maker/vector-role/blob/main/screenshots/Ubuntu_xenial_test.png)

## 2. Создание сценария тестирования `vector-role`

Для роли `vector-role` создан отдельный Molecule-сценарий.

Сценарий создан в каталоге:

``` text
molecule/default/
```

Для данного этапа отдельный скриншот не прикладывается.

## 3. Добавление дистрибутивов и тестирование роли

В сценарий добавлено тестирование роли `vector-role`.

Результат выполнения:

[![Vector
test](https://github.com/deminilyadev-maker/vector-role/blob/main/screenshots/Vector_test.png)](https://github.com/deminilyadev-maker/vector-role/blob/main/screenshots/Vector_test.png)

[Vector_test.png](https://github.com/deminilyadev-maker/vector-role/blob/main/screenshots/Vector_test.png)

## 4. Добавление проверок в `verify.yml`

В `verify.yml` добавлены проверки работоспособности роли `vector-role`.

Для данного этапа отдельный скриншот не прикладывается.

## 5. Повторный запуск тестирования

После внесения изменений тестирование роли было запущено повторно.

Результат проверки:

[![Vector
verify](https://github.com/deminilyadev-maker/vector-role/blob/main/screenshots/vector_verify.png)](https://github.com/deminilyadev-maker/vector-role/blob/main/screenshots/vector_verify.png)

[vector_verify.png](https://github.com/deminilyadev-maker/vector-role/blob/main/screenshots/vector_verify.png)

------------------------------------------------------------------------

# Tox

## 1. Добавление файлов из `example`

В репозиторий добавлены необходимые файлы для работы Tox.

В результате в роли присутствуют:

``` text
tox.ini
tox-requirements.txt
```

Для данного этапа отдельный скриншот не прикладывается.

## 2. Запуск контейнера

Для выполнения задания использовался контейнер с репозиторием
`vector-role`.

Команда запуска:

``` bash
docker run --privileged=True -v <path_to_repo>:/opt/vector-role -w /opt/vector-role -it aragast/netology:latest /bin/bash
```

Для данного этапа отдельный скриншот не прикладывается.

## 3. Запуск `tox` внутри контейнера

В контейнере была выполнена команда:

``` bash
tox
```

Для данного этапа отдельный скриншот не прикладывается.

## 4. Создание облегчённого сценария Molecule с Podman

Создан отдельный облегчённый сценарий:

``` text
molecule/podman/
```

Сценарий использует драйвер:

``` yaml
driver:
  name: podman
```

Результат выполнения Podman-сценария:

[![Podman
test](https://github.com/deminilyadev-maker/vector-role/blob/main/screenshots/podman%20test.png)](https://github.com/deminilyadev-maker/vector-role/blob/main/screenshots/podman%20test.png)

[podman
test.png](https://github.com/deminilyadev-maker/vector-role/blob/main/screenshots/podman%20test.png)

## 5. Настройка `tox.ini`

В `tox.ini` добавлена команда запуска облегчённого сценария:

``` ini
commands =
    {posargs:molecule test -s podman --destroy always}
```

Для данного этапа отдельный скриншот не прикладывается.

## 6. Запуск `tox`

После настройки `tox.ini` выполнен запуск:

``` bash
tox
```

Результат успешного выполнения:

[![Final
Tox](https://github.com/deminilyadev-maker/vector-role/blob/main/screenshots/final_tox.png)](https://github.com/deminilyadev-maker/vector-role/blob/main/screenshots/final_tox.png)

[final_tox.png](https://github.com/deminilyadev-maker/vector-role/blob/main/screenshots/final_tox.png)

------------------------------------------------------------------------

# Результат

В репозитории реализованы два Molecule-сценария:

``` text
molecule/
├── default/
└── podman/
```

Также добавлен:

``` text
tox.ini
```

Репозиторий:

<https://github.com/deminilyadev-maker/vector-role>

## Git tags

В репозитории используются версии:

``` text
1.0.0
1.2.0
1.3.0
```

Для текущего задания добавлен тег:

``` text
1.3.0
```
