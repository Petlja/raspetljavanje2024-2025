Вежбе
======

.. ZADATAK 1
.. questionnote:: 

    Напиши програм који израчунава производ свих бројева од 1 до унетог броја.

.. activecode:: petlje_vezba1
    :coach:

    n = int(input("Unesite broj: "))
    proizvod = 1

    # DOPUNI

    print(proizvod)

Како бисмо решили овај проблем потребно је да прођемо кроз све бројеве од 1 до унетог броја и да их помножимо. 
Ово успевамо успевамо кроз петљу која пролази кроз све потребне бројеве и множи их са тренутним производом.

.. infonote::
    **МАТЕМАТИЧКА ЗАНИМЉИВОСТ** 

    Производ свих бројева од 1 до датог броја се зове **факторијел** тог броја и обележава се са`n!`.

    .. math::
            
            n! = 1 \cdot 2 \cdot 3 \cdot \ldots \cdot n


.. ZADATAK 2
.. questionnote:: 

    Напиши програм који исписује све бројеве од 1 до унетог који су дељиви са 3 или 5 али изостави оне који су делјиви са оба броја.

.. activecode:: petlje_vezba2
    :coach:

    n = int(input())
    for i in range(n):
        # DOPUNI

У прошлој лекцији научили смо како проверавамо дељивост броја са неким бројем. 
Сада је потребно да се тај поступак примени на све бројеве од 1 до унетог броја.


.. ZADATAK 3
.. questionnote:: 

    Napiši program koji ispisuje broj cifata unetog broja.

.. activecode:: petlje_vezba3
    :coach:

    broj = int(input("Unesi broj: "))
    count = 0
    
    while broj != 0:
        broj = # DOPUNI
        count += 1
    
    print("Broj cifara je:", count)


.. ZADATAK 4
.. questionnote:: 

    Напиши програм који израчунава збир цифара унетог броја.

.. activecode:: petlje_vezba4
    :coach:

    broj = int(input("Unesi broj: "))
    zbir = 0
    while broj != 0:
        # DOPUNI
    print("Zbir cifara je:", zbir)


.. ZADATAK 5
.. questionnote:: 

    Напиши програм који проверава да ли је број прост.

