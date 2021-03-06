# Linux

Подборка упражнений, задач и решений.

## Содержание

1. Who is the inventor of Linux?
1. What does GNU stands for?
1. Which Linux distribution was the basis for Ubuntu?
1. How to find out what version of Linux you are running?
1. How long can a filename in Linux be?
1. Which command is used to see the online manual?
1. What is the symbolic representation of this numeric permission: 644?
1. Which of the following are valid Linux wildcards?
1. What are the contents of /bin directory?
1. What are the contents of /etc directory?
1. What are the contents of /dev directory?
1. What are the contents of /home directory?
1. Для чего нужен cron?
1. What is the default administrator username?
1. Где хранятся пароли пользователей?
1. Что означает право на исполнение для директории?
1. Как создать пользователя?
1. Как напечатать на экран значение переменной `а`?

### Who is the inventor of Linux?

Кто является изобретателем Linux?

a. Richard Stallman

b. Linus Torvalds

c. Andrew Tanenbaum

d. Ken Thompson

**a. ЛОЖЬ**. Ричард Мэттью Столлман — основатель движения свободного программного обеспечения, проекта GNU, Фонда свободных программ и Лиги за свободу программирования.

**b. ИСТИНА**. Воодушевлённый прочтением книги Эндрю Таненбаума, посвящённой операционной системе Minix, Линус создал Linux — ядро операционной системы GNU/Linux, являющейся на данный момент самой распространённой из свободных операционных систем.

**c. ЛОЖЬ**. Э́ндрю Стюарт Таненба́ум (англ. Andrew Stuart Tanenbaum) (родился 16 марта, 1944 года) — профессор Амстердамского свободного университета, где возглавляет группу разработчиков компьютерных систем; защитил докторскую диссертацию по физике в Калифорнийском университете в Беркли. Известен как автор Minix (свободная Unix-подобная операционная система для студенческих лабораторий), книг по компьютерным наукам и RFID-вируса. Также является главным разработчиком пакета «Amsterdam Compiler Kit». Сам он считает свою преподавательскую деятельность наиболее важной.

**d. ЛОЖЬ**. Кен То́мпсон — пионер компьютерной науки, известен за свой вклад в создание языка программирования C и операционной системы UNIX.

### What does GNU stands for?

a) Gnu’s not Unix

b) Geek Needed Unix

c) Genuinely Not Unix

d) Great New Unix

### Which Linux distribution was the basis for Ubuntu?

a) Fedora

b) CentOS

c) FreeBSD

d) Debian

### How to find out what version of Linux you are running?

Как узнать, какую версию Linux вы используете?

a. cat /etc/lsb-release

b. lsb_release -d

c. cat /proc/version

d. cat /etc/issue

**a. НЕИЗВЕСТНО**. "cat (от англ. concatenate) — утилита UNIX, выводящая последовательно указанные файлы (или устройства), таким образом, объединяя их в единый поток. Если вместо имени файла указывается «-», то читается стандартный ввод... Может использоваться в следующих случаях:... когда требуется просмотреть содержимое файла", "Cat" https://ru.wikipedia.org/wiki/Cat

"Таблица 10.8. Некоторые важные каталоги, существующие в большинстве систем Linux... Каталог ```etc``` содержит разные системные файлы". "Современные операционные системы", "Глава 10. Изучение конкретных примеров: Unix, Linux и Android. 10.6. Файловая система UMIX. 10.6.1. Фундаментальные принципы", Эндрю Таненбаум, 849 страница.

**b. ЛОЖЬ**. "Команда lsb-release -- это простой инструмент, который помогает определить какой Linux используется и его соответствие Linux Standard Base. Отчёт по соблюдению LSB не выводится, если не установлены требуемые метапакеты". https://packages.debian.org/ru/sid/lsb-release

"-d is a operator to test if the given directory exists or not". "What is the meaning of `! -d` in this Bash command?", https://stackoverflow.com/questions/37403759/what-is-the-meaning-of-d-in-this-bash-command. Например, если ввести директорию с оператором ```-d```, то после вывода адреса существующей папки появится информация ": is a directory".

