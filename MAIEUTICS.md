# MAIEUTICS.md

> *"Die Hebamme bringt nicht selbst zur Welt — sie hilft dem, was bereits da ist, herauszukommen."*
> — Sokrates, Theaitetos 149a

Dieses Dokument beschreibt das **sokratische Standardprotokoll**, das nach jedem bewiesenen Theorem ausgeführt wird.
Es ist kein optionaler Anhang — es ist die Methode, durch die das Programm lebt.

---

## Das Protokoll: 3 Pflichtfragen nach jedem Theorem

Nach jedem Theorem `T` werden exakt diese drei Fragen gestellt und schriftlich beantwortet.
Die Antworten werden entweder direkt in `theorems/index.md` eingetragen oder als neue Einträge in `questions/question-dag.md` übernommen.

---

### Frage 1 — Die Voraussetzungsfrage

> **Was hat dieses Theorem vorausgesetzt, ohne es selbst zu beweisen?**

Ziel: Alle impliziten Annahmen sichtbar machen.
Jede Annahme, die nicht bewiesen ist, ist ein **offener Angriffspunkt** (🔴) oder eine **neue Frage** (🌱).

**Protokollformat:**
```
Voraussetzungen von T:
  - [A1]: <Aussage> — Status: ✅ / 🟡 / 🔴 / ❓
  - [A2]: <Aussage> — Status: ✅ / 🟡 / 🔴 / ❓
  ...
Schwache Stelle: [Ai] ist der einzige ungesicherte Input.
```

---

### Frage 2 — Die Negationsfrage

> **Was würde folgen, wenn eine Hypothese des Theorems *falsch* wäre?**

Ziel: Die **Gegenbeispielklasse** konstruieren und die Grenzen des Theorems verstehen.
Ein Theorem, dessen Negation nichts Interessantes ergibt, ist schwach.
Ein Theorem, dessen Negation das gesamte Programm kollabieren lässt, ist zentral.

**Protokollformat:**
```
Negationsanalyse von T:
  - Wenn [A1] falsch: <Konsequenz>
  - Wenn [A2] falsch: <Konsequenz>
  ...
Zentralität: T ist [peripher / wichtig / kritisch] für das Programm.
```

---

### Frage 3 — Die Objektfrage

> **Welche Objekte *mussten existieren*, damit der Beweis funktioniert?**

Ziel: Neue mathematische Strukturen identifizieren, die der Beweis implizit einführt.
Diese Objekte sind oft der Keim der nächsten Theorie.

**Protokollformat:**
```
Implizite Objekte in T:
  - [O1]: <Objekt/Struktur> — bisher benannt? Ja/Nein
  - [O2]: <Objekt/Struktur> — bisher benannt? Ja/Nein
  ...
Neue Kandidaten für den DAG: [O_i] könnte Frage F_neu erzeugen.
```

---

## Beispielprotokoll (Paper XXII, Theorem P13)

```
THEOREM: P13 — inf σ(D_Edge) > 0
Datum: Mai 2026

--- FRAGE 1: Voraussetzungen ---
Voraussetzungen von P13:
  - [A1]: Operator-Identifikation D_Edge — Status: ✅
  - [A2]: Airy-Gap δ_Airy ≥ F_TW(0) ≈ 0.96 (Tracy-Widom) — Status: ✅
  - [A3]: Arithmetische Störungsschranke ||ε_c||_op → 0 (Montgomery–Vaughan) — Status: 🟡
  - [A4]: Min-Max-Satz — Status: ✅
Schwache Stelle: [A3] ist der einzige ungesicherte Input — dies ist O5.

--- FRAGE 2: Negation ---
Negationsanalyse von P13:
  - Wenn [A2] falsch (kein universeller Airy-Gap): gesamter RG-Rahmen kollabiert.
  - Wenn [A3] falsch (Primzahlen stören zu stark): P13 gilt nur konditionell unter GRH.
  - Wenn [A1] falsch (falsche Operator-Identifikation): Theorem irrelevant.
Zentralität: P13 ist KRITISCH — alle weiteren Resultate hängen an inf σ(D_Edge) > 0.

--- FRAGE 3: Objekte ---
Implizite Objekte in P13:
  - [O1]: Der IR-Kern als RG-Fixpunkt — bisher benannt: Ja (XXII_ir_kernel.md)
  - [O2]: Die „Breite des Airy-Fensters“ h ~ c^{1/3} als Maß für epistemischen Abstand RH/GRH
          — bisher benannt: Nein → Kandidat für NEU-RH-2
Neue Kandidaten für den DAG: [O2] erzeugt Frage NEU-RH-2 (siehe new-rh-questions/).
```

---

## Wann wird das Protokoll ausgeführt?

| Auslöser | Pflicht? |
|----------|----------|
| Neues Theorem bewiesen (✅ oder 🟡) | **Ja** |
| Theorem widerlegt (✗) | **Ja** (Negationsanalyse rückwirkend) |
| Statuswechsel 🔴 → 🟡 | **Ja** |
| Neue Frage in DAG aufgenommen | Nein (aber empfohlen) |

---

## Wo werden die Ergebnisse abgelegt?

| Ergebnis | Zieldatei |
|----------|-----------|
| Neue offene Voraussetzung | `questions/question-dag.md` als 🔴-Eintrag |
| Neue implizite Struktur | `questions/question-dag.md` als 🌱-Eintrag |
| Zentralitätsbewertung | `theorems/index.md` (Spalte: Zentralität) |
| Freie Spekulationen | `SCRATCHPAD.md` |

---

*Stand: 14. Juni 2026*