.. activecode:: petlje_vezba5
    :coach:

    broj = int(input("Unesi broj: "))
    if broj < 2:
        print("Nije prost")
    else:
        i = 2
        broj_je_prost = False
        for i in range(# DOPUNI):
            if # DOPUNI:
                broj_je_prost = True
                break

    if broj_je_prost:
        print("Prost")
    else:
        print("Nije prost")

Да би број био прост потребно је да није дељив ни са једним бројем сем са 1 и са самим собом. 
Да бисмо поверили да ли је број прост потребно је да проверимо његову дељивост са свим бројевима пре нјега 
(јер сигурно није длејив са бројевима већим од самог себе).

Ако детектујемо да је број дељив са неким другим бројем нема потребе да далје проверавамо јер већ знамо да број није прост.


.. ZADATAK 6
.. questionnote:: 

    Напиши програм који учитава број`n` и исписује првих n чланова Фибоначијевог низа.

.. activecode:: petlje_vezba6
    :coach:

    n = int(input("Unesi broj n: "))
    a, b = 0, 1
    for _ in range(n):
        print(a)
        # DOPUNI: Ažuriraj a i b

.. infonote::

    Fibonacijev niz je niz brojeva gde je svaki broj jednak zbiru prethodna dva broja. Prva dva člana niza su 0 i 1.
    Prvih nekoliko članova niza su: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, ...

    .. math::

        F_0 = 0, F_1 = 1\\
        F_n = F_{n-1} + F_{n-2}\\

    .. math::

            \begin{align*}    
            F_2 &= F_1 + F_0 = 1 + 0 = 1\\
            F_3 &= F_2 + F_1 = 1 + 1 = 2\\
            F_4 &= F_3 + F_2 = 2 + 1 = 3\\
            F_5 &= F_4 + F_3 = 3 + 2 = 5\\
            F_6 &= F_5 + F_4 = 5 + 3 = 8\\
            F_7 &= F_6 + F_5 = 8 + 5 = 13\\
            &\ldots
            \end{align*}
        

.. ZADATAK 7
.. questionnote:: 

    Напиши програм који исписује табелу множења од 1 до 5 користећи угњеждене `for` петље.

.. activecode:: petlje_vezba7
    :coach:

    for i in range(1, 6):
        for j in range(1, 6):
            # DOPUNI

.. infonote::

    Угњеждене петље су петље које се налазе једна унутар друге. 
    У овом случају, унутрашња петља се извршава за сваки члан унутрашње петље, а затим се извршава спољашња петља.

    .. math::

        \begin{align*}
        1 \times 1 &= 1 & 1 \times 2 &= 2 & 1 \times 3 &= 3 & 1 \times 4 &= 4 & 1 \times 5 &= 5\\
        2 \times 1 &= 2 & 2 \times 2 &= 4 & 2 \times 3 &= 6 & 2 \times 4 &= 8 & 2 \times 5 &= 10\\
        3 \times 1 &= 3 & 3 \times 2 &= 6 & 3 \times 3 &= 9 & 3 \times 4 &= 12 & 3 \times 5 &= 15\\
        4 \times 1 &= 4 & 4 \times 2 &= 8 & 4 \times 3 &= 12 & 4 \times 4 &= 16 & 4 \times 5 &= 20\\
        5 \times 1 &= 5 & 5 \times 2 &= 10 & 5 \times 3 &= 15 & 5 \times 4 &= 20 & 5 \times 5 &= 25\\
        \end{align*}


.. ZADATAK 8
.. questionnote:: 

    Написати програм који учитава број `n`, а затим учитава `n` бројева и исписује њихов збир.

.. activecode:: petlje_vezba8
    :coach:

    n = int(input("Unesi broj n: "))
    zbir = 0

    for _ in range(n):
        broj = int(input("Unesi broj: "))
        # DOPUNI
        
    print("Zbir unetih brojeva je:", zbir)

У овом примеру видимо како можемо користити петље за унос података када нам није унапред 
познато колико података корисник жели да унесе. Када користимо петље за уношење података 
неопходно је да постоји услов за завршетак уноса података. У овом случају, корисник уноси 
`н` бројева и када унесе свих `н` бројева програм завршава са радом.


.. ZADATAK 9
.. questionnote:: 

    Направити програм који тражи од корисника да унесе број све док збир свих унетих бројева не пређе 100.

.. activecode:: petlje_vezba9
    :coach:

    zbir = 0
    while zbir < 100:
        # DOPUNI

У овом примеру услов за прекид уношења је да збир свих унетих бројева пређе 100. 
Често се за прекид уноса користи кључна реч или број, на пример: ако корисник унесе -1, 
програм ће прекинути унос и завршити са радом.


.. ZADATAK 10
.. questionnote:: 
  
   Напиши програм који тражи од корисника да уноси бројеве док не унесе реч 'стоп'. 
    На крају, програм треба да испише средњу вредност унетих бројева користећи wхиле петљу.
.. activecode:: petlje_vezba10
    :coach:

    zbir = 0
    count = 0
    while True:
        unos = input("Unesi broj ili 'stop' za kraj: ")
        if unos.lower() == 'stop':
            break
        # DOPUNI
    srednja_vrednost = # DOPUNI
    print("Srednja vrednost je:", srednja_vrednost)

У овом примеру користи се кључна реч `stop` за прекид уноса.

|

Када се користи кључна реч за прекид уноса потребно је проверити да ли је унети податак 
податак за прекид уноса пре било какве обраде. Из овог разлога у задатку се не конвертује 
унос у `int` тип податка већ се проверава да ли је унос `stop`. Након провере да ли је унос 
потребно је конвертовати податак у `int` тип податка ради даље обраде.
    

.. ZADATAK 11
.. questionnote:: 

    Написати програм који униси н бројева и исписује најмањи број.

.. activecode:: petlje_vezba11
    :coach:

    n = int(input("Unesi broj n: "))
    min = int(input("Unesi broj: "))
    for _ in range(n-1):
        broj = int(input("Unesi broj: "))
        # DOPUNI

    print("Najmanji broj je:", min)

.. infonote::

    **САВЕТ ПРИ РАДУ**

    Када год се унесе нови број потребно је проверити да ли је он најмањи број до сада унет. 
    Међутим, није неопходно поредити нови број са свим, до сада унетим, бројевима. Ако је нови број 
    мањи од најмањег броја међу до сада унетим бројевима, онда је нови број најмањи број.

    |

    Ово значи да није потребно да памтимо све унете бројеве већ само најмањи, ако је нови број мањи од најмањег 
    тај број постаје нови најмањи број.

    |

    Добра аналогија за обај пример је следећи теоретски случај:

    Добили сте дугачак папир са 1000 бројева и имате задатак да нађете најмањи број. 
    Како бисте то урадили без помоћи било коаквог рачунара?
