# 06 — 數學與跨領域強主張：實際反例／保留弱版本案例庫

> 從 v1–v4.3 編譯經歷萃取。這些是未來 Skill 的測試素材與研究風險類型，**不是**代替原始來源的最終判決。引用的 W/SRC 需要由新 Session 對真實 bytes、公式版面和編譯證明再作核對。

## A. 型別錯配和定理條件

| 原文生成性想法／風險 | 可重現的限制或反例 | 應保存甚麼 |
|---|---|---|
| SIDA scalar potential 的 Hessian 「Hopf 虛特徵值」 | 實純量 C² Hessian 實對稱，特徵值實數；Hopf 使用 flow Jacobian `Df` 的複數共軛特徵值和非退化條件。見 W214／W233 | 帶真實動力學 `f` 的 bifurcation 候選，不能把 Hessian 當 Jacobian |
| `action stationary` 稱能量最小 | Euler–Lagrange 給必要駐點，未必極小、穩定或唯一。W133／W217 | Variational equations 和獨立二階／Lyapunov 條件 |
| 非負路徑懲罰 `Γ` 直接給耗散 | 非負 potential/path cost 不等於速度相關 friction；保守 gradient 項可改變等勢而不消耗能量。W025、W326 等 | 明確定義 dissipative operator 和能量單調性 |
| General Life / Dual Ledger 的 `ΔΦ=∫λ ds−Δψ` | 在凸共軛匹配下 `dΦ=λ·ds`、`dψ=s·dλ`；二次例子 `0→1` 得左邊 `1/2`、錯誤右邊 `0`。SRC-0119 / SRC-0229，W257–259/W350 | 正確的 Fenchel–Young Gap、互補的雙路帳本、跨來源錯誤傳播鏈 |
| Eigenvalue / phase condition 過度普遍化 | 對任意二狀態耦合，不必存在 `J²=-I`；引入 ℂ／Spin 結構需指明旋轉算子、保持子空間或 Clifford 表示 | 相位建模假說，而非「所有自指系統必然複數」 |
| `AGL(2,3)` 九週期／Carry | 仿射群元素階無 9；但特定非線性 `T_f(a,b)=(a+1,b+f(a)) mod3` 以 `sum f≠0 mod3` 產生 9 週期。W031/W033 | 轉換類別的分界，兩者並不矛盾 |
| Hetu 1–10 配對／Luoshu 九槽 | `(1,10)` 不能當作集合 {1,...,9} 的閉合轉移，需映射或外部邊界政策 | 組織/AI slot scheduler 的候選，分清 topology/occupancy/transition |
| RH self-adjoint 模型已證零點分布 | 自伴算子實譜不給所有 ζ 非平凡零點的位置；須建立 global spectral-zero correspondence 和 completeness。W275/W276 | 挑戰性的逆譜研究問題，無 RH 證明 |

## B. 可觀察量、同構和逆問題

| 風險 | 必須問的問題 | 原因 |
|---|---|---|
| `effective quotient` 宣稱完全無損 | 對哪一類可選行動、干預、未來 readout 與轉移？ | `π:S→P` 對某任務充分，改變 action set 會失效；PF01 |
| `endpoint valid` 被誤認為 trace 有效 | validity set 是否為 output projection 的 fibers 聯集？ | `T=π⁻¹(π(T))` 才能僅靠最終輸出驗證執行；PF13，與動力學 quotient 不同 |
| SIDA Phase/Slot/Fold 名稱匹配 | 是否保持轉移邊、合法操作序列、可達性與 readouts？ | 只有名稱雙射不是 graph/operational isomorphism |
| Purpose Belt 由觀察拓撲反推約束 | 是否存在兩組 constraint 產生同一 topology？干預可否區分？ | 逆問題一般需 identifiability/prior，非唯一便不能聲稱找出真正目的 |
| Observer Ξ=(ρ,γ,τ) 可以控制整個 3D 系統 | rank G=2 只涵蓋兩方向，是否有 Lie brackets/可達控制？ | 低維 dashboard 和真三維 controllability 不同 |
| 多觀察器 Gate 看似交換 | `P_task P_evidence=P_evidence P_task` 是否已證？ | 不同投影順序可能丟不同資訊，Skill 必須保存實際 pipeline order |
| Synthetic Attractor Fusion 宣稱 Natural Individual | stable attractor → sufficient port → functional correctness → naturally learned function，每一箭頭是否實證？ | 稳態、端口、功能、自然湧現是四個問題（SRC-0259/0260/0261） |

