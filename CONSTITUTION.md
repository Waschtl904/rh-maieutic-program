# CONSTITUTION.md

> *Die Verfassung des maieutischen Forschungsprogramms.*
> Alle anderen Dateien dieses Repositories unterliegen diesen Regeln.

---

## I. Was zählt als Beweis?

Ein **Beweis** im Sinne dieses Programms ist ein Argument, das:

1. **Explizite Voraussetzungen** nennt — keine stillschweigenden Annahmen.
2. **Eine Gegenbeispielklasse** benennt — also angibt, unter welchen Umständen das Argument *nicht* gilt.
3. **Einen epistemischen Status** trägt (siehe Symboltabelle in `README.md`).
4. **Referenzierbar** ist — entweder durch einen Paper-Link, eine Notebook-Datei, oder einen expliziten Inline-Beweis.

> **Verboten:** Ein Resultat als ✅ zu markieren, ohne Punkt 1–3 ausgefüllt zu haben.
> **Erlaubt:** Ein Resultat als 🟡 zu markieren mit explizit genannter Bedingung.

---

## II. Was zählt als neue Frage?

Eine Frage darf in `questions/question-dag.md` nur aufgenommen werden, wenn:

1. Sie **aus einer beantworteten Frage destilliert** wurde — d.h. sie hat eine dokumentierte Herkunft (`born_from: F_XY`).
2. Sie eine **Implikationsstruktur** hat — d.h. es ist angegeben, was folgt, wenn sie positiv *bzw.* negativ beantwortet wird.
3. Sie **nicht redundant** ist — d.h. sie ist nicht bereits eine Umformulierung einer bestehenden Frage.

> **Verboten:** Freie Einfälle ohne Herkunft direkt als Programmfrage eintragen.
> **Erlaubt:** Freie Einfälle in `SCRATCHPAD.md` parken und später formalisieren.

---

## III. Was zählt als Fortschritt?

Fortschritt ist **ein expliziter Statuswechsel** auf einer der folgenden Achsen:

| Von | Nach | Bedingung |
|-----|------|-----------|
| ❓ | 🔴 | Angriffspunkt identifiziert, Methode benannt |
| 🔴 | 🟡 | Konditioneller Beweis erbracht |
| 🟡 | ✅ | Bedingung bedingungslos bewiesen |
| ❓/🔴 | ✗ | Gegenbeispiel konstruiert oder Widerspruch gezeigt |
| Antwort | 🌱 | Mindestens eine neue Frage aus der Antwort destilliert |

Kein Statuswechsel ohne Commit-Eintrag mit Begründung.

---

## IV. Welche Fragen sind verboten?

Eine Frage ist **unzulässig** für das Programm, wenn:

- Sie **keine Implikation** zu einem bestehenden Theorem oder einer bestehenden Frage hat.
- Sie **nicht falsifizierbar** ist (im Sinne: kein denkbares Gegenbeispiel existiert).
- Sie eine **reine Spekulation** ohne mathematischen Anker ist.

Solche Fragen gehören in `SCRATCHPAD.md` — nicht in den DAG.

---

## V. Maieutisches Standardprotokoll

Nach **jedem** bewiesenen Theorem wird das Protokoll aus `MAIEUTICS.md` ausgeführt.
Das ist keine Option — es ist Pflicht.

Die drei Standardfragen lauten (Details in `MAIEUTICS.md`):

1. Was hat dieses Theorem vorausgesetzt, ohne es zu beweisen?
2. Was würde folgen, wenn eine Hypothese des Theorems *falsch* wäre?
3. Welche Objekte *mussten existieren*, damit der Beweis funktioniert?

---

## VI. Sprache und Stil

- **Mathematische Aussagen** auf Englisch (internationale Anschlussfähigkeit).
- **Metakommentare, Status-Notizen, Protokolle** auf Deutsch.
- **Keine Selbstüberzeugung durch Sprache:** Worte wie "offensichtlich", "trivialerweise", "klar" sind verboten, wenn kein Beweis folgt.
- **Ehrliche Labels:** Lieber 🔴 als fälschlich ✅.

---

## VII. Versionierung

- Jede Datei trägt am Ende einen `Stand:`-Eintrag mit Datum.
- Wesentliche Änderungen an bestehenden Resultaten erhalten einen eigenen Commit mit Begründung.
- Diese `CONSTITUTION.md` selbst darf nur durch expliziten Konsens geändert werden — mit Commit-Nachricht `constitution: [Begründung]`.

---

*Stand: 14. Juni 2026*
