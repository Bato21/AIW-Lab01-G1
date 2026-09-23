# Lab 1 · AI and contribution record

Members: Baptiste Vial and Vicente Rodriguez.

**How we worked:** we worked on the lab at the same time, on a call throughout, and discussed every section together to check it was correct. The table below shows who led each part, but both of us reviewed and agreed on all of it.

AI used / not used: **Used.** Tool: Claude Code (model Claude Opus 5.5), in the VS Code terminal, on 23 September 2026.

- **Our own first attempt:** we started the lab without AI. Baptiste wrote a first version of the target/audit section and a first plot and code for EDA questions 1 and 3. Vicente worked on EDA question 2, checked the work against the rubric's assigned points and reviewed all of it.
- **Rubric audit:** we asked the AI to read the brief and rubric and compare them with our notebook. It reported that our target and population were framed around a single driver (Leclerc), with final position as the target and `grid` as the predictor, which contradicted the brief (all drivers, binary top-10 target, `qualifying_position` from the qualifying table). It also found that our "qualifying-only" check actually counted retirements, and that our Q1 plots could be improved.
- **Improvements we asked for:**
  1. It rewrote section 1 and the audit for the full population (notebook: "1. Target and audit", "Audit findings", "Why the left join").
  2. It rebuilt EDA question 1 around our 4-bar idea, using a correct qualifying × race cross-table and per-season rates.
  3. It wrote EDA question 3 (selection trap: non-finishers) based on the rubric's Friday-trap requirement.
- **What we accepted / changed and why:** we accepted the section 1 rewrite because the brief fixes the target, population and predictor. We kept our 4-bar design for Q1 but accepted the corrected counts. We reviewed Q3's reasoning together before keeping it.
- **AI output that was checked and corrected:**
  - The AI first wrote that grid differs from qualifying position in "most rows". Running the check showed 381 of 1,197 (about 32%), so the text was corrected.
  - In Q3, its first code computed the training majority on the 1,197 rows that have a qualifying position (599/1,197 = 0.5004, which gives a majority of 1) instead of all 1,200 rows (600/1,200 = exactly 0.5, which gives 0 under the tie rule). This was fixed before the code was added to the notebook.

Own decision: We kept our initial structure for the data integrity checks. We made sure all the steps we did ourselves stayed in, so we fully understood the data we were working with, which gave us a complete picture for the EDA questions.

Verification, observed result and limitation (notebook reference allowed): We compared the AI's corrections directly with what we had written. In the second commit (`6ef2eb1`) we uploaded our own work as a backup, then asked the AI to review it before starting the EDA questions. We then put the new code side by side with our own to check that our thought process was still intact.

*Observed:* our duplicate check still held (no duplicate keys), but two results changed. Our Leclerc-only audit showed 0 missing values, while the full population has 3 rows with missing qualifying (notebook: "Audit findings"). And our "qualifying-only" check was actually counting retirements; the corrected check finds 0 qualifying-only rows. *Limitation:* the side-by-side comparison confirms that the reasoning is consistent, but we did not independently recompute every figure the AI produced.

| Member | Contribution and evidence reference |
|---|---|
| Baptiste Vial | Wrote the first version of the target/audit section (commit `6ef2eb1`) and the first plot and code for EDA questions 1 and 3. Led the AI-assisted rubric audit and the improvements to section 1 and EDA questions 1 and 3 (notebook sections 1, 2 and 4). Discussed every section with Vicente on call. |
| Vicente Rodriguez | Wrote EDA question 2: teammate pairs and the independence check (notebook section 3, commit `f3bf0c6`). Checked the work against the rubric's assigned points and reviewed all sections. Discussed every section with Baptiste on call. |