## C. 複數金融、量子、Gauge 與實際物理

- `Z=Ae^{iθ}` 若 `A,θ` 從同一 `Z` 定義，`Ẋ=(Ȧ/A+iθ̇)Z` 是恆等式；`ε_dyn` 在同一資料上應為零。要真模型殘差，必須用*獨立預測*增長率與相位速度（PF14；SRC-0043/W316）。
- 多期複數和有交叉項：`|ΣZ_t|²=Σ|Z_t|²+2Σ_{i<j}Re(Z_i conj(Z_j))`；單期 Pythagorean identities 不可隨意當多期風險守恆。多個金融 Q-channels 不是自然可加的守恆量。
- `1−cos(θᵢ−θⱼ)` 一般具 global shift invariance，不是獨立 local `U(1)` gauge invariant；需引入變換的 link connection `A_ij` 和對應測量。
- Ribbon／兩個 Ledger／兩次驗證，不自動具有 Spinor 4π 周期或 Fermionic Exchange Statistics；需表示理論及物理 measurement contract。
- 經典資料可編碼到 Hilbert 向量甚至非因子化形式，不構成 Bell 違反、量子糾纏的物理證據。量子 instrument 要符合 CP/TP/probability 和 history dependence；不能由符號推出意識。
- `boson-like` distributed features、`fermion-like` sparse routing 是可測工程角色類比，不是粒子交換反對稱性。
- 四元數 `ℍ≈ℝ⁴` 是實向量空間同構，並不自行附帶 Lorentzian metric；Wick rotation 類比與真物理時間亦需獨立橋樑。
- `memory/gravity-like force=-∇Φ` 要有可積分、位勢存在條件；有記憶不代表物理重力。
- 漢學／術數（四象、六爻、九宮）可為 finite-state controller 的研究靈感，**不能偷渡**天體預測、醫療功效或普適物理定律。

## D. Runtime、治理與評測的非等價

- Replayable event history ≠ 任何人不可竄改的 authenticated provenance；可修改全部事件及 hash chain 的攻擊者仍能寫出自洽鏈。
- Critic-order CSA 要實際比較不同排列 `A(B(x))`／`B(A(x))`；SRC-0242 的示例曾在不同 permutation 中記錄同一原始多數決，因此測不到宣稱的 order sensitivity。
- 多次驗證並不等於多個**獨立**證據來源。模型自己為自己評分，須有 external oracle／human audit／holdout。
- Prompt 的「不得提交」、「先測試」不等於真正 Runtime permission gate；需要外部 API、event trace、rollback、authority boundaries、adversarial probing。
- Agent controls 的矩陣秩冗餘不保證受限成本、權限、延遲及作業資源下仍可刪控制。
- 採用「n_bad_events/n_malicious_inputs」作比例，若一個輸入可觸發多個 channel，值可能 >1；分母與 unit of analysis 要寫清楚。
- 九宮／道德拓撲／SIDA 多版本的共名結構，不可把同一項反例複製成多個「新定理」。但也不要刪去其不同版本的歷史來源。

## E. 不要誤用案例庫

