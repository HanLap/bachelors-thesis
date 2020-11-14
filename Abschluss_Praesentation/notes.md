

## What is CouchEdit?
- Model Driven Develepmonet -> syntaktisch korrekte modelle -> graphische modelling tools
- aktuelle Modelling tools schlechte User experience weil enge kopplung zwischen graphischer und abstrakter representation 
- CouchEdit versucht das zu lösen
- Modeling Language agnostisches modelling framework entwickelt von Nachreiner in Rahmen einer MA
- klarere trennung zwischen representationen

## Seite 4
- Konzeptionell verwendet CouchEdit 3 Metamodelle
- RenderMM definiert nur die simpelsten graphischen Objekte
- AbstraMM definiert Abstrakte Representation
- ConcreteMM verantwortlich graphische auf abstrakte representation zu mappen 

## Hypergraph
- CouchEdit baut sich dazu einen Hypergraphen auf
- Hypergraph beinhaltet Graphische Objekte von RenderMM
- modell Elemente des AbstractMM
- Und Relationen die ConcreteMM zwischen den beiden aufbaut

## Modular Architecture
- Hypergraph wird von Unabhängigen Komponenten - genannt Prozessoren - Aufgebaut und Bearbeitet
- Jeder Prozessor für einen Bereich des Hypergraphen zuständig
- Manche Prozessoren werden für jeden Syntax benötigt
- z.B. SpatialProcessor verantwortlich zu analysieren wie GraphischeObjekte zu einander stehen, nebeneinander, schneidet, beinhaltet
- Prozesorren die Verbindung zwischen RenderMM und AbstractMM herstellen sind meist Sprach Spezifisch und müssen für jeden modeling syntax neu geschrieben werden

## Problem
- Besonders das schreiben dieser Prozessoren hat sich als relativ aufwendig und Fehler anfällig heraus gestellt.
- Die momentane referenz konfiguration, welche einen Teil des Statechart Syntax Umsetzt umfässt 1942 LoC 
- Deswegen war die Idee, ein neues Metamodel zu entwickeln welches diese 3 metamodelle spezifiziern kann und es ermöglicht eine funktionierende Language Konfiguration inklusive den entsprechenden Prozessoren für CouchEdit zu Generieren

## Design Science Research
- Grundlegend wollte ich hier ein Artefact Entwickeln, dementsprechend hab ich natürlich nach dem Design Science Research prinzpip gearbeitet.
- das heißt, ...


## Related Work
- Um einen überblick der möglichen Ansätze zu bekommen lohnt es sich natürlich einen Blick in verwandte Arbeit zu schauen

## Tripe-Graph-Grammars
- Das Konzept von zwei Separaten Metamodellen, verbunden durch ein weiteres Metamodell, erinnert stark an Triple-Graph-Grammers.
- ...

## DiaGen
- Ein weiteres interessantes projekt in der Domain von CouchEdit ist DiaGen
- DiaGen ist ein tool dass ganze modell editoren aus einer formalen spezifikation generieren kann. 
- ähnlich zu CouchEdit erlaubt DiaGen Temporäre Inkonsitenzen zwischen graphischer und abstrakter Representation.
- allerdings arbeitet DiaGen anders als CouchEdit nicht mit Graphischen Primitiven, sondern mit vordefinierten Objekten. in dem Bild zum Beispiel, sind Kreis und Label fester teil eines vordefinierten Elements.

## Making Metamodels Aware of Concrete Syntax
- Eine weiter Interessante Arbeit und auch die haupt inspiration für meinen Ansatz kommt von fondement und Baar, Making Metamodel Aware of Concrete Syntax.
- in der Arbeit beklagen die Authoren, dass es genügend Spezifikationen für den Abstrakten Syntax gibt, aber der Graphische syntax und die verbindung zu diesem, meist informal gehalten sind. 
- Deswegen Schlagen sie einen Ansatz vor genau das zu formalisieren

## [2]
- Der ansatz Besteht aus 2 Teilen, Recognition and Synchronization.
- Im Recognition Teil werden zunächst Graphische Objekte, teil eine abstrakte Representation aheb zu einem Composite Objekt zusammen geführt.
- An dieses Composite Objekt wird dann ein sogenannter DisplayManager gehangen, welcher wieder rum mit einer Abstrakten Representation verbunden ist
- Im Zweiten teil, werden dann Invarianten auf den DisplayManager definiert, welche dafür verantwortlich sind dass Graphische und Abstrakte Representation synchronisiert sind.


## Design
- DSL 





--- 


- nicht bis ins kleinste spezifiziert -> mehr spezifizierung = bessere optimi

optimizer steigert generated code ohne blau zu steigern


optimizer muss nur einmal implementiert werden




- contribution klarer hervor heben


- architektur bild

- mehr source code bilder.



