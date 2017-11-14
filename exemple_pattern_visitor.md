# Première étape

On définit une interface qui représente un élément.

CarElement.java
```java
interface CarElement {
    void accept(CarElementVisitor visitor);
    // Méthode à définir par les classes implémentant CarElements
}
```

# Deuxième étape

On crée les classes qui étendent de cette interface.

Wheel.java
```java
class Wheel implements CarElement {
    private String name;

    Wheel(String name) {
        this.name = name;
    }

    String getName() {
        return this.name;
    }

    public void accept(CarElementVisitor visitor) {
        visitor.visit(this);
    }
}
```

Engine.java
```java
class Engine implements CarElement {
    public void accept(CarElementVisitor visitor) {
        visitor.visit(this);
    }
}
```

Body.java
```java
class Body implements CarElement {
    public void accept(CarElementVisitor visitor) {
        visitor.visit(this);
    }
}
```

Car.java
```java
class Car {
    CarElement[] elements;

    public CarElement[] getElements() {
        return elements.clone(); // Retourne une copie du tableau de références
    }

    public Car() {
        this.elements = new CarElement[] {
                new Wheel("front left"),
                new Wheel("front right"),
                new Wheel("back left"),
                new Wheel("back right"),
                new Body(),
                new Engine()
            };
    }
}
```

# Troisième étape

On crée une interface qui représente Visitor.

CarElementVisitor.java
```java
interface CarElementVisitor {
    void visit(Wheel wheel);
    void visit(Engine engine);
    void visit(Body body);
    void visitCar(Car car);
}
```

# Quatrième étape

On crée deux classes visitor qui étendent l'interface précédente.

CarElementPrintVisitor.java
```java
class CarElementPrintVisitor implements CarElementVisitor {
    public void visit(Wheel wheel) {
        System.out.println("Visiting "+ wheel.getName() + " wheel");
    }

    public void visit(Engine engine) {
        System.out.println("Visiting engine");
    }

    public void visit(Body body) {
        System.out.println("Visiting body");
    }

    public void visitCar(Car car) {
        System.out.println("\nVisiting car");
        for(CarElement element : car.getElements()) {
            element.accept(this);
        }
        System.out.println("Visited car");
    }
}
```

CarElementDoVisitor.java
```java
class CarElementDoVisitor implements CarElementVisitor {
    public void visit(Wheel wheel) {
        System.out.println("Kicking my "+ wheel.getName());
    }

    public void visit(Engine engine) {
        System.out.println("Starting my engine");
    }

    public void visit(Body body) {
        System.out.println("Moving my body");
    }

    public void visitCar(Car car) {
        System.out.println("\nStarting my car");
        for(CarElement carElement : car.getElements()) {
            carElement.accept(this);
        }
        System.out.println("Started car");
    }
}
```

# Cinquième étape

On crée une classe de test pour la démonstration grâce aux deux classes précédentes.

TestVisitorDemo.java
```java
public class TestVisitorDemo {
    static public void main(String[] args) {
        Car car = new Car();

        CarElementVisitor printVisitor = new CarElementPrintVisitor();
        CarElementVisitor doVisitor = new CarElementDoVisitor();

        printVisitor.visitCar(car);
        doVisitor.visitCar(car);
    }
}
```

Voilà à quoi ressemble le diagramme de classe de notre exemple :

![Diagramme de classe de l'exemple Visiteur](https://img4.hostingpics.net/pics/123507diagrammeclassevisiteur.png)


# Sixième étape

On vérifie que tout cela fonctionne.


```java runnable
// Interface CarElement { autofold 
interface CarElement {
    void accept(CarElementVisitor visitor);
}
// }

// Classe Wheel { autofold 
class Wheel implements CarElement {
    private String name;

    Wheel(String name) {
        this.name = name;
    }

    String getName() {
        return this.name;
    }

    public void accept(CarElementVisitor visitor) {
        visitor.visit(this);
    }
}
// }

// Classe Engine { autofold 
class Engine implements CarElement {
    public void accept(CarElementVisitor visitor) {
        visitor.visit(this);
    }
}
// }

// Classe Body { autofold 
class Body implements CarElement {
    public void accept(CarElementVisitor visitor) {
        visitor.visit(this);
    }
}
// }

// Classe Body { autofold 
class Car {
    CarElement[] elements;

    public CarElement[] getElements() {
        return elements.clone(); // Retourne une copie du tableau de références
    }

    public Car() {
        this.elements = new CarElement[] {
                new Wheel("front left"),
                new Wheel("front right"),
                new Wheel("back left"),
                new Wheel("back right"),
                new Body(),
                new Engine()
            };
    }
}
// }

// Interface CarElementVisitor { autofold 
interface CarElementVisitor {
    void visit(Wheel wheel);
    void visit(Engine engine);
    void visit(Body body);
    void visitCar(Car car);
}
// }

// Classe CarElementPrintVisitor { autofold 
class CarElementPrintVisitor implements CarElementVisitor {
    public void visit(Wheel wheel) {
        System.out.println("Visiting "+ wheel.getName() + " wheel");
    }

    public void visit(Engine engine) {
        System.out.println("Visiting engine");
    }

    public void visit(Body body) {
        System.out.println("Visiting body");
    }

    public void visitCar(Car car) {
        System.out.println("\nVisiting car");
        for(CarElement element : car.getElements()) {
            element.accept(this);
        }
        System.out.println("Visited car");
    }
}
// }

// Classe CarElementDoVisitor { autofold 
class CarElementDoVisitor implements CarElementVisitor {
    public void visit(Wheel wheel) {
        System.out.println("Kicking my "+ wheel.getName());
    }

    public void visit(Engine engine) {
        System.out.println("Starting my engine");
    }

    public void visit(Body body) {
        System.out.println("Moving my body");
    }

    public void visitCar(Car car) {
        System.out.println("\nStarting my car");
        for(CarElement carElement : car.getElements()) {
            carElement.accept(this);
        }
        System.out.println("Started car");
    }
}
// }

public class Main{//On remplace ici le nom de la classe TestVisitorDemo par Main pour être éxécuter sur tech.io
    static public void main(String[] args) {

        Car car = new Car();

        CarElementVisitor printVisitor = new CarElementPrintVisitor();
        CarElementVisitor doVisitor = new CarElementDoVisitor();

        printVisitor.visitCar(car);
        doVisitor.visitCar(car);
    }
}
```

# Quiz

?[Combien y a t-il d'étapes dans notre tutoriel ?]
-[ ] 8
-[ ] 4
-[x] 6

?[Combien d'interfaces avons-nous défini ?]
-[ ] 3
-[x] 2
-[ ] 0

?[Chaque classe pouvant être "visitée" doit mettre à disposition une méthode publique :]
-[ ] accepted
-[x] accept
-[ ] visited

?[Quelle est la première étape ?]
-[x] Créer l'interface CarElement.java
-[ ] Créer l'interface CarElementVisitor.java
-[ ] Créer les classes Wheel.java, Engine.java, Body.java et Car.java


#### Merci d'avoir suivi ce playground !
