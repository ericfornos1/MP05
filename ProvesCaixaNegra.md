# Proves de caixa negra:

# Pizzeria Pepe:

### Codi programa:

```
public class pizzeriaPepe {

    public static boolean potCarregar(int pizzes){
        boolean pot = false;
        if(pizzes <=10 && pizzes >= 1){
            pot = true;
        }
        return pot;
    }
}
```

### Codi programa de test:

```
import org.junit.jupiter.api.*;


class pizzeriaPepeTest {

 
    @Test //Valor entre els límits
    void prova1() {
        boolean pot = pizzeriaPepe.potCarregar(3);
        Assertions.assertTrue(pot);
    }
    
    @Test //Valor superior al límit superior
    void prova2() {
        boolean pot = pizzeriaPepe.potCarregar(11);
        Assertions.assertFalse(pot);
    }


    @Test //Valor inferior al límit inferior
    void prova3() {
        boolean pot = pizzeriaPepe.potCarregar(-2);
        Assertions.assertFalse(pot);
    }
    
    
    @Test//Valor no és un número
    void prova4() {
        Exception exception = Assertions.assertThrows(NumberFormatException.class, () -> {
            pizzeriaPepe.potCarregar(Integer.parseInt("cinc"));
        });
}
```
# Transports Jean Claude:

### Codi programa:

```
public class TransportsJeanClaude {

    public static int pot_portar(int furgoneta, int càrrega) {
        if (càrrega < 500 || càrrega > 900) {
            return -1;
        } else if (furgoneta < 500 || furgoneta > 750) {
            return -1;
        } else if (càrrega > furgoneta) {
            return -1;
        } else {
            return 0;
        }
    }
    
    public static void main(String[] args) {
        System.out.println(pot_portar(500, 500)); // esperat: 0
        System.out.println(pot_portar(750, 750)); // esperat: 0
        System.out.println(pot_portar(750, 900)); // esperat: -1
        System.out.println(pot_portar(400, 500)); // esperat: -1
    }

}
```

## Taula de casos vàlids i no vàlids.

| Càrrega | Furgoneta | Resultat |
|---------|-----------|----------|
| 499     | 500       | -1       |
| 500     | 500       | 0        |
| 750     | 750       | 0        |
| 900     | 750       | -1       |
| 901     | 750       | -1       |

# ControlTemperatura

## Codi programa.

```
import java.util.Scanner;

public class ControlTemperatura {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Entrada de temperatura del medidor
        System.out.print("Introdueix la temperatura del medidor (entre -10 i 50 graus): ");
        double medidor = sc.nextDouble();

        // Entrada de temperatura del termostat
        System.out.print("Introdueix la temperatura del termostat (entre 15 i 40 graus): ");
        double termostat = sc.nextDouble();

        // Càlcul de la potència del sistema de calefacció
        int potencia;
        if (medidor > termostat) {
            potencia = 0;
        } else if (medidor >= termostat - 2) {
            potencia = 1;
        } else {
            potencia = 2;
        }

        // Sortida de la potència del sistema de calefacció
        System.out.println("La potència del sistema de calefacció és: " + potencia);

        sc.close();
    }
}
```

## Taula de casos vàlids i no vàlids.

| Medidor | Termostat | Resultat |
|---------|-----------|----------|
| <-10ºC  | -         | -        |
| -10ºC   | 15ºC-40ºC | 0        |
|15ºC-40ºC| 15ºC-40ºC | 1        |
| <15ºC   | 15ºC-40ºC | 1        |

# Factorial.

### Codi programa:

```
package exercici1;

public class Factorial {
    public static int factorial(int num) {
        int result = 1;
        for (int i = num; i >= 1; i--) {
            result *= i;
        }
        return result;
    }

    public static void main(String[] args) {
        int num = 5;
        System.out.println("El factorial de " + num + " és " + factorial(num));
    }
}

```

![Captura de pantalla de 2023-03-20 11-46-34](https://user-images.githubusercontent.com/113585897/226317767-736733a1-2235-43b8-a445-d306db9b440f.png)






