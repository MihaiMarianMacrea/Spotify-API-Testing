# Spotify API Testing

Acest proiect demonstrează cum să testezi diferite metode API de la Spotify folosind Postman. Metodele testate includ:

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
    git clone https://github.com/numele-tau/spotify-api-testing.git
    cd spotify-api-testing
    ```

2. Deschide Postman și importă colecția `Spotify API Tests.postman_collection.json`.

3. Configurează variabilele de mediu pentru tokenul de acces Spotify.

![Generate_code](images/Generate_Code.JPG)
![Generate_Token](images/Generate_Token.JPG)

## Teste API

### GET Album

Această metodă recuperează informații despre un album specific.

![GET Album](images/Get_Album_method.JPG)

#### Teste efectuate:
- Verifică dacă răspunsul are statusul 200.
- Verifică dacă răspunsul este în format JSON.
- Verifică ca timpul de respuns este mai mic de 400ms
- Verifică faptul ca album_type are valoare album
- Verifică ca numele artistului este Disturbed
- Verifică ca numele primei piese este corect
- Verifică ca toate piesele conting numele corect al albumului

![Teste GET Album](images/Get_Album_tests.JPG)

### GET Playlist

Această metodă recuperează informații despre un playlist specific.

![GET Playlist](images/Get_Playlist.JPG)

#### Teste efectuate:
- Verifică dacă răspunsul are statusul 200.
- Verifică dacă răspunsul este în format JSON.
- Verifică ca timpul de respuns este mai mic de 600ms
- Verifică ca numele playlistului este "API Playlist Actualizat"
- Verifică daca playlistul este public
- Verifică daca numele primei piese este "Immoralized"
- Verifică daca toate piesele sunt disponibile pentru piata din Romania

![Teste GET Playlist](images/Get_Playlist_test.JPG)

### PUT Change Playlist Details

Această metodă modifică detaliile unui playlist specific.

![PUT Change Playlist Details](images/Change_Playlist_Details.JPG)  

#### Teste efectuate:
- Verifică dacă răspunsul are statusul 200.
- Verifică ca timpul de respuns este mai mic de 600ms
- Verifică dacă descrierea playlistului a fost actualizată corect.
- Verifică dacă starea publică/privată a playlistului a fost actualizată corect.

![Teste PUT Change Playlist Details](images/Change_Playlist_Details_Tests.JPG) 

![Verifica daca modificarile s-au facut si Bug la parametrul 'public'](images/Change_Playlist_Details_+BUG.JPG) 

### POST Add Items to Playlist

Această metodă adaugă piese într-un playlist specific.

![POST Add Items to Playlist](images/Add_Items_to_Playlist.JPG)

#### Teste efectuate:
- Verifică dacă răspunsul are statusul 201.
- Verifică dacă răspunsul este în format JSON.
- Verifică dacă răspunsul conține câmpul `snapshot_id`.
- Verifică dacă `snapshot_id` nu este gol.

![Teste POST Add Items to Playlist](images/Add_items_to_Playlist_Test.JPG)

### DELETE Remove Playlist Items

Această metodă elimină piese dintr-un playlist specific.

![DELETE Remove Playlist Items](images/Remove_Playlist_Items.JPG)

#### Teste efectuate:
- Verifică dacă răspunsul are statusul 200.
- Verifică dacă răspunsul este în format JSON.
- Verifică dacă răspunsul conține câmpul `snapshot_id`.
- Verifică dacă `snapshot_id` nu este gol.

![Teste DELETE Remove Playlist Items](images/Remove_Playlist_Items_Tests.JPG)

## Contribuții

Contribuțiile sunt binevenite! Te rog să deschizi un pull request sau să raportezi probleme în secțiunea de issues.

## Licență

Acest proiect este licențiat sub licența ITFACTORY.

