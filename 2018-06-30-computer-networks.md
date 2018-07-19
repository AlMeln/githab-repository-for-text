# Компьютерные сети

Подборка упражнений, задач и решений с доказательствами.

## Содержание

1. [Что такое SSL?](#ssl)
1. [Что такое RSA?](#rsa) 
1. [Что есть сокет?](#socket)
1. [Что такое топология сети?](#topology)
1. [Что такое сетевой протокол?](#protocol)
1. Что такое IP-адрес? а) Символическое имя, входящее в состав адреса сайта. Например mail.ru б) Четыре числа, разделенные точкой, используемые для адресации хоста, если речь не идет об IPv6. Например 77.77.88.88 в) Уникальный адрес компьютера, состоящий из 6 байт. Например 52:50:00:01:02:03.

### Что такое SSL? <a name="ssl"></a>
а) Криптографический протокол, "уровень защищенных сокетов"
б) Шифрованный http
в) Протокол для безопасного администрирования, Secure ShelL
г) Механизм архивирования, для чего существует HTTP-заголовок Content-Encoding: ssl, альтернатива gzip-у

**а) Истина**. The Secure Sockets Layer (SSL) - уровень защищенных сокетов. Криптографический протокол. RFC6101 "The Secure Sockets Layer (SSL) Protocol Version 3.0", August 2011.

**б) Ложь**. Шифрованный http - это HTTPS. HyperText Transfer Protocol Secure - расширение протокола HTTP для поддержки шифрования в целях повышения безопасности. HTTPS связан с SSL, поскольку данные в HTTPS передаются поверх криптографических протоколов SSL или TLS.

**в) Ложь**. Secure ShelL или "безопасная оболочка" - это SSH. SSH является сетевым протоколом прикладного уровня и позволяет производить удаленное управление операционной системой и туннелирование TCP-соединений (например, для передачи файлов). 

**г) Ложь**. Поле заголовка ответа Content-Encoding указывает на дополнительный способ кодирования тела HTTP объета с целью сжатия при передаче. Например, заголовок Content-Encoding: gzip обычно устанавливается, когда возвращаемое содержимое сжимается.

### Что такое RSA? <a name="rsa"></a>
а) Протокол прикладного уровня, используемый в IP-телефонии
б) Асимметричный алгоритм, названный по имени авторов
в) Resourseless Secure Authentication - механизм авторизации по паролю, используемый в HTTP

**а) Ложь**. Протоколами используемыми в IP-телефонии являются: Session Initiation Protocol — протокол установления сеанса; MGCP или Media Gateway Control Protocol дословно — Протокол контроля медиашлюзов. Протоколы прикладного уровня - протоколы верхнего (7-го) уровня сетевой модели OSI, обеспечивают взаимодействие сети и пользователя. Уровень разрешает приложениям пользователя иметь доступ к сетевым службам, таким, как обработчик запросов к базам данных, доступ к файлам, пересылке электронной почты. Также отвечает за передачу служебной информации, предоставляет приложениям информацию об ошибках и формирует запросы к уровню представления. Пример: HTTP (англ. HyperText Transfer Protocol — «протокол передачи гипертекста»), POP3 (англ. Post Office Protocol Version 3 — протокол почтового отделения, версия 3), SMTP (англ. Simple Mail Transfer Protocol — простой протокол передачи почты).

**б) Истина**. Аббревиатура от фамилий Rivest, Shamir и Adleman - американский специалист по криптографии Рональд Линн Ривет, израильский криптоаналитик Ади Шамир и американский ученый-теоретик в области компьютерных наук Леонард Макс Адлеман. Криптографический алгоритм с открытым ключом. Криптосистема RSA стала первой системой, пригодной и для шифрования, и для цифровой подписи.

