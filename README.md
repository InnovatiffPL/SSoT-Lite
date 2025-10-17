# SSoT-Lite

Niniejszy projekt jest wciąż rozwijającą się wersją MVP dla Startupu, którego założeniem jest zarządzanie operacyjne i tworzenie rozwiązań dla firm micro-SMB, oraz budowanie sieci ekspertów, służących jako przedłużenie kompetencji firmy. W fazie MVP postawiłem na uproszczoną architekturę SSoT, która posiada znaczne ograniczenia technologiczne. Dokument ten stanowi zarys i schemat SSoT.

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


12. Gdy projekt się kończy, eksportuje się cały projekt w CVS/xml i załącza do rekordu w Trello, następnie usuwa się z Jira.


Z czego korzysta?

Projekt wykorzystuje darmowe narzędzia do automatyzacji oraz przetwarzania danych. Dzieli się on na 6 głównych platform:

1. Formy Google
2. Listy Google
3. Trello
4. Jira
5. Obsidian
6. HubSpot CRM

Wymienione wyżej narzędzia stanowią warstwy SSoT, działając w sposób symbiotyczny; każde narzędzie jest w pewnym zakresie ze sobą powiązane. Razem tworzą architekturę SSoT w fazie testowania produktu.
