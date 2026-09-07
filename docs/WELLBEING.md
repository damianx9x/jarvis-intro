# JARVIS Wellbeing / Daily Journal

## Cel

Moduł ma działać jako lekki pamiętnik i warstwa doraźnego wsparcia. Użytkownik nie musi wypełniać formularzy — może pisać naturalnie, a JARVIS porządkuje dane i proponuje następny mały krok.

## Model wpisu dnia

Przykładowe pola:

```json
{
  "date": "YYYY-MM-DD",
  "wake_time": null,
  "work_start": null,
  "work_end": null,
  "food": [],
  "hydration": null,
  "mood_1_10": null,
  "energy_1_10": null,
  "activities": [],
  "triggers": [],
  "substance_log": [],
  "social_contact": [],
  "notes": [],
  "wins": [],
  "next_small_step": null
}
```

## Zasady działania

1. **Bez moralizowania.** Opisujemy fakty i wzorce, nie wartość użytkownika.
2. **Małe kroki.** Preferowane są działania na najbliższe 10–60 minut zamiast wielkich deklaracji.
3. **Potknięcie nie zeruje planu.** Kolejna decyzja jest nowym punktem wejścia.
4. **Triggery są danymi.** JARVIS zapisuje kontekst poprzedzający zachowanie: nuda, samotność, stres, konflikt, pora dnia, brak jedzenia itd.
5. **Rozdzielenie impulsu od działania.** Gdy jest to bezpieczne, system może sugerować opóźnienie decyzji i zmianę kontekstu.
6. **Relacje.** System obserwuje, czy intensywne szukanie kontaktu nie pogłębia poczucia odrzucenia i sugeruje mniej obciążające formy kontaktu.
7. **Żywienie i objawy fizyczne.** JARVIS może prowadzić dziennik objawów, ale nie zastępuje diagnostyki medycznej.
8. **Bezpieczeństwo.** Przy objawach alarmowych albo sygnałach kryzysu system porzuca zwykły coaching i rekomenduje odpowiednią pomoc.

## Cele i open loops

Moduł może utrzymywać aktywne cele w rodzaju:
- poranny start dnia,
- regularne jedzenie i nawodnienie,
- ograniczanie wybranego zachowania według ustalonego celu,
- przerwanie określonego automatu zachowania,
- minimum jednej wartościowej aktywności dziennie,
- kontakt społeczny bez presji na natychmiastową odpowiedź.

Cele powinny mieć status: `active`, `paused`, `completed`, `needs_review`.

## Check-in

Minimalny wieczorny check-in:
- nastrój 1–10,
- energia 1–10,
- co dziś pomogło,
- co było triggerem,
- co zrobiłem mimo trudności,
- jaki jest jeden następny krok na jutro.

## Integracja z iOS / Shortcuts

Docelowo moduł może przyjmować check-iny z iOS Shortcuts, np. po alarmie pobudki, o określonej godzinie lub po zakończeniu pracy. Skrót powinien przekazywać tylko minimalny zestaw danych potrzebny do aktualnego check-inu.

## Prywatność

Dane osobiste i zdrowotne nie mogą być commitowane do publicznego repozytorium. `jarvis-intro` przechowuje wyłącznie definicję modułu i interfejs. Właściwe wpisy powinny znajdować się w prywatnym magazynie danych JARVIS.
