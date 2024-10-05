For петља
===========

Lekcija: `for` Petlja u Pajtonu

U Pajtonu, `for` petlja služi za ponavljanje određenih radnji više puta, po elementima neke kolekcije (kao što su liste, rečnici, skupovi, itd.) 
ili unutar određenog intervala vrednosti. Sa `for` petljom možemo proći kroz svaki element određene sekvence i izvršiti neku radnju za svaki od njih.

Osnovna sintaksa:

.. activecode:: for1
   :coach:

   for element in sekvenca:
       # ovde ide kod koji će se izvršiti za svaki element


- **`element`** predstavlja promenljivu koja uzima vrednost svakog pojedinačnog elementa iz sekvence.
- **`sekvenca`** je kolekcija elemenata kroz koje petlja prolazi.


Primer 1: `for` petlja kroz listu

.. activecode:: for2
   :coach:

   voce = ["jabuka", "banana", "kruska"]
   for vocka u voce:
       print(vocka)



Primer 2: Korišćenje `range()` funkcije
Funkcija `range()` generiše niz brojeva, koji se često koriste sa `for` petljom.

.. activecode:: for3
   :coach:

   for broj u range(5):
       print(broj)


Ovde `range(5)` generiše brojeve od 0 do 4 (ne uključujući 5).

Primer 3: Korišćenje `range(start, stop, step)`

Funkcija `range()` može imati do tri parametra:
- **start** (početna vrednost),
- **stop** (krajnja vrednost, ali ne uključena),
- **step** (korak, odnosno interval).

.. activecode:: for4
   :coach:

   for broj u range(2, 10, 2):
       print(broj)


Primer 4: Ugnježđena `for` petlja

Možete imati jednu `for` petlju unutar druge.

.. activecode:: for5
   :coach:

   for i in range(3):
       for j in range(2):
            print(f"i: {i}, j: {j}")



Primer 5: `for` petlja i `else`
`else` blok može biti korišćen sa `for` petljom. On će se izvršiti kada se završi petlja, osim ako nije došlo do prekida `break` naredbom.

.. activecode:: for6
   :coach:


   for broj u range(3):
       print(broj)
   else:
       print("Petlja je završena!")



Ključne stvari koje treba zapamtiti:
- `for` petlja u Pajtonu služi za ponavljanje kroz elemente neke kolekcije ili intervala.
- Može se kombinovati sa `range()` funkcijom za generisanje niza brojeva.
- Može se koristiti `else` blok za dodatne radnje nakon završetka petlje.

`For` petlje su moćan način za obradu podataka u Pajtonu, posebno kada treba da prođete kroz velike količine podataka na efikasan način.