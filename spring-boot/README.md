## Spring-Boot Fragen

Folgende Fragen sind ausschließlich über die Spring-Doku und API zu recherchieren und in einem README.md zu dokumentieren (QUELLEN immer angeben, siehe zweite Tafel)

1. Beschreibe folgende Annotationen

- **@SpringBootApplication**
  @SpringBootApplication deutet eine @Configuration Klasse an, die eine oder mehrere Beans verwendet. Eine @Configuration Klasse zeigt an, dass eine oder mehrere @Bean Methoden vom Spring Container verarbeitet werden müssen.  Zusätzlich werden @EnableAutoConfiguration, welche die Beans vermutet und konfiguriert aufgerufen. [Quelle](https://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/autoconfigure/SpringBootApplication.html)
- **@Bean**
  @Bean zeigt an, dass eine Methode eine Bean erzeugt, die vom Spring Container verarbeitet werden soll [Quelle](https://docs.spring.io/spring-framework/docs/5.1.6.RELEASE/javadoc-api/org/springframework/context/annotation/Bean.html?is-external=true)
- **@RestController**
  Die @RestController Annotation tragen jene Klasse dessen @RequestMapping Methoden die @ResponseBody Semantik anninmt [Quelle](https://docs.spring.io/spring/docs/current/javadoc-api/org/springframework/web/bind/annotation/RestController.html)
- **@RequestMapping**
  @RequestMapping ist eine Annotation, die vor einer Methode verwendet wird. Als Parameter wird der Pfad angegeben, in dem der Inhalt dieser Methode ausgegeben wird. [Quelle](https://docs.spring.io/spring/docs/current/javadoc-api/org/springframework/web/bind/annotation/RequestMapping.html)
  **1 a) Was sind Annotationen?**
  Annotationen bieten Meta-Daten für das Element an dem sie angeschrieben werden, ohne direkt vom Compiler betroffen zu sein.
  **1 b) Welche Möglichkeiten gibt es diese selbst zu implementieren?**

	```java
  public @interface MyAnnotation{}
	```

**1 c) Wie hängen Annotationen mit Interfaces zusammen? Welche Gemeinsamkeiten gibt es?**
Die Schreibweise bei einer Annotation beginnt ca. wie bei einem Interface, nur steht ein @ vor interface, z.b.

  ```java
  public @interface RestController
  ```
**1 d) Kann man die @SpringBootApplication auch anders anschreiben?**
Man kann anstatt die @SpringBootApplication Annotation, @Configuration, @EnableAutoConfiguration und @ComponentScan verwenden. [Quelle](https://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/autoconfigure/SpringBootApplication.html)
**1 e) Welche @Target Optionen gibt es und was bedeuten diese?**
@Target gibt an in welchem Kontext diese Annotation anwendbar ist. [Quelle](https://docs.oracle.com/javase/8/docs/api/java/lang/annotation/Target.html?is-external=true) 
Folgende Optionen werden in einem Enum als Konstanten definiert
* ANNOTATION_TYPE

* CONSTRUCTOR

* FIELD

* LOCAL_VARIABLE

* METHOD

* PACKAGE

* PARAMETER

* TYPE

* TYPE_PARAMETER

 * TYPE_USE
[Quelle](https://docs.oracle.com/javase/8/docs/api/java/lang/annotation/ElementType.html)
**1 f) Was hat @Retention zu bedeuten?**
Gibt an, wie lange eine Annotation erhalten bleiben soll. Wenn diese Annotation angegeben wird, dann richtet man sich an die default Retention-Policy RententionPolicy.class [Quelle](https://docs.oracle.com/javase/7/docs/api/java/lang/annotation/Retention.html)
**2a) Wo erwartet sich SpringBoot das application.properties File?**
Im Normalfall ohne etwas zu konfigurieren unter: src/main/resources
**2b) Ist dies für das Gradle-Plugin auch so?**
    **2c) Wie kann man eigene Configurations-Settings in SpringBoot setzen?**

  **2d) Wo kann man die wichtigsten Default-Configuration von SpringBoot vorfinden?**

## Kenn mich nicht aus

- [] Was macht das gradle-plugin mit den vorgefundenen applications.properties
- 2b) Ist dies für das Gradle-Plugin auch so?
- 2c) Wie kann man eigene Configurations-Settings in SpringBoot setzen?
- 2d) Wo kann man die wichtigsten Default-Configuration von SpringBoot vorfinden?**

## Resources

[1] [Definition von @SpringBootApplication; SpringBoot Docs, zuletzt verwendet am 5.4.2019; online](https://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/autoconfigure/SpringBootApplication.html)