**в) Ложь**. В сети не обнаружил информацию о существовании "Resourseless Secure Authentication". Видимо это выдумка Geekbrains.ru. Существуют механизмы авторизации в Интернете: базовая утентификация, дайджест-аутентификация, HTTPS, аутентификация по предъявлению цифрового сертификата, аутентификация по Cookies, децентрализованная аутентификация по OpenID, децентрализованная аутентификация по OpenAuth, децентрализованная аутентификация по OAuth, многофакторная аутентификация. Механизмом авторизации по паролю, используемом в HTTP может быть базовая аутентификация. Парольная система аутентификации является видkv однофакторной аутентификации. При использовании базовой аутентификации имя пользователя и пароль включаются в состав веб-запроса (HTTP POST и HTTP GET). Любой перехвативший пакет, легко узнает секретную информацию. Дайджест-аутентификация предполагает передачу пароль пользователя в хешированном виде. Пароль хешируется всегда с добавлением произвольной строки символов, которая генерируется на каждое соединение заново. Таким образом при каждом соединеиии генерируется новый хэш пароля и перехват его ничего не даст. Дайджест-аутентификация поддерживается всеми популярными серверами и браузерами. (Википедия "Аутентификация в Интернете".) 

### Что есть сокет? <a name="socket"></a>
а) Механизм, предоставляемый ядром операционной система возможностям стека TCP/IP. Прикладные программы для доступа к канальному, сетевому и транспортному уровню стека используют сокеты.

б) Разъем на сетевой карте, куда подключается патч-корд.

в) Зашифрованное соединение.

**а) Истина**. "Чтобы поощрить принятие новых протоколов, ARPA заключила несколько контрактов для внедрения TCP/IP на различных компьютерных платформах, в том числе на системах IBM, DEC и HP, а также UNIX Беркли. Исследователи в Калифорнийском университете Беркли переписали TCP/IP с новым программным интерфейсом, накзванным сокетом, для следующими 4.2 BSD выпуска UNIX Беркли. Они также написали много приложений, утилит и программ управления, чтобы показать, как удобно использовать сеть с сокетами". "Компьютерные сети", "Глава 1. Введение" Эндрю Таненбаум, 74 страница.

"Теперь рассмотрим другой набор базовых операций транспортного уровня - базовые операции сокетов (иногда назвываемых гнездами), используемые для протоколов TCP (Transmission Control Protocol - протокол управления передачей). Впервые сокеты стали применяться в 1983 году... Они скоро они стали популярными и сейчас широко используются для интернет-программирования в большинстве операционные систем, особенно UNIX; кроме того, существует специальные API, предназначенный для программирования сокетов в системе Windows - "winsock". "Компьютерные сети", "Глава 6. Транспортный уровень. 6.1.3. Сокеты Беркли" Эндрю Таненбаум, 533 страница.

"В основе сервиса TCP лежат так называемые сокеты (гнезда или конечные точки), создаваемые как отправителем, так и получателем. Они обсуждались в разделе 6.1.3. У каждого сокета есть номер (адрес), состоящий из IP-адреса хоста и 16-битного номера, локального по отношению к хосту, называемого портом. Портом в TCP называют TSAP-адрес. Для обращения к сервису TCP между сокетом одной машины и сокетом другой машины должно быть явно установлено соединение. Базовые операции сокетов приведены в табл. 6.2.

| Уровни (и протоколы), используемые обычным домашним браузером с SSL |
| - |
| Прикладной (HTTP) |
| Защиты (SSL) |
| Транспортный (TCP) |
| Сетевой (IP) |
| Канальный (PPP, англ. Point-to-Point Protocol)|
| Физический (модемное соединение, ADSL, кабельное ТВ) |

Один сокет может использоваться одновременно для нескольких соединений. Дру- гими словами, два и более соединения могут оканчиваться одним сокетом. Соединения различаются по идентификаторам сокетов на обоих концах — (socket1, socket2). Номера виртуальных каналов или другие идентификаторы не используются". "Компьютерные сети", "Глава 6. Транспортный уровень. 6.5.2. Модель сервиса TCP" Эндрю Таненбаум, 587-588 страница.

