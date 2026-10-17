# SMFT / 成界之學 — Provisional Canonical Results Atlas

**Version:** v3.9 · **Snapshot:** 2026-10-15 · **Role:** L0 research-outcome front door · **Status:** PROVISIONAL / SOURCE-BOUNDED · **Not:** a proof of one unified field theory, physical ontology, AGI capability or scientific priority.

> **先讀這份，然後才有選擇地下鑽。** 本文不是按文章出版順序排列，也不是純摘要；它回答：哪些重要結果已確立於指定模型、哪些框架可以工程化、哪些仍是具體而待驗的猜想、哪些舊版強主張已被反例限制，以及甚麼問題最值得後續生成性研究。每張卡有穩定 ID、最小條件、不可以推出的結論，及來源／Witness 入口。

## A. Read protocol — 先掌握 10 個不可混淆的要點

1. **結果成熟度 ≠ 歷史原創性。** 後期的形式化未必是概念源頭；《皇極經濟》`SRC-0323` 是 Genesis，不是所有後期公式的數學證明。
2. **已證明 = 在清楚的數學前提下可重建。** 本地有限模型、代數反例、程式回歸屬限定證據，並非真正 LLM／金融／物理場景有效的證據。
3. **功能角色語言不等於物理本體。** P8D 的乾坤／坎離角色、複數風險軸、Belt／Spinor／Gauge、語義量子模型均按型別分界。
4. **Port sufficient ≠ functional correct ≠ natural individual**（`SRC-0261`）；即使找到穩定 attractor，也未證明它是功能個體。
5. **K0 是最小語法；L0 是研究結果地圖。** 不把 L0 的任何猜想直接升格成 K0 公理。
6. **證明假設與不能推論的範圍一同讀取。** 無條件宣稱「必然」「普適」通常正是需要驗證的地方。
7. **創造性保留與真偽分級可以共存。** 不刪除受反例限制的舊猜想，將其記作可修訂、可否證的 Residual。
8. **跨領域轉譯需要保結構映射和對應測量。** 語言相似只能 `TRANSLATES`，不能擅自標 `DERIVES`。
9. **來源第一輪定點覆蓋已完成，沒有完整逐頁審核。** 截至 v3.7 共 **325/325** 份有指定範圍的選讀紀錄；**零份尚未定點閱讀**。長篇合輯仍有大量未深讀章節，需要另行 SOURCE_DEPTH_GAP_AUDIT。
10. **沒有獨立 LLM blind reconstruction 或實際科學能力提升測試。** 新 Session 對 Atlas 的理解仍須由 source-hidden tasks 和獨立評分驗證。

### Maturity labels

| Label | 含義 | 可以安全地說 | 不應該說 |
|---|---|---|---|
| **M — Mathematical / scoped** | 給定明確定義及假設，普通數學／有限模型／反例成立 | 該命題在指定前提下成立 | 對所有真實世界現象有效 |
| **E — Engineering contract** | 算子、Gate、Trace、測試接口已具體化，仍缺真實環境證據 | 可以依協議設計及做對照試驗 | 已帶來實際性能突破 |
| **H — Generative hypothesis** | 有可操作狀態、公式、預測或證明義務的研究猜想 | 值得設計反駁試驗 | 已成立的定理／自然必然性 |
| **R — Repaired / refuted strong claim** | 原文主張的強版本已被條件或反例限制 | 強版本不成立，弱版本可研究 | 原構想整體作廢 |
| **O — Open bridge** | 重要研究間有缺失的映射、機制或驗證 | 目前的關鍵待解問題 | 已經證明兩領域等價 |

## B. Top-level outcome ledger — 按成果而非版本排序

以下每張卡的 `Evidence` 是**可追溯入口**，不是引文裝飾。`Wxxx` 優先在 `51_CROSS_KERNEL_INTERFACE_CONTRACT.md`，但早期 W001–W012 在 Genesis Bridge／v0.9 審核報告；W024 仍未定位；`K1` 在 `50_K1K2_MATURE_OPERATIONAL_ANCHORS.md`；`PFxx` 在 Proof Family Index；`SRC` 可按 `90_SOURCE_MANIFEST.csv` 尋回原始 tar 成員。

### B1. 可重建的條件性數學結果（M）

**RA-M01 — 任務相對的精確投影。** 若投影 `π:S→P` 保留指定干預集合下的輸出與下一步商狀態，P 才是該協議的充分有效狀態；P 的維度小並不自動成立。**界限：** 任務充分不代表自然語義個體。**Evidence:** K0 §6, `51` §12, W41/W154, PF01, SRC-0261。

