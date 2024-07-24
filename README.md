# Spotify API Testing

Acest proiect demonstrează cum să testezi diferite metode API de la Spotify folosind Postman. Metodele testate sunt:

- **GET Album**
- **GET Playlist**
- **PUT Change Playlist Details**
- **POST Add Items to Playlist**
- **DELETE Remove Playlist Items**

## Cerințe

- [Postman](https://www.postman.com/downloads/)
- Cont de dezvoltator Spotify și token de acces. [Documentație Spotify API](https://developer.spotify.com/documentation/web-api/)

## Configurare

1. Clonează acest repository:
    ```bash
    git clone https://github.com/MihaiMarianMacrea/Spotify-API-Testing.git
    cd spotify-api-testing
    ```

2. Deschide Postman și importă colecția `Spotify API Tests.postman_collection.json`.

3. Configurează variabilele de mediu pentru tokenul de acces Spotify.

![Generate_code](images/Generate%20Code.JPG)
![Generate_Token](images/Generate%20Token.JPG)

## Teste API

### GET Album

Această metodă recuperează informații despre un album specific.

![GET Album](images/Get%20Album%20method.JPG)

#### Teste efectuate:
- Verifică dacă răspunsul are statusul 200.
- Verifică dacă răspunsul este în format JSON.
- Verifică ca timpul de respuns este mai mic de 400ms
- Verifică faptul ca album_type are valoare album
- Verifică ca numele artistului este Disturbed
- Verifică ca numele primei piese este corect
- Verifică ca toate piesele conting numele corect al albumului

![Teste GET Album](images/Get%20Album%20tests.JPG)

### GET Playlist

Această metodă recuperează informații despre un playlist specific.

![GET Playlist](images/Get%20Playlist.JPG)

#### Teste efectuate:
- Verifică dacă răspunsul are statusul 200.
- Verifică dacă răspunsul este în format JSON.
- Verifică ca timpul de respuns este mai mic de 600ms
- Verifică ca numele playlistului este "API Playlist Actualizat"
- Verifică daca playlistul este public
- Verifică daca numele primei piese este "Immoralized"
- Verifică daca toate piesele sunt disponibile pentru piata din Romania

![Teste GET Playlist](images/Get%20Playlist%20test.JPG)

### PUT Change Playlist Details

Această metodă modifică detaliile unui playlist specific.

![PUT Change Playlist Details](images/Change%20Playlist%20Details.JPG)  

#### Teste efectuate:
- Verifică dacă răspunsul are statusul 200.
- Verifică ca timpul de respuns este mai mic de 600ms
- Verifică dacă descrierea playlistului a fost actualizată corect.
- Verifică dacă starea publică/privată a playlistului a fost actualizată corect.

![Teste PUT Change Playlist Details](images/Change%20Playlist%20Details%20Tests.JPG) 

![Verifica daca modificarile s-au facut si Bug la parametrul 'public'](images/Change%20Playlist%20Details%20+BUG.JPG) 

### POST Add Items to Playlist

Această metodă adaugă piese într-un playlist specific.

![POST Add Items to Playlist](images/Add%20Items%20to%20Playlist.JPG)

#### Teste efectuate:
- Verifică dacă răspunsul are statusul 201.
- Verifică dacă răspunsul este în format JSON.
- Verifică dacă răspunsul conține câmpul `snapshot_id`.
- Verifică dacă `snapshot_id` nu este gol.

![Teste POST Add Items to Playlist](images/Add%20items%20To%20Playlist%20Test.JPG)

### DELETE Remove Playlist Items

Această metodă elimină piese dintr-un playlist specific.

![DELETE Remove Playlist Items](images/Remove%20Playlist%20Items.JPG)

#### Teste efectuate:
- Verifică dacă răspunsul are statusul 200.
- Verifică dacă răspunsul este în format JSON.
- Verifică dacă răspunsul conține câmpul `snapshot_id`.
- Verifică dacă `snapshot_id` nu este gol.


![Raportrul de executie in Postman](images/Raport%20de%20executie%20al%20testelor.JPG)


### Raportul de execuție generat din Collection Runner
##[V2](images/Raport%20de%20executie%20al%20testelor%20v2.JPG)


![Teste DELETE Remove Playlist Items](images/Remove%20Playlist%20Items%20Tests.JPG)

## Contribuții

Contribuțiile sunt binevenite! Te rog să deschizi un pull request sau să raportezi probleme în secțiunea de issues.

## Licență

Acest proiect este licențiat sub licența ITFACTORY.