"Транспортный уровень — это ключ к пониманию многоуровневых протоколов. Он предоставляет различные сервисы, наиболее важным из которых является сквозной, надежный, ориентированный на соединение поток байтов от отправителя к получателю. Доступ к нему предоставляется при помощи сервисных примитивов, позволяющих устанавливать, использовать и разрывать соединения. Общепринятый интерфейс транспортного уровня обеспечивается сокетами Беркли". "Компьютерные сети", "Глава 6. Транспортный уровень. 6.8. Резюме" Эндрю Таненбаум, 642 страница.

**б) Ложь**. "Коммутационный шнур, коммутационный кабель, жарг. патч-корд (от англ. patching cord — соединительный шнур) — одна из составных частей структурированной кабельной системы. Представляет собой электрический или оптоволоконный кабель для подключения одного электрического устройства к другому или к пассивному оборудованию передачи сигнала. Может быть любых типов, но не размеров, по стандарту ANSI EIA TIA 568B.1 не должен превышать 5 м длины, за исключением расширения TSB-75 для открытых офисов (согласно TSB-75 допускается большей длины). На обоих концах кабеля обязательно присутствуют соответствующие соединяемым устройствам коннекторы...

На 10-мегабитных сетевых платах для подключения к локальной сети используются 4 типа разъёмов: 8P8C для витой пары; BNC-коннектор для тонкого коаксиального кабеля; 15-контактный разъём AUI трансивера для толстого коаксиального кабель; оптический разъём (en:10BASE-FL и другие стандарты 10 Мбит Ethernet).

Соединитель/разъём/коннектор BNC (BNC — аббревиатура от англ. bayonet Neill-Concelman) — электрический разъём с байонетной фиксацией. Назван в честь разработчиков: Пола Нейла (англ. Paul Neill) из лаборатории «Bell Labs» и Карла Концельмана (англ. Carl Concelman) из фирмы «Amphenol». Служит для подключения коаксиального кабеля c волновым сопротивлением 50 Ом или 75 Ом и диаметром до 8 мм. Потери в таком разъёме обычно не превышают 0.3 дБ.

8P8C (8 Position 8 Contact), иногда ошибочно называемый RJ45 — унифицированный разъём, используемый в телекоммуникации.

AUI (англ. attachment unit interface - интерфейс модуля присоединения) — физический и логический интерфейс, определенном в оригинальном стандарте IEEE 802.3 проводной сети 10BASE5 Ethernet[1]. Опциональный физический интерфейс представляет собой 15-контактный разъём для подключения физического сигнального подуровня (PLS) сетевого адаптера компьютера к приёмопередатчику (MAU - Medium Attachment Unit, иногда также - "трансивер")[2]. AUI-кабель может иметь длину до 50 метров, однако во многих случаях он не использовался и модули MAU и MAC имели непосредственное подключение.

На 100-мегабитных платах устанавливают либо разъём для витой пары (8P8C, ошибочно называемый RJ-45), либо оптический разъем (SC, ST, MIC).

Registered Jack (RJ, читается «ар-джей») — стандартизированный физический сетевой интерфейс, включающий описание конструкции обеих частей разъёма («вилки» и «розетки») и схемы их коммутации. Используется для соединения телекоммуникационного оборудования. К таким стандартам относятся RJ11, RJ14, RJ25, RJ45S и другие. Зачастую названия стандартов ошибочно используются для обозначения разъёмов". Wikipedia.

