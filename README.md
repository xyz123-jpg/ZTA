# ZTA Implementacija – Diplomski Rad

Ovaj projekt sadrži praktičnu implementaciju **Zero Trust Architecture (ZTA)** u simuliranom mrežnom okruženju koristeći više virtualnih mašina.

## 🖥️ Korištene virtualne mašine

| Naziv VM-a    | Svrha                                      |
|---------------|---------------------------------------------|
| `client`      | Krajnji korisnik                            |
| `admin`       | Administratorski pristup                    |
| `monitor`     | Nadgledanje prometa (npr. Zabbix, Grafana)  |
| `pfsense`     | Firewall i segmentacija                     |
| `database`    | MySQL/PostgreSQL server                     |
| `app`         | Web aplikacija (npr. NGINX + backend)       |
| `ldap`        | Autentifikacija (OpenLDAP)                  |
| `iam`         | Identity & Access Management (Keycloak)     |
| `monitoring`  | Sistemski i mrežni nadzor                   |

## 🧩 Arhitektura


## 📁 Sadržaj

- `konfiguracije/` – konfiguracijske datoteke za svaku VM
- `skripte/` – automatizacija deploya i podešavanja servisa
- `vm-upute/` – kratke upute kako postaviti svaku VM
- `dokumentacija/` – PDF rada, dijagrami i topologija

## 🚀 Pokretanje

1. Pripremi devet VM-ova prema uputama u `vm-upute/`
2. Uredi konfiguracijske fajlove prema mrežnim postavkama
3. Pokreni `skripte/deploy.sh` za inicijalno postavljanje
4. Koristi `monitoring-setup.sh` za postavljanje nadzora

> Napomena: VM-ovi nisu uploadani zbog veličine. Možeš ih kreirati prema uputama.



