﻿Лабораторна робота №2

Стадник Г.О., Ковальов К.В. група; 536ст

Мета: Ознайомитись із сервісом GCP, створити віртуальні машини двома методами та порівняти процес.

Завдання:

1\. Створити GCP аккаунт https://cloud.google.com/

2\. Ознайомитися з інтерфейсом

3\. Створити проект 

4\. У проекті створити віртуальну машину використовуючи графічний інтерфейс

5\. Створити віртуальну машину за допомогою утиліти gcloud

6\. Порівняти процес створення, назвати переваги і недоліки обох способів

7\. Записати висновки

8\. Оформити звіт і зберегти його в Git Hub репозиторії

Виконання:

Реєструємося у клауді, налаштовуємо всі необхідні компоненти, робимо всі необхідні маніпуляції для цього, переходимо далі:

![](Aspose.Words.7116f279-dec3-43ef-a563-26d3d9c2a8a0.001.png)

Рисунок 1.1 - Інтерфейс

Створюємо новий проект, налаштовуємо характеристики, та вже в ньому створюємо віртуальну машину. Отриманий результат продемонстровано на рисунку 1.2. Для нашої демонстративної роботи обираємо найдешевше розташування та найменші оптимальні параметри віртуальної машини:

![](Aspose.Words.7116f279-dec3-43ef-a563-26d3d9c2a8a0.002.png)

Рисунок 1.2 — Створення та налаштування VM

![](Aspose.Words.7116f279-dec3-43ef-a563-26d3d9c2a8a0.003.png)

Рисунок 1.3 — Виклик SSH консолі


![](Aspose.Words.7116f279-dec3-43ef-a563-26d3d9c2a8a0.004.png)

Рисунок 1.4 — Консоль SSH

```
sudo adduser [NAME USER]
```

![](Aspose.Words.7116f279-dec3-43ef-a563-26d3d9c2a8a0.005.png)

Рисунок 1.5 — Налаштування та перевірка команд SSH консолі

Команди:

```
free -h
```

```
df -h
```

```
ifconfig
```

![](Aspose.Words.7116f279-dec3-43ef-a563-26d3d9c2a8a0.006.png)

Рисунок 1.6 — Activate Cloud Shell 


Далі, виконуємо команду:

```
gcloud compute zones list
```

Після чого бачимо опцію зон ліст, дуже великий список:

![](Aspose.Words.7116f279-dec3-43ef-a563-26d3d9c2a8a0.007.png)

Рисунок 1.7 — Список зон

```
gcloud compute instances create [instance-2] [my-vm] —machine-type=[n1-standard-1] --image-project=[ubuntu-os-cloud] --image-family=[ubuntu-minimal-2204-lts] —zone=[us-east5]
```

Данною командою ми створюємо дві нові віртуальні машини:

Наступним етапом було генерація ключа та запуск двох машин. Отримано наступні результати:

![](Aspose.Words.7116f279-dec3-43ef-a563-26d3d9c2a8a0.008.png)

Рисунок 1.8 — Дві різні віртуальні машини

![](Aspose.Words.7116f279-dec3-43ef-a563-26d3d9c2a8a0.009.png)

Рисунок 1.9 — SSH консолі двох віртуальних машин

Висновки: 

В лабораторній роботі 2, ми ознайомились з  сервісом Google Cloud, далі двома способами було створено по віртуальні машини. За результатами виконання можна казати, що дана середа є наочною та відносно простою для використання, що робить її незамінною для даного роду задач. Але треба знати англійську мову, бо весь інтерфейс лише на англійській, французькій, німецькій та азіатських мовах. Якщо порівняти два способи створення, то можна сказати що ручне створення дає більш детально підібрати налаштування, і такий підхід забирає багато часу, через консоль однією командою можна створити стільки віртуальних машин скільки потрібно, і такий підхід забирає менше часу.


