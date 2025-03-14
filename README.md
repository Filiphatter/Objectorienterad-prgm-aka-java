# Java

## installation
- JDK och Intellij community / pro när folk löser det.

## Java-basics
Det vi behöver först en Main metod, kan göras med "add sample code" 

```java
public class main { //klassen
Public static void Main(string[] args {  //metoden
//kod här eg system.out.println("hello world"); kan förenklas med "sout" -> tab
  }
}
```

### skillnader mellan js o java
- Javascript är mer än tolkning av kod istället för komplierad kod, eg fel märks lättare i java istället för js. Alltså tolkas i själva kompliatorn istället för i en webläsare. 
- Java har också en strikt typning i form av variabler och hantering. exempelvis let x = 10; x = "text"; funkar i JS, medans java är strikt int x = 10; x = "text" så blir det komplieringsfel.
- Variabler och datatyper måste hanteras korrekt.
- Js har även väldigt stor flexibilitet med hur man skriver koden. Java är väldigt mer strikt med att allt måste ingå i en klass och sedan görs största delarna i metoder inom den klassen.
- Filen behöver heta samma sak som klassen i filen. 
- Viktigt är att använda ; efter rader iochmed det kommer ge ett error.

### Variabler och datatyper

```java
int heltal = 10;
double decimaltal = 10.5;
boolean TorF = true;
char Tecken = "A"; //ofta en bokstav eller liknande
String Text = "detta är textstring"; //notera stor bokstav på "String" för möjligheter av metoder med "String" som datatyp.
```

```java
//finns även saker som addeventlistner i java som heter "Scanner" för att använda det behöver man importera in det. "import java.util.scanner;"
Scanner scan = New scanner(system.in);
system.out.println("enter your name: ");
String namn = scan.nextLine(); //väntar på en input
system.out.println("your name is: " + namn);
```

### metoder

Public delen i metoder är tilgångsheten mellan filer och klasser. Om den är private kan den enbart användas inom sin klass. Public ger möjlighet för flera klasser. 
int i denna stränggen innebär return sats. Alltså måste vi använda *return* i slutet av metoden. Skulle man skrivit void så behöver man inte skriva return.
Static vilket är lite oklart verkar göra själva metoden möjlig att använda på klass nivå eller kallat globalt.
```java
public static int addNumbers (int tal1, int tal2) {
}
```
Man kan overloada med metoder, alltså om jag vill ha möjligheten att både ta in integers och doubles så kan man kopiera själva koden och skriva in en exakt likadan fast med doubles.
Då tar kompilatorn den som är "rätt" för köra så slipper man pilla med parses.
```java
public static int addNumbers (int tal1, int tal2) {
}
public static int addNumbers (double tal1, double tal2) {
}
```



