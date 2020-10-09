+++
date = "2000-01-01T00:00:00+00:02"
title = "Artist"
description = "Shows all available API Operatings for Artist"
toc = true
+++

An artist is generally a musician (or musician persona), group of musicians, or other music professional (like a producer or engineer). Occasionally, it can also be a non-musical person (like a photographer, an illustrator, or a poet whose writings are set to music), or even a fictional character. For some other special cases, see special purpose artists.

**Name**

The artist's name is the official name of an artist, whether it is a person, band, or character. In most cases, it is the name as found on releases.

**Definite articles and titles**

Only include [definite articles](https://en.wiktionary.org/wiki/definite_article) (like "The", "El" or "Der") and honorary titles (like "Sir" or "MBE") if they're used by the artist as part of its name. If it's not clear, leave them out, and just add them to the artist's credit when printed.

## Sort name

### Guidelines

1. Person artist names have sort name "family name, given name".
   1. Middle names and nicknames should be treated as a part of the given name.
   1. Names beginning with an abbreviated title, such as Dr., DJ, or MC should have the title treated as if it were a part of the given name.
   1. Family names which begin with an abbreviation should have the abbreviation expanded in the sort name.
   1. Suffixes like "Jr." and "Sr." should be listed after the given name.
2. Group artist names beginning with an article (a, an, the, etc.) have the article moved to the end of their sort name.
    1. Where a real person's name appears in a group artist's name, the artist's sort name should be the sort name for that person, followed by the remainder of the group artist's name.
3. The main artist sort name should be in Latin script for compatibility reasons. If the artist's name is normally written using a non-Latin script, use the Latin script translated or transliterated name by which the artist is most commonly known.
4. For artist names containing stylized characters, change those characters to their equivalent Latin script letter, removing any style-only punctuation, spacing, or other characters, unless the artist's name contains only stylized characters, which have no inherent meaning to translate, and which cannot be transliterated.
5. Artist sort names should retain all Latin [diacritics](https://en.wikipedia.org/wiki/Diacritic#Types) present in the artist name.

### Examples

All examples should be interpreted as clarification upon the guidelines; no new guidelines should be interpreted from any example.

**Guideline 1. Name of a person**

* Eric Clapton has sort name "Clapton, Eric"
* Eötvös Péter has sort name "Eötvös, Péter" (name follows Hungarian "Surname Name" order, but the sort name is unaffected)
* Hildur Guðnadóttir has sort name "Hildur Guðnadóttir" (Guðnadóttir is a patronymic, not a surname, as custom in Iceland)
* * But: Ólafur Arnalds has sort name "Arnalds, Ólafur" (Arnalds is a surname, not a patronymic)
* Harry Connick, Jr. has sort name "Connick, Harry, Jr."

**Guideline 1.1. Middle names and nicknames**

* Jean 'Toots' Thielemans has sort name "Thielemans, Jean 'Toots'"

**Guideline 1.2. Name begins with an abbreviated title**

* DJ Shah has sort name "Shah, DJ"
* SPC Stephen Pauls has sort name "Pauls, SPC Stephen"

**Guideline 1.3. Family name begins with abbreviation**

* Rebecca St. James has sort name "Saint James, Rebecca"
* St. Lunatics has sort name "Saint Lunatics"

**Guideline 2. Name of a group**

* A Perfect Circle has sort name "Perfect Circle, A"
* An Epic at Best has sort name "Epic at Best, An"
* Los Lobos has sort name "Lobos, Los"
* The Beatles has sort name "Beatles, The"
* Cypress Hill has sort name "Cypress Hill"
* Hootie & the Blowfish has sort name "Hootie & the Blowfish"

**Guideline 2.1. Name of a person in a group artist name**

* Ben Folds Five has sort name "Folds, Ben, Five"
* Bill Haley & His Comets has sort name "Haley, Bill & His Comets"
* Bob Marley and the Wailers has sort name "Marley, Bob and the Wailers"
* Dave Matthews Band has sort name "Matthews, Dave, Band
* Don Redman and His Orchestra has sort name "Redman, Don and His Orchestra"
* Gloria Estefan and the Miami Sound Machine has sort name "Estefan, Gloria and the Miami Sound Machine"
* Stevie Ray Vaughan and Double Trouble has sort name "Vaughan, Stevie Ray and Double Trouble"
* The Alan Parsons Project has sort name "Parsons, Alan, Project, The"
* The Jimi Hendrix Experience has sort name "Hendrix, Jimi, Experience, The"
* "The Sensational Alex Harvey Band" has sort name "Harvey, Alex, Sensational Band, The"

**Guideline 3. Latin script only**

* Пётр Ильич Чайковский "Tchaikovsky, Pyotr Ilyich"
* 布袋寅泰‎ has sort name "Hotei, Tomoyasu"

**Guideline 4. De-stylize**

* My$t:c DJz has sort name "Mystic DJz"
* *NSync has sort name "NSync"
* P!nk has sort name "Pink"
* trance[]control has sort name "trancecontrol"

*Nothing to trans(liter)ate*

* （´・д・）ﾉ has sort name "（´・д・）ﾉ"
* ♪◆m599XGSMF6 has sort name "♪◆m599XGSMF6"

## IPI Code

An IPI (interested party information) code is an identifying number assigned by the CISAC database for musical rights management. See IPI for more information, including how to find these codes.

## ISNI code

The International Standard Name Identifier for the artist. See ISNI for more information.

## CRUD Operations

### Create a new Artist.

```
POST /api/artists
```

*Request*
```json
{
    "ipi": "",
    "isni": "",
    "sortName", "",
    "name": "Red Hot Chili Peppers",
}
```

*Response*
```json
    {
        "id": "1607d150-861c-4782-8c1b-abe58254373b",
        "ipi": "",
        "isni": "",
        "name": "Red Hot Chili Peppers",
        "sortName": "",
        "createdAt": "2020-10-08T12:29:17.910156+02:00",
        "updatedAt": "2020-10-08T12:29:17.912486+02:00"
    },
```


### Find Artist by ID

```
GET /api/artists/{id}
```

By default all members of an artist are preloaded.

```json
{
    "id": "33244a4b-dfc5-4317-9039-d2cebfb12782",
    "ipi": "",
    "isni": "",
    "name": "Red Hot Chili Peppers",
    "sortName": "",
    "createdAt": "2020-10-06T13:32:24.213112+02:00",
    "updatedAt": "2020-10-06T13:32:24.214982+02:00"
}
```

### Lists all Artists

```
GET /api/artists
```


Example Response Body:

```json
[
    {
        "id": "1607d150-861c-4782-8c1b-abe58254373b",
        "ipi": "",
        "isni": "",
        "name": "Red Hot Chili Peppers",
        "sortName": "",
        "createdAt": "2020-10-08T12:29:17.910156+02:00",
        "updatedAt": "2020-10-08T12:29:17.912486+02:00"
    },
    {
        "id": "b878ddf3-8c9e-42d5-8c73-bd7f2fd5e530",
        "ipi": "",
        "isni": "",
        "name": "Anthony Kiedis",
        "sortName": "",
        "createdAt": "2020-10-08T12:29:17.911585+02:00",
        "updatedAt": "2020-10-08T12:29:17.911585+02:00"
    },
    {
        "id": "22188e6c-371f-4a83-bbaa-4d0ff1e1aeb3",
        "ipi": "",
        "isni": "",
        "name": "Michael „Flea“ Balzary",
        "sortName": "",
        "createdAt": "2020-10-08T12:29:17.911585+02:00",
        "updatedAt": "2020-10-08T12:29:17.911585+02:00"
    },
]
```

### Deletes an artist by its ID

```
DELETE /api/artists/{id}
```

Returns `204 No Content`