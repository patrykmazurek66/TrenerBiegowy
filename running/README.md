# Dziennik biegowy

Przestrzeń do dokumentowania treningów i przygotowań do półmaratonu.

## Pliki
- [Profil](profile.md) — cel, kontekst i historyczne punkty odniesienia.
- [Indeks treningów](training-log.md) — krótkie zestawienie wykonanych sesji.
- [Plan](plan.md) — ustalenia dotyczące przyszłych treningów, oddzielone od wykonania.
- [Sesje](sessions/2026-11-17.md) — szczegółowe wpisy; źródło prawdy o wykonaniu.

## Zasady danych
- Szczegółowe wpisy w `sessions/` są źródłem prawdy. W razie rozbieżności poprawiamy indeks na podstawie sesji.
- Plan i wykonanie pozostają oddzielone; planowane treningi nie trafiają do indeksu wykonanych sesji.
- Oddzielamy dane i odczucia użytkownika, wartości obliczone oraz interpretacje i rekomendacje.
- Nie wymyślamy brakujących danych. Braki oznaczamy „niepodane” lub „—”, nigdy automatycznie jako zero.
- Niepodany ból nie oznacza braku bólu.
- RPE zapisujemy w skali 0–10; RPE końcówki nie zastępuje RPE całego treningu.
- Daty: YYYY-MM-DD. Czasy i prędkości zawsze z jednostkami. Oddzielamy czas całkowity od czasu części głównej.
- Dystans opisujemy źródłem: odczyt bieżni, GPS albo obliczony z odcinków. Brak odczytu pozostaje brakiem.
- Nie wyliczamy tempa samego biegu ze średniej obejmującej marsz, rozgrzewkę i schłodzenie.
- Nie przypisujemy treningom nieznanych dat. Historyczne punkty bez daty pozostają w profilu, nie jako osobne sesje.
- Stosujemy względne odnośniki między plikami.

## Aktualizacja
1. Użytkownik podaje wykonanie i odczucia zwykłą wiadomością.
2. Tworzymy lub aktualizujemy szczegółowy wpis sesji.
3. Aktualizujemy odpowiadający mu wiersz indeksu.
4. Późniejsze informacje o regeneracji dopisujemy do tej samej sesji z datą i porą obserwacji, jeśli jest znana; nieznanej pory nie wymyślamy.
5. Pytamy tylko o braki istotne dla interpretacji. Pola opcjonalne mogą pozostać nieuzupełnione.
6. Planowane treningi zapisujemy tylko w planie.
7. Zmiany planu zapisujemy z datą i powodem.
8. Nie zwiększamy automatycznie obciążenia po jednym udanym treningu.

## Szablon szczegółowej sesji
```markdown
# YYYY-MM-DD — rodzaj treningu

## Informacje i plan
- Data: YYYY-MM-DD.
- Rodzaj: niepodane.
- Cel: niepodany.
- Miejsce: niepodane (bieżnia / na zewnątrz).
- Plan: niepodany; jeśli znany, opisz odcinki i różnice względem wykonania.
- Opcjonalnie: nachylenie, warunki, tętno, sen, buty, ostatni FBW nóg — tylko jeśli podane.

## Wykonanie — dane użytkownika
| Kolejność | Etap | Czas | Prędkość / tempo |
|---|---|---|---|
| — | niepodane | — | — |

- Czas całkowity: niepodany.
- Czas części głównej: niepodany.
- Dystans i źródło (bieżnia / GPS / obliczony z odcinków): niepodane.
- Różnice względem planu: niepodane.

## Odczucia — relacja użytkownika
- RPE całej sesji (0–10): niepodane.
- RPE kluczowych odcinków lub końcówki (0–10): niepodane.
- Oddech: niepodany.
- Zapas: niepodany.
- Ból: niepodany.

## Wartości obliczone
Niepodane; ewentualne obliczenia opisuj wraz z podstawą i oddziel od pomiarów.

## Regeneracja — relacja użytkownika
- Data obserwacji: niepodana; pora opcjonalna.
- Obserwacje: niepodane.

## Interpretacja robocza — ocena, nie relacja użytkownika
Brak oceny.

## Ustalenia dotyczące dalszych treningów
Brak ustaleń. Dodawaj wyłącznie faktycznie podjęte ustalenia, z datą; propozycja nie oznacza wykonania.
```