**RA-M02 — Endpoint Sufficiency / fibre saturation。** 對 `π:X→Y` 與有效集合 `T⊆X`，最終輸出可單獨決定有效性 iff `T=π⁻¹(π(T))`。**界限：** 不推出動力系統可 lump。**Evidence:** W308, PF13, SRC-0234 Appendix G。

**RA-M03 — 九周期 Carry 判準。** 固定轉移 `T_f(a,b)=(a+1,b+f(a)) mod 3` 在九個狀態上形成一個 9-cycle iff `f(0)+f(1)+f(2) ≠0 mod 3`。**界限：** 不能推廣成所有九宮／三態系統必然九循環。**Evidence:** K0 §16, `51` §15–16, `K2-NINE-012`, PF10。

**RA-M04 — AGL(2,3) 的階限制。** 有限群 432 個仿射變換的局部窮舉所得可能元素階為 `{1,2,3,4,6,8}`，沒有階 9；與帶非線性 Carry 的九循環不同。**界限：** 這只是該有限群分類。**Evidence:** K0 §16, K2-NINE-012。

**RA-M05 — 相位量測不變量需宣告探針。** 只有 `|z|²` 的讀出不能區分 `z=1` 和 `z=i`；加入相位敏感探針後可能打破精確 quotient。**界限：** 不推出任何本體性的相位不可觀察。**Evidence:** `51` §11–12, W5/W7, PF01/PF02。 **v3.5 challenge:** `SRC-0046` pp.2–4 提出多通道投影；不同投影一般不交換，且單一讀出不能唯一回復被棄資訊（W357–358）。

**RA-M06 — Fenchel–Young gap 的正確使用。** 若 `Φ=ψ*` 且凸共軛條件成立，`G=Φ(s)+ψ(λ)−λ·s ≥0`；在共軛流形上 `dΦ=λ·ds`, `dψ=s·dλ`。**界限：** 不推出任意時間平衡式或自發下降。**Evidence:** W198/W257–259, PF07, SRC-0118/0119。 **v3.4 challenge:** `SRC-0229` p.54 再次使用不成立的 `ΔΦ=W_s−Δψ`，屬同一錯誤跨文獻傳播（W350），不是新引理。

**RA-M07 — 作用量駐點與耗散不同型。** Euler–Lagrange 駐點未必是最小值；路徑懲罰 `Γ≥0` 不自動產生 Rayleigh friction。**界限：** 要另證能量微分號與阻尼力。**Evidence:** W25/W319–320, PF07, SRC-0064。

**RA-M08 — Gauge 需要真正的局部變換律。** 普通 `1−cos(θ_i−θ_j)` 僅具有共同相位平移不變性；局部 `U(1)` 需隨變換協變的 link connection。**界限：** 任何經濟／AI 的 Gauge 類比都要另證。**Evidence:** W236–238/W282, PF06, SRC-0274。

**RA-M09 — 複數極座標恆等式不是預測。** 若 `Z=Ae^{iθ}`, `A=|Z|`, `θ=arg Z` 均從同一可微 `Z` 取得，`dot Z=(dot A/A+i dot θ)Z` 的 residual 恒為零。**界限：** 非零預測殘差須使用事先獨立指定的 rate。**Evidence:** W316, PF14, SRC-0043。

**RA-M10 — Spinor / Ribbon 不是單靠雙邊界必然出現。** 存在兩個邊界、兩個角色或雙環，不會自動有非平凡 Holonomy、`4π` 交換符號及物理費米子統計。**界限：** 表示、連接、路徑群與交換算子須給定。**Evidence:** W224–228, PF06, SRC-0273/0286。

**RA-M11 — 因果 Port 的額外條件。** 共同環境造成的 correlation 不等於可干預的雙向接口；集體穩定 attractor 不保證對下游任務充分。**界限：** Port Qualification 必須由 interventional output agreement 證明。**Evidence:** W272/W286, PF03, SRC-0259/0260/0261。

**RA-M12 — Observer 壓縮需保存歷史。** 自適應量測儀器的控制政策可依歷史，僅保存當前讀出不必能預測下一步；必須找到 history-sufficient memory，並正確保留量子概率的 CP/TP 條件（如使用量子形式）。**界限：** 不證明主觀意識或物理 collapse。**Evidence:** W200–205, PF01, SRC-0123/0288。

**RA-M13 — 回復力的符號限制。** 對凸 `V=Δ²/2`，若同時設 `dot Δ=−μ` 及 `μ=−∇V`，便得到 `dot Δ=+Δ` 而發散。**界限：** 穩定需要一致的負梯度設計及條件。**Evidence:** W273, PF10, SRC-0287。