**c. ИСТИНА**. "If you cat the /proc/version file, this is what you're going to see (I'm using a RedHat 5.2 system for this)", "Use /proc/version to identify your Linux release" https://www.unixtutorial.org/2009/04/use-proc-version-to-identify-your-linux-release/

"Файловая система /proc является механизмом для ядра и его модулей, позволяющим посылать информацию процессам (отсюда и название /proc ). С помощью этой виртуальной файловой системы Вы можете работать с внутренними структурами ядра, получать полезную информацию о процессах и изменять установки (меняя параметры ядра) на лету. Файловая система /proc располагается в памяти в отличие от других файловых систем, которые располагаются на диске". "О файловой системе /proc", Sandeep Grover http://rus-linux.net/lib.php?name=/MyLDP/proc/fs-proc.html

**d. ИСТИНА**. "Через issue (OpenSUSE/Debian) - ```$ cat /etc/issue```", "Определить дистрибутив Linux"

P.S. на MacOS можно узнать ```system_profiler SPSoftwareDataType```.

### How long can a filename in Linux be?

a. 8 characters

b. 11 characters

c. 64 characters

d. 255 characters

**d. ИСТИНА**. "Каталог UNIX содержит по одной записи для каждого файла этого каталога. Каждая запись каталога максимально проста, так как в системе UNIX используется система i-узлов (см. рис. 4.10). Запись каталога, как показано на рис. 4.27, состоит всего из двух полей: имени файла (14 байт) и номера i-узла для этого файла (2 байта)". "Современные операционные системы", "Глава 4. Файловые системы. 4.5.2. Файловая система UNIX V7", Эндрю Таненбаум, 365 страница.

"Стандартом ISO 9660 определены так называемые три уровня. На уровне 1 применяются самые жесткие ограничения и определяется, что имена файлов ограничиваются уже рассмотренной схемой 8 + 3 символа, а также требуется, чтобы все файлы были непрерывными согласно ранее данному описанию. Кроме того, на этом уровне определено, что имена каталогов ограничены восемью символами и не могут иметь расширений. Использование этого уровня предоставляет максимальные возможности того, что компакт-диск будет читаться на любом компьютере.

На уровне 2 делаются послабления ограничений по длине. На нем именам файлов и каталогов позволено иметь длину до 31 символа, но при сохранении того же набора символов". "Современные операционные системы", "Глава 4. Файловые системы. 4.5.3. Файловые системы компакт-дисков", Эндрю Таненбаум, 369 страница.

"Имена файлов в Linux были 14 байтов в более ранней версии Unix. Но современная система Linux имеет 255 байт для имен файлов. Поскольку для символа требуется 1 байт, длина становится 255 символов. Также папки рассматриваются как файлы в системе Linux". Anwar, "[How long can file names be?](https://askubuntu.com/questions/166764/how-long-can-file-names-be)"

### Which of the following are valid Linux wildcards?

a. *

b. .

c. %

d. ?

**a. ИСТИНА**. "Чтобы было легче указывать группы файлов, оболочка принимает так называемые волшебные символы (magic charecters), иногда называемые также групповыми (wild cards). Например, символ «звездочка» означает все возможные текстовые строки, так что строка

```ls *.c```

дает указание программе `ls` вывести список всех файлов, имена которых оканчиваются на `.c`. Если существуют файлы x.c, y.c и z.c, то данная команда эквивалентна команде 

```ls x.c y.c z.c```". "Современные операционные системы", "Глава 10. Изучение конкретных примеров: Unix, Linux и Android", Эндрю Таненбаум, 798 страница.

"Подстановочный знак - это символ, который может использоваться в качестве замены любого класса символов в поиске, тем самым значительно увеличивая гибкость и эффективность поиска.

