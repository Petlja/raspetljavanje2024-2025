Променљиве и типови података
==============================

==================
Променљиве
==================

Текст и бројеве које желимо да користимо више пута можемо сачувати у променљиве. Променљиве служе да рачунар запамти вредности које смо му задали.
Сваку променљиву можемо да замислимо као полицу на којој нешто чувамо. У сваком тренутку то нешто можемо склонити са полице и заменити нечим другим. 
Ако имамо невероватно велики број полица, потребно нам је да им дајемо одговарајуће називе да бисмо се снашли (као што у библиотеци постоје полице за 
белетристику, поезију, крими романе, стручну литературу итд).

Променљива је дакле, простор у меморији рачунара коме смо дали неко име. Важно је да име које смо простору дали буде такво да јасно означава шта се у 
простору чува и да нам помогне да се снађемо у коду. У том простору чувамо неку учитану или израчунату вредност. Као име променљиве обично користимо 
низ слова енглеске абецеде. У именима могу још да се појаве и слова других језика, доње црте и цифре, али цифра не може да буде на првом месту.




Променљиву користимо навођењем њеног имена:

.. activecode:: promenljive1

   
   ime = "Марија"
   print("Здраво, ја се зовем", ime)
   print("Име", ime, "добила сам по мојој баки која се такође зове", ime)
   
.. questionnote::
   
   У свом радном окружењу направи фајл под називом zanimljivost_o_imenu.py и промени га тако да исписује твоје име и неку занимљивост о њему.

====================================
Како нам фиока користи?
====================================

- Можемо да прикажемо шта се налази у фиоци,

- Можемо да променимо садржај фиоке

- Можемо да се питамо да ли се у фиоци налази одређени податак


.. image:: ../../_images/Promenljive.gif
   :width: 800 px
   :alt: alternate text



==================
Типови података
==================

Python подржава више различитих типова података који се користе за чување и рад са вредностима. 
Најчешћи типови података укључују целе бројеве, реалне бројеве (децимале), стрингове, логичке 
вредности и сложеније структуре као што су листе и речници.


- Цео број (Integer)

Цели бројеви су бројеви без децимала, као што су 1, 42 или -100.

.. activecode:: tipovi1
   :coach:

   x = 10
   y = -3
   print(x)
   print(y)


Можете извршавати основне математичке операције са целим бројевима, као што су сабирање, одузимање, множење и дељење.

.. activecode:: tipovi2
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

.. activecode:: tipovi3
   :coach:

   pi = 3.14159
   tezina = 70.5
   print(pi)
   print(tezina)


Python такође подржава операције са реалним бројевима.

.. activecode:: tipovi4
   :coach:

   a = 7.5
   b = 2.3
   zbir = a + b
   proizvod = a * b
   print(zbir, proizvod)



- Стринг (String)

Стринг је низ знакова обухваћен двоструким или једноструким наводницима. Стринг може садржати слова, бројеве и симболе.

.. activecode:: tipovi5
   :coach:
   
   ime = "Марија"
   poruka = 'Здраво, светe!'
   print(ime)
   print(poruka)
   
   
- Испис целих бројева, реалних бројева и стрингова  

   Пајтон препознаје тип податка који се додељује променљивој и та променљива постаје променљива тог типа након доделе вредности.	
   Можете исписивати различите типове података као што су целобројни, реални бројеви и стрингови.

.. activecode:: tipovi6
   :coach:

   x = 42
   y = 3.14
   ime = "Marija"
   print(x, y, ime)
   
   
- Комбиновање типова података  
   
   Користећи зарезе, можете комбиновати више различитих типова у једном исказу.

.. activecode:: tipovi7
   :coach:

   x = 42
   y = 3.14
   print("Rezultat je:", x, "a broj pi je:", y)
   
 
- Логички тип (Boolean)

Логичке вредности у Python-у могу бити само `True` или `False`. Најчешће се користе у условним исказима и петљама.

.. activecode:: tipovi8
   :coach:
   
   tacno = True
   netacno = False
   print(tacno)
   print(netacno)


Логичке вредности се добијају коришћењем оператора за поређење, као што су `==`, `!=`, `>`, `<`, `>=`, `<=`.


.. activecode:: tipovi9
   :coach:

   a = 5
   b = 10
   print(a > b)  # False
   print(a < b)  # True


- Konverzija između tipova podataka podrazumeva pretvaranje jedne vrste podataka u drugu. U većini programskih jezika, ovo se radi automatski (implicitna konverzija) ili eksplicitno pomoću posebnih funkcija

Evo nekoliko primera za eksplicitnu konverziju (poznatu kao casting) u Python-u:

- Konverzija iz stringa u broj (integer): Pretvaranje stringa koji sadrži broj u integer

.. activecode:: tipovi10
   :coach:

   str_num = "123"
   int_num = int(str_num)
   print(int_num)  


- Konverzija iz broja u string: Pretvaranje integer-a u string.


.. activecode:: tipovi11
   :coach:

   int_num = 456
   str_num = str(int_num)
   print(str_num)  


- Konverzija iz float-a u integer: Pretvaranje broja sa decimalom u ceo broj (decimale se odbacuju).


.. activecode:: tipovi12
   :coach:

   float_num = 9.99
   int_num = int(float_num)
   print(int_num)  


- Konverzija iz integer-a u float: Pretvaranje celog broja u broj sa decimalom.


.. activecode:: tipovi13
   :coach:

   int_num = 7
   float_num = float(int_num)
   print(float_num)  


- Konverzija iz integer-a u boolean: Pretvaranje celog broja u boolean vrednost (0 je False, sve ostalo je True)


.. activecode:: tipovi14
   :coach:

   int_num = 0
   bool_value = bool(int_num)
   print(bool_value)  


Svaka konverzija treba da bude pažljiva, posebno kada radimo sa različitim tipovima podataka, kako bi se izbegle greške poput neodgovarajućih
formata ili gubitka podataka.
   


Резиме

- Цео број (Integer): Бројеви без децимала, нпр. `42`, `-10`.
- Реални број (Float): Бројеви са децималама, нпр. `3.14`, `-0.01`.
- Стринг (String): Низ знакова у наводницима, нпр. `"Здраво"`, `'Python'`.
- Логички тип (Boolean): Логичке вредности `True` и `False`.


Ови типови података представљају основе за рад са подацима у Python-у.


