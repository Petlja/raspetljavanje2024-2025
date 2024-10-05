Веза између for и while петље
=============================


Lekcija: Veza između `for` i `while` petlje u Pajtonu

U Pajtonu postoje dve glavne vrste petlji: `for` petlja i `while` petlja. Oba tipa petlji omogućavaju ponavljanje bloka koda, ali se razlikuju po tome kako funkcionišu i kada se koriste. Razumevanje njihove veze pomaže u izboru pravog alata za rešavanje određenih problema.

Osnovne razlike između `for` i `while` petlje

- **`for` petlja** se koristi kada znamo tačan broj iteracija (ponavljanja) ili kada iteriramo kroz kolekcije podataka (npr. listu, rečnik, skup, string).
- **`while` petlja** se koristi kada ponavljanje zavisi od ispunjavanja određenog uslova, a broj iteracija nije unapred poznat.

Sintaksa:
- **`for` petlja**:

.. activecode:: forwhile1
   :coach:

   for element in sekvenca:
        # kod koji se izvršava za svaki element
   

- **`while` petlja**:
 
.. activecode:: forwhile2
   :coach: 
    
	while uslov:
        # kod koji se izvršava dok je uslov tačan
    

Veza između `for` i `while` petlje

Iako su ove dve petlje različite u načinu rada, mnogi problemi koji se rešavaju `for` petljom mogu se rešiti i pomoću `while` petlje, i obrnuto. Razlika je u načinu na koji se kontroliše petlja.

Primer 1: `for` petlja kao `while` petlja

Pogledajmo klasičan primer `for` petlje koja iterira kroz listu:

.. activecode:: forwhile3
   :coach: 

   voce = ["jabuka", "banana", "kruska"]
   for vocka in voce:
       print(vocka)


Ova petlja može biti napisana pomoću `while` petlje tako što ćemo koristiti brojač za praćenje indeksa liste:

.. activecode:: forwhile4
   :coach: 

   voce = ["jabuka", "banana", "kruska"]
   i = 0
   while i < len(voce):
       print(voce[i])
       i += 1


U ovom slučaju, koristimo `while` petlju kako bismo prošli kroz svaki element liste koristeći indeks. U oba primera dobijamo isti rezultat, iako je `for` petlja prirodnija za rad sa kolekcijama.

Primer 2: `while` petlja kao `for` petlja

Kada znamo tačan broj iteracija, možemo zameniti `while` petlju sa `for` petljom. Na primer, ako želimo da ispišemo brojeve od 1 do 5 koristeći `while` petlju:

.. activecode:: forwhile5
   :coach: 

   broj = 1
   while broj <= 5:
       print(broj)
       broj += 1


Ova petlja može biti preformulisana u `for` petlju koristeći `range()` funkciju:

.. activecode:: forwhile6
   :coach: 

   for broj in range(1, 6):
       print(broj)


Ovo je elegantniji način za rešavanje problema kada se unapred zna broj iteracija.

Kada koristiti `for`, a kada `while` petlju?

1. **Kada koristiti `for` petlju**:
   - Kada radimo sa kolekcijama podataka (listama, stringovima, rečnicima, skupovima).
   - Kada unapred znamo koliko puta treba da ponovimo blok koda.
   - Kada koristimo funkciju `range()` za iteriranje kroz sekvencu brojeva.

2. **Kada koristiti `while` petlju**:
   - Kada broj ponavljanja zavisi od uslova koji se menja u toku izvršavanja programa.
   - Kada unapred ne znamo koliko iteracija je potrebno, već čekamo da se ispuni neki uslov.
   - Kada se petlja može prekinuti u bilo kom trenutku na osnovu promenljive vrednosti (npr. korisnički unos).

Sličnosti između `for` i `while` petlje

- **Besonačnost**: Obe petlje mogu kreirati beskonačne petlje ako se uslovi za izlazak iz petlje ne postave pravilno.
  
    - Beskonačna `for` petlja (npr. sa `range()` bez granice):

.. activecode:: forwhile7
   :coach:      
      
   for broj in range(1, 99999999):
      # neka radnja
     
      
- Beskonačna `while` petlja:
 
.. activecode:: forwhile8
   :coach: 
      
   while True:
       # neka radnja
     

- **Kontrola toka**: Obe petlje mogu koristiti kontrolne naredbe kao što su `break` (za prekid petlje) i `continue` (za preskakanje trenutne iteracije).

- Primer sa `break`:
    
	
.. activecode:: forwhile9
   :coach: 
   
   for broj in range(1, 10):
       if broj == 5:
           break
       print(broj)
 
.. activecode:: forwhile10
   :coach:  
     
   broj = 1
   while broj < 10:
       if broj == 5:
           break
       print(broj)
       broj += 1
      

Zaključak

- **`for` petlja** je pogodnija kada radimo sa kolekcijama podataka ili kada znamo tačan broj ponavljanja.
- **`while` petlja** je fleksibilnija za slučajeve kada je potrebno ponavljati blok koda dok neki uslov važi, a broj iteracija nije unapred poznat.

Izbor između `for` i `while` petlje zavisi od prirode problema koji rešavate. Oba tipa petlji su moćni alati u Pajtonu za ponavljanje zadataka.