# pd5356-projekt-CONT

## Opis projektu

Projekt przedstawia mikroserwis do analizy plików FASTQ z wykorzystaniem FastQC oraz udostępniania wyników przez NGINX.

## Wykorzystane technologie

* Docker
* Docker Compose
* FastQC 0.12.1
* NGINX
* Ubuntu 22.04

## Struktura projektu

* Dockerfile
* docker-compose.yml
* nginx.conf
* input/
* images/

## Uruchomienie

```bash
docker compose up --build
```

Raport FastQC dostępny jest pod adresem:

```text
http://localhost:8080
```

## Architektura

Projekt wykorzystuje:

* kontener FastQC do analizy pliku FASTQ,
* kontener NGINX do hostowania raportu HTML,
* wolumen Docker `fastqc_results`,
* sieć Docker `fastqc_network`.

## Wynik

Raport FastQC został wygenerowany poprawnie i udostępniony przez NGINX.

