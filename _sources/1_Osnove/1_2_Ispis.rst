==================
Испис - print()
==================


- Шта је функција print()?  
   print() је уграђена Python функција која исписује вредности у конзолу.
   
   
   
Покрени следећи програм и пробај да измениш бројеве и симболе. Посматрај како се вредност израза мења.

.. activecode:: print1
   :coach:

   print("Zdravo, svete!")

.. infonote::

  Обрати пажњу да се **=** користи када променљивој **додељујемо** вредност, а да се **==** користи за **поређење** да ли су две вредности једнаке.   

- Испис целих бројева, реалних бројева и стрингова  
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
   
   
- Нови ред (`\n`)  
    Користи се за прекид линије и премештање текста на нови ред.


.. activecode:: print4
   :coach:

   print("Prva linija\nDruga linija")
   
- Табулатор (`\t`)  
   Табулатор користимо за уметање размака између речи.
   
.. activecode:: print5
   :coach:
   
   print("Kolona 1\tKolona 2\tKolona 3")

- Коришћење ф-стрингова  
    Ф-стрингови омогућавају једноставно укључивање вредности у текстуални исказ.

   
.. activecode:: print6
   :coach:
   
   ime = "Petar"
   godina = 23
   print(f"{ime} ima {godina} godine.")
   
   
- Форматирање бројева  
    Можете контролисати број децимала у испису реалних бројева.

.. activecode:: print7
   :coach:
   
   broj = 3.14159
   print(f"Broj pi je priblizno: {broj:.2f}")

   
- Метод `.format()`  
    Ово је старији метод за форматирање стрингова.

.. activecode:: print8
   :coach:
   
   tekst = "Cena proizvoda je {} dinara."
   cena = 250
   print(tekst.format(cena))

- Параметар sep  
    Користи се за прилагођавање симбола који раздваја елементе.
    
.. activecode:: print9
   :coach:
   
   print("Marija", "Petar", "Jovana", sep=", ")
   

- Параметар end  

    Можете прилагодити завршни карактер након исписа. Подразумевани је нови ред (`\n`).
    
.. activecode:: print10
   :coach:
   
   print("Ovo je kraj", end="!")
   print("Sledeća linija neće biti u novom redu.")
    

- Испис табела  
    
   Форматирање података у табеларном облику.
    
.. activecode:: print12
   :coach:    
   
   print("Ime\tPredmet\tOcena")
   print("Marija\tMatematika\t5")
   print("Petar\tFizika\t4")
   

- Испис током рада програма
    print() је често коришћен за праћење тока извршавања програма.
    
.. activecode:: print13
   :coach: 
   
   for i in range(3):
       
      print(f"Obrada podataka {i+1}")
   

- Заборављање на формат стрингова  
    Када се користе променљиве у print(), морате бити сигурни да су коректно форматиране. Овај исказ ће дати грешку јер је година у променљивој 'broj' податак типа integer.
    
.. activecode:: print14
   :coach: 
   
   godina = 23
   print("Petar ima" + godina + "godine.")


Исправљен исказ

.. activecode:: print15
   :coach: 
   
   godina = 23
   print("Petar ima " + str(godina) + " godine.")

- Употреба print() у петљама  
    Када се print() користи унутар петљи, то може успорити извршавање програма због превеликог броја исказа.
    
.. activecode:: print16
   :coach:   
   
   for i in range(1000):
       print(i)
    
