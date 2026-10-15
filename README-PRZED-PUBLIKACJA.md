# Numi Step — publikacja polityki prywatności (PL + EN)

**Wydawca:** Grzegorz Kalinowski  
**Kontakt:** numistep@kalinowski.me  
**Stan dokumentów:** treść dostosowana do audytu kodu przekazanego przez Cursora, 16.10.2026. Strona nie została jeszcze opublikowana. To projekt informacyjny, nie niezależna opinia prawna.

## Zawartość

- `index.html` — polska strona, domyślna.
- `en/index.html` — angielska strona.
- `polityka-prywatnosci.md` — treść polska.
- `en/privacy-policy.md` — treść angielska.

## Ustalenia uwzględnione w dokumentach

- Nazwa aplikacji: **Numi Step**.
- Dane wydawcy i adres e-mail zostały wpisane do obu wersji językowych.
- Bez kont, własnego backendu, analityki, reklam i zewnętrznego crash reportingu.
- Profile, postępy, wyniki i materiały edukacyjne pozostają lokalnie w Room/DataStore.
- Auto Backup do chmury wyłączony (`allowBackup=false` oraz reguły backupu); możliwe niuanse transferu między urządzeniami zależne od Androida.
- Google Play Billing 9.1.0 obsługuje zakup miesięczny i Lifetime; informacje zakupowe nie zawierają postępów edukacyjnych.
- Eksport PDF odbywa się na żądanie użytkownika poprzez mechanizmy Androida.
- Korespondencja wysłana dobrowolnie do wydawcy podlega przetwarzaniu przy obsłudze zgłoszenia.

## Publikacja na GitHub Pages

1. Utwórz publiczne repozytorium GitHub, np. `numi-step-privacy`.
2. Umieść **zawartość tego folderu** w katalogu głównym repozytorium (nie sam folder jako dodatkowe zagnieżdżenie).
3. W GitHub: `Settings → Pages → Build and deployment → Deploy from a branch`; ustaw `main` oraz `/ (root)`.
4. Po publikacji strona będzie mieć adres np. `https://TWOJ-LOGIN.github.io/numi-step-privacy/`, a wersja angielska `/en/`.
5. Sprawdź oba adresy bez logowania, także na telefonie. Linki językowe powinny działać w obie strony.
6. Ten **rzeczywisty adres** wpisz w Play Console i do `legal_privacy_policy_url` (zachowaj spójność wszystkich obsługiwanych plików `strings.xml`).
7. `legal_terms_url` zostaw pusty, jeśli nie publikujesz jeszcze odrębnego regulaminu. Nie ustawiaj linku do polityki jako regulaminu.

## Przed opublikowaniem aplikacji w Google Play

- Upewnij się, że w Play Console wydawca i nazwa aplikacji są spójne z polityką.
- Skontroluj końcowy **release AAB**, jego scalony manifest, zależności i faktyczne przepływy danych. Audyt kodu jest dobrym punktem wyjścia, lecz nie zastępuje testów release.
- Sprawdź zgodność sekcji **Data safety (Bezpieczeństwo danych)** z rzeczywistym zakresem danych. Nie zakładaj automatycznie, że wszystkie pola dotyczące zbierania danych powinny mieć odpowiedź „nie”: pytania o historię zakupów i dane obsługiwane przez SDK mogą wymagać osobnej oceny.
- Sprawdź zgodność aplikacji z zasadami Families, jeżeli w Play Console deklarujesz dzieci w grupie docelowej.
- Sprawdź, czy polityka jest dostępna także z aplikacji i czy link otwiera się bez błędów.
- Rozważ formalną weryfikację prawną, szczególnie przed większą sprzedażą lub wejściem na kolejne rynki.

## Oficjalne źródła do weryfikacji

- Google Play — User data: https://support.google.com/googleplay/android-developer/answer/10144311
- Google Play — Data safety: https://support.google.com/googleplay/android-developer/answer/10787469
- Google Play — zasady prywatności: https://support.google.com/googleplay/android-developer/answer/18258653
- Android — Auto Backup: https://developer.android.com/identity/data/autobackup