1. 反例否定的是一個**量詞和前提清楚的強主張**，不一定否定來源整體的弱版本或創造性研究方向。
2. 同一 source 裡作者可能已先提醒這個限制；編譯器應記成 `PRESERVES_SOURCE_GUARDRAIL`，不要誇大為新發現。
3. 對任何高風險公式仍應回到原文頁面；不要只憑本案例庫評審尚未核對的原始版本。
4. 若看到兩個 Witness 同家族，先檢查其量詞、可行域、控制類別、輸出通道，再選 `SHARED_LEMMA`、`GENERALIZES`、`REFINES` 或 `NOT_EQUIVALENT`；**不能自動 delete/merge**。

## v4.8 補錄：模型秩、投影秩與商空間是三種不同測試

- local Jacobian low rank `rank(DF−DF₀)≤r` 僅在清楚宣告 `F=F₀+Γ∘h`, `h:X→ℝʳ` 等相應微分分解時跟隨 chain rule。若回灌係數 c(x) 依狀態變化，必須包括 `y Dc`。`SRC-0106` p.34 與 `L48-02`；不可用通道數量當導數秩。
- `rank(DF−DF₀)≤r` 不是 `π∘F=\bar F∘π`。前者是局部算子分解；後者要求在同一 π-fiber 下全部准許的未來轉移與觀測一致。`L48-03`。
- `ε_cl=||Δ_J||/||J−J₀||` 若分母為 0 不可計算；若 J₀/normalization 自由調整，「小 ε」無可識別內容。應報告原分子、原分母、基準與負對照；`L48-04`。
- return operator 維度 r 不等於系統全部 eigenmodes 的數量，特徵式分解只在 resolvent defined 處直接套用；`L48-05`。
- Kan–Li 的 Memory/Focus 是一種 implementation，不是與 Li admissibility predicate、Kan path constructor 互換的 primitive type。`L48-01` / `SRC-0106` §5。


## v4.9 — 來源真的發生的交互矩陣方向錯置，與跨學科版本語義漂移

**原始實例：** `SRC-0279` PDF p.88 原方程 `dot a_i=a_i[b_i+Σ_j W_ij a_j−φ_i]`，其 `W_G,A=+` 代表 **A→G**，與同篇 pp.47,75 註明的 productive `G→A` 相反。這不是 LLM 錯讀「五相是否漂亮」，而是輸出 state-update Jacobian `∂dot a_i/∂a_j=a_i W_ij` 可核驗的定向錯位。**必做檢查：** 對每個有號邊固定 source、target、矩陣 row/col、動力學 index convention，設單一 regime 微小干預核對受影響的節點；若方向不一致，不要為了保存五相而假裝它只是字詞差異。可修正：轉置 W 或修改求和索引。

同源 `Σ a_i=1` 是設計上可能使用的 normalized intensity，並非所列 multiplicative ODE 的自動 invariant；必須測試 `Σ dot a_i=0`。`K5` 有兩個 complementary undirected cycles 是真定理，但 `K7` 亦能分解成三個 7-cycles；「精巧配對」不能升級成五相的唯一自然必然性。

**其他真的源文重新發現的 drift：** RA-E03 將較早流水線標籤「木發散、火收斂、土構形、金核驗、水反思」與後期 `SRC-0279` 的 **Generation–Activation–Closure–Selection–Retention** 混為無條件同型；後者明定 hybrid regimes 非必定依序執行。這與 v4.8 的 Kan–Li canonical drift 類似，但出於另一期原始來源：不能把概念的相似中文字直接作為模型 transport。將兩者存為**原版工程映射**與**後期候選控制模式**，以來源日期及 typed mappings 串接。

`SRC-0309` 原始 DOCX 有 98 paragraphs 和 **4 個實際 table objects**；只用 `doc.paragraphs` 會**遺漏**先天／後天八卦、四對交互角色的實質內容。作 source-depth review 時必須列出 body paragraph 與 table-cell 讀取數；不能把全文文字擷取稱為 fully read 而漏掉關鍵表格。參見 `SOURCE_IDENTITY_CHECK_v4.9.json`、`L49-01–04/08`。