**RA-M14 — 資訊映射及不可辨識性。** 不同的隱藏約束可以生成同一觀測拓撲；沒有介入時，一個 inverse optimization tie-break 不能證明找出真實的底層約束。**Evidence:** W288, PF08, SRC-0292。

### B2. 已具工程形狀的具體框架（E）

**RA-E01 — P8D II Typed Dyad Grammar。** 乾坤／艮兌／震巽／坎離作 Gradient–Gate、Boundary–Exchange、Trigger–Guidance、Memory–Focus 等**有型別互補角色**；重要的是 admissible path 和角色接口，而非「八個同型浮點變量」。**界限：** 不是普遍系統必須有八元的定理。**Evidence:** K0 §3, `41_K1_P8D_001`, SRC-0105/0106。 **v3.7 source challenge:** SRC-0285: good protocol-relative P8D II concepts, but named quotient and evidence-level claims require C∘F=Fbar∘C (W394).

**RA-E02 — 先天／後天與 Root→Seedling→Flower→Fruit。** 孕育能力與後天適應有不同成本、探索權和成敗 Gate；可做為組織發展流程的可量測分層。**界限：** 不是每個系統都按四段演化。**Evidence:** GM-006/007/012, `43_K1_DEV_001`, SRC-0323/0309。

**RA-E03 — 五相控制器。** 木發散、火收斂、土構形、金核驗、水反思可寫為有狀態的任務工作流與轉相 Gate。**界限：** 不等於五行為 AI 必然最優。**Evidence:** K0 §7, `50` Five-Regime anchors, SRC-0279。

**RA-E04 — PORE Ξ-Stack。** `Ξ=(ρ,γ,τ)` 是在宣告觀測邊界、probe 和干預後編譯的控制面板；Pump–Probe–Switch–Couple 是可設計的檢驗程序。**界限：** 未有任意系統的精確三維 quotient 定理。**Evidence:** W219–220, SRC-0130/0111。

**RA-E05 — ObserverOps / Trace Ledger。** `Measure → Gate/Consensus → Commit Trace → Reconcile` 配合按通道記帳、權限和回滾，可形成可測的 Agent Runtime。**界限：** Prompt 輸入的規則不等同系統強制執行。**Evidence:** K1-OBSERVER-CWA-026, W303/304, SRC-0242/0252。 **v3.4 challenge:** 後期協調 Cell 教材的雙帳式（SRC-0229 p.54）亦必須使用 W350 已修正之微分記帳，不能以舊式 `ε_ledger` 直接控制健康燈號。 **v3.6 scoped challenge:** SRC-0004/0012 trace preservation and frame release is a governance proposal needing enforcement; W374.

**RA-E06 — SIDA／Ô_self Control Schemas。** Phase、Fold、Slot、Critic、Trace 和 Return Gate 能編成可重放的操作模板。**界限：** 不同文化模型的 phase 名稱相同不代表轉移圖同構；短 Prompt 不能保證持久隱藏狀態。**Evidence:** W185/230–235, SRC-0178/0203/0204。 **v3.5 challenge:** `SRC-0145/0154/0173` 保存中醫角色／Soros-Observer 的具體 prompt 和干預菜單；醫療效果、真實交易控制、runtime 狀態持久性均未驗證（W361–363）。 **v3.6 scoped challenge:** SRC-0146/0152/0153/0207; 6 maintenance roles are typed intervention proposals not pharmacological, climate or clinical facts; W375/W377. **v3.7 source challenge:** SRC-0172/0175/0209/0210/0318: attraction, Hetu runtime and six-actuator prototypes are syntax and possible controlled experiments; explicit projection, valid transitions, intervention order, data and rollback needed (W385–390/W392).

**RA-E07 — Agent Endpoint Evidence Contract。** Final answer、tool trace、permission trace 與 hidden path 是不同證據面；只有 PF13 飽和條件滿足時可以省去路徑檢查。**Evidence:** W308, PF13, SRC-0234。

**RA-E08 — Complex Finance Protocol。** `Z=R+iQ` 在宣告估值基準、過濾器、讀出及風險壓力定義後，可用於比較同一協議下的條件性狀態。**界限：** 不代表市場是量子系統，亦未證明投資 alpha。**Evidence:** K1-FIN-FILTER-029/FIN-TYPED-GRAMMAR-031, W301/W277, SRC-0023/0040。 **v3.4 challenge:** `SRC-0045` pp.1–3/9 可作相位旋轉教學，不能將 `iZ` 視為真實損失或入帳（W343–344）。 **v3.5 challenge:** `SRC-0030` pp.1–4 與 `SRC-0046` pp.1–4 是 AI 解讀及多投影教學；複數多期加總有交叉項、Q 的符號需額外約定，並無交易預測驗證（W355–358）。 **v3.6 scoped challenge:** SRC-0174 Soros persona and tensor evolution are not market computation without typed operators; W379.