**в) Ложь**. "Когда веб-технологии были впервые представлены широкой публике, они использовались для распространения статических страниц. Однако еще давным-давно некоторые компании задумались об использовании Всемирной паутины для выполнения финансовых транзакций, таких как покупка товаров по кредитным картам, онлайновые банковские операции, электронная торговля ценными бумагами. Для таких приложений требовалась организация защищенных соединений. В 1995 году тогдашний лидер среди производителей браузеров, корпорация Netscape Communications, в ответ на это представила систему безопасности под названием SSL (Secure Sockets Layer — протокол защищенных сокетов). Соответствующее программное обеспечение, как и сам протокол, в наше время используется очень широко (в том числе программами Firefox, Safari, Internet Explorer), поэтому стоит рассмотреть SSL более детально.

Итак, SSL создает защищенное соединение между двумя сокетами, позволяющее:
1) клиенту и серверу договориться об используемых параметрах;
2) провести аутентификацию сервера клиентом;
3) организовать тайное общение;
4) обеспечить защиту целостности данных.

Расположение SSL в структуре обычного стека протоколов показано на рис. 8.44. По сути дела, между прикладным и транспортным уровнями появляется новый уровень, принимающий запросы от браузера и отсылающий их по TCP для передачи серверу. После установки защищенного соединения основная задача SSL заключается в поддержке сжатия и шифрования. Если поверх SSL используется HTTP, этот вариант называется HTTPS (Secure HTTP — защищенный HTTP), несмотря на то что это обычный протокол HTTP. Впрочем, возможно и отличие: скажем, доступ может осуществляться через новый порт (443) вместо стандартного (80). Кстати говоря, область применения SSL не ограничивается исключительно веб-браузерами, но это наиболее распространенное применение. Он также может обеспечивать взаимную аутентификацию".

"Компьютерные сети", "Глава 6. Транспортный уровень. 8.9.3. SSL — протокол защищенных сокетов" Эндрю Таненбаум, 902 страница.

### Что такое топология сети? <a name="topology"></a>

а) Способ соединения узлов сети, изображаемый в виде графа, вершинами которого будут узлы сети и телекоммуникаицонное оборудование, а ребрами - связи между вершинами.

б) Таблица, которая задает порядок передачи пакетов на следующие узлы (можно посмотреть с помощью команд route или netstat -r в зависимости от системы)

в) Порядок следования через маршрутизаторы в выводе команды tracert или traceroute - в зависимости от системы.

г) Таблица, которая задает правила обработки входящих, исходящих и транзитных пакетов через узел.

**а) Истина**. "Сетевая топология - это конфигурация графа, вершинам которого соответствуют конечные узлы сети (компьютеры) и коммуникационное оборудование (маршрутизаторы), а ребрам - физический или информационные связи между вершинами". Wikipedia

**б) Ложь**. "Правила маршрутизации определяют, куда отправлять IP-пакеты. Данные маршрутизации хранятся в одной из таблиц ядра. Вести таблицы маршрутизации можно статически или динамически. Статический маршрут — это маршрут, который задается явно с помощью команды route. Динамическая маршрутизация выполняется процессом-демоном (routed или gated), который ведет и модифицирует таблицу маршрутизации на основе сообщений от других компьютеров сети. Для выполнения динамической маршрутизации разработаны специальные протоколы: RIP, OSPF, IGRP, EGP, BGP и т. д.

Динамическая маршрутизация необходима в том случае, если у вас сложная, постоянно меняющаяся структура сети и одна и та же машина может быть доступна по различным интерфейсам (например, через разные Ethernet или SLIP интерфейсы). Маршруты, заданные статически, обычно не меняются, даже если используется динамическая маршрутизация.

Для персонального компьютера, подключаемого к локальной сети, в большинстве ситуаций бывает достаточно статической маршрутизации командой route. Прежде чем пытаться настраивать маршруты, просмотрите таблицу маршрутизации ядра с помощью команды netstat -n -r". Форум русскоязычного сообщества Ubuntu, RigoN http://forum.ubuntu.ru/index.php?topic=12454.0

