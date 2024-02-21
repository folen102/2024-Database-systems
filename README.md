# 2024-Database-systems
Homework and materials for the Database Systems course

## Нулевое задание

### Вопрос
Согласно теореме CAP к какой части вы можете отнести СУБД: **DragonFly ScyllaDB ArenadataDB**

### Ответ
Теорема **CAP** (известная также как теорема Брюера) — эвристическое утверждение о том, что в любой реализации распределённых вычислений возможно обеспечить не более двух из трёх следующих свойств:

* согласованность данных (англ. consistency) — во всех вычислительных узлах в один момент времени данные не противоречат друг другу;
* доступность (англ. availability) — любой запрос к распределённой системе завершается откликом, однако без гарантии, что ответы всех узлов системы совпадают;
* устойчивость к разделению (англ. partition tolerance) — расщепление распределённой системы на несколько изолированных секций не приводит к некорректности отклика от каждой из секций. 

[Википедия](https://ru.wikipedia.org/wiki/%D0%A2%D0%B5%D0%BE%D1%80%D0%B5%D0%BC%D0%B0_CAP)

### 1. [DragonFly](https://www.dragonflydb.io/)

На [официальном сайте](https://www.dragonflydb.io/redis-alternative) написано, что DragonFly позиционируется как более масштабируемая и производительная версия Redis, а Redis в свою очередь позиционируется как **CP** (Consistency and
Partition tolerance).

Ответ: CP

### 2. [ScyllaDB](https://www.scylladb.com/)
Scylla или ScyllaDB — распределённая отказоустойчивая колоночная СУБД с открытым исходным кодом.

Scylla была создана по образу и подобию Apache Cassandra с целью достижения более высоких показателей пропускной способности и снижения задержек. Как и Cassandra, Scylla поддерживает язык запросов CQL и формат файлов SSTable. Но это полностью переписанная реализация: Cassandra написана на Java, а ScyllaDB — на C++. [Источник](https://web-creator.ru/technologies/scylladb)

[Из документации](https://opensource.docs.scylladb.com/stable/architecture/architecture-fault-tolerance.html):
>ScyllaDB chooses availability and partition tolerance over consistency, such that:
> * It’s impossible to be both consistent and highly available during a network partition;
> * If we sacrifice consistency, we can be highly available.

Ответ: AP

### 3. [ArenadataDB](https://arenadata.tech/products/arenadata-db/)

Arenadata DB (ADB) – **Российская** распределенная СУБД, использующая концепцию MPP (massively parallel processing, массивно-параллельные вычисления) и основанная на СУБД с открытым исходным кодом – Greenplum.

Про консистентность (consistency) можно найти прямо на [сайте](https://arenadata.tech/products/arenadata-db/). А про Availability можно узнать из [документации](https://docs.arenadata.io/adb) и из того что она основана на Greenplum, а она уже позиционируется как **CA** (Consistency and Availability) [(см. картинку на сайте)](https://bigdataschool.ru/wiki/cap)

Ответ: CA