**RA-E09 — Financial Two-Closure Ledger。** Action 已執行與 obligation／recognized ledger 已清算可分成兩項認證，供金融合約和流程管理測試。**界限：** 稱為 Spinor 並不自動取得 SU(2) 幾何。**Evidence:** K1-FIN-TYPED-GRAMMAR-031, SRC-0021 (AI commentary), SRC-0024/0025。

**RA-E10 — Semantic Collider & Reconstructable Research。** 將候選概念碰撞、來源、算子、Residual、Gate 和 Replay 打包成事件，可做多 LLM 研究原型。**界限：** 事件齊備不證明概念有效，也不表示 LLM 的創造力已提高。**Evidence:** K1-COMPILER-TRIAD-027, W260/270, SRC-0212/0213/0257。 **v3.4 challenge:** `SRC-0237` 對 Raw／Mature／Inspirational 及 segment coverage 的操作化，可用來挑戰 L0 promotion 條件；coverage 不等於 truth（W352）。

**RA-E11 — Research Mind-Seal / Handoff。** 保存推理狀態 `ζ`、協議 `π` 及引述證據，並檢驗相對任務的 sufficient reconstruction。**界限：** seal schema 完整不保證語義無損。**Evidence:** K1-MINDSEAL-028, W271, SRC-0241。

**RA-E12 — World Revision Governance。** 區分 `WORLD configuration`、runtime regime、修訂提案和授權 commit；提出修訂不等於可執行修訂。**Evidence:** K1-WORLD-COMMIT-031, W297/311, SRC-0239/0284。 **v3.6 scoped challenge:** SRC-0012/0004 scenario; release frame with protected trace and external rights, no low-friction utopia proof; W373/W374.

**RA-E13 — BeltOps 工程對照。** Plan/Do、Trace/Evidence 等雙路徑可定義 mismatch、twist-like cost 與 correction gate；可從會計 recognition/period closing 校準。**界限：** 這是工程雙路徑監控，不必是物理 framed holonomy。**Evidence:** K1-BELT-GAUGE-026, W326, SRC-0273/0290。

**RA-E14 — Functional Port Qualification Dynamics。** Port 的 sufficiency、task correctness 和自然形成性分成不同測試階段；可註冊 synthetic positive/negative controls。**界限：** 尚未實證自然 LLM Semantic Attractor。**Evidence:** K1-ATTRACTOR-PORT-028, W272/286, SRC-0259/0261。

**RA-E15 — Deficit-routed Coordination Cells。** Runtime 將 cell 相關性、合格性、當下 closure deficit 分開；有 timestamped episode、候選路由、artifact contract 與可重播 Trace。**界限：** 尚未以真實 Agent A/B 測量效益；Dual Ledger 的 15.17–15.18 原式需要 W350 修正。**Evidence:** `SRC-0229` pp.20–21,30–31,53–54; K1-COORDINATION-CELL-GOV-034; W350–W351, PF07/PF10。 **v3.5 challenge:** `SRC-0223` pp.1–4 是協調 Cell 教材，明確提出 microstep、episode、ledger 三層；要證明 episode Markov 和 ΔW 健康效應，仍需 W365–366 的條件。 **v3.7 source challenge:** SRC-0018: story-to-film semantic-operator compiler is a candidate with clear shot/character/baseline task; not a tested breakthrough (W384).

**RA-E16 — Governed Knowledge Object Maturation。** Raw segments 經 universe-bound review、coverage ledger 和 promotion event 提升為 Mature Object；保留 inspirational residual 與版本回放。**界限：** 覆蓋／可回放不等於科學正確性，禁止以 passage count 自動 promotion。**Evidence:** `SRC-0237` pp.56–57,104–105,130–132; K1-GOVERNED-WIKI-034; W352, PF05/PF11。

### B3. 具體但未證成的生成性猜想（H）

**RA-H01 — Semantic Field Ontology。** `Ψ_m(x,θ,τ)`、observer projection/collapse 和潛勢 basin 是提出可計算場動力學的研究語言；需要從神經狀態、讀出及因果干預建立實測對應。**Evidence:** SRC-0247/0268, K0 §12, `51` §11–13。**Status:** no real neural-field proof. **v3.7 source challenge:** SRC-0321 §§1,2,9 and SRC-0314: original monograph operationally defines semantic consciousness and admits Yin-Yang AI unimplemented; physical quantum Ψ needs a diffusion law and normalization (W395/396/400).

