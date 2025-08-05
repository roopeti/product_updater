# Step-by-Step Ohjeet

1. Lataa [Node.js LTS](https://nodejs.org/en)
2. Varmista, että npm on olemassa: terminaaliin node -v ja npm -v. 

<img width="435" height="103" alt="image" src="https://github.com/user-attachments/assets/6cb26881-9b66-4b9f-ab5f-f719fe38c11a" />

4. Navigoi oikeaan directoryyn (mihin ikinä oletkin tallentanut projektin):
<img width="518" height="36" alt="image" src="https://github.com/user-attachments/assets/17118c80-0465-4e13-bd1f-2072baa6d1ea" /> 


5. Asenna riippuvuudet: npm install. Tämä antaa jonkin näköisiä varoituksia todennäköisesti, mutta niillä ei väliä. 
<img width="458" height="161" alt="image" src="https://github.com/user-attachments/assets/b4f62cc3-2e99-4ea1-9523-b7f3858793c1" />

## 5. Configuraatio
   Avaa config.js, esim vscodella tai vastaavalla ohjelmalla, jolla voi editoida. Varmista, että käyttäjätunnus, salasana, autentikaatio Legrand API:hin ja API_BASE:t ovat oikein.

6. Aloita aplikaatio: npm start. CMD toimii ihan hyvin tähän tarkoitukseen.
<img width="457" height="150" alt="image" src="https://github.com/user-attachments/assets/06bbd0d7-874f-4897-bd3a-ab503146327b" />


Electron ikkunan pitäisi aueta automaattisesti. Loki tiedostot voi ladata painamalla niitä alhaalta, tai niitä voi tarkastella "logs" kansiosta projektin sisältä.


Ensin ohjelma hakee kaikki tuotetiedot STK:lta ja tallentaa ne "full-data" tiedostoon.

<img width="322" height="318" alt="image" src="https://github.com/user-attachments/assets/8e9791fd-9f60-4f2d-b318-33d4ebffa63a" />

Sitten se poimii tuotekoodit niistä tuotetiedoista <img width="709" height="20" alt="image" src="https://github.com/user-attachments/assets/80002b17-8473-4718-9fce-48cf28d38bac" />
, ja hakee kaikki päivitetyt tuotetiedot Legrandin API:sta. Nämä tuotetiedot se tallentaa raakana tiedostoon legrand_raw_products. Ja sitten mäppäyksen jälkeen tiedostoon legrand_products_mapped. 

<img width="398" height="132" alt="image" src="https://github.com/user-attachments/assets/d1ca329c-3f8d-4908-946e-065427e8b291" />


Kaikki tuotteet, joita ei löytynyt Legrandin API:sta tallentuu tiedostoon legrand_not_found_ids. Ja kaikki tuotteet, joille ei löytynyt mitään kuvia tai dokumentteja se tallentaa tiedostoon legrand_removed_no_documents. 


7. Paina update all nappia, jos haluat päivittää kaikkien tuotteiden tiedot.

<img width="568" height="383" alt="image" src="https://github.com/user-attachments/assets/9e9fe4ac-9c6f-4d71-aaf3-e02f1bd9a066" />

Napin painamisen jälkeen saatta mennä noin minuutti, ennen kuin tuotetiedot alkaa päivittyä. 