Подстановочные знаки обычно используются в командах shell в Linux и других Unix-подобных операционных системах. Shell - это программа, которая предоставляет текстовый пользовательский интерфейс и основной функцией которого является выполнение команд, введенных пользователями, и отображение их результатов.

Подстановочные знаки также используются в регулярных выражениях и языках программирования. Регулярные выражения представляют собой систему сопоставления шаблонов, которая использует строки (то есть последовательности символов), построенные в соответствии с предопределенными правилами синтаксиса для поиска нужных строк в тексте.

Звездный символ

Три типа подстановочных знаков используются с командами Linux. Наиболее часто используемый и, как правило, самый полезный - это групповой символ звезды, который совпадает с звездочкой (*). Символ «звезда» имеет самый широкий смысл - любой из подстановочных знаков, поскольку он может представлять нулевые символы, все одиночные символы или любую строку. 

Например, команда файла предоставляет информацию о любом объекте файловой системы (т.е. файле, каталоге или ссылке), который предоставляется ему в качестве аргумента (т.е. ввода). Поскольку групповой символ звезды представляет каждую строку, его можно использовать в качестве аргумента для файла для возврата информации о каждом объекте в указанном каталоге. Таким образом, следующее будет отображать информацию о каждом объекте в текущем каталоге (то есть каталоге, в котором пользователь в настоящее время работает): ```file *```". [How to Use Wildcards](http://www.linfo.org/wildcard.html)

**b. ЛОЖЬ**. "Большинство операционных систем, поддерживающих иерархическую систему каталогов, имеют в каждом каталоге специальные элементы «.» и «..», которые обычно произносятся как «точка» и «точка-точка». Точка является ссылкой на текущий каталог, а двойная точка — на родительский каталог (за исключением корневого каталога, где этот элемент является ссылкой на сам корневой каталог). Чтобы увидеть, как они используются, обратимся к дереву каталогов системы UNIX (рис. 4.5). Пусть у нас есть некий процесс, для которого каталог /usr/ast является рабочим. Чтобы переместиться вверх по дереву, он может использовать обозначение «..». К примеру, он может копировать файл /usr/lib/dictionary в собственный каталог при помощи команды

```cp ../lib/dictionary .```

Первый указанный путь предписывает системе подняться вверх по дереву (к каталогу usr), затем опуститься вниз к каталогу lib и найти в нем файл dictionary". "Современные операционные системы", "Глава 4. Файловые системы. 4.2. Каталоги", Эндрю Таненбаум, 798 страница.

**c. ЛОЖЬ**. The LIKE operator is used in a WHERE clause to search for a specified pattern in a column. There are two wildcards used in conjunction with the LIKE operator:  ```%``` - The percent sign represents zero, one, or multiple characters; ```_``` - The underscore represents a single character". . [The SQL LIKE Operator](https://www.w3schools.com/sql/sql_like.asp).

**d. Истина**. "Другим групповым символом является вопросительный знак, который заменяет один любой символ. Кроме того, в квадратных скобках можно указать множество символов, из которых программа должна будет выбрать один. Например, команда 

```ls [ape]?```

выводит все файлы, имя которых начинается с символов «a», «p» или «e»". "Современные операционные системы", "Глава 10. Изучение конкретных примеров: Unix, Linux и Android", Эндрю Таненбаум, 798 страница. 

### Which command is used to see the online manual?

a. manual

b. man

c. help

d. readme


### What is the symbolic representation of this numeric permission: 644?

a. rwxr-xr-x

b. rw-r--r--

c. rw-------

d. r--rw-rw-

**a. Ложь**. Символьное представление ```rwx``` в самом начале маски содержит указание на реализацию для владельца управления доступа к файлам и каталогам в Unix по трем флагам: право на чтение (Read) из файла, право на запись (Write) в файл (в частности перезапись или изменение) и право на исполнение (eXecute) файла. ```rwx``` для файла и для папки означает полные права. Символьное представление ```rwx``` в восьмеричном представлении будет представлено значением 7.

