---
slug: test-desiderata
title: Test desiderata
authors: [petro_ostapuk]
tags: [test]
---

# Бажані тести

```
    Йди спокійно серед шуму і поспіху,
    і пам'ятай, який мир може бути в тиші
```
Нещодавно я опублікував цей твіт (Kent Beck):
```
    Тести повинні бути пов'язані з поведінкою коду і відокремлені від 
    структури коду. Побачивши тести, які не спрацьовують за обома пунктами.
```
Я думав, що ця властивість тестів очевидна і широко зрозуміла, але твіт вибухнув. Я бачив тести, які є просто жахливим синтаксисом, 
що повторює в точності те, що вже сказано у вихідному коді, який тестується. Я пішов і перечитав TDD: На прикладі, 
і цих властивостей ніде не було, тож, гадаю, не варто було дивуватися.

<!--truncate-->

Цей досвід змусив мене задуматися про інші властивості тестів, які я сприймаю як належне. Отже, ось список цих властивостей.
Не всі тести повинні мати всі властивості. Однак від жодної з них не варто відмовлятися, не отримавши натомість ту, 
що має більшу цінність.

**Властивості**:
* Ізольовані - тести повинні повертати однакові результати незалежно від порядку їх запуску.
* Компоновані - якщо тести ізольовані, то я можу запустити 1, 10, 100 або 1 000 000 тестів і отримати однакові результати. 
* Швидкий - тести повинні виконуватися швидко. 
* Натхненні - успішне проходження тестів має надихати на впевненість.
* Легко писати - тести повинні бути дешевими у написанні порівняно з вартістю коду, який тестується. 
* Читабельними - тести повинні бути зрозумілими для читача, викликаючи мотивацію для написання саме цього тесту. 
* Поведінкові - тести повинні бути чутливими до змін у поведінці коду, що тестується. Якщо поведінка змінюється, 
результат тесту повинен змінюватися. 
* Нечутливі до структури - тести не повинні змінювати свій результат при зміні структури коду. 
* Автоматизовані - тести повинні виконуватися без втручання людини. 
* Конкретними - якщо тест не проходить, причина невдачі повинна бути очевидною. 
* Детермінованими - якщо нічого не змінюється, результат тесту не повинен змінюватися. 
* Передбачуваність - якщо всі тести пройдені, то код, що тестується, повинен бути придатним для виробництва(релізу).

**Комбінації**

Ось деякі атрактори в просторі всіх можливих тестів:

1. [ ] **Програмістські** (вони ж "модульні" тести). Жертвують прогнозованістю та натхненням заради швидкості, писання та конкретності.
2. [ ] **Приймальні тести**: Роблять тести читабельними для непрофесіоналів, жертвуючи швидкістю та конкретністю.
3. [ ] **Моніторинг**: Жертвують прогнозованістю та автоматизацією (за винятком сповіщень).
Моніторинг відмовляється від передбачуваності та певною мірою автоматизованості (за модулем оповіщення).

**І що з того?**

Подивіться на останній тест, який ви написали. Які властивості він має? Яких йому бракує? Це той компроміс, на який ви хочете піти?

Оригінал:

https://medium.com/@kentbeck_7670/test-desiderata-94150638a4b3