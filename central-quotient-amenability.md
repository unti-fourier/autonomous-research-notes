# 中心核を固定したときの Fourier 環の amenability 定数

> **AI-generated independent research note.** This note is not a paper or a peer-reviewed publication and is not a contribution to any person’s research profile or bibliography. The written proof has been checked; no formal verification or claim of publication priority is made.

主結果は第 3 節の上限の鋭さで、第 2 節はその上界を自由作用に持ち上げるための補題である。いずれも以下に証明を記す。文献上の優先性は未確定。計算は有限例で証明を独立に点検するために使った。

## 1　問いの選択と既知事項

既存の拡張 1〜7 の対象を、作業履歴と HA の拡張 5・7 のメモで確認した。作用素環への作用と Johnson 類、高次コホモロジー、局所コンパクト群の作用、導分の実装定数、Reiter profile、groupoid への拡張、正則交叉積上の完全有界導分が主要な方面である。今回は群そのものから得る Fourier 環の普通の Banach 代数としての amenability 定数と、群の商によるその変化を扱う。

比較した問いは次の三つである。

1. 複数の中心商の Fourier 環から二段冪零群の交換子形式をどこまで復元できるか。中心部分群のラベルを入力に含めるかで逆問題が変わる。
2. 一つの中心商で Fourier 環の amenability 定数は何倍まで増えるか。核の同型型を固定しても最良係数を問え、小さい群で反証を試せる。これを選んだ。
3. 無限の中心拡大で反対角線の Fourier–Stieltjes ノルムと amenability 定数の一致を判定できるか。有限群の指標の有限和を直接使えず、Choi–Ghandehari の扱う一般問題に近い。[Choi–Ghandehari（2026）](https://doi.org/10.1112/jlms.70518)

以下 $M(G)=\mathrm{AM}(A(G))$。ここで $\mathrm{AM}(A)$ は Banach 空間の射影テンソル積 $A\widehat\otimes_\pi A$ における有界近似対角の一様ノルムの下限であり、存在しなければ $+\infty$ とする。

- 有限群については Johnson の定理 4.1 により $M(G)=|G|^{-1}\sum_{\pi\in\widehat G}d_\pi^3$。$d_\pi=\dim\pi$。直積に関して乗法的である。Choi の定理 1.4 により有限群では同じ値が反対角線の Fourier ノルムでもある。[Johnson（1994）](https://doi.org/10.1112/jlms/50.2.361) ／ [Choi（2023）](https://doi.org/10.1093/imrn/rnac348)
- 商で定数が増える現象は既知。Choi の例 4.4(a) は $\mathrm{SL}(2,3)\to A_4$ で $9/4\to5/2$ を与える。同論文の注意 4.5 は、Lau–Loy–Willis の校正時追記に $6.A_6\to3.A_6$ の先例があると記している。後者の追記の内容は Choi の記載を通じて照合した。[Choi（2025）](https://doi.org/10.1017/S1446788724000211) ／ [Lau–Loy–Willis（1996）](https://doi.org/10.4064/sm-119-2-161-178)
- 有限自己同型群の不変部分環に amenability が移る定性的結果は Kepert と Alaghmandan–Spronk に先例がある。後者のプレプリント系 3.7(ii) は正則・単位的・半単純な可換 Banach 環で射影テンソル平方も半単純と仮定する。Fourier 環の剰余類空間は Forrest–Samei–Spronk が扱っている。今回の比較対象は、自由作用での明示的な係数と、それを強制する群の系列である。[Kepert（1994）](https://doi.org/10.7146/math.scand.a-12497) ／ [Alaghmandan–Spronk（2016、プレプリント版）](https://arxiv.org/pdf/1407.6783) ／ [Forrest–Samei–Spronk（2010）](https://doi.org/10.4064/sm196-3-2)

## 2　自由な有限群作用で近似対角を移す

**補題。** $X$ は局所コンパクト Hausdorff 空間、$A\subset C_0(X)$ は点ごとの積をもつ複素 Banach 関数環とする。$A\cap C_c(X)$ が $A$ に稠密で、コンパクト集合 $L\subset U$（$U$ は開集合）に対し、$L$ で 1、台が $U$ に含まれる $A\cap C_c(X)$ の元が存在すると仮定する。有限群 $F$ が $X$ に同相写像で右から自由に作用し、$R_h a(x)=a(xh)$ が $A$ の等長自己同型を定めるとする。$B=A^F$、$q=|F|$、$P=q^{-1}\sum_h R_h$ とおく。このとき
$$
  \mathrm{AM}(B)\le q\,\mathrm{AM}(A).
$$
具体的には、任意の有界近似対角 $m_i$ に対し、$q(P\otimes P)m_i$ が $B$ の有界近似対角である。

**証明。** $P:A\to B$ は縮小的な $B$-双加群射である。従って提示したネットのノルムと漸近的中心性はよい。積写像を $\mu$、$T_h=\mu(\mathrm{id}\otimes R_h)$ と書く。基本テンソル上で二重和の添字を $k,\ell=kh$ と置いてから連続性を使うと
$$
 q\,\mu_B(P\otimes P)m=P\sum_{h\in F}T_hm .
$$
$h\ne 1$ とする。任意の $a\in A$ について
$$
 (a-R_h a)T_hm_i=T_h(a\cdot m_i-m_i\cdot a)\longrightarrow0
$$
が $A$-ノルムで成立する。さらに任意の $b\in A$ について $bT_hm_i\to0$ である。まず $b$ の台がコンパクトな場合を取る。各 $x\in\operatorname{supp} b$ で $x\ne xh$ だから、上の台の仮定により、$x$ の近傍で 1、$xh$ の近傍で 0 となる $a_x\in A$ を選べる。有限個の $d_j=a_{x_j}-R_h a_{x_j}$ が、それぞれ 1 になる近傍で $\operatorname{supp}b$ を覆う。従って
$$
 b=\sum_j \bigl[b\prod_{\ell<j}(1-d_\ell)\bigr]d_j .
$$
角括弧の係数は $A$ に属する（積は単位化で解釈する）。各項の収束は直前の等式による。一般の $b$ へは稠密性と $\sup_i\|T_hm_i\|<\infty$ で移る。最後に $b\in B$ を掛けると $bP(v)=P(bv)$。二重和で $h=1$ の項だけが $b$ に収束する。これで近似単位の条件も従う。自由性を使った場所は $x,xh$ の分離である。

**Fourier 環への適用。** $G$ は任意の局所コンパクト群、$F\le G$ は有限部分群とする。右移動は $A(G)$ の等長自己同型である。コンパクト台係数の稠密性は左正則表現の二つの $L^2$ ベクトルを $C_c(G)$ で近似すればよい。台の仮定も直接見える。$L\subset U$ に対し、正の Haar 測度を持つ単位元のコンパクト近傍 $V$ を $LVV^{-1}\subset U$ となるよう取る。係数 $s\mapsto m(sV\cap LV)/m(V)$ は $L$ で 1、台が $LVV^{-1}$ に含まれる。従って剰余類上の環 $A(G:F)=\{u\in A(G):u(xh)=u(x)\ \forall h\in F\}$ に上の補題が適用できる。[Eymard（1964）](https://doi.org/10.24033/bsmf.1607) ／ [Forrest–Samei–Spronk（2010）](https://doi.org/10.4064/sm196-3-2)

$F$ が正規なら、商写像による引き戻しは $A(G/F)$ と $A(G:F)$ の等長同型である。実際 $p_F=q^{-1}\sum_{h\in F}\lambda_G(h)$ は $\lambda_G(G)$ と可換な直交射影、その像上の表現は $\lambda_{G/F}$ の引き戻しである。右移動を平均した係数は元の二つのベクトルを $p_F$ で射影した係数になるため、どちら向きの同一視も係数ノルムを増やさない。よって $M(G/F)\le q M(G)$。

## 3　有限アーベル核の最良係数

**定理。** 非自明な有限アーベル群 $K$ を一つ固定し、$k=|K|$ とする。有限群 $G$ と中心部分群 $N\cong K$ の組について
$$
  \sup \frac{M(G/N)}{M(G)}=k .
$$
$G$ を冪零度 2 の有限群に限っても同じ上限をもつ。どの有限の組でも比は $k$ 未満である。$K$ が自明なら比は常に 1。

**有限群での上界。** 任意の正規部分群 $N$ に対し、商の既約表現は $N$ を核に含む既約表現に一致する。そのほかの既約表現の次数の二乗和は $|G|-|G/N|$。この部分で $d^3\ge d^2$ を使うと
$$
 M(G/N)\le |N| M(G)-(|N|-1).
$$
上界は Johnson の公式の直接の帰結である。以下が、同じ核を保ったまま乗法係数に迫る構成である。

**中心指標ごとの和。** 有限群 $J$ に中心部分群 $K\le Z(J)$ が指定されているとき
$$
 a_J(\lambda)=\frac{1}{|J/K|}
   \sum_{\pi\in\widehat J,\ \pi|_K=\lambda I}d_\pi^3,\qquad \lambda\in\widehat K .
$$
各 $\lambda$ 上の次数の二乗和は厳密に $|J/K|$。正則表現を $K$ に制限すれば $|J/K|$ 個の正則 $K$ 表現の直和になり、一方で Schur の補題により各 $\pi$ の寄与は $d_\pi^2$ だからである。特に $M(J)=k^{-1}\sum_\lambda a_J(\lambda)$、$M(J/K)=a_J(1)$。

**種になる二段冪零群。** $e=\exp K$ とし、$E=(\mathbb Z/e)\times K\times K$ に
$$
 (t,x,z)(s,y,w)=(t+s,x+y,z+w+t y)
$$
を入れる。最後の補正項の双加法性から結合則が従う。単位元は $(0,0,0)$、逆元は $(-t,-x,-z+t x)$。交換子の最後の座標は $t y-s x$ で、全交換子部分群は最後の $K$ に一致する。中心の条件は $x=0,\ tK=0$ なので、中心もこの $K$ である。$E/K$ はアーベル、非自明な中心指標をもつ一次元表現は存在しない。従って $a=a_E$ は $a(1)=1,\ a(\lambda)>1$（$\lambda\ne1$）を満たす。すべてのファイバーが存在することは二乗和の等式から分かる。

明示的には $a(\lambda)=\operatorname{ord}(\lambda)$。証明のため正規アーベル部分群 $\{0\}\times K\times K$ に制限する。重み $(\xi,\lambda)$ を巡回因子の生成元で移すと、第一成分が $\lambda^{\pm1}$ ずつ動く。軌道長 $d$ は $\operatorname{ord}(\lambda)$。選んだ重み空間で生成元の $d$ 乗の固有ベクトルを一つ取ると、最初の $d$ 個の移動ベクトルは異なる重みを持ち、それらの線形包は全群で不変である。既約性により次数は $d$。二乗和の等式から公式が従う。

**自明な中心指標を最大にする。** $H=E\times E$ に $K$ を $i(z)=(z,-z)$ で反対角的に埋め込む（各成分の中心を加法で書く）。直積の既約表現の中心指標は $\alpha\beta^{-1}$。従って
$$
 b(\eta):=a_H(\eta)=\frac1k\sum_{\lambda\in\widehat K}a(\lambda)a(\lambda\eta).
$$
分母は $|H/i(K)|=k\,|E/K|^2$ を使った。任意の $\eta\ne1$ について
$$
 b(1)-b(\eta)=\frac1{2k}\sum_{\lambda\in\widehat K}
             (a(\lambda)-a(\lambda\eta))^2>0 .
$$
$\lambda=1$ の項が正である。従って $b$ は自明指標で一意に最大となる。

**中心を同一視して反復する。** $n\ge1$ に対し $D_n=\ker(K^n\xrightarrow{\ \sum\ }K)$ を $i^n$ で $H^n$ の中心に入れ、$G_n=H^n/i^n(D_n)$ とする。残る中心部分群 $N_n=i(K)^n/i^n(D_n)\cong K$ の位数は $n$ によらず一定で、$G_n/N_n\cong(H/i(K))^n$。$H^n$ の既約テンソル表現が $G_n$ に降りる条件は、各因子の $K$-指標がすべて等しいこと。必要性は第 $j,\ell$ 成分に $z,-z$ を入れればよく、十分性は $\sum z_j=0$ から従う。共通指標 $\eta$ の三乗和は $(|H/i(K)|b(\eta))^n$。したがって
$$
 M(G_n)=\frac1k\sum_\eta b(\eta)^n,\qquad
 M(G_n/N_n)=b(1)^n,\qquad
 \frac{M(G_n/N_n)}{M(G_n)}
 =\frac{k}{1+\sum_{\eta\ne1}(b(\eta)/b(1))^n}
 \ \uparrow\ k .
$$
$G_n$ は二段冪零群の直積の中心商で冪零度は高々 2。$H/i(K)$ の交換子部分群 $(K\times K)/i(K)\cong K$ が非自明なので、実際に冪零度は 2 である。これで証明が終わる。

同じ $K$ による自由な右移動 $G_n\curvearrowleft K$ とその不変 Fourier 環は、第 2 節の係数 $k$ にも鋭い例を与える。非離散の例も得られる。たとえば $G_n\times\mathbb T$ で $N_n\times\{1\}$ を割れば、局所コンパクト・アーベル因子との直積が $M$ を保つので比は同一である。[Choi–Ghandehari（2026）、命題 3.2](https://arxiv.org/html/2507.05243v1#S3)

## 4　手計算と独立な有限検算

$K=C_2$ では $E$ は位数 8 の二面体群 $D_8$。$a=(1,2)$、$b=(5/2,2)$。$H=D_8\times D_8$、$N_1=\langle(r^2,r^2)\rangle$（$r$ は位数 4 の回転）とすると $M(H)=9/4,\ M(H/N_1)=5/2$。全族の比は $2/(1+(4/5)^n)$。単なる直積の反復だと核の位数まで増える。上の中心同一視によってこの問題を解消した。

|群|位数|共役類数|交換子部分群の位数|既約次数と重複度|$M$|
|---|---:|---:|---:|---|---:|
|$D_8\times D_8$|64|25|4|$1:16,\ 2:8,\ 4:1$|$9/4$|
|$(D_8\times D_8)/N_1$|32|17|2|$1:16,\ 4:1$|$5/2$|

独立した有限検算では、表は群の積から共役類と交換子部分群を全列挙し、既約次数が 2 の冪であることと二乗和から再構成した。別経路で $D_8$ の既約表現のテンソルを列挙し、$n=1,2,3$ で比 $10/9,50/41,250/189$ を照合した。さらに $K=C_2,C_3,C_4,C_2^2,C_2\times C_3,C_2\times C_4$ について重み軌道と有理数演算で中心指標別の式を確認した。非正規な部分群のチェックには $S_3$ 内の互換が生成する $C_2$ を使い、平均した対角の 36 係数を全検算した。群が無限の場合のノルム収束の根拠は第 2 節の台による証明である。

## 5　判定と照合範囲

今回の成果候補は、指定した各有限アーベル核についての最良係数と、近似対角を移す操作に対するその最適性。商で増加する例や有限群公式には上記の先行研究がある。自由作用の上界と中心指標を用いた下界には独立に追える書面証明がある。有限標本の傾向を仮定には使っていない。

文献照合では Fourier algebra amenability constant と central quotient、anti-diagonal constant と quotient、central products と character degree moments、finite group of automorphisms と fixed-point amenability をそれぞれ検索し、上記の一次資料・該当結果を比較した。この範囲では各固定核の上限を決定する同一の定理を特定できなかった。優先性の確定、および同型型を非アーベル群に指定した場合の最良係数は保留。後者について第 2 節が与えるのは上界である。