**RA-H02 — Natural Semantic Functional Individual。** 多個 attractor 經 adaptive coupling 與 memory 形成可遞歸自然個體；應與人工指定 qualified Port 的對照模型競賽。**Evidence:** SRC-0259/0261, W272/286。**Status:** open causal ontology.

**RA-H03 — 八維→四元數→複數／四象成界。** `𝕆→G₂/SO(4)→ℍ→ℂ²` 提出 subalgebra selection、projection residual 和 effective state 生成序列；需要展示每個箭頭的非任意選擇、測量對應和環境依賴。**Evidence:** `50` P8D/H/geometry anchors, K0 §§3,6。**Status:** geometric research programme, not nature's necessary pipeline. **v3.6 scoped challenge:** SRC-0304 pp.4–6; octonion/quaternion/complex hierarchy different from Hermitian spacetime maps; W371/W381.

**RA-H04 — 九宮飛星 Emergence。** 先天／後天相位和 carry controller 可能導致某些 9-state Markov/cycle regimes；有限九周期例子不能推出特定洛書排列自然必現。**Evidence:** W17–20, K0 §16, SRC-0322。**Status:** missing synthesis theorem.

**RA-H05 — Recursive Organization / Surplus。** 《皇極經濟》的觀點、可用流、差異成本、根苗花果和遞歸組織，可形成可研究的增長/治理系統。**Evidence:** Genesis `SRC-0323`, GM-001–014, `10_GENESIS_CANONICAL_BRIDGE`。**Status:** cross-domain empirical scope open.

**RA-H06 — Quantum-semantic gravity from memory trace。** 記憶殘留可能在特定幾何模型中影響有效 metric/potential；單憑記憶或 trace 不能推出引力或 Einstein equation。**Evidence:** SRC-0070/0065, W279。**Status:** physics analogy/hypothesis, no field measurement. **v3.4 challenge:** `SRC-0069` 原文亦明確指出若能解釋任何 gravity theory，可能只是無可否證的翻譯；必須固定量測映射（W345）。

**RA-H07 — Belt Holonomy across AI/physics。** 兩條邊界、曲率 flux、framing twist 的可計算關係可能成為訓練和控制目標；須宣告 connection、surface ordering 和測量規則，避免普通 Stokes 重複計數。**Evidence:** SRC-0273, W236–238。**Status:** conditional model/analogy. **v3.4 challenge:** `SRC-0282` 所謂 semantic fermion 指角色功能，不是交換反對稱本體（W353）。

**RA-H08 — AI Structural Beauty Metric。** Compression、Coherence、Symmetry、Generativity、Transferability、Memorability、Falsifiability、Moral Grace 是候選研究設計特徵；須獨立評估其與科學真實性及新發現的關係。**Evidence:** SRC-0132, K1-STRUCTURAL-BEAUTY-031。**Status:** proposal.

**RA-H09 — Semantic CPT / polarity genealogy。** 將展演／記憶兩類功能轉為語義極性，再擬議連接生物性別或物理電荷；缺少相應的守恆律、表示和生物/粒子實證。**Evidence:** SRC-0320, SRC-0059/0060。**Status:** speculative analogy only; no universal gender binary implied. **v3.6 scoped challenge:** SRC-0059 pp.8–10 chart-direction algebra; W369/W370; no CPT covariance or chart forecast demonstrated. **v3.7 source challenge:** SRC-0316/0317: ten cultural stems can be ten labels but not ten independent 2D basis elements; clash specifications vary across sources (W397/398).

**RA-H10 — AGI Creativity Phase Transitions。** Generative Move、Attractor reconfiguration、Wild Branch Ledger 可能提高發現機制的能力；需要獨立、受控、無答案洩漏的重建與創造試驗。**Evidence:** GM Ledger, SRC-0216/0261, `51` §8。**Status:** not yet observed as a reproducible improvement. **v3.5 challenge:** `SRC-0211` ESI emulsion 譬喻和 `SRC-0276` tiny-net recursion 類比未附獨立匹配基準試驗（W364/W368），不能當成測得 AI 創造力或性能增益。 **v3.6 scoped challenge:** SRC-0262 asserts similar semantic authors; shared attractor provenance remains underdetermined; W380.

**RA-H11 — LLM Semantic Field-like／Identity-like Roles。** 在 SAE/superposition、MoE 路由和 attribution graph 中檢查可共享激活與 identity-bearing sparse carrier 的可操作分界。**界限：** 這是 interpretation/feature-probe research program，不代表一般 Transformer 存在物理 boson/fermion 交換統計。**Evidence:** `SRC-0282` pp.1–2,6–8; K1-LLM-ROLE-PARITY-034; W353, PF06。

