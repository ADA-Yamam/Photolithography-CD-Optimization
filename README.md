# Photolithography CD Optimization for TSMC

## Project Overview
Optimization of Critical Dimension (CD) in photolithography process using Six Sigma (DMAIC) and Lean methodologies.

## Physical & Chemical Knowledge Application

Before any statistical analysis, root causes were hypothesized based on photolithography physics and chemistry:

| Factor | Physical/Chemical Relationship | Expected Effect |
|--------|-------------------------------|-----------------|
| **Dose** | Higher dose → more photons break PAC molecules → more acid generation → more resist dissolution | Dose ↑ → CD ↓ |
| **PEB_Temp** | Higher temperature accelerates acid diffusion and deprotection reaction | PEB_Temp ↑ → CD ↓ |
| **Focus** | Defocus blurs the aerial image, enlarging the printed pattern | \|Focus\| ↑ → CD ↑ |

This knowledge directed our analysis immediately to **Dose** and **PEB_Temp** as primary suspects, saving time by avoiding trial-and-error testing of irrelevant factors.

## Six Sigma DMAIC Application

**Define:** CD exceeded target (0.726μm vs 0.65μm) with Cpk=0.44 (incapable), causing 9.3% scrap.

**Measure:** Collected 20 wafers data. Distribution analysis confirmed right-skewed CD. Power analysis (85% power) validated sample size adequacy.

**Analyze:** Fit Y by X and Partition identified root causes: low Dose (30.5 mJ/cm²) and low PEB_Temp (120°C). Regression (R²=0.989) and Residuals analysis confirmed model validity.

**Improve:** DOE + Profiler optimized parameters (Dose=35, PEB_Temp=130, Focus=0). Paired t-test confirmed significance (P=0.0001).

**Control:** Cpk improved to 2.075. Prediction Formula enables real-time CD forecasting. Recommended Control Charts for future batches.

## Key Results
| Metric | Before | After |
|--------|--------|-------|
| Cpk | 0.44 | 2.075 |
| Mean CD (μm) | 0.726 | 0.6608 |
| Scrap rate | 9.3% | 0% |

## Lean Application
- Eliminated 9.3% waste (scrap)
- Reduced process variation (Std Dev: 0.053 → 0.022)
- Standardized optimal parameters for production

## Optimal Settings
- Dose: 35 mJ/cm²
- PEB_Temp: 130°C
- Focus: 0 μm

## Repository Files
| File | Description |
|------|-------------|
| `Custom Design.jmp` | Main JMP data table with all analyses and embedded scripts |
| `Lithography.txt` | Complete step-by-step methodology - how the analysis was performed from start to end |
| `photolithography_data.csv` | Raw experimental data |
| `*.jsl` | Individual JMP script files for quick access to specific analyses |

## How to Open
1. Click on `Custom Design.jmp` in this repository
2. Click **View** (or download and open in JMP)
3. The file will download to your computer
4. Open JMP software
5. `File → Open` → Select the downloaded `Custom Design.jmp`
6. All data and scripts will load automatically

## Quick Access to Individual Scripts
For faster access to specific analyses, open any `.jsl` file directly in JMP:
- `Distributions.jsl` - Distribution analysis (Mean CD = 0.726μm)
- `Process capability.jsl` - Capability analysis (Cpk = 0.44 before optimization)
- `Fit-Response Cd.jsl` - Regression model (R² = 0.989)
- `Distributions_Residual Cd.jsl` - Residuals analysis (Shapiro-Wilk P = 0.3458, Durbin-Watson = 1.81)
- `Partition for Cd.jsl` - Decision tree (Dose > 35 gives CD = 0.626μm)
- `prediction Profiler.jsl` - Optimal settings (Dose = 35, PEB_Temp = 130, CD = 0.6608μm)
- `Matched pairs.jsl` - Paired t-test (P = 0.0001)

## Complete Methodology Reference
For the full step-by-step workflow including:
- Data cleaning process
- All JMP commands used
- Statistical test selection rationale
- Physical interpretation of results

**Open `Lithography.txt`** in this repository to read the complete methodology documentation.

## Tools Used
- **JMP:** Distribution, Capability, Fit Y by X, Fit Model, Regression, Residuals Analysis (Shapiro-Wilk, Durbin-Watson), Partition (Decision Tree), DOE (Response Surface), Prediction Profiler, Matched Pairs (Paired t-test), Predictive Modeling (Prediction Formula)
- **Six Sigma:** DMAIC (Define, Measure, Analyze, Improve, Control)
- **Lean:** Waste elimination, Variation reduction, Process standardization
- **Physical & Chemical Knowledge:** Photolithography physics (Dose, PEB_Temp, Focus effects on CD)

## Author
ADA-Yamam

## Date
May 2026
