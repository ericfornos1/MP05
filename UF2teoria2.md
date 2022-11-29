# Disseny de les proves i tipus de proves:

**Després de dur a terme un pla de proves** el següent pas es dissenyar les proves.

El disseny consisteix en establir els **casos de prova**.

## Cas de prova:

Un cas de prova defineix com es portaran a terme les proves, especificant, entre d’altres: 
- El tipus de proves. 
- Les entrades de les proves.
- Els resultats esperats.
- Les condicions sota les quals s’hauran de desenvolupar.

Serveixen per a **identificar els errors** que hi ha al programari.

**Segueixen un cicle de vida clàssic:**
- Definició dels casos de prova.
- Creació dels casos de prova.
- Selecció dels valors per als tests.
- Execució dels casos de prova.
- Comparació dels resultats obtinguts amb els resultats esperats.

**Els casos de prova hauríen d'implementar:**
- Identificador del cas de prova.
- Mòdul o funció a provar.
- Descripció del cas de prova detallat.
- Entorn que s’haurà de complir abans de l’execució del cas de prova.
- Dades necessàries per al cas, especificant els seus valors.
- Tasques que executarà el pla de proves i la seva seqüència.
- Resultat esperat.
- Resultat obtingut.
- Observacions o comentaris després de l’execució.
- Responsable del cas de prova.
- Data d’execució.
- Estat (finalitzat, pendent, en procés).

## Proves de caixa blanca:

Les proves de caixa blanca serveixen per a provar el màxim % del codi que es vol testejar.

![image](https://user-images.githubusercontent.com/110727546/204605793-0e0efc35-9e15-446e-88db-338587a12242.png)

Per a fer una prova de caixa blanca **necessitem conèixer el codi** que estem testejant.

Permetran **recórrer tots els possibles camins del codi** i veure què succeeix en cada cas possible. 

Es provarà què ocorre amb les **condicions i els bucles** que s’executen. 

Les proves es duran a terme amb **dades que garanteixin que han tingut lloc totes les combinacions** possibles.

### Complexitat ciclomàtica:

Per saber quantes proves hem de fer a un codi utilitzem un número anomenat complexitat ciclomàtica.

Aquest nom el va el posar el matemàtic Thomas J. McCabe al nombre de camins independents d'un diagrama de flux i va proposar la fórmula següent per calcular-lo.

```
Complexitat ciclomàtica = nombre de branques – nombre de nodes + 2
```
Tenint en compte com crear les branques i els nodes de la representació del nostre programa:

![image](https://user-images.githubusercontent.com/110727546/204613744-508c210c-7181-4540-9c0e-535f7191b818.png)

#### Activitat 1:

A l'exemple següent quina serà la CC?

![image](https://user-images.githubusercontent.com/110727546/204612433-f3fb7e69-8db8-4645-8c6c-672d29e274c9.png)

També podem utilitzar la fórmula:

```
Complexitat ciclomàtica = nombre de sentencies condicionals + 1
```

#### Activitat 2:

Tenint en compte els diagrames de flux vistos a classe, quina serà la CC d'aquest programa?

![image](https://user-images.githubusercontent.com/110727546/204614214-5a73d89b-66e4-4f1b-8e4a-bbfd6e1885b6.png)

El diagrama anterior correspon al pseudocodi següent:

![image](https://user-images.githubusercontent.com/110727546/204614333-30ccb3e7-00f7-45fe-b0aa-332847c1fcd5.png)

Segons la Complexitat Ciclomàtica del nostre codi ens trobarem davant d'un codi definit a la següent taula:

![image](https://user-images.githubusercontent.com/110727546/204614806-25949541-7ea2-498c-89b0-65336bf32dee.png)

#### Resolució de les activitats:

- Activitat 1: CC = 8 - 7 + 2 = 3
- Activitat 2: CC = 1 + 1 = 2

### Un cop tenim la Complexitat Ciclomàtica què fem?

La CC ens serveix per determinar **quants casos de prova** necessitem per testejar tot el codi.

En quant tenim la complexitat ciclomàtica:

- Definim el número de camins independents que ha de seguir cada test (seran tants com la CC).
- Determinar els casos de prova que ens permeten executar els camins anteriors i codificar-los.
- Executar cada cas de prova i comprovar que la sortida és l'esperada.

#### Exemple:

Utilitzant el codi anterior:

![image](https://user-images.githubusercontent.com/110727546/204614333-30ccb3e7-00f7-45fe-b0aa-332847c1fcd5.png)

Tenim una complexitat ciclomàtica de valor 2, això vol dir que necessitem crear dues proves per testejar el codi.

1. Un cas que faci que B > C es compleixi. B = 1 i C = 0
2. Un cas que faci que B > C NO es compleixi. B = 1 i C = 1

Per al primer cas tenim que la sortida serà 1 , 1, 0.

Per al segon cas tenim que la sortida serà 1, 1, 1.

Amb aquests dos únics casos haurem provat tots els camins possibles dins el nostre codi.