**в) Ложь**. "Traceroute — это служебная компьютерная программа, предназначенная для определения маршрутов следования данных в сетях TCP/IP. Traceroute может использовать разные протоколы передачи данных в зависимости от операционной системы устройства. Такими протоколами могут быть UDP, TCP, ICMP или GRE. Компьютеры с установленной операционной системой Windows используют ICMP-протокол, при этом операционные системы Linux и маршрутизаторы Cisco — протокол UDP". Wikipedia

"Хитрый способ использования этого сообщения, предложенный Ван Джейкобсоном в 1987 году, — утилита traceroute. Она находит маршрутизаторы, расположенные в узлах пути от хоста к адресу назначения. При этом ей не требуется особый уровень поддержки. Метод состоит в отправке на адрес назначения последовательности пакетов с временем жизни 1, 2, 3 и т. д. Маршрутизаторы, на которых счетчики достигают нуля, располагаются в том порядке, в котором пакет проходит их при пересылке. Эти маршрутизаторы послушно отправляют обратно на хост сообщения ВРЕМЯ ИСТЕКЛО. По этим сообщениям хост определяет их IP-адреса и получает информацию о пути. Сообщение ВРЕМЯ ИСТЕКЛО, конечно, предназначалось не для этого. Но вполне возможно, что это самый полезный инструмент отладки сети всех времен". "Компьютерные сети", "Глава 5. Сетевой уровень. 5.6.4. Управляющие протоколы Интернета
" Эндрю Таненбаум, 499 страница.

**г) Ложь**. "Сервису с установлением соединения нужна сеть виртуального канала. Рассмотрим ее работу. Идея виртуальных каналов состоит в предотвращении выбора своего маршрута для каждого пакета, как было показано на рис. 5.2. Вместо этого маршрут от отправляющей до получающей машины выбирается в процессе установления соединения и хранится в специальных таблицах, встроенных в маршрутизаторы. Один и тот же маршрут используется для всего трафика, проходящего через данное соединение. Именно так работает телефонная система. Когда соединение разрывается, виртуальный канал также прекращает свое существование. При использовании сервиса, ориентированного на установление соединения, каждый пакет включает в себя идентификатор виртуального канала". использовать сеть с сокетами". "Компьютерные сети", "Глава 5. Сетевой уровень. 5.1.4. Реализация сервиса с установлением соединения" Эндрю Таненбаум, 389 страница.

"Алгоритм маршрутизации по вектору расстояний иногда называют по именам его создателей распределенным алгоритмом Беллмана—Форда (Bellman—Ford) (Bellman, 1957; Ford и Filkerson, 1962). Этот алгоритм изначально применялся в сети ARPANET и в Интернете был известен под названием RIP.

При маршрутизации по вектору расстояний таблицы, с которыми работают и которые обновляют маршрутизаторы, содержат записи о каждом маршрутизаторе сети. Каждая запись состоит из двух частей: предпочитаемый номер линии для данного получателя и предполагаемое расстояние или время прохождения пакета до этого получателя. В качестве меры расстояния можно использовать число транзитных участков или другие единицы измерения (о которых мы говорили при обсуждении длины кратчайшего пути)". "Компьютерные сети", "Глава 5. Сетевой уровень. 5.2.4. Маршрутизация по вектору расстояний" Эндрю Таненбаум, 400 страница.

"При использовании иерархической маршрутизации маршрутизаторы разбиваются на отдельные так называемые регионы (regions). Каждый маршрутизатор знает все детали выбора маршрутов в пределах своей области, но ему ничего не известно о внутреннем строении других регионов. При объединении нескольких сетей естественно рассматривать их как отдельные регионы, при этом маршрутизаторы одной сети освобождаются от необходимости знать топологию других сетей.

