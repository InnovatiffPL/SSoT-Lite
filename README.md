# SSoT-Lite

Niniejsza dokumentacja dotyczy wdrożenia Fundamentalnego Systemu Orkiestracji (FSO) Coretex Hub — Minimalnie Satysfakcjonującego Produktu (MVP). FSO ma na celu transformację zarządzania operacyjnego w sektorze micro-SMB poprzez sieć zweryfikowanych Ekspertów, służących jako rozszerzenie wewnętrznych kompetencji firm.

Charakterystyka MVP: Projekt koncentruje się na walidacji modelu Value-Based Pricing (VBP) i pomiaru wartości (Time Savings ROI - TS-ROI). W fazie tej, architektura FSO opiera się na rygorze proceduralnym Single Source of Truth (SSoT), strategicznie neutralizując ograniczenia technologiczne narzędzi i skupiając się na funkcjonalnościach krytycznych dla pomiaru wartości. Dokument ten stanowi zarys i schemat wdrożonej architektury SSoT.

Jak to działa?

1. Podczas konsultacji agent wypełnia formę o kluczowych informacjach i wstępnych ustaleniach z klientem na projekt.


2. Tworzy się kontakt w systemie CRM; ekspert/klient. System zaciąga dane z formy dopisane do profilu klienta.


3. Tworzy się projekt w Jira połączony z ID eksperta.


4. System CRM dopasowuje eksperta do danego projektu. Ekspert ma wgląd do specyfikacji projektu i musi wstępnie go zaakceptować.


5. Po akceptacji eksperta otwiera się rekord projektu w Trello, który generuje task przypisany do projektu w Jira.


6. Następnie uzupełnia się metrykę projektu w Jira.


7. Projekt jest zawieszony w Jira dopóki klient nie przejdzie pełnego etapu credentialingu (ustali się wszystko i zbierze kompletną dokumentację w Trello).


8. Ekspert dostaje dostęp do projektu w Jira i może zacząć pracować na tasku.


9. Trello posiada funkcję helpdesk; przez odpowiednią formę mogą się kontaktować zarówno klienci jak i eksperci (medium kontaktowe w aktywnej fazie projektu).


10. Projekty są monitorowane z poziomu Trello i można je modyfikować/blokować jeśli jest taka konieczność.


11. Gdy projekt się kończy, eksportuje się cały projekt w CVS/xml i załącza do rekordu w Trello, następnie usuwa się z Jira.


Z czego korzysta?

Projekt wykorzystuje darmowe narzędzia do automatyzacji oraz przetwarzania danych. Dzieli się on na 6 głównych platform:

1. Formy Google
2. Listy Google
3. Trello
4. Jira
5. Obsidian
6. HubSpot CRM

Wymienione wyżej narzędzia stanowią warstwy SSoT, działając w sposób symbiotyczny; każde narzędzie jest w pewnym zakresie ze sobą powiązane. Razem tworzą architekturę SSoT w fazie testowania produktu.

Postawiłem na 4 filary projektu:

- Logika SSoT - do tego wykorzysuję Bank Wiedzy "Obsidian".

- Strategia i oprogramowanie służące do zarządzania interakcjami firmy z obecnymi i potencjalnymi klientami (CRM) - korzystam z "HubSpot" CRM.

- Przepływ pracy (bazujący na odrębnych projektach klientów) - każdy odrębny projekt jest bezpośrednio zarządzany w "Jira" przez ekspertów.

- Zarządzanie dokumentacją, komunikacją i kontrola nad przepływem procesów - Wszystko jest zarządzane i kontrolowane z poziomu "Trello".

Po agregacji danych ze wstępnej konsultacji do systemu CRM, ekspert akceptuje projekt, co przypisuje te dane w Jira. Następnie po zebraniu dokumentacji projekt się odblokowuje i ekspert nad nim pracuje. Do komunikacji na linii klient-firma-ekspert służy prosty system helpdesk zintegrowany z Trello, które jest również zintegrowane z Jira. Po zakończeniu projektu wszystkie dane z Jira (w tym metryka definiująca koszt i wartość projektu) są importowane spowrotem do Trello, po czym projekt się usuwa; kluczowe dane natomiast zostają.

Następne kroki to stworzyć system vettingu i credentialingu ekspertów oraz walidacji projektowej klienta. Stworzę jeszcze Agenta AI, który przeczyta dokumenty i zweryfikuje je z protokołami. Dodatkowo zautomatyzuje statusy projektowe i zarządzi dostępami.
