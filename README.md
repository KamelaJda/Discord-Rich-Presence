# Discord Rich Presence

## Jak uruchomić?

1. Pobierz najnowszy plik `.jar` [KLIK](https://github.com/KAMIL0024/Discord-Rich-Presence/releases)
2. Uruchom program wpisując komendę w konsoli `java -jar DiscordRPC.jar`
3. Przy pierwszym uruchomieniu stworzy się plik `config.json`. Ustaw go do swoich potrzeb.


## Konfiguracja

```
{
  "applicationId": "tutaj dać id aplikacji",
  "state": "pierwszy wyświetlany napis",
  "details": "napis pod tym - zostaw "" aby tego nie było",
  "date": {
    "start": liczba startu w unixie. Ustaw 0 żeby była na teraz lub na -1 żeby tego nie było,
    "end": liczba końca w unixie. Ustaw -1 żeby program tego nie wliczał
  },
  "imageLarge": {
    "key": "nazwa duża zdjęcia (zdjecie musi być w aplikacji wstawione)",
    "text": "tekst po najechaniu na zdjęcie"
  },
  "imageSmall": {
    "key": "nazwa małego zdjęcia"
  },
  "party": {
    "partySize": Ilość osób. Ustaw -1 żeby program tego nie wliczał,
    "partyMax": 9
  }
}
```
Przykładowy config:
```json
{
  "applicationId": "720384857921814648",
  "state": "Eloelo",
  "details": "test1",
  "date": {
    "start": -1,
    "end": -1
  },
  "imageLarge": {
    "key": "test",
    "text": "siema"
  },
  "imageSmall": {
    "key": "test1"
  },
  "party": {
    "partySize": 6,
    "partyMax": 9
  }
}
```

Efekt z wykorzystaniem przykładowego configu

![tak](https://cdn.discordapp.com/attachments/549359078342787092/720406623327223838/unknown.png)

## Jak stworzyć aplikacje?
1. Wchodzisz [tutaj](https://discord.com/developers/applications/).
2. Klikasz przycisk na prawym rogu `New Application`.
3. Pod nazwą masz jego ID, przyda się do uzupełnienia klucza `applicationId` w configu.
4. Przejdź do sekcji Rich Presence (po lewej to jest)
5. Kliknij `Add Image(s)`. Nazwy zdjęć będą odpowiadać za klucze `key` w configu.
6. Zapisz i gotowe.

## Komendy w konsoli

Możesz używać AŻ dwóch komend w konsoli (po odpaleniu programu ofc)

	1. stop   - Zatrzymuje program.
	2. reload - Aktualizuje Rich Presence (jeżeli zmieniłeś coś w configu to, to wpisz).