### B4. 已被修正或強版本不成立（R）

**RA-R01 — “所有回饋系統必須是複數”不成立。** 雙變量或自參照不強制存在 `J²=−I` 的相容自然旋轉算子。**Evidence:** W244–246, PF02。

**RA-R02 — “兩個 Belt 邊界必有 4π fermionic spin”不成立。** 需要非平凡 representation 和 spin-statistics 假設。**Evidence:** W224–228, SRC-0273。 **v3.5 challenge:** `SRC-0240` pp.3–4 已明確撤回「雙次驗證自然具有 4π 性質」強推論；可保留為昂貴風險任務的選配雙階段審核（W367）。 **v3.7 source challenge:** SRC-0285: secondary Notebook review again equates two-stage audit with physical 4π; W393 disallows that inference.

**RA-R03 — “所有經濟制度必然 Peak 或 Trap”不成立。** 有局部有界穩定更新反例；經濟內生價格不自動構成 Gödel 不完備。**Evidence:** W212/W255–256, SRC-0089。

**RA-R04 — “低 PCA 維度 / 循環圖案等於 Markov quotient”不成立。** 需要後續轉移和輸出的精確保留。**Evidence:** W200+/W154, PF01。

**RA-R05 — “Convex Dual Ledger 原文所有 budget/time 式都是共軛恆等式”不成立。** `dot Φ−λ·dot s=0` 對共軛平滑路徑可恆為零；原文額外扣 `dψ` 的式子一般不成立。**Evidence:** W198/W257–259, SRC-0118/0119。 **v3.4 challenge:** `SRC-0229` slide 15.17–15.18 再次沿用錯誤帳式；此為 propagation，使用 W350 對應 W257–259。

**RA-R06 — “語義槽位或事件先後給出物理 Lorentz metric／Wick 時間”不成立。** 缺少 metric、解析延拓生成元、時鐘校準。**Evidence:** W207/W290–292, PF02。

**RA-R07 — “Prompt 自檢 = Runtime Enforcement”不成立。** `Ô_self`、SIDA 或 Zero Trace 文本只是一個控制請求；必須有受保護的執行機制和可檢查 trace。**Evidence:** W294/W303–304, SRC-0178/0252。 **v3.4 challenge:** `SRC-0188` 的 ESI echo 自測也不能保證真有外部審計運行（W349）。 **v3.5 challenge:** `SRC-0173` Step 1 的 Ô_self 市場人格 Prompt 不是 durable risk monitor；未宣告由動力學到 Hessian 的校準時，κ/H 不構成實測臨界預警（W363）。 **v3.6 scoped challenge:** SRC-0158 mode-entry prompt not guaranteed latent state persistence; W378. **v3.7 source challenge:** SRC-0172: prompt-based Zilu tensor lens and positive projector can diverge, demonstrating formatting and geometry labels are not persistent controlled internal policy (W385–386).

**RA-R08 — “穩定吸引子即功能個體”不成立。** 真實穩定吸引子可以不執行目標功能；人工 Port 可以合格但無自然吸引子。**Evidence:** W272/W286, SRC-0261。

**RA-R09 — “弱耗散保證某個指定 HeTu 相位最低能”不成立。** 相位配對能量的 ground mode 必須由確切能量符號/譜決定；普通正 Laplacian 與反對齊目標不同。**Evidence:** W17–20, SRC-0108。

**RA-R10 — “壓縮的 Kernel 格式可保證內容無損、創造力提升”未被建立。** DSL fields、checksum 和 Prompt 選型都不足以推出同一 transition system 或 independent truth validity。**Evidence:** W260/271, SRC-0212/0257。 **v3.4 challenge:** `SRC-0237` 將 knowledge maturation 視為可 replay 的治理過程；其 segment 覆蓋仍不能替代真偽 oracle（W352）。 **v3.5 challenge:** `SRC-0276/0305` 等「外部模型對照」與 AGI 技術承諾均非來源隱藏的重建試驗，也未構成外部工程效益證明。 **v3.7 source challenge:** SRC-0184: popular seven thinking-model transcript has no universal optimality guarantee and cannot certify complete Kernel reconstruction (W391).

