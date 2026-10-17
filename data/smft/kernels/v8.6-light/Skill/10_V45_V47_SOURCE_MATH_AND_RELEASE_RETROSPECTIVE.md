# 10 — v4.5–v4.7 實際研究編譯經驗補記（v4.8 補回）

> **身份：** 非執行式 field note。這是 2026-10-15 v4.8 從已封存的 v4.5、v4.6、v4.7 FULL 及真實原始來源，追補未曾回寫到 `Skill/` 的經驗。**不是**完成的 GitHub Skill、規格或獨立 LLM benchmark。當中源於「前一輪報告」與「本輪重新核查原頁」的事實須明確分開。

## 1. 缺漏是怎樣發生的

v4.4 的 `Skill/` 十份筆記被持續視為 frozen；v4.5、v4.6、v4.7 的主要修正寫進 `90_PROVENANCE/`、L0 和 `51`，但沒有把後三輪可泛化方法回寫到 Skill Folder。下一個全新 Session 即使讀完 `Skill/`，仍可能只知道早期 Dual Ledger 錯誤，而不知道後來發現的 **robust envelope、discrete quadrature、source norm、training-checkpoint transport、source-anchored proof graph** 等具體誤區。這是**能力交接失真**，不是 Kernel 自身必然缺 source content。

**處理原則：** 已發生的錯誤與反例 → 精確來源／公式／版本 → 何以失敗 → 可複製檢查 → 對下一步的保留條件。切勿只寫「小心數學」或把 hypothetical failure 冒充實際事故。

## 2. v4.5 源文數學陷阱（核查過的版本結果）

參照 `PROOF_DEPENDENCY_RECONSTRUCTION_v4.5.md`、`SOURCE_IDENTITY_CHECK_v4.5.json`，原始來源 `SRC-0118/0119/0229/0108/0274` 的有界 PDF 頁面。

| 真正問題 | 來源／本地 audit | 為何一般語義濃縮容易失敗 | 未來檢查動作 |
|---|---|---|---|
| `ΔΦ=W_s−Δψ` 沿跨多文獻複製，但不是凸共軛 identity | `L45-01`, `SRC-0119` §3.5, `SRC-0229` p.54 | 後文重述造成「多來源佐證」錯覺 | 用 `ψ=Φ=t²/2` on-manifold 駁斥，記錯誤傳播 lineage；勿多計獨立 evidence |
| `Σλ_k·Δs_k` 不是真實 `ΔΦ` 的精確 tick ledger | `L45-02` | 忽略積分 vs 左端採樣；誤把差額標記為「耗散」 | 寫 `ΔΦ=Σλ_k·Δs_k+ΣD_Φ(s_{k+1}||s_k)`，測試凸二次成本 |
| 分別取 `sup_q Φ_q` 與 `sup_q ψ_q` 不是共軛 | `L45-03`, `SRC-0119` §7 | pointwise nonnegative gap 容易被誤當 conjugacy/equality test | Bernoulli(0.2/0.8) 反例，對每個 q 使用 paired dual，或重新取 conjugate |
| 正交 projector 少了正規化因子 2 | `L45-04`, `SRC-0108` §5.1 | 投影子空間正確不代表能量 coefficient 正確 | 用十站標準範數和單基向量直接算兩邊 |
| 定相差 `π` 不等於向量 `a_{n+5}=-a_n` | `L45-05` | 固定/自由振幅與零相位混在同一定理 | 分開量詞；若固定振幅不等，僅可得反相、不能得相等模長 |
| 有號 `βΣL` 不保證非負、可下界 | `L45-06`, `SRC-0274` §2 | 把「penalty」標籤當作數學性質 | 取負 L 趨 −∞，需絕對值/平方/限制/規範化；另檢 gauge transformation |

**保留生成價值：** 反例限制的是原公式的無條件強版本。Δ5 反對稱 `ker(P_+)` 仍是標明前提下的有效數學結果；Belt 的實驗設想仍可保留為假說，不可當作經過 spin-statistics 證明。

## 3. v4.6 源文及模型證據邊界

參照 `PROOF_DEPENDENCY_RECONSTRUCTION_v4.6.md`, `GLOBAL_CONSOLIDATION_v4.6.md`，原始 `SRC-0119/0259/0260/0261`。

- Robust log-partition 在多個最優 baseline 交叉的地方可不可微；不能從「存在一個 log-partition」推至唯一 Fisher Hessian 或 inverse mass。陰性例：兩個 Bernoulli baseline 在 λ=0 的不同 one-sided derivative。
- Importance sampling ratio 若 clipping，則「無偏」必須另證；時變 reference q 的 `dΦ` 包含額外 base drift，不能重複套固定基準微分式。
- `Joint Port` 是相對觀察、干預和環境的 quotient theorem；**充分性、功能正確性、自然吸引子、自然生成的功能個體**是四種不同實驗負擔。
- 長篇合輯可搜尋不等於深入閱讀；四份 source 的 exact SHA 核對和 selected physical pages 不等於其 34–446 頁全部審核。

**編譯決策：** 與其增加 K1 的吸引子名稱，應輸出 `General lemma → assumptions → conditional result → original locator → falsifier → residual`。Benchmarks/source-hidden model trial 仍未執行。