В очень больших сетях двухуровневой иерархии может оказаться недостаточно. Может потребоваться группировать регионы в кластеры, кластеры в зоны, зоны в группы и т. д., пока у нас не иссякнет фантазия на названия для новых образований. В качестве примера многоуровневой иерархии рассмотрим маршрутизацию пакета, пересылаемого из университета Беркли (Berkeley), штат Калифорния в Малинди (Malindi) в Кении. Маршрутизатор в Беркли знает детали топологии в пределах Калифорнии, но трафик, направляющийся за пределы штата, он посылает маршрутизатору в Лос-Анджелесе. Маршрутизатор в Лос-Анджелесе может выбрать прямой маршрут для трафика в пределах США, но все пакеты, направляемые за рубеж, переправляет в Нью-Йорк. Нью-йоркский маршрутизатор направит трафик на маршрутизатор страны назначения, ответственный за прием трафика из-за границы. Он может располагаться, например, в Найроби. Наконец, направляясь вниз по дереву иерархии уже в пределах Кении, пакет попадет в Малинди". "Компьютерные сети", "Глава 5. Сетевой уровень. 5.2.6. Иерархическая маршрутизация" Эндрю Таненбаум, 400 страница.

### Что такое сетевой протокол? <a name="protocol"></a>

а) набор правил, определяющих поведение компонентов сети при передаче данных и структуру передаваемых данных.

б) системный реестр сетевого программного обеспечения, хранящий настройки.

в) журнал в котором протоколирующая факты отправки, приема, перепрела и отказа в приеме данных.

**а) Истина**. "Уровень n одной машины поддерживает связь с уровнем n другой машины. Правила и соглашения, используемые в данном общении, называются протоколом уровня n. По сути, протокол является договоренностью общающихся сторон о том, как должно происходить общение. По аналогии, когда женщину представляют мужчине, она может протянуть ему свою руку. Он, в свою очередь, может принять решение либо пожать, либо поцеловать эту руку, в зависимости от того, является ли эта женщина американским адвокатом на деловой встрече или же европейской принцессой на официальном балу. Нарушение протокола создаст затруднения в общении, а может и вовсе сделает общение невозможным". "Компьютерные сети", "Глава 1. Введение. 1.3. Сетевое программное обеспечение. 1.3.1. Иерархия протоколов" Эндрю Таненбаум, 45 страница.

"Службы и протоколы являются различными понятиями. Различие между ними столь важно, что мы хотели бы еще раз обратить на него ваше внимание. Служба (или сервис) — это набор примитивов (операций), которые более низкий уровень предо- ставляет более высокому. Служба определяет, какие именно операции уровень будет выполнять от лица своих пользователей, но никак не оговаривает, как должны реализовываться эти операции. Служба описывает интерфейс между двумя уровнями, в котором нижний уровень является поставщиком сервиса, а верхний — его потребителем.

Напротив, протокол — это набор правил, описывающих формат и назначение кадров, пакетов или сообщений, которыми обмениваются объекты одного ранга внутри уровня. Объекты используют протокол для реализации определений своих служб. Они могут менять протокол по желанию, при условии, что при этом остаются неизменными службы, предоставляемые ими своим пользователям. Таким образом, служба и протокол оказываются практически независимыми. Это — ключевое понятие, которое должен хорошо понять любой проектировщик сетей". "Компьютерные сети", "Глава 1. Введение. 1.3.5. Службы и протоколы" Эндрю Таненбаум, 56 страница.

**б) Ложь**. "Корень пространства имен NT поддерживается в ядре. Система хранения (тома фай- ловой системы) связана с пространством имен NT. Поскольку пространство имен NT собирается при каждой загрузке системы, как система узнает об особенностях кон- фигурации? Ответ состоит в том, что Windows подключает к пространству имен NT файловую систему особого типа (оптимизированную для небольших файлов). Эта фай- ловая система называется реестром (registry). Реестр организован в отдельные тома, называемые разделами (hives). Каждый раздел хранится в отдельном файле (в каталоге C:\Windows\system32\config\ загрузочного тома)1. Когда Windows загружается, раздел SYSTEM грузится в память той же самой программой загрузки, которая загружает ядро и прочие файлы загрузки (такие, как загрузочные драйверы) с загрузочного тома". "Современные операционные системы", "Глава 11. Изучение конкретных примеров: Windows 8. 11.2.3. Реестр Windows" Эндрю Таненбаум, 950 страница.

