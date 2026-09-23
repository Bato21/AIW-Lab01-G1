# Lab 1 · Runbook

1. Extract the complete package into your course repository; preserve labs/lab_01 and data/samples/lab01_v1.
2. Use your Week 2 Python environment. If needed: `python -m pip install -r requirements_lab01_v1.txt` from the package root.
3. Open labs/lab_01/Lab01_EDA_Baselines_Student_v1.ipynb with that environment's Python kernel. Default MODE is snapshot; no network is used by the notebook.
4. Work through train, then calibration. Complete the written evidence and freeze record before enabling RUN_TEST.
5. Restart and Run All after completing the notebook. Save its outputs. Confirm that you can reproduce the frozen evaluation without modifying decisions.
6. Record your actual Python/package versions, operating system, any changes to this procedure, the submitted commit and the date/result of your check below. Keep the source CSVs unchanged.

Actual environment and execution evidence:

- **OS:** Windows 11 (10.0.26200).
- **Kernel:** Anaconda Python 3.13.5 with numpy 2.1.3, pandas 2.2.3, matplotlib 3.10.0, ipykernel 6.29.5. These differ from the tested versions in `requirements_lab01_v1.txt` (numpy 1.26.4, pandas 2.3.1, matplotlib 3.10.3); the notebook ran without errors, so nothing was reinstalled.
- **Editor:** VS Code with the Jupyter extension, kernel set to the Anaconda Python above.
- **Data:** `MODE="snapshot"`, local CSVs in `data/samples/lab01_v1`, unchanged. No network or API credentials used.
- **Procedure changes:** none. Train and calibration were completed first. The freeze record was committed as `9db1efa` before setting `RUN_TEST=True`.
- **Check:** Restart and Run All on 23/09/2026. All 9 code cells ran in order (execution counts 1–9) with no errors, and outputs are saved in the notebook. Calibration reproduced exactly (majority 0.500; qualifying top ten 0.764). Test result: majority accuracy 0.499 / balanced accuracy 0.500; qualifying top ten accuracy 0.797 / balanced accuracy 0.797 (n = 919, 0 missing qualifying). The numbers quoted in sections 5–7 match the saved outputs.
- **Commits:** method frozen at `9db1efa`, freeze record at `1aecf8d`. The submitted commit is the final commit on `main` of https://github.com/Bato21/AIW-Lab01-G1 containing this runbook; its identifier is given on Canvas.

Submission uses GitHub + Canvas as stated in the brief. Include support code and the six CSVs plus lab01_manifest_v1.json. No API credentials are needed. If your environment is blocked, record the exact error and contact the teaching team; do not label synthetic practice as real data.