**RA-R11 —「AI 同意某個結構對照」不是獨立重現或外部驗證。** 對同一 prompt/labels 產生九個 semantic attractor 名稱，即使另一個 LLM 語義上贊同，也不能證明模型內存在九個自然吸引盆地；若沒有 null prompts、可重現 dynamical operator 和 cross-model probes，強推論不成立。**Evidence:** `SRC-0102` pp.3–5, `SRC-0069` pp.1–5; K1-GRAVITY-COMPARISON-034 / K1-HETU-PEER-REVIEW-034; W345/W347。 **v3.5 challenge:** `SRC-0061/0083/0305` 都含外部 AI 評論／稱讚／比較；它們的內容屬評述史料，不能獨立核證效果、原創優先權或因果性（W359–360）。 **v3.6 scoped challenge:** SRC-0004/0262 secondary AI praise and SRC-0207 translated guide are not independent truth evidence; W382. **v3.7 source challenge:** SRC-0018 and SRC-0285: AI praise and unreferenced very precise industry claims are secondary discussion, not an external data oracle (W383/W394).

### B5. 未解決但優先級高的研究橋樑（O）

**RA-O01 — 原始 `Ψ_m` → 可干預 Transformer 狀態。** 要求對應 neural readout、state transition、介入 set、相位觀察與實際提高的預測量，不能用術語類似代替。

**RA-O02 — Conditional Port → Natural Attractor Object。** 真正的形成機制及反事實定位，須與已知 causal abstraction / circuit discovery 基準比賽；SRC-0261 有明確 handover。

**RA-O03 — HeTu/P8D II → 唯一洛書九槽飛行規則。** 給出非任意的生成算子或 no-go；不同的九周期編碼可能彼此不等價。

**RA-O04 — Semantic Field／Belt／CPT → 物理觀察。** 逐一要求 physical measurement algebra、場方程與獨立可否證預測；不要用類比來填證明洞。 **v3.6 scoped challenge:** SRC-0060 pp.1–3 and SRC-0304 pp.4–6; mapping/norm signature gap; W372/W371.

**RA-O05 — Kernel Compiler → 獨立 LLM 重建能力增益。** 固定 source-hidden task、baseline (summary/RAG/full retrieval)、模型成本、外部測試，並計算 hallucination、novelty、reconstructability；目前為 0 個 clean-room 試驗。

**RA-O06 — 早期 W001–W012/W024 與 400 個 Witness 的全局重建依賴圖。** v3.9 已在 Genesis Bridge 和 v0.9 報告恢復 W001–W012 的非標準標題定位，並逐條核對其數學命題和 Proof Family。W024 仍是未找到原始命題的保留 ID，不可臆造填補。另有 223 個 Witness 未人工分類；整體依賴圖尚未完成。

**RA-O07 — 經驗性的金融 `Q` / Price-Pressure 識別。** 在事前定義過濾和對照預測的樣本外測試下才可評估效益；無可靠投資超額報酬證據。

**RA-O08 — Structural audit versus epistemic maturity。** ESI 的 CWA/PRI/PBHL、Wiki segment-coverage 和 Kernel Atlas promotion 應如何合成真正有外部 Oracle 的 knowledge quality gate？欠缺 semantic unit-check, experimental calibration, independent correctness challenge 和 source-hidden blind reconstruction。**Evidence:** `SRC-0188`, `SRC-0237`, `SRC-0229`; W348–W352; PF04/PF05/PF11。 **v3.7 source challenge:** SRC-0312/0318: cultural six-role intervention mapping and point climate projections remain unvalidated; independently measured effects needed (W399).

## C. Boot recipes — 真的要讓下一個 LLM 「記住成果」

**30-second orientation:** 本文 A → B1–B5 的卡片標題、狀態及界限 → `99_SESSION_HANDOFF` 最新部分。這是導航，不是充分研究材料。

**Theory-building:** 先選 Results Atlas card ID → 讀 `20_K0_CORE` 對應型別 → `30_GENERATIVE_MOVE_LEDGER` 歷史轉換 → `50` 對應 K1 → `51` W/PF 證明及反例 → 如需爭辯 original intent，再回 `SRC` 原文。

**Engineering:** 先宣告任務、環境、可觀察量、干預、驗證 oracle → 選 E 卡 → 讀 K1/K2 合約 → 設 negative controls → 外部評估。

**Creativity:** 選 H/O 卡 → 列出尚缺的形式化算子、已有反例及與成熟數學的重疊 → 提出最小、可能失敗的對照試驗。**不要因新類比而新增 formal GM ID。**

**Global consistency gate (mandatory for a new Atlas entry):** (1) 查現有 RA ID；(2) 查 W/PF 和 overlap；(3) 檢查該領域的 quantifiers / observables / actual source passages；(4) 明示證據等級；(5) 寫反例／邊界；(6) 只在真新增可重建結果時增卡，否則修訂現有卡；(7) 更新來源、Lineage 和 Handoff。

