While петља
============

Lekcija: `while` Petlja u Pajtonu

`while` petlja u Pajtonu se koristi kada želimo da ponavljamo određeni blok koda dok neki uslov ostaje tačan. Ova petlja će nastaviti da izvršava kod sve dok je uslov `True`. Kada uslov postane `False`, petlja se prekida i prelazi se na ostatak programa.

Osnovna sintaksa:

.. activecode:: while1
   :coach:

   while uslov:
       # kod koji se izvršava dok je uslov tačan


- **`uslov`** je logički izraz koji se proverava pre svakog prolaska kroz petlju.
- Petlja će se nastaviti sve dok je vrednost uslova `True`.

Primer 1: Jednostavna `while` petlja
Ovaj primer će štampati brojeve od 1 do 5.

.. activecode:: while2
   :coach:

   broj = 1
   while broj <= 5:
       print(broj)
       broj += 1



Ovde petlja traje dok je vrednost promenljive `broj` manja ili jednaka 5. Nakon svakog prolaska, `broj` se uvećava za 1.

Primer 2: Beskonačna `while` petlja
Ako uslov u `while` petlji uvek ostaje tačan, petlja će se izvršavati beskonačno, što može dovesti do problema ako se ne zaustavi. U nastavku je primer beskonačne petlje:

.. activecode:: while3
   :coach:
   
   while True:
       print("Ova petlja traje zauvek!")


**Napomena**: Da bi se zaustavila ovakva petlja, koristimo neku formu prekida, poput naredbe `break`.

Primer 3: Korišćenje `break` u `while` petlji
Naredba `break` se koristi za prevremeni prekid petlje, čak i ako uslov još uvek važi.

.. activecode:: while4
   :coach:

   broj = 1
   while True:
       print(broj)
       if broj == 3:
           break
       broj += 1


Ova petlja bi teoretski trajala zauvek, ali kada promenljiva `broj` postane 3, `break` naredba prekida petlju.

Primer 4: Korišćenje `continue` u `while` petlji
Naredba `continue` preskače ostatak koda u trenutnom prolasku petlje i prelazi na sledeći prolazak.

.. activecode:: while5
   :coach:
   
   
   broj = 0
   while broj < 5:
       broj += 1
       if broj == 3:
           continue
       print(broj)


Kada `broj` postane 3, `continue` preskače tu iteraciju, pa se broj 3 ne ispisuje.

Primer 5: `while` petlja sa `else` blokom
Slično kao kod `for` petlje, `else` blok se može koristiti sa `while` petljom i on će se izvršiti kada petlja završi na prirodan način (bez prekida `break` naredbom).

.. activecode:: while6
   :coach:

   broj = 1
   while broj <= 3:
       print(broj)
       broj += 1
   else:
       print("Petlja je završena!")



Ključne stvari koje treba zapamtiti:
- `while` petlja se izvršava sve dok je uslov tačan.
- Koristite `break` za prevremeni izlaz iz petlje.
- `continue` se koristi za preskakanje trenutnog prolaska i prelazak na sledeći.
- Petlja sa `else` blokom omogućava dodatnu radnju nakon završetka petlje.

`While` petlje su korisne kada ne znamo tačno koliko puta treba da ponovimo radnju, već se oslanjamo na neki dinamički uslov koji kontroliše izvršavanje petlje.