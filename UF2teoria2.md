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

Segueixen un cicle de vida clàssic:
- Definició dels casos de prova.
- Creació dels casos de prova.
- Selecció dels valors per als tests.
- Execució dels casos de prova.
- Comparació dels resultats obtinguts amb els resultats esperats.

Els casos de prova hauríen d'implementar:
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

Per a fer una prova de caixa blanca necessitem conèixer el codi que estem testejant.

