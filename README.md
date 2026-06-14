# rh-maieutic-program

> *"Ich weiß, dass ich nichts weiß — aber ich weiß, welche Frage als nächste folgt."*
> — nach Sokrates

---

## Was ist das hier?

Ein **maieutisches Forschungsprogramm** zur Riemannschen Hypothese.

Kein loses Notizbuch. Kein Paper-Dump. Sondern ein gerichtetes Programm, das:

- jede Frage aus einer **bewiesenen Antwort** gebiert,
- jeden Beweis mit **expliziten Voraussetzungen und Gegenbeispielklassen** dokumentiert,
- jede neue RH-Frage als **logisches Kind** einer vorherigen Einsicht kennzeichnet,
- und den epistemischen Status jedes Resultats **ehrlich und öffentlich** ausweist.

Das Programm ist inspiriert von Imre Lakatos (*Proofs and Refutations*) und der sokratischen Hebammenkunst: Man hilft nicht, Antworten zu *erfinden* — man hilft, was bereits *latent* ist, zur Welt zu bringen.

---

## Struktur

```
rh-maieutic-program/
│
├── CONSTITUTION.md          ← Spielregeln: Was zählt als Beweis, Frage, Fortschritt?
├── MAIEUTICS.md             ← Das sokratische Standardprotokoll (3 Fragen nach jedem Theorem)
│
├── catalog/
│   ├── part1.md             ← Fragenkatalog Teil 1 (Ebenen I–VI)
│   ├── part2.md             ← Fragenkatalog Teil 2 (Ebenen VII–XIV)
│   └── part3.md             ← Fragenkatalog Teil 3 (Ebenen XV–XVI, Gesamtbilanz)
│
├── questions/
│   └── question-dag.md      ← DAG aller Fragen: Herkunft, Status, Implikationen
│
├── theorems/
│   └── index.md             ← Theorem-Register mit Status und Abhängigkeiten
│
└── new-rh-questions/
    └── README.md            ← Neue RH-Fragen, die noch nie so gestellt wurden
```

---

## Epistemische Status-Symbole

| Symbol | Bedeutung |
|--------|-----------|
| ✅ | Bewiesen (bedingungslos) |
| 🟡 | Konditionell bewiesen (unter explizit genannter Voraussetzung) |
| 🔴 | Offen — aktiver Angriffspunkt |
| ❓ | Offen — unklar ob angreifbar |
| ✗ | Widerlegt (mit Gegenbeispielklasse) |
| 🌱 | Neu geboren — aus letzter Antwort destilliert |

---

## Verbundene Repositories

| Repo | Rolle |
|------|-------|
| [`prolate-gram-coercivity`](https://github.com/Waschtl904/prolate-gram-coercivity) | Hauptprogramm: Prolate Koerzivität, Attack Plans, Paper-Koordination |
| [`prolate-primes-paper`](https://github.com/Waschtl904/prolate-primes-paper) | LaTeX-Manuskripte Papers I–XVII |
| [`arith-spectral-bridge`](https://github.com/Waschtl904/arith-spectral-bridge) | Explorationsprojekt: Arithmetik → Spektraltheorie |

---

## Leitprinzip

> Jede beantwortete Frage trägt die nächste bereits **in sich**.
> Die Aufgabe des Programms ist es, sie methodisch zu **entbinden** — nicht zu erfinden.

---

*Stand: Juni 2026 — aktiv in Bearbeitung*