Символьное представление ```r-x``` в середине и конце маски говорит о правах группового владельца и остальных пользователей в отношении файла на чтение и исполнение файла, а если речь идет о папке, то о правах на чтение имен файлов и доступ к файлам и их атрибутам. Символьное представление ```r-x``` в восьмеричном представлении будет представлено значением 5. Итого для символьного представления получаем восьмеричное представление `755`.

**b. Истина**. Символьное представление `rw-` в начале маски содержит указание на наличие у владельца файла или каталога прав на чтение и запись файла или прав только на чтение имен файлов. В восьмеричном представлении маска будет иметь значение 6.

Символьное представление ```r--``` в середине и конце маски содержит указание на наличие прав группового владельца и остальных пользователей на чтение файла или только на чтение имен файлов в каталоге. В восьмеричном представлении маска будет иметь значение 4. Итого для символьного представления получаем восьмеричное представление `644`.

**c. Ложь.** `rw-` в начале маски - право владельца файла на чтение и запись или владельца каталога только на чтение имен файлов. Или занчение 6 в восьмеричном представлении. `---` в середине и конце маски - отсутствие прав в отношении файла или каталога у группового владельца и всех остальных пользователей. Или значение 0 в восьмеричном представлении. Итого 600.

**d. Ложь**. `r--` в начале маски - право владельца файла на чтение или только на чтение имен файлов. И `4` в восьмизначной системе счисления. `rw-` в середине и в конце маски - право групповых владельцев и всех остальных на чтение файла и запись или для каталога только на чтение имен файлов. Значение `6` в восьмизначной системе. Итого 466. 

"В Unix каждому файлу соответствует набор прав доступа, представленный в виде 9-ти битов режима. Он определяет, какие пользователи имеют право читать файл, записывать в него данные или выполнять его...

Существует три пути управления доступом к файлу или каталогу. Было определено, что каждый файл должен иметь владельца (*owner*), группового владельца (*group owner*), а также может потребоваться доступ для всех остальных пользователей (*everyone*). Эти названия обычно приводятся как пользователь/группа/остальные (user/group/others) или коротко ugo. Реализация управления доступом к файлам и каталогам в Unix позволяет или запрещает доступ по трем флагам: флаг чтения (**Read**), флаг записи (**Write**), флаг выполнения (**eXecute**).

Посмотреть права доступа на объекты можно командой `ls` c ключем `-l` («л»). Также можно добавить ключ `-a`, для того,чтобы были отображены скрытые объекты.

Для назначения прав используются три группы флагов, первая определяет права для владельца, вторая - права для основной группы пользователей, третья - для всех остальных пользователей в системе.

Для файлов: **r** - право на чтение из файла; **w** - разрешает запись в файл (в частности перезапись или изменение); **x** - позволяет исполнить файл.

Для каталогов, флаги **r w x** имеют несколько отличный смысл: **r** - позволяет читать только имена файлов в каталоге; **x** - позволяет иметь доступ к самим файлам и их атрибутам (но не именам); **w** имеет смысл только в сочетании с **x**, и позволяет (в дополнение к **x**) манипулировать файлами в каталоге (создавать, удалять и переименовывать). **w** без **x** - не имеет никакого эффекта.". [Права доступа Unix, SUID, SGID, Sticky биты](http://help.ubuntu.ru/wiki/стандартные_права_unix)

### What are the contents of /bin directory?

Каково содержимое каталога / bin?

a. Third party applications

b. Device drive information

c. System commands

d. Common linux commands

