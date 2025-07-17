# VM: monitor

## OS
Ubuntu Server

## Uloga
Nadzor mrežnog prometa i perfomansi sustava.

## Postavljanje
Instaliraj alate: ELK stack, grafana stack

Tok logova:
    filebeat -> elasticsearch -> kibana
    nodeexporter -> prometheus -> grafana
