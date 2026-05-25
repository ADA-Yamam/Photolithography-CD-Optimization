# Photolithography-CD-Optimization
# Photolithography CD Optimization for TSMC

## Project Overview
Optimization of Critical Dimension (CD) in photolithography process using Six Sigma (DMAIC) and Lean methodologies.

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

## File Contents
- `photolithography_analysis.jmp` - All data, analyses, scripts, and JMP output

## How to Open
1. Open JMP software
2. File → Open → Select `photolithography_analysis.jmp`

## Tools Used
- JMP (Distribution, Capability, Fit Y by X, Regression, Residuals, Partition, DOE, Profiler, Paired t-test, Predictive Modeling,....)
- Six Sigma (DMAIC)
- Lean (Waste elimination, Variation reduction)
