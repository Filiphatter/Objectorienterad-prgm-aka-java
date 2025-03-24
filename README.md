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

### regex
Ett sätt att felsöka/kontrollera att användares input stämmer överens men komplicerade tecken för datorn skall förstå, googla efter behov.

### listor
Det finns två typer av lister, array list och linked list, array list är oftast använd men linked list är bra för en upprepande använding.
man kan också göra en array till en list

```java
public static void listExempel() {
String[] stringArray = {"hej", "på", "dig"};
// <> betyder generics vilket är att man kan bestämma vilken datatyp metoden ska använda. alltså vilken datatyp som lagras i detta fallet.
List<String>() stringList = new ArrayList<>();

stringList.add("String");
stringList.add("text");
stringList.add("en till sträng");

// private static void getInput() {
Scanner scanner = new Scanner(System.in);
string input = scanner.nextLine();
}

//här skapar vi en input som sparas i en lista. 
public static void addStuffToListWithScanner(){

List<String> myList = new ArrayList<>();
while(true){
    String input = getInput() //metod med input scanner

      myList.add(input);
      system.out.println("want to adda string?");
        if(getInput().equals("nej"){
        break}
  }
system.out.println("myList = " + myList)
} 

```
### Nils start av oop 03-24
- vad är en klass? En mall för objekt basically, exempelvis något mer generellt inga attributer, kan även vara uträkningar exempelvis en samling av metoder.
- vad är ett objekt? skapat av klassen, instans (instance)
- klassens byggstenar
  1. Klassvariabler, fields. 
     - hittade grejer som kan vara relevant
     - Class variables also known as static variables are declared with the static keyword in a class, but outside a method, constructor or a block.           There would only be one         copy of each class variable per class, regardless of how many objects are created from it. https://www.tutorialspoint.com/What-are-class-variables-instance-      variables-and-          local-variables-in-Java
     - https://www.w3schools.com/java/java_class_methods.asp public v static
  2. Konstruktor, en metod som körs när man skapar ett objekt. man kör alltid konstruktorn men om man inte explicit skapar en konstruktor kör den en tom konstruktor.
      När man skapar en instans av klassen så körs alltid konstruktorn.
  3. getter, ett sätt att hämta värdet utan exposea variablen
  4. setter, sätter ett värde, antingen genom krav eller validering
  5. toString, konverterar andra typer av variabler till en String, exempelvis en int 5 till en string blir "5"

### klasserochobject med nils
```java
//Book.java
public class Book {

String title;
String author;
int pages;
String ISBN;
boolean isLoaned = false;

//konstruktor
public Book(String title, String author){
this.title = title;
this.author = author;
this.isLoaned = false;
this.isbn = "isbn:"+title.length() + author.length() + "00000" + "943";
//System.out.println("object has been created here is the information");
//System.out.println("Title: " + this.title + " Author: " + this.author + " isbn: " + this.isbn);
}
}
//här programmet kör ig
//Main.java
public class Main {
            //här skapar man själva objektet 
Book myBook = new Book("Bamse", "Rune Andreasson"); 
//här sparas de i variabel

myBook.toString();

Library blentarpsbiblotek = new Library();
Library mamlobibbla = new Library();
System.out.println(blentarpsbiblotek.books.get(0));
                                          //get är en del av arrayList, en getter. 0 är index
}

Library.java

import java.util.Arraylist
public class Library {

ArrayList<Book> books = new ArrayList<>();

public Library(){
books.add(new Book("bamse", "Rune"));
books.add(new Book("Emil", "AD"));
books.add(new Book("Lasse och Maja", "Dekdektivbyro"));
}

}

```





