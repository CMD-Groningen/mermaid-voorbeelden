# Mermaid voorbeelden


## Pie Chart diagram
```pre
pie title Inlogprocedure
    "Problematisch" : 200
    "Niet gelukt" : 50
    "Gelukt" : 100
```
```mermaid
pie title Inlogprocedure
    "Problematisch" : 200
    "Niet gelukt" : 50
    "Gelukt" : 100
```


## Happy flow met boxen

```c
stateDiagram
    aanmelden --> inloggen
    aanmelden --> inschrijving

    state inloggen {
    ingelogd_wachtwoorden --> invoer_wachtwoorden : wachtwoord fout
    invoer_wachtwoorden --> ingelogd_wachtwoorden : wachtwoord goed
       }

    state inschrijving {
    ingelogd_gegevens --> invoer_gegevens : gegevens fout
    invoer_gegevens --> ingelogd_gegevens : gegevens goed
       }

    ingelogd_gegevens -->  Toelating
    ingelogd_wachtwoorden -->  Toelating
```
```mermaid
stateDiagram-v2
    aanmelden --> inloggen
    aanmelden --> inschrijving

    state inloggen {
    ingelogd_wachtwoorden --> invoer_wachtwoorden : wachtwoord fout
    invoer_wachtwoorden --> ingelogd_wachtwoorden : wachtwoord goed
       }

    state inschrijving {
    ingelogd_gegevens --> invoer_gegevens : gegevens fout
    invoer_gegevens --> ingelogd_gegevens : gegevens goed
       }

    ingelogd_gegevens -->  Toelating
    ingelogd_wachtwoorden -->  Toelating
```

## Happy flow zonder boxen

```c
stateDiagram-v2
    aanmelden --> inloggen
    aanmelden --> inschrijving

  inloggen --> invoer_wachtwoorden
    ingelogd_wachtwoorden --> invoer_wachtwoorden : wachtwoord fout
    invoer_wachtwoorden --> ingelogd_wachtwoorden : wachtwoord goed
       
inschrijving --> invoer_gegevens
    ingelogd_gegevens --> invoer_gegevens : gegevens fout
    invoer_gegevens --> ingelogd_gegevens : gegevens goed
       

    ingelogd_gegevens -->  Toelating
    ingelogd_wachtwoorden -->  Toelating
```

```mermaid
stateDiagram-v2
    aanmelden --> inloggen
    aanmelden --> inschrijving

  inloggen --> invoer_wachtwoorden
    ingelogd_wachtwoorden --> invoer_wachtwoorden : wachtwoord fout
    invoer_wachtwoorden --> ingelogd_wachtwoorden : wachtwoord goed
       
inschrijving --> invoer_gegevens
    ingelogd_gegevens --> invoer_gegevens : gegevens fout
    invoer_gegevens --> ingelogd_gegevens : gegevens goed
       

    ingelogd_gegevens -->  Toelating
    ingelogd_wachtwoorden -->  Toelating
```

## Customer journey voorbeeld

```c
journey
    title Fiets bestellen
    section Inlogprocedure
      Wachtwoord invoeren: 1: Koper
      Webshop geeft toegang: 3: Koper, Webshop
      Ingelogd: 5: Koper
    section Fiets kiezen
      Categoriepagina openen: 5: Koper
      Electrische fiets kiezen: 5: Koper, Webshop
```

```mermaid
journey
    title Fiets bestellen
    section Inlogprocedure
      Wachtwoord invoeren: 1: Koper
      Webshop geeft toegang: 3: Koper, Webshop
      Ingelogd: 5: Koper
    section Fiets kiezen
      Categoriepagina openen: 5: Koper
      Electrische fiets kiezen: 5: Koper, Webshop
```

## Tijdlijn voorbeeld

```pre
timeline
  title Lesopbouw Project Prototyping
  section coaching  
      week 1 : Inleiding voorwaarden (2 uur)
      week 2 : Opstellen voorwaarden (2 uur)
  
                        
section aan de slag!
   week 3 : Overleggen werkschema prototyping
          : Workshop Circuits
   week 4 : Bouwen prototype
          : Workshop Interface Design 
```

```mermaid
      timeline
         title Lesopbouw Project Prototyping
         section coaching  
            week 1 : Inleiding voorwaarden (2 uur)
            week 2 : Opstellen voorwaarden (2 uur)
  
                        
         section aan de slag!
            week 3 : Overleggen werkschema prototyping
                     : Workshop Circuits
            week 4 : Bouwen prototype
                     : Workshop Interface Design 
```

## Sankey Flow diagram
```pre
sankey-beta
Inlogprocedure, Problematisch, 200
Inlogprocedure, Niet gelukt, 50
Inlogprocedure, Gelukt, 100
```
```mermaid
sankey-beta
Inlogprocedure, Problematisch, 200
Inlogprocedure, Niet gelukt, 50
Inlogprocedure, Gelukt, 100
```
