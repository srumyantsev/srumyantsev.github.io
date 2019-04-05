# Principles

* [Favor query objects over repositories](https://lostechies.com/jimmybogard/2012/10/08/favor-query-objects-over-repositories/)
* [Is the Repository pattern useful with Entity Framework? – part 2](https://www.thereformedprogrammer.net/is-the-repository-pattern-useful-with-entity-framework-part-2/)

Репозитории + EntityFramework скорее всего избыточны.

Скорее всего не надо делить репозитории на основании таблиц (один репозиторий, одна таблица). Надо сделать один общий репозиторий (типа как DbContext). На самом деле репозиториев может быть несколько (по одному на подсистему, баундед контекст или т.п.).
Репозиторий должен уметь обрабатывать QueryObject которые содержат логику запроса. Эта архитектура аналогична уникальным методам в репозиториях, но позволяет упростить кол-во методов в репозиториии до одного - который принимает запросы в виде QO. Таким образом можно скрыть репозиторий  забизнес сервисами или вообще от него избавиться и делегировать данный функционал сервисам.
