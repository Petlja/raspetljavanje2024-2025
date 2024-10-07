Гуглање
=====================

**Debagovanje putem Guglanja**

Kada pišemo programe, ponekad naiđemo na greške koje ne možemo lako da rešimo. U takvim situacijama, često možemo dobiti pomoć od interneta, posebno putem pretrage na Guglu. U ovoj lekciji, naučićemo kako da koristimo Gugla za debagovanje naših programa.

--

**Zašto guglanje?**

Guglanje može biti veoma korisno jer:

1. **Pristup ogromnom znanju**: Na internetu postoji mnogo članaka, vodiča i foruma gde su ljudi već razgovarali o sličnim problemima.
2. **Brzo pronalaženje rešenja**: Umesto da trošite vreme razmišljajući o grešci, možete brzo pronaći rešenje putem pretrage.
3. **Razumevanje greške**: Čitanjem informacija o grešci možete bolje razumeti zašto se desila i kako da je izbegnete u budućnosti.

--

**Kako guglanje može pomoći?**

1. **Identifikujte grešku**: Kada dobijete poruku o grešci, zabeležite je. Na primer, ako dobijete grešku poput `IndexError: list index out of range`, to može biti vaša pretraga.
   
2. **Koristite specifične ključne reči**: Umesto da pretražujete samo reč "greška", koristite celokupnu poruku o grešci. To može uključivati i naziv programskog jezika, npr. "Pajton IndexError: list index out of range".

3. **Pretražujte uz pomoć foruma**: Web stranice poput Stack Overflow-a su odlične za postavljanje pitanja i pregledanje rešenja koja su drugi korisnici pronašli.

4. **Pogledajte tutorijale i blogove**: Mnogi programeri i edukatori postavljaju sadržaje koji objašnjavaju uobičajene greške i kako ih rešiti. Ovi resursi su često veoma korisni.

5. **Korišćenje dokumentacije za pajton**


--

**Primer: Kako koristiti guglanje za rešavanje greške**

Zamislimo da imamo sledeći kod koji izaziva grešku:

.. activecode:: guglanje1
   :coach:

   lista = [1, 2, 3]
   print(lista[3])


Kada pokrenemo ovaj kod, dobićemo grešku:

IndexError: list index out of range


**Koraci za guglanje:**

1. **Zabeležite grešku**: `IndexError: list index out of range`.
   
2. **Guglanje**: U pretragu upišite "Pajton IndexError: list index out of range".

3. **Pregledajte rezultate**: Prvi rezultati će vas obično odvesti na forume ili blogove gde drugi korisnici objašnjavaju ovu grešku.

4. **Pročitajte rešenja**: Naći ćete objašnjenja kao što su "Greška se dešava kada pokušate da pristupite indeksu koji ne postoji u listi. U ovom slučaju, lista ima 3 elementa, a indeksi su 0, 1, i 2."

5. **Ispravite grešku**: U ovom slučaju, možete promeniti kod tako da pristupite indeksu 2 umesto 3:

.. activecode:: guglanje2
   :coach:

   lista = [1, 2, 3]
   print(lista[2])  # Ovo će ispravno ispisati 3


--


Debugovanje putem guglanja je veština koja može značajno olakšati rešavanje problema u programima. Kroz pretragu poruka o greškama i korišćenje resursa dostupnih na internetu, možete brzo doći do rešenja i naučiti više o programiranju. Uvek zapamtite, niste sami – internet je tu da vam pomogne!