Vežbe
=====

Zadatak 1
-----------

Napiši program koji učitava broj n i ispisuje sve parne brojeve od 1 do n.

.. activecode:: zadatak1
    :coach:
    
    # Dopuni

**Primer 1**:

**Ulaz**:  
10  

**Izlaz**:  
2 4 6 8 10  

**Objašnjenje izlaza**:  
Svi parni brojevi između 1 i 10 su ispisani.

**Primer 2**:

**Ulaz**:  
7  

**Izlaz**:  
2 4 6  

**Objašnjenje izlaza**:  
Svi parni brojevi između 1 i 7 su ispisani.

.. learnmorenote:: Rešenje

    .. code-block:: python

        n = int(input("Unesite broj: "))  # Učitavanje gornje granice
        for i in range(1, n + 1):         # Petlja prolazi kroz sve brojeve od 1 do n
            if i % 2 == 0:                # Provera da li je broj paran
                print(i, end=" ")         # Ispis parnih brojeva


Zadatak 2
-----------

Napiši program koji proverava da li je uneti broj prost.

.. activecode:: zadatak2
    :coach:
    
    # Dopuni

**Primer 1**:

**Ulaz**:  
13  

**Izlaz**:  
Broj 13 je prost.  

**Objašnjenje izlaza**:  
Broj 13 je deljiv samo sa 1 i samim sobom.

**Primer 2**:

**Ulaz**:  
10  

**Izlaz**:  
Broj 10 nije prost.  

**Objašnjenje izlaza**:  
Broj 10 ima više delilaca osim 1 i samog sebe (npr. 2 i 5).

.. learnmorenote:: Rešenje

    .. code-block:: python

        n = int(input("Unesite broj: "))  # Učitavanje broja
        if n < 2:                         # Provera da li je broj manji od 2
            print("Broj nije prost.")
        else:
            prost = True                  # Pretpostavljamo da je broj prost
            for i in range(2, int(n ** 0.5) + 1):  # Prolazimo do kvadratnog korena broja
                if n % i == 0:            # Provera da li postoji delilac osim 1 i n
                    prost = False
                    break
            if prost:
                print(f"Broj {n} je prost.")
            else:
                print(f"Broj {n} nije prost.")


Zadatak 3
-----------

Napiši program koji računa faktorijel unetog broja.

.. activecode:: zadatak3
    :coach:
    
    # Dopuni

**Primer 1**:

**Ulaz**:  
5  

**Izlaz**:  
Faktorijel broja 5 je 120.  

**Objašnjenje izlaza**:  
Faktorijel se računa kao :math:`5! = 5 \times 4 \times 3 \times 2 \times 1 = 120`.

**Primer 2**:

**Ulaz**:  
3  

**Izlaz**:  
Faktorijel broja 3 je 6.  

**Objašnjenje izlaza**:  
Faktorijel se računa kao :math:`3! = 3 \times 2 \times 1 = 6`.

.. learnmorenote:: Rešenje

    .. code-block:: python

        n = int(input("Unesite broj: "))  # Učitavanje broja
        faktorijel = 1                   # Inicijalizacija faktorijela
        for i in range(1, n + 1):         # Petlja od 1 do n
            faktorijel *= i              # Množenje trenutnog broja
        print(f"Faktorijel broja {n} je {faktorijel}.")


Zadatak 4
-----------

Napiši program koji proverava da li je uneti broj Armstrongov broj.

.. activecode:: zadatak4
    :coach:
    
    # Dopuni

**Primer 1**:

**Ulaz**:  
153  

**Izlaz**:  
Broj 153 je Armstrongov broj.  

**Objašnjenje izlaza**:  
Cifre broja 153 podignute na treći stepen daju: :math:`1^3 + 5^3 + 3^3 = 1 + 125 + 27 = 153`. 

**Primer 2**:

**Ulaz**:  
123  

**Izlaz**:  
Broj 123 nije Armstrongov broj.  