"Реестр — это странная помесь файловой системы и базы данных (причем он отличается и от той и от другой). Для описания реестра написаны целые книги (Born, 1998; Hipson, 2002; Ivens, 1998), возникло даже множество компаний, которые продают специальное программное обеспечение для того, чтобы справиться со сложностью реестра". "Современные операционные системы", "Глава 11. Изучение конкретных примеров: Windows 8. 11.2.3. Реестр Windows" Эндрю Таненбаум, 951 страница.

**в) Ложь**. "Для того чтобы разрешить непонимание относительно того, какая станция будет отправлять данные, в стандарте 802.11 прослушивание канала определяется на фи- зическом и виртуальном уровнях. При физическом прослушивании среда просто проверяется на наличие сигнала. Виртуальное прослушивание заключается в том, что каждая станция ведет логический журнал использования канала, отслеживая NAV (Network Allocation Vector, вектор распределения сети). Каждый кадр содержит поле NAV, которое сообщает, как долго последовательность, включающая данный кадр, будет передаваться". "Компьютерные сети", "Глава 4. Подуровень управления доступом к среде. 4.4. Беспроводные локальные сети. 4.4.3. Стандарт 802.11: протокол подуровня управления доступом к среде" Эндрю Таненбаум, 331 страница.

"Современные веб-серверы выполняют гораздо больше функций, чем просто прием имен путей и отправка файлов. На самом деле, реальная обработка каждого запроса может оказаться достаточно сложной. По этой причине на многих серверах каждый обрабатывающий модуль выполняет последовательности действий. Входной модуль передает каждый входящий запрос первому доступному модулю, который обрабатыва- ет его путем выполнения некоторого подмножества указанных ниже шагов, в зависи- мости от того, что именно требуется для данного запроса. Эти шаги появляются после того, как было создано TCP-соединение и какой-либо защищенный транспортный механизм (как SSL/TLS, который будет описан в главе 8). 1. Вычисление имени запрашиваемой веб-страницы... 7. Добавление записи в журнал активности сервера... Шаг 7 создает для административных целей запись в системном журнале и сохра- няет другую важную статистику. Такие журналы могут быть исследованы на наличие полезной информации о поведении пользователей, например о том, в каком порядке люди посещают страницы на сайте". "Компьютерные сети", "Глава 7. Прикладной уровень. 7.3. Всемирная паутина. Сторона сервера" Эндрю Таненбаум, 696-697 страница.

### Номер порта

а) меняется при каждом прохождении маршрутизатора.

б) не меняется при прохождении маршрутизатора, но может быть изменен при прохождении NAT-шлюза.

в) никогда не меняется.

"Метод трансляции сетевого адреса, NAT (Network Address Translation), описанный в RFC 3022. Суть его мы рассмотрим ниже, а более подробную информацию можно найти в (Dutcher, 2001)".

"Основная идея трансляции сетевого адреса состоит в присвоении каждой фирме или семье одного IP-адреса (или, по крайней мере, небольшого числа адресов) для интернет-трафика. Внутри абонентской сети каждый компьютер получает уникальный IP-адрес, используемый для маршрутизации внутреннего трафика. Однако, как только пакет покидает пределы абонентской сети и направляется к провайдеру, выполняется трансляция адреса, при которой уникальный внутренний IP-адрес становится общим публичным IP-адресом. Для реализации этой схемы было создано три диапазона так называемых частных IP-адресов. Они могут использоваться внутри сети по ее усмо- трению. Единственное ограничение заключается в том, что пакеты с такими адресами ни в коем случае не должны появляться в самом Интернете".

