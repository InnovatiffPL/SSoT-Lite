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

Przepływ pracy:

Przepływ pracy procesu od konsultacji po finalizację projektu:

Platforma rozróżnia trzy typy użytkowników:

Admin: Zarządza projektem i może nanosić modyfikacje, lub blokować procesy.
Ekspert: Zarządza projektem z poziomu Jira, dokumentuje, aktualizuje i realizuje go.
Klient: Dostarcza kluczowych danych o projekcie.

Każdy ekspert jest uprzednio weryfikowany dzięki procesowi vettingu; zdobywa się dokumentację niezbędną do weryfikacji działalności (np. numer KRS), portfolio (jeśli możliwe), sprawozdanie w formie dokumentu, formularz zgłoszeniowy, rozmowa weryfikacyjna. Dopiero zbiór tych danych jest odpowiednio filtrowany przez Agenta AI, który podejmuje decyzję o dołączeniu lub wykluczeniu eksperta z dalszego procesu.

Jeśli ekspert przechodzi ten etap pozytywnie, generuje się jego profil w systemie CRM i zakłada osobnego maila/konto dla Jira. Na tym etapie ekspert nie ma jeszcze dostępu do konta.

Po krótkiej konsultacji wstępnej z klientem szacuje się złożoność i cenę za projekt, na podstawie której uzupełniane są kluczowe dane dotyczące złożoności i wyceny projektu. Dane te są agregowane do systemu CRM, tworząc profil klienta i generuje się rekord w Trello (z pełną specyfikacją projektu) - na tym etapie kompletuje się potrzebną dokumentację od klienta zarówno jak i ustala plan działań. Wszelkie metryki i dane są uzupełniane, a następnie system tworzy kartę projektu, która jest porównywana z istniejącą siecią ekspertów przez Agenta AI i następuje proces credentialingu.

Każdy dopasowany ekspert dostaje powiadomienie o dostępnym projekcie, posiadając wstępne informacje o projekcie. Pierwszy klient, który zaakceptuje wstępnie projekt zostaje do niego przypisany. Na tym etapie Agent ustala szczegóły wyceny i projektu z ekspertem, briefuje go do schematu pracy i szczegółów projektu, po czym otwiera się projekt w Jira (za pomocą automatyzacji z Trello) i nadaje dostęp ekspertowi.

Kluczowym elementem w aktywnej fazie projektu jest możliwość kontaktu ze strony klienta i eksperta przez zintegrowany system helpdesk, co służy jako medium komunikacyjne na linii klient-firma, ekspert-firma. To spełnia warunek pełnej kontroli i odpowiedzialności za projekt przez Coretex; w tym jakość komunikacji między stronami.

Ekspert pracuje na zadaniach, do których można tworzyć zadania podrzędne (główne zadanie to tylko pełna specyfikacja projektu i orientacja co należy wykonać), dopiero te zadania podrzędne definiują odrębne prace jakie wykona ekspert. Do każdego zadania należy załączyć dokumentację potwierdzającą wykonanie, w tym czasie kalkuluje się czas pracy eksperta na każdym zadaniu i zadaniu nadrzędnym - co później jest wykorzystane do kalkulacji TS-ROI.

Gdy ekspert zakończy pracę na projekcie, aktualizuje jego status w Jira, po czym eksportuje pełne metadane z projektu i załącza w komentarzu na głównym zadaniu. Ten dokument jest później agregowany do rekordu w Trello, po czym projekt w Jira się usuwa. Następnie tworzy się dedykowane portfolio w osobnym systemie dla eksperta w oparciu o te wyeksportowane dane z projektu.

Wszelkie dane i dokumentacja są pierw wpisywane do Trello, a po zakończeniu projektu bądź w razie nanoszenia istotnych poprawek - aktualizowane. Stanowi to główny punkt odniesienia integracji i kontroli nad danymi i procesem. Każde zadanie z Jira może być bezpośrednio kontrolowane i modyfikowane z poziomu Trello, wszystkie dokumenty wraz z informacjami są przechowywane na rekordzie projektowym (karcie), komunikacja odbywa się również przez zintegrowany helpdesk w Trello w czasie rzeczywistym; w tym obsługa e-maili.
