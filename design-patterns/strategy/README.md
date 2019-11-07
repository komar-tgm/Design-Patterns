## Strategy-Pattern

### Problemdescription
Beim Strategy Pattern möchte man alle Klassen die unterschiedlich ist kapseln. Man baut auf ein Grundprinzip auf(z.B. Berechnen) und kapselt jede Rechnungsart in eine eigene Klasse. Das Prinzip, dass man nur eine Klasse hat die immer bei Neuerungen geändert werden muss, wird hierbei behandelt.
### Context
Das Strategy-Pattern definiert eine Familie von Algorithmen, kapselt sie einzeln und macht sie austauschbar. Wir streben beim Strategy das Prinzip an, dass alles was sich ändern kann, gekapselt werden soll, das heißt, dass jeder "Task" oder jede konkrete Aufgabe, wird in einer eigenen Klasse behandelt. Das Grundprinzip bleibt aber immer gleich.

### Solution

#### Design
![uml-strategy](resources/strategy.png)

#### Code
In der Context-Klasse:

```java
	public class Context{
        private Strategy strategy	//Interface-Objekt
		
		public int executeStrategy(){
        	this.strategy.execute(this.value1,this.value2);	
		}
	}
```
Mithilfe von Polymorphie kann nun in einer Konkreten Klasse dieser Task ausgeführt werden.
z.B. eine Addition
```java
	public class ConcreteAddition implements Strategy{
        @Override
		public int execute(int value1, int value2){
        	return value1+value2;
		}
	}
```

### Quellen
* [Heads First](https://www.oreilly.com/library/view/head-first-design/0596007124/)