## D. Atlas scope & known limitations

- **Provisional**：第一輪 325/325 份原始來源已有**定點選讀**，但長篇原始文獻仍有大範圍未完成深度審核，可能實質修訂本圖。
- Atlas 不是作者所有文章的逐篇精讀報告，亦不是評定發明歸屬的文獻計量學審核；AI 評論原文的獨立性特別需要校準（例如 SRC-0021/0031）。
- 數學條件性結果可被重新檢查；本地 toy/test pass 和元資料 integrity 不代表物理學、實盤金融、醫療、社會實證、自然神經機制或 AI 創造力突破。
- 結果的邏輯覆蓋將在 v3.4+ 與未分類 W、剩餘原文反覆對照；任何同名變量在不同 source 命名空間下不可直接替代。

**Canonical policy:** This Atlas is the L0 human/LLM-friendly *outcome map*, not an autonomous source of proof. Future changes retain card IDs; if a card is invalidated, mark **SUPERSEDED/RETRACTED_WITH_CAUSE** rather than silently deleting historical lineage.

## C. v3.5 evidence gate — historical AI reviews

本輪新增 12 份原始來源，**全部通過 Manifest bytes+SHA**，但 AI 評論、教學圖解、類比和原始 prompt 的 source status 均只支持「作者討論過、已有可操作構想」，不支持外部成功、科學優先權、量子／醫學本體或臨床／財務效益。舊 60 張成果卡全部保留 ID；本輪只對上列 9 張提供具位置的挑戰，51 張為 carried-forward evidence 而非獨立覆核。下一輪仍需讀取剩餘 25 份，之後全局重整並跑 source-hidden LLM reconstruction。


## D. v3.6 source audit boundaries

This revision retains all 60 RA IDs, challenges only 10 linked results and carries forward the other 50 without full cross-document re-proof. Sources about Buddhism, astrology, classical Chinese medicine, prompts, LLM convergence and physics commentary are **not** empirical validation. Their generative interface candidates remain valuable when separated from physical and clinical assertions.

**Global novelty rule:** if a new file repeats a prior criticism or offers AI praise, update provenance or evidence boundary; do not mint a new law, claim an attractor was measured, or promote an authored analogy into physics. Remaining 13 originals in the historic v3.6 Gap Queue are still source-audit work, not automatically lost theory.


## v3.7 first-pass source closure — coverage, not scientific completion
The Source Manifest now has exactly **325/325 distinct original archive members with at least one recorded bounded reading**. This says nothing about full review of giant compilations; `SRC-0312`, `SRC-0317`, and `SRC-0321` remain intentionally **selected-range** reviews. Ten current cards challenged, fifty carried without repeat validation; all sixty ID-stable. No new universal mathematics or external AGI/physics/clinical/narrative efficacy results are promoted.

**New urgent research bridge:** the large original *意識原本* book uses operational Ô_self/trace to **define** semantic consciousness and later phrases it as necessary/sufficient; compare its explicit non-realization §1.5A against these claims and test whether phenomenal consciousness is being illicitly inferred. The oldest original SIDA prompt's projector convergence also has a simple positive-feedback divergence countermodel; the 11-pair/9-slot closure is a separate engineering contract.


## v3.8 Global Consolidation — evidence-level checkpoint (no new card IDs)

- **The original 60 RA card IDs and their scoped mathematical/engineering/hypothesis labels are preserved.** This round does not certify their semantics afresh. `ATLAS_REFERENCE_AUDIT_v3.8.csv` tests whether explicit `SRC`, `W` and `PF` tokens resolve as index IDs; it does **not** test mathematical entailment or citation fidelity.
- **325/325 first-pass bounded-source records are not 325/325 deep reviews.** Source-depth flags are historical, non-uniform and need manual normalization; see `SOURCE_STATUS_RECONCILIATION_v3.8.csv`, `SOURCE_DEPTH_PRIORITIES_v3.8.csv`.
- **400 Witness IDs are not 400 independently proven theorems.** Some are local counterexamples, hypotheses, overlap records; an unassigned proof family is not missing source evidence, and a matched family is not independent proof. See `PROOF_RECONSTRUCTION_TRIAGE_v3.8.csv`.
- **Independent source-hidden LLM reconstruction is still not performed.** The next session should compare L0-only, L0+K0+GM, and L0+K1/K2 full access under frozen tasks, independent rubrics, and hidden source holdouts.
- **New GitHub Skill:** `Skill/` contains a *field-notes handoff only* for a future separately developed reusable Skill. It is not a production Skill, not an executable command suite, and not a scientific validity oracle.