**Objašnjenje izlaza**:  
Cifre broja 123 podignute na treći stepen daju: :math:`1^3 + 2^3 + 3^3 = 1 + 8 + 27 = 36`. 

.. infonote::
    
    **Šta je Armstrongov broj?**

    Armstrongov broj je broj koji je jednak zbiru svojih cifara podignutih na stepen jednak broju cifara u tom broju.

    **Primer:**

    - Broj 153 ima tri cifre: (1, 5, 3).

    - Zbir cifara podignutih na treći stepen je:

    :math:`1^3 + 5^3 + 3^3 = 1 + 125 + 27 = 153`

    - Pošto je zbir jednak broju 153, to je Armstrongov broj.
        
    **Još primera Armstrongovih brojeva:**
    - 370, 371, 407 (trocifreni Armstrongovi brojevi).
    - 9474 (četvorocifreni Armstrongov broj).


.. learnmorenote:: Rešenje

    .. code-block:: python

        n = int(input("Unesite broj: "))  # Učitavanje broja
        suma = 0                          # Inicijalizacija sume cifara na stepen
        broj_cifara = len(str(n))         # Broj cifara u broju
        original = n                      # Čuvamo originalnu vrednost broja
        while n > 0:
            cifra = n % 10                # Ekstrakcija poslednje cifre
            suma += cifra ** broj_cifara  # Dodavanje cifre na odgovarajući stepen
            n //= 10                      # Uklanjanje poslednje cifre
        if suma == original:              # Provera da li je zbir jednak originalu
            print(f"Broj {original} je Armstrongov broj.")
        else:
            print(f"Broj {original} nije Armstrongov broj.")


Zadatak 5
-----------

Napiši program koji ispisuje sve trocifrene brojeve kod kojih je zbir cifara jednak 10.

.. activecode:: zadatak5
    :coach:
    
    # Dopuni

**Primer 1**:

**Ulaz**:  
(Nema dodatnog unosa, trocifreni brojevi se proveravaju automatski.)  

**Izlaz**:  
118 127 136 145 226 235 244 334  

**Objašnjenje izlaza**:  
Ispisani su svi trocifreni brojevi gde je zbir cifara jednak 10, na primer: za 118, :math:`1 + 1 + 8 = 10`.


