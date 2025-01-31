Activitat Diagrama:
---
Utilitzarem Lucid per crear els diagrames de classes següents:


persona.

llibre.

vehicle.

ordinador.

Penseu els seus atributs i operacions així com la visibilitat dels mateixos.

![1](https://user-images.githubusercontent.com/113585897/223164017-eaf00726-b1ef-45dd-8860-f22524339e0a.PNG)


Activitats de Recerca:
---

Cerca per Internet i respon a aquestes preguntes.

Buscar quines són les principals versions de UML publicades fins la més actual i de quin any són.

versió 1.0 - 1997

versió 1.1 - 1997

versió 1.2 - 1999

versió 2.0 - 2005

versió 2.2 - 2009

versió 2.5.1 - 2017

**Qui va crear UML?**

Grady Booch

Ivar Jacobson

Jim Rumbaugh



**Què és Rational Rose?**

Una eina de disseny orientada a objectes que dona suport de modelatge visual. Permet representar un sistema gràficament. Funcionava sobre frameworks de desenvolupament com MVS.


**Què té que veure Rational Rose amb UML?**


Rational Rose utilitza UML per a modelar software.


**Quan va ser publicada UML per la International Organization for Standardization (ISO)?**


La versió 1.4.2 va ser publicada per la ISO l'any 2005.

**Què vol dir OMG?**

Object Management Group - estandaritzar el Object Modelling en totes les seves formes.


**Què té que veure OMG amb UML?**

OMG és responsable de mantindre UML des de que es va convertir en un estàndar.



**Composició:**

**Activitat cardinalitat i Associació**
---

Escrivim quines associacions poden tenir les següents classes, nom d'associació i cardinalitat:


**Cardinalitat:**
---

persona, DNI: Relació exactament un a exactament un (1:1)

persona, comics: Relació exactament un a diversos (1:*)

persona, tren: Relació un o més a un o més (1..:1..)

animal, persona: Relació exactament un a diversos (1:*)

persona, persona: Relació un o més a un o més (1..:1..)

persona, cotxe: Relació un o més a un o més (1..:1..)

persona, adreça: Relació opcional un a exactament un (0..1:1)

taxi, client: Relació exactament un a diversos (1:*)



**Nom d'associació:**

persona, DNI: Identificació

persona, comics: Col·lecciona

persona, tren: Viatja

animal, persona: Mascota

persona, persona: Coneix

persona, cotxe: Condueix

persona, adreça: Viu

taxi, client: Transporta




**Activitat Composició**
---

Utilitzarem Lucid per crear 5 relacions de composició:


1.
![Captura de pantalla de 2023-03-06 13-50-20](https://user-images.githubusercontent.com/113585897/223116777-5425f411-4962-424c-901c-0effd28cd623.png)

2.
![Captura de pantalla de 2023-03-06 13-52-18](https://user-images.githubusercontent.com/113585897/223116780-5cceb45e-9cc0-453e-91b3-34757794e02e.png)


3.
![Captura de pantalla de 2023-03-06 13-53-55](https://user-images.githubusercontent.com/113585897/223116782-985f4a50-1176-4bc7-80d1-e12fc4eb45dd.png)

4.
![Captura de pantalla de 2023-03-06 13-55-42](https://user-images.githubusercontent.com/113585897/223116783-99622d87-5730-4a8b-8e4a-5e10724493f5.png)


5.
![Captura de pantalla de 2023-03-06 13-57-05](https://user-images.githubusercontent.com/113585897/223116785-44e82e99-cc0c-449a-bbba-2b866467a584.png)

**Agregació**
---


Es tracta d'un cas especial d'associació entre dos o més objectes.

Un objecte anomenat base que podrà incloure l'altre tipus d'objectes, com si fos un contingut.

L'objecte base necessita de l'objecte inclòs per existir, però l'objecte inclòs, si desapareix l'objecte base segueix existint.

4 exemples de agregacions, (si l'objecte base desapareix, segueix existing)

![Captura de pantalla de 2023-03-15 08-56-02](https://user-images.githubusercontent.com/113585897/225243655-2d6e5625-5d49-46ce-a400-49edefd70db6.png)

**Classe associativa**
---

Hi ha vegades que una associació entre classes té propietats o mètodes propis, llavors aquesta es representa amb una línia discontinua unida a la línia d'associació.

La línia i la classe nova representen el mateix element conceptual de l'associació.

A l'exemple següent tenim una associació entre la classe estudiant i la classe assignatura, l'associació es diu està cursant i té la propietat pròpia nota.

![Captura de pantalla de 2023-03-15 09-47-28](https://user-images.githubusercontent.com/113585897/225256078-1b5bf621-973d-4997-848d-65de88abd321.png)

![Captura de pantalla de 2023-03-15 09-48-30](https://user-images.githubusercontent.com/113585897/225256083-6498049f-f7a2-486e-8028-71a639b050a4.png)

![Captura de pantalla de 2023-03-15 09-49-18](https://user-images.githubusercontent.com/113585897/225256086-caee8357-1f7b-4eb5-912a-61d8c173161c.png)



*Interfície (interface)**
---

La interfície és una classe abstracta que conté la declaració (i només la declaració) de les propietats i operacions que s'hauran d'implementar per una classe.


![Captura de pantalla de 2023-03-15 10-23-07](https://user-images.githubusercontent.com/113585897/225265320-3ff24a69-5c3c-4485-964d-ce20ec767744.png)
