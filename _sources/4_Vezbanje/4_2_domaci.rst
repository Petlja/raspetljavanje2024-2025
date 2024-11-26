.. Zadatak 1: Prikupljanje donacija
.. questionnote::

    **Priča:** Organizacija prikuplja donacije za izgradnju škole. Potrebno je zabeležiti koliko donatora je dalo više od proseka, kao i ukupnu sumu svih donacija.

    **Zadatak:** 
    Unesi iznose donacija (npr. 100, 200, 300, 400, 500). Izračunaj:
    
    1. Ukupan iznos donacija.
    2. Prosečan iznos donacija.
    3. Broj donatora koji su dali više od proseka.

.. activecode:: donacije
    :coach:

    # DOPUNI

**Primer 1**:

**Ulaz**:
100, 200, 300, 400, 500

**Izlaz**:
Ukupan iznos donacija: 1500  
Prosečan iznos donacija: 300.0  
Broj donatora koji su dali više od proseka: 2  

**Primer 2**:

**Ulaz**:
50, 150, 250, 350, 450  

**Izlaz**:
Ukupan iznos donacija: 1250  
Prosečan iznos donacija: 250.0  
Broj donatora koji su dali više od proseka: 2  

**Primer 3**:

**Ulaz**:
500, 600, 700, 800, 900  

**Izlaz**:
Ukupan iznos donacija: 3500  
Prosečan iznos donacija: 700.0  
Broj donatora koji su dali više od proseka: 2  

.. learnmorenote:: **Rešenje**

    .. code-block:: python

        donacije = [100, 200, 300, 400, 500]
        ukupno = sum(donacije)  # Izračunavanje ukupne sume donacija
        prosek = ukupno / len(donacije)  # Prosečna donacija
        iznad_proseka = sum(1 for d in donacije if d > prosek)  # Donatori iznad proseka

        print("Ukupan iznos donacija:", ukupno)
        print("Prosečan iznos donacija:", prosek)
        print("Broj donatora koji su dali više od proseka:", iznad_proseka)


.. Zadatak 2: Određivanje pobednika
.. questionnote::

    **Priča:** U trci je učestvovalo nekoliko učesnika. Njihovo vreme završetka je zapisano u sekundama.

    **Zadatak:** 
    Unesi vremena završetka (npr. 12.3, 11.5, 13.7, 10.9, 11.1). Pronađi:
    
    1. Ko je pobedio.
    2. Koliko je iznosilo pobedničko vreme.

.. activecode:: odredjivanje_pobednika
    :coach:

    # DOPUNI

**Primer 1**:

**Ulaz**:
12.3, 11.5, 13.7, 10.9, 11.1  

**Izlaz**:
Pobednik je učesnik broj: 4  
Njegovo vreme je: 10.9 sekundi  

**Primer 2**:

**Ulaz**:
15.2, 14.8, 15.6, 14.5, 15.0  

**Izlaz**:
Pobednik je učesnik broj: 4  
Njegovo vreme je: 14.5 sekundi  

**Primer 3**:

**Ulaz**:
9.8, 10.1, 9.5, 10.2, 10.0  

**Izlaz**:
Pobednik je učesnik broj: 3  
Njegovo vreme je: 9.5 sekundi  

.. learnmorenote:: **Rešenje**

    .. code-block:: python

        vremena = [12.3, 11.5, 13.7, 10.9, 11.1]
        pobednicko_vreme = min(vremena)  # Najmanje vreme
        pobednik = vremena.index(pobednicko_vreme) + 1  # Pronalaženje pobednika (indeks + 1)

        print("Pobednik je učesnik broj:", pobednik)
        print("Njegovo vreme je:", pobednicko_vreme, "sekundi")


.. Zadatak 3: Магична врата
.. questionnote::

    **Опис:** 
    У древном храму постоје магична врата која се отварају само ако унесеш бројеве `a` и `b` тако да је збир њихових цифара једнак `k`.

    **Задатак:** 
    Напиши програм који проверава све парове бројева од 1 до `n` и исписује оне који испуњавају услов.

    **Улаз:**
    - `n`: Максимална вредност броја.
    - `k`: Циљни збир цифара.

    **Излаз:**
    Сви парови бројева `(a, b)` који испуњавају услов.

.. activecode:: magicna_vrata
    :coach:

    # DOPUNI

**Primer 1**:

**Ulaz**:
n = 10, k = 5  

**Izlaz**:
(1, 4)  
(2, 3)  

**Primer 2**:

**Ulaz**:
n = 15, k = 6  

**Izlaz**:
(3, 3)  
(4, 2)  
(5, 1)  

**Primer 3**:

**Ulaz**:
n = 20, k = 7  

**Izlaz**:
(3, 4)  
(4, 3)  
(5, 2)  
(6, 1)  

.. learnmorenote:: **Rešenje**

    .. code-block:: python

        def zbir_cifara(broj):
            zbir = 0
            while broj > 0:
                zbir += broj % 10
                broj //= 10
            return zbir

        n = 50  # Primer: Maksimalna vrednost
        k = 5   # Primer: Ciljni zbroj

        for a in range(1, n + 1):
            for b in range(1, n + 1):
                if zbir_cifara(a) + zbir_cifara(b) == k:
                    print(f"({a}, {b})")


.. Zadatak 4: Ротирање стринга
.. questionnote::

    **Опис:** 
    Дат је стринг `S` и број `K`. Напиши програм који ротира сваки карактер у стрингу `K` позиција у азбуци. Ако `K` пређе крај азбуке, наставља се од почетка.

    **Пример:** 
    - Ако је `S="abc"` и `K=3`, излаз би био `"def"`.

    **Улаз:**
    - `S`: Стринг.
    - `K`: Број за ротирање.

    **Излаз:** 
    Шифровани стринг.

.. activecode:: rotacija_stringa
    :coach:

    # DOPUNI

**Primer 1**:

**Ulaz**:
S = "abc", K = 3  

**Izlaz**:
"def"  

**Primer 2**:

**Ulaz**:
S = "xyz", K = 2  

**Izlaz**:
"zab"  

**Primer 3**:

**Ulaz**:
S = "python", K = 5  

**Izlaz**:
"udymts"  

.. learnmorenote:: **Rešenje**

    .. code-block:: python

        S = "abc"  # Primer: početni string
        K = 3      # Primer: broj rotacija

        rezultat = ""
        for karakter in S:
            nova_pozicija = (ord(karakter) - ord('a') + K) % 26 + ord('a')
            rezultat += chr(nova_pozicija)

        print("Šifrovani string je:", rezultat)
