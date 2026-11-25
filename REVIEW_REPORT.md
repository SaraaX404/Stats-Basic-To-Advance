# Course notebook review

## Original theory expansion and combined files

All 41 topic notebooks now contain their own newly written theory and lab in one file. The expansion adds 305 theory subsections, approximately 16,100 words, covering definitions, assumptions, mathematical reasoning, tests and estimation procedures, edge cases, interpretation and common mistakes. [Theory coverage](THEORY_COVERAGE.md) lists the included subtopics for every notebook.

The signed-rank notebook explains one-sample and paired designs, symmetry and location, all three alternatives, zero and tie rules, rank construction, directional decision rules, exact inference, normal approximation and corrections, software conventions, sign-test tails, effect summaries and reporting. Its added calculation checks the tied-rank variance against the complete exact sign distribution and compares exact and approximate p-values.

The 59 separate lecture-copy notebooks, all PDF-page screenshots and previous combined copies were moved outside the course project into the ignored local reference area. Original PDFs remain outside the course folder. Standalone Python helper files were also moved outside; Python learning code remains in the combined notebooks. No lecture screenshots or copied page text are used as the new notes.

## Teaching changes

All 41 section notebooks were reviewed for missing hand-calculation steps. Each now contains an original worked example with a question, assumptions, numbered procedure, visible Markdown tables, executable calculations, and an interpretation. There are 88 new worked tables.

| Subject | Calculation trail added |
|---|---|
| Descriptive Statistics | Frequencies and denominators; deviations; grouped midpoint and cumulative frequencies; moments and Lorenz shares |
| Probability and Distribution Theory I | Outcomes; empirical counts; conditional tables; tree paths; Bayes normalization; random-variable mapping; PMF moments; density areas |
| Sampling Techniques | Objective-to-questionnaire plan; sample enumeration; finite-population SE; stratum weights; cluster-total expansion |
| Linear Regression Analysis | Centred products; fitted values and residuals; dummy-variable rows; pure-error and lack-of-fit decomposition |
| Spreadsheet Modelling | Missing/duplicate checks; logical truth columns; pivot aggregates; weighted margins; interval/test substitutions |
| Statistical Inference | Bias and MSE contributions; t intervals; rejection cutoffs and power; likelihood and score; variance-pivot inversion |
| Nonparametric Statistics | Binomial tails; signed ranks and sign counts; empirical-CDF gaps; expected counts; run numbering; pooled ranks; median categories |
| Design and Analysis of Experiments | Pooled t; CRD ANOVA; contrast coefficients and SE; treatment/block/error RCBD ANOVA |

## Wilcoxon example

[Open the signed-rank and sign-test notebook](07_STA_507_1.0_Nonparametric_Statistics/Lab_02_Wilcoxon_Signed_Rank_Test_and_Sign_Test.ipynb).

The example shows before/after scores, differences, absolute differences, a zero exclusion, average tied ranks, positive and negative rank columns, both rank sums, and T=min(W+,W−). All 256 sign assignments of the eight nonzero ranks are enumerated. W+=32, W−=4, and the exact conditional two-sided p-value is 14/256=.0546875. At alpha=.05 the test does not reject. The sign test is worked on the same pairs.

The tied-rank enumeration is explicit: a no-ties critical-value table cannot be substituted without checking its applicability. Zero conventions, measurement precision, test direction and interpretation are explained.

## Statistical conventions reviewed

- Wilcoxon: zeros, average ranks, two-sided statistic, symmetry and tied-rank enumeration.
- K–S: both sides of each empirical CDF jump, a fully specified continuous null, and a finite-sample critical-value decision.
- Chi-square: uncorrected hand calculations are labelled; software continuity-correction defaults are explained.
- Mood median: median categories and ties; small expected counts are flagged, followed by an exact fixed-margin 2×2 calculation and decision.
- Mann–Whitney: pooled ranks, both U statistics, first-input convention and limits of a median interpretation.
- Regression and ANOVA: sums-of-squares partitions and degrees of freedom are checked.

Official references: [Wilcoxon](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.wilcoxon.html), [Mann–Whitney U](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.mannwhitneyu.html), [chi-square contingency](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.chi2_contingency.html).

## GitHub separation

Ignore rules at both supported repository roots exclude original PDFs and local reference material. Lecture-page images and copied lecture notebooks have also been physically moved out of the course folder. Public navigation links only to combined theory-and-lab notebooks and original visual guides.

No Git repository existed in this workspace during review; nothing was committed or pushed. Ignore-rule checks use a separate temporary repository and do not initialize the user's project.

## Validation scope

The 41 new calculation cells were executed with their embedded arithmetic and consistency checks. Public code cells were checked for Python syntax, and public links and images were checked without depending on ignored lecture material. Actual Git ignore behavior was checked for both possible repository roots.

Existing NumPy/SciPy/Matplotlib simulations were not executed in this runtime, which lacks SciPy and Matplotlib. This review does not claim a complete proof of every existing statistical statement or that every source equation has a dedicated simulation.

Inspect [VALIDATION_REPORT.json](VALIDATION_REPORT.json) for notebook/link/calculation checks and [THEORY_VALIDATION.json](THEORY_VALIDATION.json) for the theory, navigation and project-content checks. Validation helpers are retained outside the published course folder.
