# HLS groupoid の Fourier 環の amenability 定数

> **AI-generated independent research note.** This note is not a paper or a peer-reviewed publication and is not a contribution to any person’s research profile or bibliography. The written proof has been checked; no formal verification or claim of publication priority is made.

まず、$D_8$ を**位数8**の二面体群、その中心の非自明元を $z$ として、
$$
F=D_8\times D_8,\qquad
K=\langle(z,z)\rangle\cong C_2
$$
と置きます。以下、
$$
M(H):=\mathrm{AM}(A(H))
$$
は、**点ごとの積を持つ Fourier 環の、通常の Banach amenability 定数**です。ここでは Haar 畳み込み環は扱いません。

$D_8$ の既約表現は、1次元が4個、2次元が1個です。したがって $F$ では、1次元が16個、2次元が8個、4次元が1個になります。対角中心 $K$ で割ると、2次元の8個は降りず、1次元の16個と4次元の1個が残ります。Johnson（1994, Thm 4.1）の有限群公式
$$
M(H)=\frac1{|H|}\sum_{\pi\in\widehat H}(\dim\pi)^3
$$
によって、
$$
M(F)=\frac{16+8\cdot2^3+4^3}{64}=\frac94,
\qquad
M(F/K)=\frac{16+4^3}{32}=\frac52.
$$
この公式は [Choi–Ghandehari（2025年初稿、式(1.1)）](https://arxiv.org/html/2507.05243v1)にも記載されています。

この変化を、HLS groupoid の**最初の有限ファイバーだけ**に埋め込めます。無限遠の群を
$$
G_\infty=\Gamma=F\times\mathbb Z
$$
とし、二つの近似列を
$$
\begin{aligned}
N_1&=\{e\}\times\mathbb Z,
&
N'_1&=K\times\mathbb Z,\\
N_n&=N'_n=\{e\}\times2^{\,n-1}\mathbb Z
&& (n\ge2)
\end{aligned}
$$
で定めます。どちらも有限指数正規部分群の下降列で、共通部分は自明です。それぞれから作る HLS groupoid を $\mathcal G,\mathcal G'$ とすると、ファイバーは次のとおりです。

| ファイバー | $\mathcal G$ | $\mathcal G'$ |
|---|---|---|
| $n=1$ | $F$、定数 $9/4$ | $F/K$、定数 $5/2$ |
| $n\ge2$ | $F\times C_{2^{n-1}}$、定数 $9/4$ | 同じ |
| $\infty$ | $F\times\mathbb Z$、定数 $9/4$ | 同じ |

アーベル群との直積が $M$ を変えないことには、[Choi–Ghandehari（2025年初稿、Prop 3.2）](https://arxiv.org/html/2507.05243v1)を使っています。

以下で示す一般公式により、**環全体の定数も**
$$
\boxed{\mathrm{AM}(A(\mathcal G))=\frac94
\quad\longrightarrow\quad
\mathrm{AM}(A(\mathcal G'))=\frac52}
$$
と変わります。一方、共通の無限遠ファイバー $F\times\mathbb Z$ は amenable なので、両方の環にノルム1以下の近似単位が存在します。これは [DeGaetani–Ghandehari（2026、Cor 5.5）](https://arxiv.org/html/2611.21572v1)によります。

ここで不変なのは、**近似単位を持つという性質と、その一様ノルム上界1**です。異なる二つの環で、個々の近似単位が同じだという意味ではありません。

---

一般の書面結果は、次の等式です。離散群 $\Gamma$ と近似列 $(N_n)$ から作る HLS groupoid
$$
\mathcal G=\bigsqcup_{n\in\mathbb N\cup\{\infty\}}\{n\}\times G_n,
\qquad
G_n=\Gamma/N_n,\quad G_\infty=\Gamma
$$
について、
$$
\boxed{
\mathrm{AM}(A(\mathcal G))
=
\sup_{n\in\mathbb N\cup\{\infty\}}
\mathrm{AM}(A(G_n)).
}
$$
両辺は $+\infty$ を許します。有限ファイバーについて Johnson の公式を代入すれば、
$$
\mathrm{AM}(A(\mathcal G))
=
\max\left\{
M(\Gamma),\
\sup_{n\ge1}\frac1{|G_n|}
\sum_{\pi\in\widehat{G_n}}(\dim\pi)^3
\right\}.
$$

定数の意味を明確にしておきます。$B=A(\mathcal G)$ とし、通常の Banach 射影テンソル積を $B\widehat\otimes_\pi B$、積写像を $\mu$ とします。近似対角とは、
$$
a\cdot m_\alpha-m_\alpha\cdot a\longrightarrow0,
\qquad
\mu(m_\alpha)a\longrightarrow a
\quad(a\in B)
$$
を満たすネットです。$\mathrm{AM}(B)$ は有界近似対角の一様ノルム上界の下限で、存在しなければ $+\infty$ とします。近似単位と違い、テンソル積上の交換子条件も要求しています。

証明の基盤になる既知の構造は、次の三点です。

- 有限ファイバーからの零延長 $\iota_n:A(G_n)\to B$ は等長なイデアル埋め込みである。
- 各制限 $R_n:B\to A(G_n)$ は metric quotient、すなわち商ノルムを正確に与える全射である。
- 任意の $a\in B$ について
$$
  \|a\|=\sup_n\|R_na\|,
  \qquad
  \lim_{n\to\infty}\|R_na\|=\|R_\infty a\|.
$$

それぞれ [DeGaetani–Ghandehari（2026）の Lemma 4.1、Thm 4.2、Prop 5.1・Cor 5.2](https://arxiv.org/html/2611.21572v1)です。特に、
$$
I:=\ker R_\infty
\cong c_0\text{-}\bigoplus_{n\ge1}A(G_n)
$$
が等長に成り立ちます。

ここで、有限直和の議論だけでは何が足りないかが分かります。[Kania–Kąkol（2026、Cor 5.1）](https://onlinelibrary.wiley.com/doi/full/10.1002/mana.70201)の既知の公式から、
$$
\mathrm{AM}(I)=\sup_{n\ge1}\mathrm{AM}(A(G_n))
$$
は得られます。しかし、
$$
\overline{\bigcup_N\bigoplus_{n\le N}A(G_n)}=I
$$
であって、この有限直和の合併は **$B$ 全体には稠密ではありません**。実際、$R_\infty a\ne0$ なら
$$
\operatorname{dist}(a,I)=\|R_\infty a\|>0.
$$
また、個々の元のノルムを保つ持ち上げがあっても、それだけで $B$ を $I\oplus_\infty A(G_\infty)$ という環の直和に分解できるわけではありません。無限遠から来る部分を扱う追加の議論が必要です。

下界は短く済みます。各 $R_n$ は縮小的な全射準同型なので、近似対角を $R_n\widehat\otimes R_n$ で送ると、
$$
\mathrm{AM}(A(G_n))\le \mathrm{AM}(B).
$$
全ファイバーについて上限を取れば下界が出ます。右辺に対応する上限が無限大なら、これで等式が成立します。

上界では
$$
S:=\sup_n\mathrm{AM}(A(G_n))<\infty
$$
と仮定します。有限個のテスト元 $E\subset B$ と小さい $\eta>0$ を固定し、$q=R_\infty$、$C=A(G_\infty)$ と書きます。

まず $C\widehat\otimes_\pi C$ で、ノルムが $S+\eta$ 未満、かつ $q(E)$ に対する二つの近似対角誤差が $\eta$ 未満の元 $m_\infty$ を選びます。射影テンソル積の商性により、
$$
Q=q\widehat\otimes q:
B\widehat\otimes_\pi B\longrightarrow
C\widehat\otimes_\pi C
$$
も metric quotient です。したがって、
$$
Qw=m_\infty,\qquad \|w\|_\pi<S+2\eta
$$
となる持ち上げ $w$ を取れます。

交換子については、一段の補正が重要です。$a\in E$ に対して
$$
c_a=a\cdot w-w\cdot a
$$
と置くと、分かっているのは $\|Qc_a\|_\pi<\eta$ であり、$Qc_a=0$ ではありません。そこで、
$$
Qv_a=Qc_a,\qquad \|v_a\|_\pi<2\eta
$$
という小さい持ち上げを選びます。すると初めて、
$$
c_a-v_a\in\ker Q
=
\overline{I\otimes B+B\otimes I}
$$
となります。

次に、最初の $N$ 個のファイバーを消す縮小射影
$$
P_Na=a-\sum_{n\le N}\iota_n(R_na)
$$
を使います。$i\in I$ なら $\|P_Ni\|\to0$ なので、
$$
(P_N\widehat\otimes P_N)k\longrightarrow0
\quad
\left(k\in\overline{I\otimes B+B\otimes I}\right).
$$
**両因子を tail に切る**ことで、核に属する誤差を小さくできるわけです。よって
$$
t_N=(P_N\widehat\otimes P_N)w
$$
は、十分大きい $N$ で
$$
\|a\cdot t_N-t_N\cdot a\|_\pi<3\eta
\quad(a\in E)
$$
を満たします。

積の誤差には、ファイバーノルムの連続性を使います。
$$
r_a=\mu(w)a-a
$$
と置けば $\|qr_a\|<\eta$ ですから、十分大きい $N$ で
$$
\|P_Nr_a\|<2\eta.
$$
一方、$P_N$ の定義から
$$
\mu(t_N)a-P_Na=P_Nr_a.
$$
したがって、tail 上では積の条件も満たせます。テスト元は有限個なので、同じ $N$ を全てに選べます。

残る最初の $N$ 個には、それぞれの有限次元環の正確な対角
$$
d_n=\sum_{g\in G_n}\delta_g\otimes\delta_g,
\qquad
\|d_n\|_\pi=\mathrm{AM}(A(G_n))\le S
$$
を置きます。ここで単純な三角不等式を使うと、ノルムのコストが和になってしまいます。最大値を保つのが、**Rademacher 符号による平均**です。

具体的には、有限直和 $D=\bigoplus_{j=0}^N{}_\infty D_j$ と各ブロックのテンソル $u_j$ に対し、
$$
\left\|\sum_j(J_j\widehat\otimes J_j)u_j\right\|_\pi
=\max_j\|u_j\|_\pi
$$
が成り立ちます。上界を見るには、共通の $L>\max_j\|u_j\|_\pi$ を取り、各 $u_j/L$ を単位球内の基本テンソルの平均として表します。ブロック間で独立な符号 $\varepsilon_j\in\{-1,1\}$ を選び、**両因子には同じ $\varepsilon_j$** を掛けると、
$$
\mathbb E\!\left[
\left(\sum_j\varepsilon_jJ_jx_j\right)
\otimes
\left(\sum_j\varepsilon_jJ_jy_j\right)
\right]
=
\sum_j(J_j\otimes J_j)\mathbb E(x_j\otimes y_j).
$$
異なるブロックの項は消え、同じブロックの項は残ります。両因子のノルムは $\ell^\infty$ ノルムなので1以下です。$L$ を下げれば上界が得られ、逆向きは座標射影から従います。

これを
$$
B\cong
\left(\bigoplus_{n\le N}{}_\infty A(G_n)\right)
\oplus_\infty P_NB
$$
に適用します。tail のブロックには今作った $t_N$ を使い、
$$
D_{E,\eta}
=t_N+\sum_{n\le N}(\iota_n\widehat\otimes\iota_n)d_n
$$
と置けば、
$$
\|D_{E,\eta}\|_\pi<S+2\eta.
$$
有限ブロックでの誤差はゼロで、tail での交換子誤差と積の誤差はそれぞれ $3\eta,2\eta$ 未満です。有限集合 $E$ を増やし、$\eta$ を小さくすることで、任意の $\varepsilon>0$ に対して上界 $S+\varepsilon$ の近似対角が得られます。従って $\mathrm{AM}(B)\le S$ となり、等式が証明されます。

---

最初の構成は、先の固定核の結果もそのまま運びます。一般の有限群 $F$ と中心部分群 $K$ について
$$
\alpha=M(F),\qquad \beta=M(F/K)
$$
とすると、上記の二つの HLS groupoid では
$$
\mathrm{AM}(A(\mathcal G))=\alpha,
\qquad
\mathrm{AM}(A(\mathcal G'))=\max\{\alpha,\beta\}.
$$
したがって増大倍率は、正確には
$$
\max\{1,\beta/\alpha\}
$$
です。商側の定数が下がる場合でも、共通の他のファイバーが $\alpha$ を保つため、全体の定数は下がりません。

[中心核についてのノート](central-quotient-amenability.md)で扱ったのは、**任意に固定した非自明な有限アーベル群 $K$** に対し、中心核が $K$ と同型の有限群の系列で
$$
\frac{M(F/K)}{M(F)}\longrightarrow |K|
$$
とできる、という結果でした。この系列に上の構成を適用すると、HLS Fourier 環でも増大倍率が $|K|$ に迫ります。$K=C_2$ の系列では、
$$
\frac{\mathrm{AM}(A(\mathcal G'_r))}
     {\mathrm{AM}(A(\mathcal G_r))}
=
\frac{2}{1+(4/5)^r}\longrightarrow2.
$$

ここで同一なのは、**各比較対の内部での無限遠ファイバーと $n\ge2$ のファイバー**です。上限に近づく系列全体では $F$ が変わります。各対の両側には、引き続きノルム1以下の近似単位があります。

さらに明快な極端例として、群の直和
$$
\Gamma=\bigoplus_{j\ge1}D_8,
\qquad
N_n=\bigoplus_{j>n}D_8
$$
を取れます。すると $G_n\cong D_8^n$ なので、
$$
M(G_n)=\left(\frac32\right)^n\longrightarrow\infty.
$$
従って対応する HLS Fourier 環では
$$
\boxed{\mathrm{AM}(A(\mathcal G))=\infty.}
$$
一方、$\Gamma$ は局所有限群なので amenable であり、Cor 5.5 により $A(\mathcal G)$ には contractive approximate identity が存在します。**近似単位の上界1と、近似対角に有限の一様上界があることは、これほど異なる条件です。**

文献上の位置づけとして、制限写像・ノルム連続性・近似単位の特徴づけは DeGaetani–Ghandehari（2026）、$c_0$ 直和の公式は Kania–Kąkol（2026、指定 DOI は共著論文）、アーベル直積による定数の不変性は Choi–Ghandehari（2025年初稿）の既知の結果です。全 HLS Fourier 環の上限公式と、一つの有限ファイバーの変更への適用は、それらに上記の持ち上げ・tail 切断・符号平均を組み合わせた今回の帰結として位置づけます。**この帰結の文献上の優先性は未確定です。**
