# 🍕 Pizza-App

Dieses Projekt wurde im Rahmen des Moduls **„Anwendungsentwicklung mit Python“ (FS25)** an der FHNW umgesetzt. Ziel war es, ein interaktives Konsolenprogramm zu entwickeln, das auf Basis einer objektorientierten Klasse (`Pizza`) verschiedene Funktionalitäten bietet. Die Datenbasis wurde als **Fake-Datenbank (Dictionary in Python)** umgesetzt.  

---

## 1. Projektübersicht
Das System ermöglicht es Nutzer:innen,  
- alle verfügbaren Pizzen mit ihren Details anzuzeigen,  
- Pizzen nach eingegebenen Belägen zu filtern,  
- eine Pizza über den Namen auszuwählen und  
- den Preis (inkl. optionalem Gutscheincode `PIZZA10`) berechnen zu lassen.  

**Technologien & Tools**
- IDE: Visual Studio Code  
- Sprache: Python 3  
- Versionsverwaltung: Git & GitHub  

**Architektur (Schichtenmodell)**
- **Model Layer (Pizza-Klasse):** Datenmodell mit Attributen & Methoden  
- **Fake-Datenbank:** Dictionary mit Pizza-Objekten  
- **Business Logic:** Filter- & Preisberechnungslogik  
- **UI Layer:** Konsolenmenü mit Benutzereingaben  

---

## 2. Klassendiagramm & Modellierung
Die objektorientierte Modellierung basiert auf einer zentralen Klasse `Pizza` mit den Attributen `name`, `toppings` und `price_chf`. Die Instanzen werden in einer Fake-Datenbank (Dictionary) verwaltet.  

```mermaid
classDiagram
    class Pizza {
        +name : str
        +toppings : List[str]
        +price_chf : float
        +has_all_toppings(wanted: List[str]) bool
        +details() str
    }


