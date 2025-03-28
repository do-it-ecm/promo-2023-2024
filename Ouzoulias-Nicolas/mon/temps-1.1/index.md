---
layout: layout/mon.njk

title: "Petite initiation au Java et à la Programmation Orientée Objet"
authors:
  - Nicolas Ouzoulias

date: 2023-09-17

temps: 1
tags:
  - Java
  - POO
  - Débutant

description: "Mon premier MON pour découvrir quelques bases sur le langage Java et la Programmation Orientée Objet."
---

## Sommaire

I. Introduction

II. Les bases

III. La Programmation Orientée Objet (POO)

IV. Conclusion

## I. Introduction

A travers ce premier MON de l'année j'ai souhaité suivre une initiation au langage Java. Depuis ma découverte de l'informatique en prépa je n'ai fait que du Python et même si ce langage me plaît je pense qu'avoir au moins les bases d'un autre peut être toujours utile.

Pour cela j'ai suivi une formation sur OpenClassRoom retrouvable juste [ici](https://openclassrooms.com/fr/courses/6173501-apprenez-a-programmer-en-java) ainsi que quelques vidéos en ligne.

De plus cette formation m'a permis d'approfondir mes connaissances sur la Programmation Orienté Objet que j'avais à peine découverte sur Python lors d'un stage.



## II. Les bases

Mon principal objectif était de découvrir et d'apprendre la syntaxe Java, car ayant connaissance de Python la logique de programmation derrière les deux langages est globalement la même. Cependant contrairement à Python, le Java est plus exigeant en termes de syntaxe et rien que le fait de devoir utiliser le " `;` " et les " `{}` " de manière si fréquente n'est pas facile au début et il faut s'y habituer.

De plus, un programme Java est structuré en **packages** et en **classes**, et aucun code n'est écrit en dehors d'une classe ce qui signifie que toutes les fonctions sont des **méthodes**.

La construction en bloc et l'utilisation des `{}` pour marquer le début et la fin d'un bloc de code rendent les variables accessibles uniquement dans le contexte dans lequel elles ont été déclarée. Il faut donc faire attention à la **portée** d'une variable et faire attention lorsqu'on la déclare à désigner un niveau de contrôle.

![exemple portée](https://user.oc-static.com/upload/2021/12/02/16384489205392_p1c5-4.png)

*Schéma provenant de l'Open ClassRoom : <https://openclassrooms.com/fr/courses/6173501-apprenez-a-programmer-en-java/6446031-saisissez-la-portee-des-variables>*

- ***public*** : visible pour tous et par conséquent le moins restrictif ;

- ***protected*** : visible pour le package et l'ensemble de ses sous-classes ;

- ***package-protected*** : généralement visible uniquement par le package dans lequel il se trouve (paramètres par défaut). Ne pas mettre de mot clé déclenche ce niveau de contrôle ;

- ***private*** : accessible uniquement dans le contexte dans lequel les variables sont définies (à l'intérieur de la classe dans laquelle il est situé).

Cette *encapsulation* du code peut permettre de sécuriser l'accès aux données ainsi que de limiter les modifications accidentelles lors de l'écriture de celui-ci.

#### Différences de syntaxe avec Python :

***Java :***
```java
public class Main {
    public static int max(int a, int b) {
        if (a > b) {
            return a;
        } else {
            return b;
        }
    }

    public static void main(String[] args) {
        int num1 = 10;
        int num2 = 20;
        int resultat = max(num1, num2);
        System.out.println("Le plus grand nombre est : " + resultat);
    }
}
```
***Python :***
```python
def max(a, b):
    if a > b:
        return a
    else:
        return b

num1 = 10
num2 = 20
resultat = max(num1, num2)
print("Le plus grand nombre est :", resultat)
```
Pour une même fonction très simple qui renvoie le maximum entre deux nombres on observe facilement les différences de syntaxe entre les 2 langages et pourquoi Python peut être considéré comme plus simple à prendre en main, il y a moins de lignes et de caractères tout en semblant plus procédurale.

## III. La Programmation Orientée Objet (POO)

Une grande partie de la formation se concentrait sur la POO et comment bien l'utiliser en Java. N'ayant que très peu pratiquer ce type de programmation j'ai pu découvrir les bases de celles-ci tout en mettant en pratique ce que je venais d'apprendre en Java.

![descriptionPOO](https://www.data-transitionnumerique.com/wp-content/uploads/2021/03/classe.webp)

*Schéma provenant du site : <https://www.data-transitionnumerique.com/apprendre-programmation-objet/>*

La POO est une manière de programmer en se basant sur le concept d'*objets* possédant des *attributs* et des *méthodes*.

```java
public class TestObjet{

	public static void main(String[] args) {
		Voiture voiture = new Voiture();
		voiture.start();

		Bateau bateau = new Bateau();
		bateau.start();
	}
}
class Vehicule{
	void start() {
		System.out.println("VROOM");
	}
}
class Voiture extends Vehicule{

	@Override
	void start() {
		super.start();
		allumerFeux();
	}

	void allumerFeux() {
		System.out.println("Allumage Feux ! ");
	}
}

class Bateau extends Vehicule{

}
```

Comme sur l'exemple précédent des classes filles peuvent **hériter** d'une classe mère mais également utiliser différemment les méthodes mères sans les modifier directement, c'est le **polymorphisme**.

Ici les classes `Voiture` et `Bateau` descendent de la classe `Vehicule` et possèdent donc la méthode `.start()`, cependant cette dernière est différente pour les voitures.

#### Avantages de la POO :

- Facile à lire et à comprendre
- Facilement modifiable
- Le Java semble bien s'y prêter avec les différentes portées des variables

**Mais** cela ne doit pas devenir une obligation, elle n'est à utiliser que lorsque le programme s'y prête et la programmation procédurale classique continue de très bien fonctionner dans la plupart des cas, *surtout à mon niveau de programmation peu élevé...*

## IV. Conclusion

Je ne suis pas du tout devenu un expert en Java, loin de là, mais je pense avoir bien appréhendé les bases de ce langage et si j'ai un jour besoin de l'utiliser je m'y adapterai plus rapidement. Désormais seul le temps et l'expérience me feront gagner en vitesse de code et en connaissances.

De même pour la POO, la formation m'a permis de mieux comprendre l'utilité de celle-ci et comment bien organiser mon code pour en tirer profit. Il ne me reste plus qu'à faire de la POO en Python que je maîtrise plus, et je crois avoir un [cours](https://francoisbrucker.github.io/cours_informatique/cours/algorithme-code-th%C3%A9orie/code/programmation-objet/) à porter de main pour m'aider à cela ...

### Sources

- Le contenu principal de ma formation qui explique en détail la syntaxe et l'écriture en Java : <https://openclassrooms.com/fr/courses/6173501-apprenez-a-programmer-en-java/6173508-tirez-le-maximum-de-ce-cours>
- Des petits exercices pour expérimenter : <https://www.cours-gratuit.com/java>
- Une formation supplémentaire sur la POO : <https://www.data-transitionnumerique.com/apprendre-programmation-objet/>