Ten dokument ma charakter poglądowy i nie zawiera szczegółów technicznych związanych z Coretex IP, agentami AI ani kodem źródłowym platformy.

# SSoT‑Lite  
Fundamentalny System Orkiestracji (FSO) – Coretex Hub MVP  

## Opis projektu  

SSoT‑Lite to Proof of Concept (PoC) dla minimalnie satysfakcjonującego produktu (MVP), obecnie w fazie bootstrapowej; opracowany w ramach projektu **Coretex Hub**, którego celem jest stworzenie skalowalnego zaplecza organizacyjnego dla firm sektora **micro‑SMB** – mikroprzedsiębiorstw i samozatrudnionych, którzy posiadają złożoność operacyjną, lecz nie mają zasobów, by zarządzać nią samodzielnie.  

Startup (Coretex) pełni rolę operatora i partnera technologicznego, który przejmuje na siebie zarządzanie procesami tych firm poprzez autorskie rozwiązania i kapitał intelektualny (Coretex IP). Sieć ekspertów jest wartością komplementarną i uruchamiana jest tylko wtedy, gdy projekt wymaga specjalistycznej wiedzy lub ponadprzeciętnej złożoności.  

Architektura projektu bazuje na zasadzie **Single Source of Truth (SSoT)** - jednego, spójnego źródła prawdy dla wszystkich procesów, narzędzi i decyzji biznesowych. System eliminuje ryzyko błędów międzywarstwowych, synchronizując dane w czasie rzeczywistym i zachowując pełną chronologię procesów.  

***

## Główne założenia  

SSoT‑Lite opiera się na połączonym ekosystemie narzędzi i agentów AI zarządzających danymi w sposób deterministyczny i kontrolowany:  

> Formularze Google - służą do zbierania danych ze spotkań konsultacyjnych z klientem.

> Arkusze Google - agregują i synchronizują dane operacyjne między warstwami.

> HubSpot CRM - pełni funkcję autorytatywnego rejestru (Master Record). Zawiera rejestry klientów, projektów i ekspertów.

> Jira - stanowi silnik logiki i realizacji zadań. To tutaj odbywa się pomiar wydajności i TS‑ROI (Time Savings Return on Investment).

> Trello - jest  centrum zarządzania zespołu Coretex (startupu). To repozytorium dokumentacji, w tym umów z klientami i ekspertami dla konkretnego  projektu. Każdy projekt posiada  własną kartę, która  jest walidowana z poziomu Trello w Jira i CRM. Eksperci nie mają tu dostępu.

> Obsidian - to  repozytorium logiki biznesowej (Coretex IP).  Zawiera wersjonowaną strukturę procesową, z instrukcjami zapisanymi  w języku znaczników (markup language),  czytelną  dla agentów  AI  i wykorzystywaną do walidacji operacji. Dostęp posiada jedna osoba – co chroni przed nadpisaniem lub manipulacją treścią.

***

## Jak to działa  

>Po wypełnieniu formularza konsultacyjnego dane trafiają automatycznie do CRM, gdzie model AI analizuje specyfikę projektu i dopasowuje ekspertów na podstawie danych profilowych. Model jest nieustannie trenowany i walidowany pod kątem dopasowań kompetencyjnych oraz wydajności.

> Proces credentialingu odbywa się po stronie ekspertów - jest to etap weryfikacji i  zbierania dokumentów, które  potwierdzają ich kwalifikacje  do konkretnego projektu. Na tym etapie agenci AI oceniają zgodność danych i zestawiają kompletność dokumentacji.  

> Eksperci otrzymują informację o projekcie –  ten, który pierwszy  zaakceptuje zlecenie, otrzymuje dostęp do pełnej specyfikacji i  briefingu w Jira,  a dopiero po  potwierdzeniu  gotowości  uruchamiany  jest projekt produkcyjny.  

>Jeden z agentów AI cyklicznie eksportuje metadane z Jira (do CSV/XML), co zapewnia chronologię i nieprzerwaną integrację danych. Po każdym eksporcie plik jest zewnętrznie archiwizowany w bezpiecznej chmurze, a także dodawany do portfolio klienta, które bazuje na tych samych metadanych z Jira i pełni funkcję trwałego rekordu projektowego. Takie działanie dodatkowo umacnia integralność informacji i ciąg procesowy.  

***

## System agentów AI

Każdy etap przepływu danych jest zarządzany przez sieć agentów AI działających we współpracy. Każdy agent ma ściśle zdefiniowaną rolę (logikę na podstawie plików z Obsidiana), a ich komunikacja oparta jest na architekturze RAG (Retrieval Augmented Generation), aby zapobiec kaskadowym błędom decyzyjnym.  

Nadrzędny agent AI nieustannie monitoruje spójność danych we wszystkich warstwach. Każda niespójność powoduje automatyczne wstrzymanie danego agenta i utworzenie raportu diagnostycznego, z dokładnym wskazaniem punktu i powodu błędu. Dzięki temu debugowanie i naprawa procesów odbywa się natychmiast – co eliminuje ryzyko rozchodzenia się niepoprawnych stanów w SSoT.  

***

## Kluczowe funkcjonalności

> Jedno źródło prawdy dla całego cyklu projektowego (SSoT).

> Dopasowywanie ekspertów przez walidowany model AI.

> Ciągły eksport i archiwizacja metadanych Jira w chmurze i portfolio klienta.

> Repozytorium umów i dokumentów projektowych w Trello (z walidacją do CRM i Jira).
 
> Weryfikacja danych na każdym etapie przez agentów AI z autokontrolą bieżących stanów.

> Mechanizmy RAG zapobiegające powstawaniu błędów kaskadowych.

> Obsidian jako repozytorium logiki systemu dla AI – wersjonowany, kontrolowany i zrozumiały dla modeli językowych.

> Pełny pomiar TS‑ROI (Time Savings ROI).

***

## Skalowalność i adaptacyjność

System jest skalowalny pionowo (zwiększanie liczby projektów i procesów operacyjnych) oraz adaptacyjny technicznie. Jego modularna architektura umożliwia łatwą migrację do bardziej zaawansowanych środowisk (np. Airtable, Notion, Make, n8n) lub rozszerzenie w pełnoprawną platformę iPaaS. Każda zmiana w systemie jest deterministycznie aktualizowana w całym cyklu danych, bez naruszania spójności lub historycznych rekordów.  

***

## Licencja

© 2025 Coretex / InnovatiffPL – Wszelkie prawa zastrzeżone.  
Projekt jest w fazie MVP i przeznaczony do celów badawczo‑rozwojowych oraz walidacyjnych. Wykorzystanie komercyjne wymaga pisemnej zgody właściciela IP.
Udostępnione informacje służą wyłącznie celom edukacyjnym i koncepcyjnym; kopiowanie lub wtórne użycie elementów procesowych, logiki systemu lub integracji AI bez zgody właściciela IP jest zabronione.
