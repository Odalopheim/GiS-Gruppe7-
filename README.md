# **Beredskap i Agder**

## Problemstilling 

I denne oppgaven blir det undersøkt hvordan beredskapen er i Agder, med fokus på tilgjengeligheten til beredskapsinstitusjoner som brannstasjoner, tilfluktsrom, legevakt og sykehus. Vi analyserer forholdet mellom befolkningstettheten og disse institusjonene for å identifisere potensielle sårbare områder. På denne måten håper vi å visualisere og analysere disse datasettene i et interaktivt kart for å gi innsikt i beredskapssituasjonen og mulige forbedringer.  
 
## Teknologivalg
Vi har valgt følgende teknologier for implementere løsningen: 

- **Backend & Database**: Supabase med PostGIS for lagring og spørringer av geografiske data. Her ble pgAdmin4 bruk som et mellomledd mellom QGIS og Supabase. 
- **API**: Supabase API for å hente og filtrere data.
- **Frontend**: Leaflet for kartvisualisering og interaktivitet.
- **Bearbeiding av data**: QGIS for forbehandling av geodata.

Disse valgene ble tatt fordi Supabase gir en enkel, skalerbar og effektiv løsning for å lagre og hente geografiske data, mens Leaflet gir gode muligheter for visualisering av kartdata på en brukervennlig måte.

## Datasett 
Vi har brukt følgende datasett: 

1. Befolkning på grunnkretsnivå
      - https://kartkatalog.geonorge.no/metadata/befolkning-paa-grunnkretsniv/7eb907de-fdaa-4442-a8eb-e4bd06da9ca8?search=Befolkning
2. Tilfluktsrom – Offentlige
      - https://kartkatalog.geonorge.no/metadata/tilfluktsrom-offentlige/dbae9aae-10e7-4b75-8d67-7f0e8828f3d8?search=offent
3. Brannstasjoner
      - https://kartkatalog.geonorge.no/metadata/brannstasjoner/0ccce81d-a72e-46ca-8bd9-57b362376485?search=Branstasione
4. Sykehus
      - Selvlaget datasett med informasion hentet fra Google maps
5. Legevakt
      - Selvlaget datasett med informasion hentet fra Google maps
6. OpenStreetMap - leaflet
      - https://leafletjs.com/download.html

## **Implementasjon**
### **1. Datainnhenting og lagring**
- Datasettene ble lastet ned og importert i QGIS for filtrering og gjort om til GeoJSON filer.
- Dataene ble deretter lastet opp til Supabase/PostGIS for enkel spørring og visualisering. Dette ble gjort ved bruk av DB manager i QGIS. 

### **2. Backend/API**
- Supabase API ble brukt for å hente data fra databasen. Vi bruker API URL og API Key for å få tilgang til dette i Index.html-filen. 

### **3. Frontend & Visualisering**
- Leaflet ble brukt for å vise kartlag med brannstasjoner, tilfluktsrom, sykehus og befolkningsfordeling.
- Bruker kan interagere med kartet ved å zoome inn og ut, og krysse av og på for å visualisere de ulike elementene. 

## **Bruksanvisning**
### **Lokal kjøring**
1. Klon repoet:  
   ```bash
   git clone <repo-url>
   ```
2. Installer avhengigheter:  
   Hvis du bruker VS Code, kan du installere Live Server-utvidelsen og klikke "Go Live".

## Kjøring via GitHub
1. Gå til GitHub Repo (legg inn riktig lenke)!!!!.
2. Følg README-instruksjonene for å sette opp løsningen. 

## **Bilder/Video**
Her er noen eksempler på visualiseringene av applikasjonen:
[gif_av_kart](https://github.com/user-attachments/assets/517444a3-aa46-4c48-b119-370199e66adb)
