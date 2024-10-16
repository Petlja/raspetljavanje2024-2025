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

    Написати програм који учитава број н, а затим учитава н бројева и исписује њихов збир.

.. activecode:: petlje_vezba8
    :coach:

    n = int(input("Unesi broj n: "))
    zbir = 0

    for _ in range(n):
        broj = int(input("Unesi broj: "))
        # DOPUNI
        
    print("Zbir unetih brojeva je:", zbir)


