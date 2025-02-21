Чести типови проблема
=====================


**Дебаговање** је процес откривања и исправљања грешака у коду. Пајтон, као и сваки други програмски језик, има типичне проблеме са којима се програмери сусрећу током писања кода. 
Ова лекција ће покрити честе типове грешака и технике за њихово исправљање.


----------------------------------------------------------------------

**Чести типови грешака у Пајтону:**


1. **Синтаксне грешке (SyntaxError)**
2. **Грешке током извршавања (RuntimeError)**
3. **Грешке типа (TypeError)**
4. **Индексне грешке (IndexError)**
5. **Именске грешке (NameError)**
6. **Грешке вредности (ValueError)**
7. **Кључне грешке (KeyError)**
8. **Атрибутске грешке (AttributeError)**
9. **Логичке грешке**




**1. Синтаксне грешке (SyntaxError)**

**Синтаксна грешка** настаје када кôд не прати правила Пајтона. Интерпретер не разуме инструкцију јер је нешто неправилно написано.

**Пример:**

.. activecode:: debagovanje1
   :coach:
   
   print("Hello World)


Овде недостаје затварач наводника.

**Како исправити:**

- Исправите синтаксу према правилима Пајтона.
  
**Исправка:**

.. activecode:: debagovanje2
   :coach:

   print("Hello World")


**2. Грешке током извршавања (RuntimeError)**

**Грешке током извршавања** се јављају током извршавања програма и често настају услед ситуација као што су дељење са нулом или непостојећи фајл.

**Пример:**


.. activecode:: debagovanje3
   :coach:

   broj = 10 / 0


Овде ће доћи до `ZeroDivisionError` јер није могуће делити број са нулом.

**Како исправити:**

- Уверите се да број са којим делите није 0.
  
**Исправка:**


.. activecode:: debagovanje4
   :coach:

   broj = 10 / 2  # или користите провере пре дељења са нулом



**3. Грешке типа (TypeError)**

**TypeError** се јавља када операција укључује неподударне типове података.

**Пример:**

.. activecode:: debagovanje5
   :coach:

   broj = 5 + "5"


Пајтон не може да сабере цео број (`int`) и стринг (`str`).

**Како исправити:**

- Конвертуј стринг у цео број или обрнуто.

**Исправка:**

.. activecode:: debagovanje6
   :coach:

   broj = 5 + int("5")

**4. Индексне грешке (IndexError)**

**IndexError** настаје када покушате да приступите елементу из листе или низа помоћу индекса који не постоји.

**Пример:**

.. activecode:: debagovanje7
   :coach:

   lista = [1, 2, 3]
   print(lista[5])


Овде нема елемента на индексу 5 јер листа има само 3 елемента (индекси 0, 1, 2).

**Како исправити:**

- Проверите да ли индекс постоји пре приступања елементу.

**Исправка:**

.. activecode:: debagovanje8
   :coach:

   lista = [1, 2, 3]
   if len(lista) > 5:
       print(lista[5])
   else:
       print("Индекс не постоји у листи.")




**5. Именске грешке (NameError)**

**NameError** се јавља када се покуша употребити променљива која није дефинисана или када се погрешно напише име променљиве или функције.

**Пример:**

.. activecode:: debagovanje9
   :coach:

   print(ime)


Ако променљива `ime` није претходно дефинисана, настаће `NameError`.

**Како исправити:**

- Уверите се да је променљива дефинисана пре коришћења.

**Исправка:**

.. activecode:: debagovanje10
   :coach:

   ime = "Јован"
   print(ime)




**6. Грешке вредности (ValueError)**

**ValueError** се јавља када функција добије исправан тип аргумента, али вредност није прихватљива.

**Пример:**

.. activecode:: debagovanje11
   :coach:

   broj = int("abc")


Овде покушавамо да конвертујемо стринг који не садржи број у цео број, што изазива `ValueError`.

**Како исправити:**

- Провери да ли је вредност исправног формата пре конверзије.

**Исправка:**

.. activecode:: debagovanje12
   :coach:

   broj_str = "123"
   broj = int(broj_str)


**7. Кључне грешке (KeyError)**

**KeyError** се јавља када покушавате да приступите неком кључу у речнику који не постоји.

**Пример:**

.. activecode:: debagovanje13
   :coach:

   reci = {"име": "Јован", "године": 30}
   print(reci["адреса"])


Овде речник нема кључ под називом `"адреса"`, што изазива `KeyError`.

**Како исправити:**

- Проверите да ли кључ постоји у речнику пре приступања.

**Исправка:**

.. activecode:: debagovanje14
   :coach:

   reci = {"име": "Јован", "године": 30}
   if "адреса" in reci:
       print(reci["адреса"])
   else:
       print("Кључ не постоји у речнику.")




**8. Атрибутске грешке (AttributeError)**

**AttributeError** се јавља када објекат нема одређени атрибут или метод који покушавамо да користимо.

**Пример:**

.. activecode:: debagovanje15
   :coach:

   lista = [1, 2, 3]
   lista.append(4)
   lista.upper()


Овде долази до `AttributeError` јер листе немају метод `upper()`.

**Како исправити:**

- Проверите који методи и атрибути су доступни за одређени објекат.

**Исправка:**

.. activecode:: debagovanje16
   :coach:

   tekst = "zdravo"
   tekst.upper()  # Ово ради јер стрингови имају метод upper()



**9. Логичке грешке**

**Логичке грешке** се јављају када програм ради без грешке, али не даје очекиване резултате. Оне су најтеже за проналажење јер не изазивају прекид програма.

**Пример:**

.. activecode:: debagovanje17
   :coach:

   brojevi = [1, 2, 3, 4, 5]
   suma = 0

   for broj in brojevi:
       suma = broj  # Грешка: требало је да додамо број на суму, а не да га заменимо

   print(suma)


Овде програм не даје грешку, али резултат суме је погрешан јер се вредност суме замењује уместо да се сабира.

**Како исправити:**

- Исправи логику програма.

**Исправка:**

.. activecode:: debagovanje18
   :coach:

   brojevi = [1, 2, 3, 4, 5]
   suma = 0
   for broj in brojevi:
       suma += broj  # Исправно сабирање

   print(suma)


**Технике дебаговања у Пајтону:**
-------------------------------------



1. **Исписивање порука (print debugging)**: Једноставно додавање `print()` израза у кôд на кључним местима како бисте видели ток извршавања и вредности променљивих.
   
Пример дебаговања са наредбом print

.. activecode:: argumenti111
   :coach:

   n = 5
   rezultat = 1

   print("Израчунавање факторијела броја", n)
   print("Почетна вредност резултата:", rezultat)  # Дебаг: почетна вредност резултата

   # Петља за рачунање факторијела
   for i in range(1, n + 1):
      print("Пре множења:", "резултат = ", rezultat, "тренутни број i = ", i)  # Дебаг: стање пре множења
      rezultat *= i
      print("После множења: резултат = ", rezultat)  # Дебаг: нова вредност резултата после множења

   print("Факторијел броја", n, "је:", rezultat)


.. infonote:: Објашњење

   1. **Почетна вредност резултата**: Програм почиње са иницијалном вредношћу резултата као 1, јер факторијел било ког броја почиње од 1.
      
   2. **Принт изрази унутар петље**:
      - Пре сваког множења, принтамо тренутни резултат и тренутни број који множимо.
      - Након што се број помножи, принтамо нову вредност резултата.

   3. **Петља**: Петља пролази кроз све бројеве од 1 до `n` и множи их како би израчунала факторијел.

Ако покренете овај кôд са бројем 5, излаз ће изгледати овако:


.. code-block:: python 
   
   Израчунавање факторијела броја 5:
   Почетна вредност резултата: 1
   Пре множења: резултат = 1, тренутни број i = 1
   После множења: резултат = 1
   Пре множења: резултат = 1, тренутни број i = 2
   После множења: резултат = 2
   Пре множења: резултат = 2, тренутни број i = 3
   После множења: резултат = 6
   Пре множења: резултат = 6, тренутни број i = 4
   После множења: резултат = 24
   Пре множења: резултат = 24, тренутни број i = 5
   После множења: резултат = 120
   Факторијел броја 5 је: 120


.. infonote:: Објашњење излаза

   - Програм почиње са резултатом 1.
   - Петља се извршава за сваку вредност `i` од 1 до 5.
   - У свакој итерацији, програм исписује тренутну вредност резултата пре и после множења, како би показали како се вредности мењају у току рачунања.
   - Када петља заврши, програм исписује финални резултат, који је факторијел броја 5, што је 120.
   
   
2. **Коришћење дебагера**: Уграђени модул `pdb` у Пајтону омогућава корак-по-корак извршавање кода и праћење промена у вредностима.
   
.. code-block:: python
   
   import pdb
   pdb.set_trace()
   
   
3. **Изузеци и обрада грешака**: Коришћење блока `try-except` за хватање и обраду изузетака у коду.

.. activecode:: debagovanje21
   :coach:   
   
   try:
       broj = int("abc")
   except ValueError:
       print("Није могуће конвертовати стринг у број.")
   


Дебаговање је важан део процеса програмирања. Честе грешке као што су синтаксне, индексне, именске и логичке грешке могу се релативно лако уочити и исправити.