## 4. v4.7 跨 Checkpoint 和 Genesis 交接的教訓

參照 `PROOF_DEPENDENCY_RECONSTRUCTION_v4.7.md`, `GLOBAL_CONSOLIDATION_v4.7.md`，原始 `SRC-0323/0283/0261/0259/0241`。

- 同一 checkpoint 的兩個 sufficient Port，不推出跨 checkpoint 身份或 transport；有且僅當已聲明學習對應 `L` 在舊 π-fibers 上飽和，才存在與 π 相容的 deterministic transport `R` (`L47-01/02`)。
- Activation 距離或相似度可能因座標重標記而巨大，即使控制等價；需比較可觀測/介入效果，且識別 alignment gauge (`L47-03`)。
- Post-hoc 發現電路 ≠ 形成時刻；訓練時身份、因果 mediation 需 longitudinal controls/interventions (`L47-04/08`)。
- Mind-Seal 的 `ζ,π` schema 包含信息字段不保證任何接收模型實際遵從，也不保證有 Runtime enforcement (`L47-05`)。
- 經典 `SRC-0323` 的「觀點」是歷史思想源頭；`SRC-0283` 的 right-congruence/coarsest exact quotient 是後期 formal construction。不可把 genealogy 邊寫作邏輯 `DERIVES` (`L47-06/07`)。

**真正排查方式：** 故意建構「同樣終點但不同歷史」、「同樣輸出但不同轉移」、「same-function different coordinates」的負對照，並要求模型指出需要加入何種介入或 frame transport 才可修復推論。

## 5. v4.8 本輪重新核證的新發現：跨層 Current Canonical Drift

重新開啟 `SRC-0106` pp.7–9,19–26 和 `SRC-0268` pp.1–3 後，發現 **v4.7 Results Atlas RA-E01 仍將 Kan–Li 預設為 Memory–Focus**。然而 v4.7 的 `20_K0_CORE_v0.1.md` §3 和受保護 `41_K1_P8D_001` 已寫得正確：P8D II 的 canonical 是 **Realization–Admissibility**；Memory–Focus 僅為此前的 engineering instantiation。`SRC-0106` p.20 eqs.5.1–5.3 確切聲明這個修正。本輪屬新發現的 **current L0 vs current K0/K1 漂移**，不要冒稱是 v4.7 曾發現的事故。

**可泛化規則：** 一個完整 Kernel 會出現兩種不同錯配：`Source → Compiled Claim` 的證據錯配；以及 `Latest Core → Current Atlas` 的版本漂移。每輪必須檢查 **兩個方向**，尤其是同名的「成熟核心」是否比更顯眼的 L0 更新。若新版其實只是限縮舊用途，應用 `REFINES/REVISES`，勿將歷史的 Memory–Focus 用途刪除或追認為假科學。

另外 `SRC-0106` pp.34–38 關於 low-rank closure 的主張帶有隱含 preconditions；`L48-02..05` 的獨立有限反例展示「單一 mediator 不保證 rank1」、「低秩 Jacobian 不保證 exact quotient」、「ε_cl 分母可 0/0 及 baseline 任意化」、「低維 return determinant 不意味整個系統只有少數 modes」。這些是當次審核新增的 proof/guard，不是 v4.7 已有成果。

## 6. 發行 QA：數學、版本指針、flat、checksum 要分層

這次是在 v4.7 後追補 Skill。歷史正式 QA 報告記錄 v4.5 574、v4.6 584、v4.7 593 個 local unittest pass；本輪重新執行 v4.7 baseline suite 亦觀察 593/593 pass。前幾輪確曾需要處理舊版 `current Atlas` assertion、canonical/flat hash 不一致，並保留原版測試文本快照。這類失敗**不等於**數學推導被推翻；但也不能用硬刪 assertion 的方式讓測試綠燈。

實務 release gate 應分開回報：源 tar member SHA／PDF 方程頁圖片／Source Depth；typed math negative controls；current L0 與 K0/K1 一致性；14 flat/nested SHA；受保護 40–44；原始 325 manifest；historic W/PF/GM/Atlas stable IDs；完整 FULL 與 INCREMENTAL overlay byte reconstruction；以及 **never benchmark participant-visible private rubric**。

## 7. 這份 Skill 更新尚沒有完成甚麼

- 不是已寫好的 `SKILL.md`、可安裝 skill 或業界可直接部署的 schema/code pipeline。
- 不是外部原創優先權審核、所有 325 原文全文深審、自然 Transformer attractor 實驗或 LLM blind reconstruction。
- 不是把 local `L45/L46/L47/L48` nodes 變成歷史 W、GM，或把 60 個 RA 自動提升 maturity。
- 如之後進行真正獨立 benchmark，務必將 private grader、原題和所有其解答從 participant-visible file mount 隔離。

**交接入口：** `Skill/README_FIELD_NOTES.md`、`90_PROVENANCE/PROOF_DEPENDENCY_RECONSTRUCTION_v4.5.md` … `v4.8.md`、`SOURCE_DEPTH_AUDIT_v4.5..v4.8.csv`、各輪 QA JSON；請以原始 tar member 及逐頁證據再確認，而不是只看本回顧文字。