**a. Ложь**. "Many modern [UNIX](https://en.wikipedia.org/wiki/UNIX) systems (like [FreeBSD](https://en.wikipedia.org/wiki/FreeBSD) via its [ports](https://en.wikipedia.org/wiki/FreeBSD_Ports) system) install third party packages into `/usr/local` while keeping code considered part of the operating system in `/usr`." [Filesystem Hierarchy Standard](https://en.wikipedia.org/wiki/Filesystem_Hierarchy_Standard), Wikipedia

Многие современные системы UNIX (например, FreeBSD через свою систему портов) устанавливают сторонние пакеты в / usr / local, сохраняя при этом код, считающийся частью операционной системы в / usr.

b. Ложь. "Essential [device files](https://en.wikipedia.org/wiki/Device_file), *e.g.*, `/dev/null`". [Filesystem Hierarchy Standard](https://en.wikipedia.org/wiki/Filesystem_Hierarchy_Standard), Wikipedia. В каталоге /dev находятся основные [файлы устройств](https://ru.wikipedia.org/wiki/%D0%A4%D0%B0%D0%B9%D0%BB_%D1%83%D1%81%D1%82%D1%80%D0%BE%D0%B9%D1%81%D1%82%D0%B2%D0%B0) (например, `/dev/null`, `/dev/zero`).

c. Неизвестно.

d. Истина. "Essential command [binaries](https://en.wikipedia.org/wiki/Executable) that need to be available in [single user mode](https://en.wikipedia.org/wiki/Single_user_mode); for all users, *e.g.*, cat, ls, cp". [Filesystem Hierarchy Standard](https://en.wikipedia.org/wiki/Filesystem_Hierarchy_Standard), Wikipedia.

Основные [утилиты](https://ru.wikipedia.org/wiki/%D0%A3%D1%82%D0%B8%D0%BB%D0%B8%D1%82%D0%B0), необходимые как в однопользовательском режиме, так и при обычной работе всем [пользователям](https://ru.wikipedia.org/wiki/%D0%9F%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D1%8C) (например: [cat](https://ru.wikipedia.org/wiki/Cat), [ls](https://ru.wikipedia.org/wiki/Ls), [cp](https://ru.wikipedia.org/wiki/Cp)).

Каталог /bin содержит основные утилиты, необходимые как в однопользовательском режиме, так и при обычной работе всем [пользователям](https://ru.wikipedia.org/wiki/%D0%9F%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D1%8C) (например: cat, chmod, ls, mkdir, pwd, rmdir).

"Чаще всего программы находятся в /bin или в /usr/bin", 732 страница.

Таблица 10.8. Некоторые важные каталоги, существующие в большинстве систем Linux:

| Каталог | Содержание                                   |
| ------- | -------------------------------------------- |
| bin     | Двоичные (исполняемые) программы             |
| dev     | Специальные файлы для устройств ввода-вывода |
| etc     | Разные системные файлы                       |
| lib     | Библиотеки                                   |
| usr     | Каталоги пользователей                       |

### What are the contents of /etc directory?

a. System configuration files

b. Security configuration

c. Internet services configuration

d. All applications setting

### What are the contents of /dev directory?

a) Device drive information

b) Home directories of developers

c) System configuration files

d) Home directories of all users.

### What are the contents of /home directory?

a) Home directories of all users

b) Home directories of the system

c) System log files

d) System configuration files

### Для чего нужен cron?

а) Это сервис для печати (принтер)

б) Для запуска задач по расписанию

в) Так называется скрипт, который выполняется при каждом запуске системы.

### What is the default administrator username?

a) administrator

b) admin

c) root

d) superuser

### Где хранятся пароли пользователей?

а) В системном реестре

б) В /bin/pwd

в) В /etc/shadow

г) В /bin/passwd

д) В /etc/passwd

### Что означает право на исполнение для директории?

а) Можно перейти в эту директорию

б) Можно исполнять любые файлы в директории

в) Можно получить доступ к атрибутам файлов в директории

г) Можно загружать в директорию исполняемые файлы

### Как создать пользователя?

а) С помощью утилиты adduser, заполнить небольшую анкету.

б) Только с помощью панели управления

в) С помощью утилиты useradd, указав новые ключи, после с помощью passwd задать пароль.

### Как напечатать на экран значение переменной `а`?

а) `echo "a"`

б) `a.echo()` 

в ) `echo a`

г) `echo $a`

05.07.2018. Перейти на [Главную страницу](./)