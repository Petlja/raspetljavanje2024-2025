Вежбање
========

Задатак 1
-----------

Направите програм који уноси температуре за сваки дан у недељи и рачуна:
  - просечну температуру,
  - највишу температуру,
  - најнижу температуру,
  - дане са температурама вишим од просека.

.. activecode:: v6_zadatak1
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
15 20 25 30 22 18 17  

**Излаз**:  
Просечна температура: 21.0  
Највиша температура: 30  
Најнижа температура: 15  
Дани са температурама вишим од просека: 3, 4, 5  

**Пример 2**:

**Улаз**:  
10 12 14 16 18 20 22  

**Излаз**:  
Просечна температура: 16.0  
Највиша температура: 22  
Најнижа температура: 10  
Дани са температурама вишим од просека: 5, 6, 7  


.. reveal:: 6_1_resenje_6_1_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос температура за сваки дан у недељи
        temperatures = []
        for i in range(7):
            temp = float(input(f"Унесите температуру за дан {i + 1}: "))
            temperatures.append(temp)

        # Израчунавање просечне температуре
        average_temp = sum(temperatures) / len(temperatures)

        # Највиша и најнижа температура
        highest_temp = max(temperatures)
        lowest_temp = min(temperatures)

        # Дани са температурама вишим од просека
        above_average_days = []
        for i, temp in enumerate(temperatures):
            if temp > average_temp:
                above_average_days.append(i + 1)

        # Испис резултата
        print("Просечна температура:", average_temp}")
        print("Највиша температура:", highest_temp}")
        print("Најнижа температура:", lowest_temp")
        print("Дани са температурама вишим од просека:", above_average_days)



Задатак 2
-----------

Дата је листа бројева и циљани број T. Потребно је пронаћи број из листе који је најближи циљаном броју. У случају када постоји више бројева са истом разликом од циљаног броја, вратити само први такав број.

.. activecode:: v6_zadatak2
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Листа: 10 22 30 45  
Циљани број: 28  

**Излаз**:  
Број најближи циљаној вредности је: 30  

**Објашњење излаза**:  
Број 30 је најближи броју 28.  

**Пример 2**:

**Улаз**:  
Листа: 100 200 300 400  
Циљани број: 250  

**Излаз**:  
Број најближи циљаној вредности је: 200  

**Објашњење излаза**:  
Број 200 је најближи броју 250.  

.. reveal:: 6_1_resenje_6_1_2
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос листе бројева
        numbers = []
        n = int(input("Колико бројева желите да унесете? "))
        for _ in range(n):
            num = int(input("Унесите број: "))
            numbers.append(num)

        # Унос циљног броја
        T = int(input("Унесите циљни број: "))

        # Проналажење броја најближег циљном броју
        closest = numbers[0]
        for num in numbers:
            if abs(num - T) < abs(closest - T):
                closest = 





Задатак 3
-----------

Дата је листа целих бројева и циљни број T. Потребно је пронаћи подниз (континуирани сегмент листе) чија је сума једнака T, или исписати да такав подниз не постоји.

.. activecode:: v6_zadatak3
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Листа: 1 2 3 7 5  
Циљни број: 12  

**Излаз**:  
Подниз са траженом сумом: 2 3 7  

**Објашњење излаза**:  
Сума подниза 2, 3, 7 је једнака 12.  

**Пример 2**:

**Улаз**:  
Листа: 1 2 3  
Циљни број: 6  

**Излаз**:  
Подниз са траженом сумом: 1 2 3  

**Објашњење излаза**:  
Сума целе листе даје тражени резултат.  

**Пример 3**:

**Улаз**:
Листа: 1 2 3 4 5
Циљни број: 11

**Излаз**:
Не постоји подниз са траженом сумом.

.. reveal:: 6_1_resenje_6_1_3
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос листе бројева
        numbers = []
        n = int(input("Колико бројева желите да унесете? "))
        for _ in range(n):
            num = int(input("Унесите број: "))
            numbers.append(num)

        # Унос циљног броја
        T = int(input("Унесите циљни број: "))

        # Проналажење подниза чија је сума једнака Т
        found = False
        for i in range(len(numbers)):
            current_sum = 0
            for j in range(i, len(numbers)):
                current_sum += numbers[j]
                if current_sum == T:
                    print(f"Пронађен подниз: {numbers[i:j+1]}")
                    found = True
                    break
            if found:
                break

        if not found:
            print("Не постоји подниз са задатом сумом.")


Задатак 4
-----------

Дата је листа бројева. Пронађите два елемента из листе чија разлика је највећа.

.. activecode:: v6_zadatak4
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Листа: 10 20 30 40  

**Излаз**:  
Два броја са највећом разликом су: 10 и 40  

**Објашњење излаза**:  
Разлика између 40 и 10 је највећа, износи 30.  

**Пример 2**:

**Улаз**:  
Листа: 1 9 3 15  

**Излаз**:  
Два броја са највећом разликом су: 1 и 15  

**Објашњење излаза**:  
Разлика између 15 и 1 је највећа, износи 14.  

.. reveal:: 6_1_resenje_6_1_4
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос листе бројева
        lista = list(map(int, input("Unesite brojeve liste odvojene razmakom: ").split()))

        # Најмањи и највећи број у листи
        najmanji = min(lista)
        najveci = max(lista)

        # Испис бројева са највећом разликом
        print("Dva broja sa najvećom razlikom su:", najmanji, "i", najveci)


Задатак 5
-----------

Дата је листа бројева. Креирајте нову листу где је сваки елемент једнак производу свих бројева у оригиналној листи осим тренутног.

.. activecode:: v6_zadatak5
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Листа: 1 2 3 4  

**Излаз**:  
Нова листа: 24 12 8 6  

**Објашњење излаза**:  
Сваки елемент нове листе израчунава се као производ свих бројева осим тренутног, нпр. за први елемент :math:`2 \times 3 \times 4 = 24`.  

**Пример 2**:

**Улаз**:  
Листа: 2 5 3  

**Излаз**:  
Нова листа: 15 6 10  

**Објашњење излаза**:  
Слично, сваки елемент се израчунава искључујући тренутни.  

.. reveal:: 6_1_resenje_6_1_45
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос листе бројева
        numbers = []
        n = int(input("Колико бројева желите да унесете? "))
        for _ in range(n):
            num = int(input("Унесите број: "))
            numbers.append(num)

        # Креирање нове листе где је сваки елемент производ свих бројева осим тренутног
        products = []
        for i in range(len(numbers)):
            product = 1
            for j in range(len(numbers)):
                if i != j:
                    product *= numbers[j]
            products.append(product)

        # Испис резултата
        print("Нова листа производа:", products)



Задатак 6
-----------

Дата је листа бројева и циљани број S. Пронађите све парове бројева из листе чији је збир једнак S.

.. activecode:: v6_zadatak6
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Листа: 1 2 3 4 5  
Циљани број: 6  

**Излаз**:  
Парови са збиром 6 су: (1, 5), (2, 4)  

**Објашњење излаза**:  
Сви парови бројева чији збир износи 6 су пронађени и исписани.  

**Пример 2**:

**Улаз**:  
Листа: 2 4 6 8  
Циљани број: 10  

**Излаз**:  
Парови са збиром 10 су: (2, 8), (4, 6)  

**Објашњење излаза**:  
Идентификовали смо парове бројева чији збир износи 10.  

.. reveal:: 6_1_resenje_6_1_5
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос листе бројева
        numbers = []
        n = int(input("Колико бројева желите да унесете? "))
        for _ in range(n):
            num = int(input("Унесите број: "))
            numbers.append(num)

        # Унос циљног збира
        S = int(input("Унесите циљни збир: "))

        # Проналажење свих парова са датим збиром
        pairs = []
        for i in range(len(numbers)):
            for j in range(i + 1, len(numbers)):
                if numbers[i] + numbers[j] == S:
                    pairs.append((numbers[i], numbers[j]))

        # Испис резултата
        if pairs:
            print("Парови са датим збиром:")
            for pair in pairs:
                print(pair)
        else:
            print("Нема парова са датим збиром.")



Задатак 7
-----------

Дата је листа бројева и број K. Ротирајте низ улево за K позиција.

.. activecode:: v6_zadatak7
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Листа: 1 2 3 4 5  
K: 2  

**Излаз**:  
Резултат: 3 4 5 1 2  

**Објашњење излаза**:  
Прва два елемента су премештена на крај листе.  

**Пример 2**:

**Улаз**:  
Листа: 10 20 30 40 50  
K: 3  

**Излаз**:  
Резултат: 40 50 10 20 30  

**Објашњење излаза**:  
Прва три елемента су ротирана на крај.  

.. reveal:: 6_1_resenje_6_1_6
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос листе бројева
        numbers = []
        n = int(input("Колико бројева желите да унесете? "))
        for _ in range(n):
            num = int(input("Унесите број: "))
            numbers.append(num)

        # Унос броја К за ротацију
        K = int(input("Унесите број К: "))

        # Ротација низа улево за К позиција
        rotated = numbers[K:] + numbers[:K]

        # Испис резултата
        print("Ротирани низ:", rotated)



Задатак 8
-----------

Напишите програм који проналази дужину најдужег растућег подниза из листе.

.. activecode:: v6_zadatak8
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Листа: 1 2 1 2 3  

**Излаз**:  
Најдужи растући подниз има дужину 3  

**Објашњење излаза**:  
Најдужи растући подниз је [1, 2, 3] и има дужину 3.  

**Пример 2**:

**Улаз**:  
Листа: 5 4 3 2 1  

**Излаз**:  
Најдужи растући подниз има дужину 1  

**Објашњење излаза**:  
Нема растућих поднизова дужих од једног елемента.  

.. reveal:: 6_1_resenje_6_1_7
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос листе бројева
        numbers = []
        n = int(input("Колико бројева желите да унесете? "))
        for _ in range(n):
            num = int(input("Унесите број: "))
            numbers.append(num)

        # Проналажење најдужег растућег подниза
        max_length = 0
        current_length = 1
        for i in range(1, len(numbers)):
            if numbers[i] > numbers[i - 1]:
                current_length += 1
            else:
                if current_length > max_length:
                    max_length = current_length
                current_length = 1

        # Проверити последњи низ
        if current_length > max_length:
            max_length = current_length

        # Испис резултата
        print("Најдужи растући подниз има дужину", max_length)



Задатак 9
-----------

Дата је листа температура измерена сваког сата током дана. Потребно је пронаћи све интервале (почетак и крај) где је температура константно опадала.

.. activecode:: v6_zadatak9
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Температуре: 30 29 28 31 30 29  

**Излаз**:  
Опадајући интервали: (0, 2), (3, 5)  

**Објашњење излаза**:  
Температуре опадају на интервалима индекса (0, 2) и (3, 5).  

**Пример 2**:

**Улаз**:  
Температуре: 25 24 23 23 22  

**Излаз**:  
Опадајући интервали: (0, 2), (3, 4)  

**Објашњење излаза**:  
Температуре опадају на интервалима индекса (0, 2) и (3, 4).  

.. reveal:: 6_1_resenje_6_1_8
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос листе температура
        temperatures = []
        n = int(input("Колико температура желите да унесете? "))
        for _ in range(n):
            temp = float(input("Унесите температуру: "))
            temperatures.append(temp)

        # Проналажење интервала са константним опадањем
        falling_intervals = []
        start = None
        for i in range(1, len(temperatures)):
            if temperatures[i] < temperatures[i - 1]:
                if start is None:
                    start = i - 1
            else:
                if start is not None:
                    falling_intervals.append((start, i - 1))
                    start = None

        # Ако је опадање трајало до краја
        if start is not None:
            falling_intervals.append((start, len(temperatures) - 1))

        # Испис резултата
        if falling_intervals:
            print("Интервали са константним опадањем:")
            for interval in falling_intervals:
                print("Од индекса", interval[0], "до", interval[1])
        else:
            print("Нема интервала са константним опадањем.")



Задатак 10
-----------

Напишите програм који проналази највећи производ било која три броја из листе.

.. activecode:: v6_zadatak10
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Листа: 1 10 2 6 5 3  

**Излаз**:  
Највећи производ је 300  

**Објашњење излаза**:  
Највећи производ је добијен од бројева 10, 6 и 5 (:math:`10 \times 6 \times 5 = 300`).  

**Пример 2**:

**Улаз**:  
Листа: -10 -10 5 2  

**Излаз**:  
Највећи производ је 500  

**Објашњење излаза**:  
Највећи производ је добијен од бројева -10, -10 и 5 (:math:`-10 \times -10 \times 5 = 500`).  

.. reveal:: 6_1_resenje_6_1_9
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос листе бројева
        numbers = []
        n = int(input("Колико бројева желите да унесете? "))
        for _ in range(n):
            num = int(input("Унесите број: "))
            numbers.append(num)

        # Проналажење највећег производа било која три броја
        max_product = float('-inf')
        for i in range(len(numbers)):
            for j in range(i + 1, len(numbers)):
                for k in range(j + 1, len(numbers)):
                    product = numbers[i] * numbers[j] * numbers[k]
                    if product > max_product:
                        max_product = product

        # Испис резултата
        print("Највећи производ три броја износи", max_product)



Задатак 11
-----------

Дата је листа која може садржавати узастопно понављање елемената. Напишите програм који замењује узастопне понављајуће елементе једним елементом и бројем понављања.

.. activecode:: v6_zadatak11
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Листа: A A B B B C A  

**Излаз**:  
Сажета листа: [(A, 2), (B, 3), (C, 1), (A, 1)]  

**Објашњење излаза**:  
Елементи се групишу са бројем њихових понављања.  

**Пример 2**:

**Улаз**:  
Листа: 1 1 1 2 3 3  

**Излаз**:  
Сажета листа: [(1, 3), (2, 1), (3, 2)]  

**Објашњење излаза**:  
Елементи се групишу са бројем њихових понављања.  

.. reveal:: 6_1_resenje_6_1_10
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос листе
        lista = input("Unesite elemente liste odvojene razmakom: ").split()

        # Сажимање листе
        sazeta_lista = []
        trenutni_element = lista[0]
        brojac = 1

        for i in range(1, len(lista)):
            if lista[i] == trenutni_element:
                brojac += 1
            else:
                sazeta_lista.append((trenutni_element, brojac))
                trenutni_element = lista[i]
                brojac = 1

        # Додавање последњег елемента
        sazeta_lista.append((trenutni_element, brojac))

        print("Sažeta lista:", sazeta_lista)


Задатак 12
-----------

Дата је листа бројева и два индекса L и R. Потребно је обрнути подниз између индекса L и R (укључујући оба).

.. activecode:: v6_zadatak12
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Листа: 1 2 3 4 5  
L: 1  
R: 3  

**Излаз**:  
Резултат: 1 4 3 2 5  

**Објашњење излаза**:  
Подниз између индекса 1 и 3 (2, 3, 4) је обрнут.  

**Пример 2**:

**Улаз**:  
Листа: 10 20 30 40 50  
L: 0  
R: 4  

**Излаз**:  
Резултат: 50 40 30 20 10  

**Објашњење излаза**:  
Цела листа је обрнута.  

.. reveal:: 6_1_resenje_6_1_11
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос листе бројева
        numbers = []
        n = int(input("Колико бројева желите да унесете? "))
        for _ in range(n):
            num = int(input("Унесите број: "))
            numbers.append(num)

        # Унос граница за обртање
        L = int(input("Унесите доњи индекс (L): "))
        R = int(input("Унесите горњи индекс (R): "))

        # Обртање подниза
        while L < R:
            numbers[L], numbers[R] = numbers[R], numbers[L]
            L += 1
            R -= 1

        # Испис резултата
        print("Листа након обртања:", numbers)



Задатак 13
-----------

Дата је листа бројева. Доминантна вредност је број који се појављује више од половине укупног броја елемената. Ако постоји доминантна вредност, исписати је, иначе исписати поруку да не постоји.

.. activecode:: v6_zadatak13
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Листа: 1 2 3 3 3  

**Излаз**:  
Доминантна вредност је 3.  

**Објашњење излаза**:  
Број 3 се појављује 3 пута, што је више од половине укупног броја елемената у листи (5).  

**Пример 2**:

**Улаз**:  
Листа: 1 2 2 3 3  

**Излаз**:  
Доминантна вредност не постоји.  

**Објашњење излаза**:  
Ниједан број се не појављује више од половине укупног броја елемената у листи.  

.. reveal:: 6_1_resenje_6_1_12
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос листе бројева
        numbers = []
        n = int(input("Колико бројева желите да унесете? "))
        for _ in range(n):
            num = int(input("Унесите број: "))
            numbers.append(num)

        # Проналажење доминирајуће вредности
        candidate = None
        count = 0

        # Проналажење кандидата
        for num in numbers:
            if count == 0:
                candidate = num
                count = 1
            elif num == candidate:
                count += 1
            else:
                count -= 1

        # Проверa да ли је кандидат заиста доминирајућа вредност
        occurrences = 0
        for num in numbers:
            if num == candidate:
                occurrences += 1

        if occurrences > len(numbers) // 2:
            print("Доминирајућа вредност је", candidate)
        else:
            print("Нема доминирајуће вредности.")



Задатак 14
-----------

Дата је листа бројева. Потребно је проверити да ли постоји индекс у листи такав да је збир елемената са леве стране једнак збиру елемената са десне стране.

.. activecode:: v6_zadatak14
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Листа: 1 7 3 6 5 6  

**Излаз**:  
Постоји индекс 3 где је збир леве и десне стране једнак.  

**Објашњење излаза**:  
Лева страна: :math:`1 + 7 + 3 = 11`, десна страна: :math:`5 + 6 = 11`.  

**Пример 2**:

**Улаз**:  
Листа: 1 2 3  

**Излаз**:  
Такав индекс не постоји.  

**Објашњење излаза**:  
Ниједан индекс не задовољава услов.  

.. reveal:: 6_1_resenje_6_1_13
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос листе бројева
        numbers = []
        n = int(input("Колико бројева желите да унесете? "))
        for _ in range(n):
            num = int(input("Унесите број: "))
            numbers.append(num)

        # Проналажење индекса равнотеже
        found = False
        for i in range(len(numbers)):
            left_sum = 0
            for j in range(i):
                left_sum += numbers[j]
            
            right_sum = 0
            for j in range(i + 1, len(numbers)):
                right_sum += numbers[j]
            
            if left_sum == right_sum:
                print("Индекс равнотеже је", i)
                found = True
                break

        if not found:
            print("Нема индекса равнотеже.")

