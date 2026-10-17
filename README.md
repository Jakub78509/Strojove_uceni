# 🏎️ Predikce pódia ve Formuli 1 – semestrální projekt SU

**Rozhodovací problém:** Skončí jezdec v závodě na pódiu (1.–3. místo), když známe jen informace dostupné **před startem**: kvalifikaci, formu z předchozích závodů, tým a trať?

- **Typ úlohy:** učení s učitelem, binární klasifikace (pódium ano/ne)
- **Instance:** jeden jezdec v jednom závodě (~5 000 instancí za 2014–2026)
- **Data:** [Jolpica F1 API](https://github.com/jolpica/jolpica-f1) (nástupce Ergast), JSON převedený na CSV
- **Rozdělení dat (podle času, ne náhodně):** trénink 2014–2023, validace 2024–2025, test 2026
- **Úprava původní úlohy:** (a) pódium → body (top 10), (b) test na sezóně 2026 s novými pravidly: jak model zvládne změnu problému (*concept drift*)

> ⚠️ Podle přednášky 01 je potřeba **téma konzultovat s vyučujícím** (cíl, data, algoritmy). Hodnocení: 25–50 bodů, projekt je potom podkladem k ústní zkoušce.

## Spuštění
```bash
pip install -r requirements.txt
jupyter notebook
```
Nejdřív spusť `notebooks/00_Stazeni_dat.ipynb`: stáhne data do `data/`, trvá pár minut. Potom notebooky spouštěj postupně podle čísel.
