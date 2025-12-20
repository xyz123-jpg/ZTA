# ZTA Implementacija

Ovaj projekt sadrži praktičnu implementaciju Zero Trust Architecture (ZTA) u simuliranom mrežnom okruženju koristeći više virtualki.

##  Korištene virtualke

| Naziv VM-a    | Svrha                                      |
|---------------|---------------------------------------------|
| `client`      | Krajnji korisnik                            |
| `admin`       | Administratorski pristup                    |
| `monitor`     | Nadgledanje prometa                         |
| `pfsense`     | Firewall i segmentacija                     |
| `database`    | MySQL/PostgreSQL server                     |
| `app`         | Web aplikacija                              |
| `ldap`        | Autentifikacija (OpenLDAP)                  |
| `iam`         | Identity & Access Management (Keycloak)     |
| `monitoring`  | Sistemski i mrežni nadzor (Grafana, Kibana) |

##  Arhitektura
<img width="1023" height="603" alt="{ABA8E9E3-F08C-4DFA-8501-0656DD6FDAF4}" src="https://github.com/user-attachments/assets/375a06c8-0468-4529-b200-d0161320adce" />


##  Firewall PfSense

U simuliranom okruženju, pfSense je postavljen kao perimetarski i interni firewall, u skladu s principima Zero Trust Architecture (ZTA), nikome ne vjeruje po defaultu, čak ni internom prometu.

Firewall ima WAN interface izlaz prema internetu i više LAN/VLAN interface za logičku i sigurnosnu segmentaciju mreže.

<img width="1280" height="800" alt="pfsense Conf" src="https://github.com/user-attachments/assets/2515185a-150f-4f55-a050-3ac28c610a79" />
<img width="1280" height="800" alt="pfsense implmentacija segmentacije" src="https://github.com/user-attachments/assets/a50f2e40-6dee-4ad0-9885-857881b3d486" />

##  ELK stack

<img width="1204" height="720" alt="diplomski block rule" src="https://github.com/user-attachments/assets/04c06e28-6358-4c30-b8af-5d73fbe4339e" />
<img width="972" height="481" alt="image" src="https://github.com/user-attachments/assets/f242b707-3864-4558-b0b0-86b0b1f9421d" />
ELK Stack je centralizirani sustav za prikupljanje, obradu, pretragu i vizualizaciju logova i događaja u realnom vremenu. Naziv dolazi od tri glavne komponente:

Elasticsearch
Logstash
Kibana

##  Grafana i Prometheus
<img width="974" height="550" alt="image" src="https://github.com/user-attachments/assets/b2e8743c-ca63-422d-bdb7-c0954e735e50" />
Kombinacija Prometheusa i Grafane omogućava brzu detekciju anomalija (CPU spike, latency baze, network zagušenje) bez narušavanja Zero Trust arhitekture.

##  IAM
<img width="974" height="351" alt="image" src="https://github.com/user-attachments/assets/f3c3c7a4-a318-42f7-a17a-314a195fb1ca" />
<img width="581" height="456" alt="oidc keycloak" src="https://github.com/user-attachments/assets/117aafff-a61e-40c5-8889-1c0262308bf0" />
Pristup aplikacijama iz user subnet-a dozvoljen je samo nakon uspješne autentikacije i validacije tokena.

##  Testiranje
<img width="1280" height="800" alt="overload" src="https://github.com/user-attachments/assets/dcd8f187-1ac0-43f1-8e6c-e41f0a1b486c" />
Prikaz metrika pod simuliranim napadom (veći broj upita) što dovodi do većeg korištenja resursa servera koji "okidaju" alarme koji su postavljeni npr. ako je korištenje CPU veće od 80% alarm šalje mail na admin adresu i sl.
