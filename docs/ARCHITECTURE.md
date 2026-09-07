# ARCHITECTURE

## Moduły JARVIS

### Wellbeing / Daily Journal

JARVIS posiada warstwę wspierającą codzienne funkcjonowanie użytkownika: pamiętnik, krótkie check-iny, obserwację wzorców zachowań, cele dnia i doraźne podpowiedzi.

Założenia:
- wejście może być bardzo krótkie i naturalne, np. „wstałem o 8:20”, „ciągnie mnie do sklepu”, „mam dziś niski nastrój”;
- JARVIS porządkuje wpis do struktury dnia bez oceniania użytkownika;
- wykrywa powtarzające się triggery i kontekst (np. nuda, samotność, stres, określona pora dnia);
- rozróżnia fakt od interpretacji;
- preferuje małe, konkretne działania możliwe do wykonania od razu;
- nie resetuje całego planu po pojedynczym potknięciu;
- może prowadzić trendy i podsumowania tygodniowe, gdy dane są dostępne;
- przy sygnałach wymagających pomocy medycznej lub kryzysowej przełącza się z trybu coachingowego na tryb bezpieczeństwa.

### Prywatność danych wellbeing

Repozytorium `jarvis-intro` zawiera wyłącznie logikę i dokumentację modułu. Nie zapisujemy w nim osobistych wpisów dziennika, informacji zdrowotnych, danych o używkach, relacjach ani innych wrażliwych danych użytkownika.

Dane dziennika powinny docelowo trafiać wyłącznie do prywatnej warstwy JARVIS (lokalnej bazy lub prywatnego backendu) z kontrolą dostępu i możliwością usunięcia danych przez użytkownika.

Szczegóły modułu: `docs/WELLBEING.md`.