"Мы до сих пор обходили одну маленькую деталь: когда приходит ответ на запрос (например, от веб-сервера), он ведь адресуется 198.60.42.12. Как же NAT-блок узнает, каким внутренним адресом заменить общий адрес компании? Вот в этом и состоит главная проблема использования трансляции сетевых адресов. Если бы в заголовке IP-пакета было свободное поле, его можно было бы использовать для запоминания адреса того, кто посылал запрос. Но в заголовке остается неиспользованным всего один бит. В принципе, можно было бы создать такое поле для истинного адреса источника, но это потребовало бы изменения IP-кода на всех машинах по всему Интернету. Это не лучший выход, особенно если мы хотим найти быстрое решение проблемы нехватки IP-адресов".

"На самом деле, происходит вот что. Разработчики NAT подметили, что большая часть полезной нагрузки IP-пакетов — это либо TCP, либо UDP. Когда мы будем в главе 6 рассматривать TCP и UDP, мы увидим, что оба формата имеют заголовки, содержащие номера портов источника и приемника. Ниже мы обсудим, что значит порт TCP, но надо иметь в виду, что с портами UDP связана точно такая же история. Номера портов представляют собой 16-разрядные целые числа, показывающие, где начинается и где заканчивается TCP-соединение. Место хранения номеров портов используется в качестве поля, необходимого для работы NAT".

"Когда процесс желает установить TCP-соединение с удаленным процессом, он связывается со свободным TCP-портом на собственном компьютере. Этот порт ста- новится портом источника (source port), который сообщает TCP-коду информацию о том, куда направлять пакеты данного соединения. Процесс также определяет порт назначения (destination port). Посредством порта назначения сообщается, кому отдать пакет на удаленной стороне. Порты с 0 по 1023 зарезервированы для хорошо извест- ных сервисов. Например, 80-й порт используется веб-серверами, соответственно, на них могут ориентироваться удаленные клиенты. Каждое исходящее сообщение TCP содержит информацию о порте источника и порте назначения. Вместе они служат для идентификации процессов на обоих концах, использующих соединение".

"Проведем аналогию, которая несколько прояснит принцип использования портов. Допустим, у компании есть один общий телефонный номер. Когда люди набирают его, они слышат голос оператора, который спрашивает, с кем именно они хотели бы со- единиться, и подключают их к соответствующему добавочному телефонному номеру. Основной телефонный номер является аналогией IP-адреса абонента, а добавочные на обоих концах аналогичны портам. Для адресации портов используется 16-битное поле, которое идентифицирует процесс, получающий входящий пакет".

"С помощью поля *Порт источника* мы можем решить проблему отображения адресов. Когда исходящий пакет приходит в NAT-блок, адрес источника вида 10.x.y.z заменяется настоящим IP-адресом. Кроме того, поле *Порт источника* TCP заменяется индексом таблицы перевода NAT-блока, содержащей 65 536 записей. Каждая запись содержит исходный IP-адрес и номер исходного порта. Наконец, пересчитываются и вставляются в пакет контрольные суммы заголовков TCP и IP. Необходимо заменять поле *Порт источника*, потому что машины с местными адресами 10.0.0.1 и 10.0.0.2 могут случайно пожелать воспользоваться одним и тем же портом (5000-м, например). Так что для однозначной идентификации процесса отправителя одного поля *Порт источника* оказывается недостаточно".

"Когда пакет прибывает на NAT-блок со стороны провайдера, извлекается значение поля Порт источника заголовка TCP. Оно используется в качестве индекса таблицы отображения NAT-блока. По найденной в этой таблице записи определяются внутренний IP-адрес и настоящий Порт источника TCP. Эти два значения вставляются в пакет. Затем заново подсчитываются контрольные суммы TCP и IP. Пакет передается на главный маршрутизатор абонента для нормальной доставки с адресом вида 10.x.y.z".

30.06.2018. Перейти на [Главную страницу](./)