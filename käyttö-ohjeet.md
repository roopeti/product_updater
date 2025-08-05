# Step-by-Step Ohjeet

1. Lataa [Node.js LTS](https://nodejs.org/en)
2. Varmista, että npm on olemassa: terminaaliin node -v ja npm -v
<img width="435" height="103" alt="image" src="https://github.com/user-attachments/assets/6cb26881-9b66-4b9f-ab5f-f719fe38c11a" />


3. Navigoi oikeaan directoryyn:
<img width="518" height="36" alt="image" src="https://github.com/user-attachments/assets/17118c80-0465-4e13-bd1f-2072baa6d1ea" /> 


4. Asenna riippuvuudet: npm install
<img width="458" height="161" alt="image" src="https://github.com/user-attachments/assets/b4f62cc3-2e99-4ea1-9523-b7f3858793c1" />

## 5. Configuraatio
   Avaa config.js, esim vscodella tai vastaavalla ohjelmalla, jolla voi editoida. Varmista, että käyttäjätunnus, salasana, autentikaatio Legrand API:hin ja API_BASE:t ovat oikein.

6. Aloita aplikaatio: npm start
<img width="457" height="150" alt="image" src="https://github.com/user-attachments/assets/06bbd0d7-874f-4897-bd3a-ab503146327b" />


Electron ikkunan pitäisi aueta automaattisesti. Loki tiedostot voi ladata painamalla niitä alhaalta, tai niitä voi tarkastella "logs" kansiosta projektin sisältä.


Ensin ohjelma hakee kaikki tuotetiedot STK:lta ja tallentaa ne "full-data" tiedostoon. Sitten se poimii tuotekoodit niistä tuotetiedoista, ja hakee kaikki päivitetyt tuotetiedot Legrandin API:sta. Nämä tuotetiedot se tallentaa raakana tiedostoon legrand_raw_products. Ja sitten mäppäyksen jälkeen tiedostoon legrand_products_mapped tiedostoon. 

Kaikki tuotteet, joita ei löytynyt Legrandin API:sta tallentuu tiedostoon legrand_not_found_ids. Ja kaikki tuotteet, joille ei löytynyt mitään kuvia tai dokumentteja se tallentaa tiedostoon legrand_removed_no_documents. 
