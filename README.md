# ZTA Implementacija

Ovaj projekt sadrži praktičnu implementaciju **Zero Trust Architecture (ZTA)** u simuliranom mrežnom okruženju koristeći više virtualnih mašina.

##  Korištene virtualne mašine

| Naziv VM-a    | Svrha                                      |
|---------------|---------------------------------------------|
| `client`      | Krajnji korisnik                            |
| `admin`       | Administratorski pristup                    |
| `monitor`     | Nadgledanje prometa (npr. Zabbix, Grafana)  |
| `pfsense`     | Firewall i segmentacija                     |
| `database`    | MySQL/PostgreSQL server                     |
| `app`         | Web aplikacija                              |
| `ldap`        | Autentifikacija (OpenLDAP)                  |
| `iam`         | Identity & Access Management (Keycloak)     |
| `monitoring`  | Sistemski i mrežni nadzor (Grafana, Kibana) |

##  Arhitektura
<img width="1023" height="603" alt="{ABA8E9E3-F08C-4DFA-8501-0656DD6FDAF4}" src="https://github.com/user-attachments/assets/375a06c8-0468-4529-b200-d0161320adce" />


##  Sadržaj

- `skripte/` – u izradi
- `vm-upute/` – kratke upute kako postaviti svaku VM
- `dokumentacija/` – PDF rada, dijagrami i topologija

##  Pokretanje

1. Pripremi devet VM-ova prema uputama u `vm-upute/`
2. Uredi konfiguracijske fajlove prema mrežnim postavkama