.. learnmorenote:: Rešenje

    .. code-block:: python

        for broj in range(100, 1000):  # Iteracija kroz sve trocifrene brojeve
            cifra1 = broj // 100       # Prva cifra
            cifra2 = (broj // 10) % 10 # Druga cifra
            cifra3 = broj % 10         # Treća cifra
            if cifra1 + cifra2 + cifra3 == 10:  # Provera da li je zbir cifara 10
                print(broj, end=" ")            # Ispis brojeva


Zadatak 6
-----------

Napiši program koji za uneti broj n ispisuje sve njegove delioce.

.. activecode:: zadatak6
    :coach:
    
    # Dopuni

**Primer 1**:

**Ulaz**:  
12  

**Izlaz**:  
1 2 3 4 6 12  

**Objašnjenje izlaza**:  
Delioce broja 12 čine svi brojevi koji bez ostatka dele 12, uključujući i 12.

**Primer 2**:

**Ulaz**:  
15  

**Izlaz**:  
1 3 5 15  

**Objašnjenje izlaza**:  
Delioce broja 15 čine 1, 3, 5 i 15.

.. learnmorenote:: Rešenje

    .. code-block:: python

        n = int(input("Unesite broj: "))  # Učitavanje broja
        for i in range(1, n + 1):         # Iteracija od 1 do n
            if n % i == 0:                # Provera da li je i delioc broja n
                print(i, end=" ")         # Ispis delilaca


Zadatak 7
-----------

Napiši program koji proverava da li je uneti broj palindrom.

.. activecode:: zadatak7
    :coach:
    
    # Dopuni

**Primer 1**:

**Ulaz**:  
121  

**Izlaz**:  
Broj 121 je palindrom.  

**Objašnjenje izlaza**:  
Broj 121 se isto čita sa leve i desne strane.

**Primer 2**:

**Ulaz**:  
123  

**Izlaz**:  
Broj 123 nije palindrom.  

**Objašnjenje izlaza**:  
Broj 123 se ne čita isto sa leve i desne strane.

.. learnmorenote:: Rešenje

    .. code-block:: python

        broj = int(input("Unesite broj: "))  # Učitavanje broja
        originalni_broj = broj               # Čuvamo originalni broj za poređenje
        obrnut_broj = 0                      # Promenljiva za čuvanje obrnutog broja

        while broj > 0:
            cifra = broj % 10                # Uzimamo poslednju cifru broja
            obrnut_broj = obrnut_broj * 10 + cifra  # Dodajemo cifru na kraj obrnutog broja
            broj //= 10                      # Uklanjamo poslednju cifru iz broja

        if originalni_broj == obrnut_broj:   # Provera da li je broj isti kao njegov obrnuti oblik
            print("Broj je palindrom.")      # Ispis ako je broj palindrom
        else:
            print("Broj nije palindrom.")    # Ispis ako broj nije palindrom



Zadatak 8
-----------

Napiši program koji ispisuje sve trocifrene brojeve kod kojih je proizvod cifara jednak zbiru cifara.

.. activecode:: zadatak8
    :coach:
    
    # Dopuni

**Primer 1**:

**Ulaz**:  
(Nema dodatnog unosa, trocifreni brojevi se proveravaju automatski.)  

**Izlaz**:  
123  

**Objašnjenje izlaza**:  
Za broj 123, :math:`1 \times 2 \times 3 = 6`, a :math:`1 + 2 + 3 = 6`.

.. learnmorenote:: Rešenje

    .. code-block:: python

        for broj in range(100, 1000):         # Iteracija kroz sve trocifrene brojeve
            cifra1 = broj // 100              # Prva cifra
            cifra2 = (broj // 10) % 10        # Druga cifra
            cifra3 = broj % 10                # Treća cifra
            proizvod = cifra1 * cifra2 * cifra3  # Proizvod cifara
            zbir = cifra1 + cifra2 + cifra3      # Zbir cifara
            if proizvod == zbir:              # Provera da li su proizvod i zbir jednaki
                print(broj, end=" ")          # Ispis brojeva


Zadatak 9
-----------

Napiši program koji za uneti broj n proverava da li je savršen broj.  
(Savršen broj je broj jednak zbiru svojih pravih delilaca, osim sebe.)

.. activecode:: zadatak9
    :coach:
    
    # Dopuni

**Primer 1**:

**Ulaz**:  
6  

**Izlaz**:  
Broj 6 je savršen broj.  

**Objašnjenje izlaza**:  
Pravi delioci broja 6 su 1, 2 i 3. Njihov zbir :math:`1 + 2 + 3 = 6`, što znači da je 6 savršen broj.

**Primer 2**:

**Ulaz**:  
8  

**Izlaz**:  
Broj 8 nije savršen broj.  

**Objašnjenje izlaza**:  
Pravi delioci broja 8 su 1, 2 i 4. Njihov zbir :math:`1 + 2 + 4 = 7`, što znači da 8 nije savršen broj.

.. learnmorenote:: Rešenje

    .. code-block:: python

        n = int(input("Unesite broj: "))  # Učitavanje broja
        zbir = 0                          # Inicijalizacija zbira pravih delilaca
        for i in range(1, n):             # Provera svih brojeva manjih od n
            if n % i == 0:                # Provera da li je i delioc broja n
                zbir += i                 # Dodavanje delilaca u zbir
        if zbir == n:                     # Provera da li je zbir jednak originalnom broju
            print(f"Broj {n} je savršen broj.")
        else:
            print(f"Broj {n} nije savršen broj.")


Zadatak 10
-----------

Napiši program koji ispisuje sve četvorocifrene brojeve gde se svaka cifra pojavljuje tačno jednom.

.. activecode:: zadatak10
    :coach:
    
    # Dopuni

**Primer 1**:

**Ulaz**:  
(Nema dodatnog unosa, četvorocifreni brojevi se proveravaju automatski.)  

**Izlaz**:  
1023 1032 1203 1230 ...  

**Objašnjenje izlaza**:  
Brojevi poput 1023 imaju cifre 1, 0, 2 i 3 koje su sve različite i pojavljuju se samo jednom.

.. learnmorenote:: Rešenje

    .. code-block:: python

        # Prolazak kroz sve četvorocifrene brojeve
        for broj in range(1000, 10000):  
            # Izdvajanje cifara broja
            hiljade = broj // 1000
            stotine = (broj // 100) % 10
            desetice = (broj // 10) % 10
            jedinice = broj % 10

            # Provera da li su sve cifre različite
            if (hiljade != stotine and hiljade != desetice and hiljade != jedinice and
                stotine != desetice and stotine != jedinice and
                desetice != jedinice):
                print(broj)



Zadatak 11
-----------

Napiši program koji za uneti broj ispisuje koliko ima cifara.

.. activecode:: zadatak11
    :coach:
    
    # Dopuni

**Primer 1**:

**Ulaz**:  
12345  

**Izlaz**:  
Broj 12345 ima 5 cifara.  

**Objašnjenje izlaza**:  
Broj 12345 ima ukupno 5 cifara, što se dobija iterativnim brojanjem.

**Primer 2**:

**Ulaz**:  
100  

**Izlaz**:  
Broj 100 ima 3 cifre.  

**Objašnjenje izlaza**:  
Broj 100 sadrži ukupno 3 cifre.

.. learnmorenote:: Rešenje

    .. code-block:: python

        broj = int(input("Unesite broj: "))  # Učitavanje broja
        brojac = 0                           # Inicijalizacija brojača cifara
        while broj != 0:                     # Petlja traje dok ima cifara u broju
            broj //= 10                      # Uklanja poslednju cifru
            brojac += 1                      # Uvećava brojač cifara
        print("Broj ima", brojac, "cifara.")  # Ispis rezultata


Zadatak 12
-----------

Napiši program koji ispisuje sve brojeve između 100 i 200 koji imaju bar dve cifre iste.

.. activecode:: zadatak12
    :coach:
    
    # Dopuni

**Primer 1**:

**Ulaz**:  
(Nema dodatnog unosa, analiziraju se brojevi između 100 i 200.)  

**Izlaz**:  
101 110 111 112 113 ...  

**Objašnjenje izlaza**:  
Brojevi poput 101 imaju dve iste cifre (1 se ponavlja), dok broj 123 nema.

.. learnmorenote:: Rešenje

    .. code-block:: python

        for broj in range(100, 200):       # Iteracija kroz brojeve od 100 do 200
            cifra1 = broj // 100           # Prva cifra
            cifra2 = (broj // 10) % 10     # Druga cifra
            cifra3 = broj % 10             # Treća cifra
            if (cifra1 == cifra2 or cifra1 == cifra3 or cifra2 == cifra3):  # Provera jednakosti cifara
                print(broj, end=" ")       # Ispis brojeva


Zadatak 13
-----------

Napiši program koji računa najmanji i najveći broj od unetih 5 brojeva.

.. activecode:: zadatak13
    :coach:
    
    # Dopuni

**Primer 1**:

**Ulaz**:  
5 10 15 2 8  

**Izlaz**:  
Najmanji broj je 2, a najveći broj je 15.  

**Objašnjenje izlaza**:  
Među unetim brojevima, 2 je najmanji, a 15 najveći.

**Primer 2**:

**Ulaz**:  
50 40 30 20 10  

**Izlaz**:  
Najmanji broj je 10, a najveći broj je 50.  

**Objašnjenje izlaza**:  
Brojevi su već sortirani, ali program računa minimum i maksimum.

.. learnmorenote:: Rešenje

    .. code-block:: python

        prvi_broj = int(input("Unesite broj: "))  # Učitavanje prvog broja
        najmanji = prvi_broj         # Inicijalizacija najmanjeg broja na prvi broj
        najveci = prvi_broj         # Inicijalizacija najvećeg broja na prvi broj
        for _ in range(4):              # Iteracija za unos 5 brojeva
            broj = int(input("Unesite broj: "))
            if broj < najmanji:         # Provera za najmanji broj
                najmanji = broj
            if broj > najveci:          # Provera za najveći broj
                najveci = broj
        print(f"Najmanji broj je {najmanji}, a najveći broj je {najveci}.")  # Ispis rezultata


Zadatak 14
-----------

Napiši program koji proverava da li su uneti brojevi u rastućem poretku.

.. activecode:: zadatak14
    :coach:
    
    # Dopuni

**Primer 1**:

**Ulaz**:  
1 2 3 4 5  

**Izlaz**:  
Brojevi su u rastućem poretku.  

**Objašnjenje izlaza**:  
Svaki naredni broj je veći od prethodnog, što znači da su u rastućem poretku.

**Primer 2**:

**Ulaz**:  
1 3 2 4 5  

**Izlaz**:  
Brojevi nisu u rastućem poretku.  

**Objašnjenje izlaza**:  
Broj 2 nije veći od broja 3, što prekida rastući poredak.

.. learnmorenote:: Rešenje

    .. code-block:: python

        prethodni = int(input("Unesite prvi broj: "))  # Učitavanje prvog broja
        rastuci = True                                 # Pretpostavljamo da je poredak rastući
        for _ in range(4):                            # Petlja za unos narednih 4 brojeva
            trenutni = int(input("Unesite sledeći broj: "))
            if trenutni <= prethodni:                 # Provera da li je trenutni broj manji ili jednak prethodnom
                rastuci = False                       # Ako nije rastući, prekida se uslov
            prethodni = trenutni                      # Ažurira prethodni broj
        if rastuci:
            print("Brojevi su u rastućem poretku.")    # Ispis ako su rastući
        else:
            print("Brojevi nisu u rastućem poretku.")  # Ispis ako nisu rastući


Zadatak 15
-----------

Napiši program koji ispisuje sve brojeve između uneta dva broja koji su prosti.

.. activecode:: zadatak15
    :coach:
    
    # Dopuni

**Primer 1**:

**Ulaz**:  
10  
20  

**Izlaz**:  
11 13 17 19  

**Objašnjenje izlaza**:  
U opsegu od 10 do 20 prosti brojevi su oni koji su deljivi samo sa 1 i sa samim sobom.

**Primer 2**:

**Ulaz**:  
5  
15  

**Izlaz**:  
5 7 11 13  

**Objašnjenje izlaza**:  
U opsegu od 5 do 15, prosti brojevi su 5, 7, 11 i 13.

.. learnmorenote:: Rešenje

    .. code-block:: python

        donja_granica = int(input("Unesite donju granicu: "))   # Učitavanje donje granice
        gornja_granica = int(input("Unesite gornju granicu: ")) # Učitavanje gornje granice
        for broj in range(donja_granica, gornja_granica + 1):  # Iteracija kroz opseg
            prost = True                                       # Pretpostavljamo da je broj prost
            if broj > 1:                                       # Broj mora biti veći od 1 da bi bio prost
                for i in range(2, int(broj**0.5) + 1):         # Provera delilaca do kvadratnog korena
                    if broj % i == 0:
                        prost = False                          # Ako je deljiv, nije prost
                        break
                if prost:
                    print(broj, end=" ")                       # Ispis prostog broja


Zadatak 16
-----------

Napiši program koji ispisuje sve brojeve od 1 do unetog broja koji imaju tačno 3 delioca.

.. activecode:: zadatak16
    :coach:
    
    # Dopuni

**Primer 1**:

**Ulaz**:  
20  

**Izlaz**:  
4 9 16  

**Objašnjenje izlaza**:  
Brojevi 4, 9 i 16 su kvadrati prostih brojeva i imaju tačno 3 delioca.

**Primer 2**:

**Ulaz**:  
30  

**Izlaz**:  
4 9 16 25  

**Objašnjenje izlaza**:  
Dodaje se 25, jer je i on kvadrat prostog broja.

.. learnmorenote:: Rešenje

    .. code-block:: python

        n = int(input("Unesite broj: "))          # Učitavanje broja
        for broj in range(1, n + 1):             # Iteracija kroz brojeve do n
            delioci = 0                          # Brojač delilaca
            for i in range(1, broj + 1):         # Provera svih potencijalnih delilaca
                if broj % i == 0:
                    delioci += 1                # Uvećanje broja delilaca
            if delioci == 3:                    # Provera da li broj ima tačno 3 delioca
                print(broj, end=" ")            # Ispis brojeva


Zadatak 17
-----------

Napiši program koji proverava da li se uneti brojevi menjaju između parnih i neparnih.

.. activecode:: zadatak17
    :coach:
    
    # Dopuni

**Primer 1**:

**Ulaz**:  
1 2 3 4 5  

**Izlaz**:  
Brojevi se ne menjaju između parnih i neparnih.  

**Objašnjenje izlaza**:  
Parni i neparni brojevi se ne smenjuju redom, već dolaze u grupama.

**Primer 2**:

**Ulaz**:  
1 2 3 4 3 2  

**Izlaz**:  
Brojevi se menjaju između parnih i neparnih.  

**Objašnjenje izlaza**:  
Svaki naredni broj menja parnost.

.. learnmorenote:: Rešenje

    .. code-block:: python

        prethodni = int(input("Unesite prvi broj: "))  # Učitavanje prvog broja
        smenjuju_se = True                            # Pretpostavka da se smenjuju
        for _ in range(4):                            # Petlja za unos 4 naredna broja
            trenutni = int(input("Unesite sledeći broj: "))
            if (prethodni % 2 == trenutni % 2):       # Provera iste parnosti
                smenjuju_se = False                  # Ako su iste parnosti, prekid uslova
            prethodni = trenutni                     # Ažuriranje prethodnog broja
        if smenjuju_se:
            print("Brojevi se menjaju između parnih i neparnih.")  # Ispis ako se smenjuju
        else:
            print("Brojevi se ne menjaju između parnih i neparnih.")  # Ispis ako se ne smenjuju


Zadatak 18
-----------

Napiši program koji za uneti broj ispisuje da li ima sve jedinstvene cifre.

.. activecode:: zadatak18
    :coach:
    
    # Dopuni

**Primer 1**:

**Ulaz**:  
12345  

**Izlaz**:  
Broj 12345 ima sve jedinstvene cifre.  

**Objašnjenje izlaza**:  
Svaka cifra u broju 12345 pojavljuje se tačno jednom.

**Primer 2**:

**Ulaz**:  
11234  

**Izlaz**:  
Broj 11234 nema sve jedinstvene cifre.  

**Objašnjenje izlaza**:  
Cifra 1 pojavljuje se dva puta.

.. learnmorenote:: Rešenje

    .. code-block:: python

        # Unos broja od korisnika
        broj = int(input("Unesite broj: "))

        # Kopija broja za izdvajanje cifara
        originalni_broj = broj
        jedinstvene = True

        # Provera svake cifre sa svim ostalim ciframa
        while broj > 0:
            trenutna_cifra = broj % 10
            privremeni_broj = originalni_broj // 10  # Počinje nakon trenutne cifre

            while privremeni_broj > 0:
                poredna_cifra = privremeni_broj % 10
                if trenutna_cifra == poredna_cifra:
                    jedinstvene = False
                    break
                privremeni_broj //= 10

            if not jedinstvene:
                break

            broj //= 10

        # Ispis rezultata
        if jedinstvene:
            print("Broj ima sve jedinstvene cifre.")
        else:
            print("Broj nema sve jedinstvene cifre.")

