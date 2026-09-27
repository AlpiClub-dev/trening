# Plan — trening pod hipertrofię w ~40 minut

Apka PWA na telefon. Jeden plik `index.html`, bez backendu, bez konta, bez internetu po pierwszym
wejściu. Wszystko siedzi w pamięci przeglądarki, kopię danych robisz do pliku JSON.

To następca starszej apki (trening + liczenie kalorii + woda + pomiary). Tu został **sam plan
treningowy**. Liczenie jedzenia, wody i pomiarów wyleciało.

## Co się zmieniło w samym planie

Stara wersja: 4 × 75 minut w planie, w praktyce schodziło po półtorej godziny.
Nowa: **4 × 37-40 minut**, serie robocze na RIR 0-2.

| | stare | nowe |
|---|---|---|
| czas sesji | 75-90 min | 37-40 min |
| tydzień | ~300-360 min | ~153 min |
| martwy ciąg klasyczny | tak | nie, został RDL |
| przerwy | pojedynczo, 2,5-3 min stania | pary naprzemienne |
| izolacje | 3-5 osobnych serii | myo-reps (1 + 3) |
| przedramiona | brak | 9 serii / tydzień |
| brzuch | 2 ćwiczenia | 4 ćwiczenia, 10 serii / tydzień |
| rozciąganie po treningu | 5 min | wypadło |

Trzy rzeczy zrobiły całą robotę:

1. **Pary naprzemienne.** Ćwiczenia chodzą po dwa (np. wyciskanie skos ↔ podciąganie). Mięsień
   dostaje te same 2,5-3 minuty regeneracji, ale w przerwie pracuje drugi, więc zegar chodzi
   o połowę krócej.
2. **Myo-reps na izolacjach.** Jedna seria do upadku, 15 s, trzy dobitki po 3-5 powtórzeń.
   Bodziec porównywalny z 4 osobnymi seriami, czas o dwie trzecie mniejszy.
3. **Wycięta objętość z zapasem.** 9-12 twardych serii na partię tygodniowo zamiast 20 serii
   z RIR 3. Seria, po której zostają trzy powtórzenia, kosztuje tyle samo czasu, a buduje ułamek.

Martwy ciąg klasyczny wypadł, bo RDL daje to samo dla tyłu uda i pośladka przy kilku razy mniejszym
zmęczeniu i bez 10 minut na rozbieganie.

## O przerwach

W karcie ćwiczenia jest przerwa **między ćwiczeniami pary**, a nie cała przerwa dla mięśnia —
apka dopisuje obok, kiedy realnie wracasz do tej samej sztangi (np. „przerwa 60 s · wracasz tu
co ~3 min 25 s"). Na dole cykl wynosi ~4 min.

Osobna sprawa to **15 sekund w bloku końcowym**: to nie jest przerwa między seriami, tylko odstęp
w środku myo-reps, czyli jednej serii rozciągniętej na dobitki. Seria do upadku → 15 s → 3-5
powtórzeń → 15 s → 3-5. Dotyczy wyłącznie izolacji, nigdy boju.

Jeśli i tak jest za krótko: przełącznik **Spokojne tempo** na karcie Planu dokłada 30 s do każdej
przerwy (myo-reps 20 s zamiast 15). Sesje robią się wtedy 44-48 min.

## Plan

| dzień | sesja | ćwiczenia | czas |
|---|---|---|---|
| poniedziałek | Góra A | skos + podciąganie / OHP hantle + wiosło hantlem / myo: bok barku, triceps, młotkowe, nadgarstki | ~37 min |
| wtorek | Dół A | przysiad + łydki stojąc / suwnica + uginanie leżąc / wznosy nóg, Pallof press | ~38 min |
| czwartek | Góra B | dipy + wiosło sztangą / ściąganie + rozpiętki / myo: bok barku, face pull, biceps, reverse curl | ~38 min |
| piątek | Dół B | RDL + łydki siedząc / bułgarskie + prostowanie / uginanie siedząc, spięcia na wyciągu, rollout | ~40 min |

Objętość tygodniowa (twarde serie, blok myo liczony jak trzy zwykłe serie, partie pomocnicze po pół):
plecy 13,5 · biceps 13,5 · czworogłowe 10 · brzuch 10 · klatka 9 · triceps 9 · przedramię 9 ·
dwugłowe 8 · pośladek 8 · bark bok 6 · łydki 6 · bark przód 4,5 · bark tył 2.
Apka pokazuje tę listę na karcie Planu i przelicza ją też dla trybu 25 minut.

Ciężary startowe pochodzą z logu ze starej apki (skos 50 kg, podciąganie +12 kg, dipy +15 kg,
wiosło hantlem 18 kg, wznosy bokiem 6 kg, triceps 20 kg, face pull 12,5 kg i reszta). Ćwiczenia
na nogi są oznaczone jako testowe, bo tam danych nie było.

## Funkcje

- **Tryb 25 minut** — zostają duże boje i blok końcowy, wypada środkowa para. Na dni, w których
  wybór jest między krótkim treningiem a żadnym.
- **Spokojne tempo** — +30 s do każdej przerwy, myo-reps 20 s zamiast 15.
- **Objętość tygodniowa** — ile twardych serii dostaje każda partia, z przedramionami i brzuchem.
- **Progresja automatyczna** — górny zakres powtórzeń we wszystkich seriach → apka podnosi ciężar
  o realny skok sprzętu (hantle 2 kg, sztanga i stos 2,5 kg, maszyny na nogi 5 kg). Dwie nieudane
  serie → zjazd o 10%. W myo-reps liczy się seria aktywacyjna.
- **Timer przerwy** z dźwiękiem i wibracją, ustawiany sam po odhaczeniu serii; w parze podpowiada,
  które ćwiczenie jest teraz.
- **Zegar sesji** z budżetem czasu policzonym z planu.
- **Deload** co 8 tygodni: połowa serii, te same ciężary, bez ruszania progresji.
- **Progres** — wykres szacowanego maksimum (Epley) w każdym ćwiczeniu, historia sesji, tygodniowe
  serie, tonaż i średnia długość treningu.
- **Kopia do pliku i z pliku** — import czyta też backup ze starej apki (bierze ciężary i historię
  treningów, resztę pomija).

## Uruchomienie

Lokalnie: dowolny serwer statyczny, np. `npx http-server -p 8080`, i wejście na `http://localhost:8080`.
Samo otwarcie pliku przez `file://` też działa, poza service workerem.

Na telefonie: wejść na adres GitHub Pages i dodać do ekranu głównego („Udostępnij → Do ekranu
początkowego” na iOS). Wtedy chodzi na pełnym ekranie i offline.

### GitHub Pages

Settings → Pages → Source: *Deploy from a branch*, gałąź `claude/workout-plans-app-3cem7q`
(albo `main`, jeśli zmiany trafią tam), katalog `/ (root)`.

## Pliki

```
index.html            cała apka: plan, logika progresji, widoki, style
sw.js                 service worker (offline)
manifest.webmanifest  PWA
icon.svg / *.png      ikony
```
