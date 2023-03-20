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


