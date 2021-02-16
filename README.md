# Keeper - хранитель паролей

> Консольное приложение, которое помогает хранить пароли для веб-сайтов в зашифрованном виде. Для доступа к хранилищу нужен пароль, который задается в момент создания хранилища;

- [Keeper - хранитель паролей](#keeper---хранитель-паролей)
  - [Фичи](#фичи)
  - [Примеры использования](#примеры-использования)
    - [Создание нового хранилища](#создание-нового-хранилища)
    - [Добавление нового пароля](#добавление-нового-пароля)
    - [Генерация нового пароля](#генерация-нового-пароля)
    - [Просмотр всех доступных паролей](#просмотр-всех-доступных-паролей)
    - [Поиск по паролям](#поиск-по-паролям)
    - [Встроенная инструкция](#встроенная-инструкция)
    - [Изменение пароля хранилища](#изменение-пароля-хранилища)
  - [Предлагаемые этапы реализации](#предлагаемые-этапы-реализации)
    - [](#)
  - [Материалы](#материалы)

## Фичи

1. создание нового хранилища;
1. хранение всех паролей на диске;
1. добавление новых паролей;
1. генерация паролей разной длины и из разных наборов символов;
1. просмотр всех доступных паролей;
1. поиск по паролям; 
1. встроенная инструкция*;
1. автокомплит команд*;
1. изменение пароля хранилища*.

## Примеры использования

### Создание нового хранилища

```shell
keeper init
```

### Добавление нового пароля

```shell
keeper add <label> <password>
```

### Генерация нового пароля

```shell
keeper gen <lenght> -a <full/medium/low> -l <label>
```

- `-a` - `alphabet` - указывает на алфавит, из которого будет сгенерирован пароль, по умолчанию `medium`
    - `full` - все буквы алфавита + цифры + символы `!@#$%^&*()[]{};"'/?.><,~\|` и пробел
    - `medium` - все буквы алфавита + цифры + символы `!@#$%^&*`
    - `low` - все буквы алфавита + цифры
- `-l` - `label` - если указан этот флаг, то сгенерированный пароль будет [добавлен в хранилище](#добавление-нового-пароля) с этой меткой.

### Просмотр всех доступных паролей

```shell
keeper list
```

### Поиск по паролям

```shell
keeper find <label>
```

### Встроенная инструкция

```shell
keeper help
```

### Изменение пароля хранилища

```shell
keeper reencrypt
```

---

_При вызове любой из команд выше `keeper` сначала спрашивает пароль от хранилища.

## Предлагаемый порядок реализации

### Генерация паролей

Реализовать возможность [генерации паролей](#генерация-паролей) без сохранения на диск.

__Почитать по теме:__
- [Command line arguments in C/C++](https://www.geeksforgeeks.org/command-line-arguments-in-c-cpp/)
- [C++ Strings](https://www.tutorialspoint.com/cplusplus/cpp_strings.htm)
- [How do I create a random alpha-numeric string in C++?](https://stackoverflow.com/questions/440133/how-do-i-create-a-random-alpha-numeric-string-in-c)
