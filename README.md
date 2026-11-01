# TNX Monitor + RDA Cluster Live 📡

Napredna Python aplikacija namijenjena radioamaterima za automatizirano praćenje i lov na **RDA (Russian District Award)** reference u stvarnom vremenu. Aplikacija sinkronizira podatke s portala `tnxqso.com` i real-time spot alerte s `rdacabinet.ru` posredstvom Socket.IO protokola, uspoređujući ih s lokalnom matričnom CSV bazom odrađenih slotova.

---
<p align="center">
  <img src="tnx1.png" width="500" alt="main gui ">
  <img src="tnx2.png" width="490" alt="slots">
</p>

## ✨ Glavne mogućnosti

* **Automatska sinkronizacija baze**: Pri svakom pokretanju aplikacija preuzima najnoviju CSV datoteku s vašeg *hunter* log linka i ažurira lokalnu bazu (`rda_slots.csv`).
* **Dvije sinkronizirane tablice**:
  * **Gornja tablica**: Prikazuje aktivne radioamaterske stanice s TNXQSO-a u stvarnom vremenu, uz automatsko označavanje crvenom bojom za stanice koje vam donose novu oblast ili novi band.
  * **Donja tablica**: 30-minutni klizeći prozor RDA cluster spotova koji se u realnom vremenu ažurira ovisno o promjeni bandova i modova.
* **Pametni sustav upozorenja**: Skočni prozori (*pop-up*) i zvučni alarmi aktiviraju se isključivo za *All-Time-New RDA* oblasti ili potpuno nove bandove, čime se eliminiraju suvišna ponavljanja.
* **Napredne kontrole**: Uključuje filter za prikaz isključivo novih slotova/oblasti te opciju *„Sakrij pop-up alert“* za neometano praćenje u pozadini.
* **Moderno sučelje (Black Night Style)**: Izrađeno pomoću `CustomTkinter` biblioteke u ugodnoj tamnoj temi, s punom prilagodljivošću veličine prozora (*resize*) i stabilnim radom na starijim operativnim sustavima (poput Windowsa 7).
* **Interaktivna RDA Cab Matrica**: Klikom na pojedinu RDA oblast otvara se vizualni matrični pregled potvrđenih i nedostajućih slotova po bandovima (od 160m do 10m) i modovima (CW, SSB, DIGI).

---

## 📦 Preduvjeti i instalacija

Prije pokretanja skripte, provjerite imate li instaliran Python te potrebne biblioteke:

```bash
pip install requests customtkinter python-socketio websocket-client

```

---

## 🚀 Pokretanje aplikacije

1. Provjerite imate li datoteku s ikonom `tnxqso2.ico` u istoj mapi.
2. Pokrenite skriptu iz naredbenog retka:

```bash
python tnxqso25.py

```

---

## ⚙️ Kompajliranje u izvršnu datoteku (.exe)

Ako želite kompajlirati aplikaciju u samostalni `.exe` program pomoću PyInstallera, koristite sljedeću naredbu:

```bash
pyinstaller --noconsole --onefile --icon=tnxqso2.ico --add-data "tnxqso2.ico;." tnxqso25.py

```

*Napomena: Osigurajte se da se datoteka `rda_slots.csv` uvijek nalazi u istoj mapi u kojoj pokrećete kompajliranu aplikaciju.*

---

## 🛠️ Tehnologije

* **Python** (Logika, dretve, obrada podataka)


* **CustomTkinter & Tkinter / ttk** (Korisničko sučelje i tablice)


* **Python-SocketIO** (Real-time komunikacija s RDA Cabinet clusterom)



```

```
