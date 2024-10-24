Типови података
===============


Python подржава више различитих типова података који се користе за чување и рад са вредностима. 
Најчешћи типови података укључују целе бројеве, реалне бројеве (децимале), стрингове, логичке 
вредности и сложеније структуре као што су листе и речници.


- 1. Цео број (Integer)

Цели бројеви су бројеви без децимала, као што су 1, 42 или -100.

.. activecode:: tipovi1
   :coach:

   x = 10
   y = -3
   print(x)
   print(y)


Можете извршавати основне математичке операције са целим бројевима, као што су сабирање, одузимање, множење и дељење.

.. activecode:: aritmetika1
   :coach:

   a = 5
   b = 2
   sabiranje = a + b
   mnozenje = a * b
   oduzimanje = a - b
   deljenje = a / b
   print(sabiranje, mnozenje, oduzimanje, deljenje)


- Реални број (Float)

Реални бројеви (floating point) су бројеви са децималама, попут 3.14 или -0.001.

.. activecode:: aritmetika2
   :coach:

   pi = 3.14159
   tezina = 70.5
   print(pi)
   print(tezina)


Python такође подржава операције са реалним бројевима.

.. activecode:: aritmetika3
   :coach:

   a = 7.5
   b = 2.3
   zbir = a + b
   proizvod = a * b
   print(zbir, proizvod)



- Стринг (String)

Стринг је низ знакова обухваћен двоструким или једноструким наводницима. Стринг може садржати слова, бројеве и симболе.

.. activecode:: aritmetika4
   :coach:
   
   ime = "Марија"
   poruka = 'Здраво, светe!'
   print(ime)
   print(poruka)
   
   
- Испис целих бројева, реалних бројева и стрингова  

   Пајтон препознаје тип податка који се додељује променљивој и та променљива постаје променљива тог типа након доделе вредности.	
   Можете исписивати различите типове података као што су целобројни, реални бројеви и стрингови.

.. activecode:: print2
   :coach:

   x = 42
   y = 3.14
   ime = "Marija"
   print(x, y, ime)
   
- Комбиновање типова података  
   Користећи запете, можете комбиновати више различитих типова у једном исказу.

.. activecode:: print3
   :coach:

   x = 42
   y = 3.14
   print("Rezultat je:", x, "a broj pi je:", y)
   
   


Можете комбиновати стрингове користећи оператор `+` или методе као што је `format()` или ф-стринг.
Пример са спајањем стрингова:

.. activecode:: aritmetika5
   :coach:

   ime = "Јован"
   prezime = "Петровић"
   puno_ime = ime + " " + prezime
   print(puno_ime)

Пример са ф-стрингом:

.. activecode:: aritmetika6
   :coach:

   ime = "Petar"
   godina = 23
   print(f"{ime} има {godina} године.")


- Логички тип (Boolean)

Логичке вредности у Python-у могу бити само `True` или `False`. Најчешће се користе у условним исказима и петљама.

.. activecode:: aritmetika7
   :coach:
   
   tacno = True
   netacno = False
   print(tacno)
   print(netacno)


Логичке вредности се добијају коришћењем оператора за поређење, као што су `==`, `!=`, `>`, `<`, `>=`, `<=`.


.. activecode:: aritmetika8
   :coach:

   a = 5
   b = 10
   print(a > b)  # False
   print(a < b)  # True



- Листа (List)

Листа је колекција података која може да садржи више вредности различитих типова. Елементи у листи су смештени у угластим заградама `[]` и раздвојени запетама.

.. activecode:: aritmetika9
   :coach:

   lista_brojeva = [1, 2, 3, 4, 5]
   lista_mesovitih_tipova = [1, "два", 3.0, True]
   print(lista_brojeva)
   print(lista_mesovitih_tipova)

Можете приступити елементима листе користећи индекс, при чему индексирање почиње од 0.

.. activecode:: aritmetika10
   :coach:

   lista_brojeva = [1, 2, 3, 4, 5]
   prvi_element = lista_brojeva[0]
   poslednji_element = lista_brojeva[-1]
   print(prvi_element)
   print(poslednji_element)


-Речник (Dictionary)

Речник је структура података која чува парове кључ:вредност. Кључеви морају бити јединствени и налазе се у витичастим заградама `{}`.



.. activecode:: aritmetika11
   :coach:

   student = {
       "ime": "Марија",
       "godine": 20,
       "fakultet": "Електротехнички факултет"
    }
   print(student)


Можете приступити вредностима у речнику користећи кључеве.

.. activecode:: aritmetika12
   :coach:

   
   student = {
       "ime": "Марија",
       "godine": 20,
       "fakultet": "Електротехнички факултет"
    }
   print(student["ime"])
   print(student["fakultet"])
   
   
   
- Konverzija između tipova podataka podrazumeva pretvaranje jedne vrste podataka u drugu. U većini programskih jezika, ovo se radi automatski (implicitna konverzija) ili eksplicitno pomoću posebnih funkcija

Evo nekoliko primera za eksplicitnu konverziju (poznatu kao casting) u Python-u:

-Konverzija iz stringa u broj (integer):
Pretvaranje stringa koji sadrži broj u integer

.. activecode:: konverzije1
   :coach:

   str_num = "123"
   int_num = int(str_num)
   print(int_num)  


-Konverzija iz broja u string:
Pretvaranje integer-a u string.


.. activecode:: konverzije2
   :coach:

   int_num = 456
   str_num = str(int_num)
   print(str_num)  


-Konverzija iz float-a u integer. Pretvaranje broja sa decimalom u ceo broj (decimale se odbacuju).


.. activecode:: konverzije3
   :coach:

   float_num = 9.99
   int_num = int(float_num)
   print(int_num)  


-Konverzija iz integer-a u float. Pretvaranje celog broja u broj sa decimalom.


.. activecode:: konverzije4
   :coach:

   int_num = 7
   float_num = float(int_num)
   print(float_num)  


-Konverzija iz integer-a u boolean. Pretvaranje celog broja u boolean vrednost (0 je False, sve ostalo je True)


.. activecode:: konverzije5
   :coach:

   int_num = 0
   bool_value = bool(int_num)
   print(bool_value)  


Svaka konverzija treba da bude pažljiva, posebno kada radimo sa različitim tipovima podataka, kako bi se izbegle greške poput neodgovarajućih formata ili gubitka podataka.
   


Резиме

- Цео број (Integer): Бројеви без децимала, нпр. `42`, `-10`.
- Реални број (Float): Бројеви са децималама, нпр. `3.14`, `-0.01`.
- Стринг (String): Низ знакова у наводницима, нпр. `"Здраво"`, `'Python'`.
- Логички тип (Boolean): Логичке вредности `True` и `False`.
- Листа (List): Колекција података смештених у угластим заградама `[]`.
- Речник (Dictionary): Парови кључ:вредност у витичастим заградама `{}`.

Ови типови података представљају основе за рад са подацима у Python-у.


