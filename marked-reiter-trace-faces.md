# どの測度で同じ近似平均を試すか

> **AI-generated independent research note.** This note is not a paper or a peer-reviewed publication and is not a contribution to any person’s research profile or bibliography. The written proof has been checked; no formal verification or claim of publication priority is made.

**結論。** 作用する空間 $X$ に加えて、その上で誤差を測る確率測度の族 $\mathcal M$ を入力に残す。離散群の Reiter 平均をこの族で一様に試す条件は、可換 $C^*$ 環では指定されたトレースに関する近似条件と一致する。測度族の閉凸包 $K$ が不変な閉じた面なら、$K$ 自身への作用からすべての有限集合での最小誤差を復元できる。一般の不変閉凸集合では、同じコンパクト凸 $\Gamma$-空間を同じ $\operatorname{Prob}(X)$ にアフィン同変に埋め込んでも、埋め込みによって従順性の判定が逆転する。非可換側では、トレースを商から引き戻す場合に同じ移送ができる。

群の比較対象は Day (1961) の固定点定理と Reiter (1965) の近似不変性である。コンパクトな群作用では Monod (2011, Theorem 2, Corollary 3) が位相的従順性を、型 M の $(\Gamma,X)$-加群 $V$ に対する $H_b^n(\Gamma,V^*)=0$（全 $n\ge1$）、型 C の双対加群の相対単射性、正規化された不変平均と結び付けている。これらは指定した任意の測度族についての主張ではない。[Day (1961)](https://doi.org/10.1215/ijm/1255631582) ／ [Reiter (1965)](https://doi.org/10.1016/S1385-7258(65)50072-X) ／ [Monod (2011)](https://doi.org/10.1093/imrn/rnq238)

## 1　指定した測度族と誤差

$\Gamma$ は可算離散群、$X$ は空でないコンパクト距離化可能空間で、$\Gamma$ は同相写像で作用する。$\mathcal M\ne\varnothing$ は $X$ 上の Borel 確率測度の任意の族。$\operatorname{Prob}(X)$ の位相は $C(X)$ による弱 $^*$ 位相とする。$K_X=\overline{\operatorname{co}}^{w^*}\mathcal M$ とおく。ここでは $\mathcal M$ の不変性や各測度の準不変性を仮定しない。

係数は左移動 $s_*p(h)=p(s^{-1}h)$ をもつ $\ell^1(\Gamma)$。証人 $m\in\mathcal C_X$ はノルム連続な確率ベクトル場 $X\to\ell^1(\Gamma)_+$ であり、ある有限集合 $L\subset\Gamma$ が全 $m(x)$ の台を含む。各証人が別の $L$ を使ってよい。これは凸集合である。通常の連続な確率場も、像のコンパクト性から尾部を一様に切り、質量を単位元に戻してこの形で一様近似できる。

有限集合 $E\subset\Gamma$ ごとに
$$
 e_s(m,x)=\|s_*m(x)-m(sx)\|_1,\qquad D_E(m,x)=\sum_{s\in E}e_s(m,x),
$$
$$
 d_E(X,\mathcal M)=\inf_{m\in\mathcal C_X}\ \sup_{\mu\in\mathcal M}\int_X D_E(m,x)\,d\mu(x).
$$
すべての有限 $E$ で $d_E=0$ であることを考える。可算性により一つの証人列で全 $s$ を扱える。一つの測度ごとに別の列を使う条件とは量化の順序が違う。コンパクト $\Gamma$-空間 $Z$ の通常の一様誤差を $u_E(Z)=\inf_{m\in\mathcal C_Z}\sup_{z\in Z}D_E(m,z)$ と書く。従って $u_E(X)=d_E(X,\operatorname{Prob}(X))$。

## 2　測度一つへの還元

$b_E(\mu)$ を、Borel 確率場 $a:X\to\operatorname{Prob}(\Gamma)$ 全体での $\int D_E(a,x)\,d\mu(x)$ の下限とする。この定義は $\mu$ が準不変でなくても使えるよう、全点で定義された Borel 場を取る。

**補題。** 各有限 $E$ について
$$
 d_E(X,\mathcal M)=\max_{\mu\in K_X} b_E(\mu). \tag{1}
$$
特に共通の近似に正の障害があれば、閉凸包の一つの測度がその大きさを実現する。実現する測度は $E$ に依存してよい。

**証明。** $m\in\mathcal C_X$ を固定すると $D_E(m,\cdot)$ は連続で有界、積分は $\mu$ について連続アフィンである。従って上限の範囲を $K_X$ に拡大できる。一様ノルムを入れた場の空間では積分は $m$ について凸で $2|E|$-Lipschitz。$K_X$ はコンパクト凸、$\mathcal C_X$ は凸なので Sion のミニマックス定理で順序を交換できる。内側の連続場に関する下限は連続関数の下限として上半連続であり、最大値を持つ。[Sion (1958), pp. 173–174](https://msp.org/pjm/1958/8-1/pjm-v8-n1-p14-s.pdf)

固定した $\mu$ では $\lambda=(\mu+\sum_{s\in E}s_*\mu)/(1+|E|)$ とおく。Borel 場の有限集合外の質量を単位元へ戻せば $L^1(\lambda;\ell^1)$ で近似できる。続いて Lusin の定理で補集合の $\lambda$-測度が小さいコンパクト集合上に連続性を得る。有限個の座標を Tietze の定理で延長し、有限次元の確率単体への最近点射影を施せば、全体で連続な同じ有限単体値の場を得る。誤差積分の差は各 $s$ について $\int\|a-m\|_1\,d(\mu+s_*\mu)$ 以下。従って Borel 場に広げても下限は同じである。□

**準不変な測度類との対応。** 正の重み $w_g$ の総和を 1 として $\rho_\mu=\sum_gw_g\,g_*\mu$ とおく。正値性により $\rho_\mu$ の零集合は全 $g_*\mu$ の共通の零集合で、準不変かつ重みの選び方によらない測度類を与える。ここで
$$
 e_s(m,gx)\le e_g(m,x)+e_{sg}(m,x)
$$
である。これは $s_*m(gx)$ と $m(sgx)$ の間に $(sg)_*m(x)$ を挿入すればよい。従って、$\mu$ について全 $s$ の積分誤差が零に向かう列は、各 $g_*\mu$ でも同じ性質を持ち、$e_s\le2$ より $\rho_\mu$ でも持つ。逆は $\mu\le w_e^{-1}\rho_\mu$ から従う。(1) より、一様条件は **$K_X$ の各 $\mu$ について $(X,\rho_\mu)$ が測度論的 Reiter 条件を満たすこと** と同値である。個々の有限 $E$ での数値を、測度の変更後の数値と同一視する必要はない。

作用 groupoid $\Gamma\ltimes X$ では、矢 $x\mapsto sx$ に沿う $\ell^1$ 差が上の $e_s$ である。準不変確率測度一つなら、これは測度付き作用の従順性の標準的な Reiter 表現である。可算群では有界な非負誤差の $L^1$ 収束から部分列を取って全 $s$ でほとんど至る所の収束にでき、逆は優収束で従う。全測度での従順性と位相的従順性の同値は既知で、離散変換 groupoidを超えた定理もある。Kranz (2026, プレプリント, Theorem A) の範囲は単位空間が Hausdorff で連続 Haar 系をもつ $\sigma$-コンパクト局所コンパクト groupoidである。[Adams・Elliott・Giordano (1994)](https://doi.org/10.1090/S0002-9947-1994-1250814-5) ／ [Anantharaman-Delaroche・Renault (2000)](https://www.unige.ch/math/FondationEnsMath/en/la-revue/monographies/monographie-no-36) ／ [Kranz (2026), §1・§2](https://arxiv.org/html/2611.10010v1)

## 3　移送と、測度の埋め込みを忘れる操作

同じ群の作用 $(X,\mathcal M_X),(Y,\mathcal M_Y)$ の間で、射として弱 $^*$ 連続な確率核 $P:X\to\operatorname{Prob}(Y)$ を取る。条件は $P_{sx}=s_*P_x$ と、各 $\mu\in\mathcal M_X$ の像 $P_*\mu=\int P_x\,d\mu(x)$ が $K_Y$ に入ること。後者は像を $K_X$ 全体で要求することと同値で、核の合成とも両立する。連続同変写像は Dirac 測度を取って得られる特別な射である。

**移送補題。** 各有限 $E$ で
$$
 d_E(X,\mathcal M_X)\le d_E(Y,\mathcal M_Y). \tag{2}
$$
実際、$Y$ の証人 $m$ を $n(x)=\int m(y)\,dP_x(y)$ として引き戻す。$n$ は $m$ と同じ有限単体に値をとる連続な確率場。核の同変性とノルムの凸性から $D_E(n,x)\le\int D_E(m,y)\,dP_x(y)$。再び積分すれば (2) を得る。□

**面に関する命題。** $K\subset\operatorname{Prob}(X)$ が空でない不変弱 $^*$ コンパクト凸集合であるとき
$$
 u_E(K)\le d_E(X,K).
$$
$K$ が $\operatorname{Prob}(X)$ の面なら、すべての有限 $E$ について等号が成り立つ。面とは、$0<a<1$ で $a\mu+(1-a)\nu\in K$ なら $\mu,\nu\in K$ となる凸集合のことである。

**証明。** $K$ の点 $\mu$ を $X$ 上の確率測度 $\mu$ へ送る核に (2) を適用する。$K$ 上の確率測度の重心は $K$ に属する。面の場合は $Y=\{x:\delta_x\in K\}$ が閉不変集合で $K=\operatorname{Prob}(Y)$ となる。証明するには $\mu\in K$ の台の $y$ に対して、縮んでいく球への $\mu$ の正規化制限を取る。面の性質によりこれらは $K$ にあり、弱 $^*$ 極限は $\delta_y$。逆の包含は有限凸結合の稠密性による。有限単体値の場は $Y$ から $X$ に延長できる（§2 の座標延長と射影）。$Y$ の不変性により $d_E(X,K)=u_E(Y)$。Dirac 埋め込み $Y\to K$ への制限から $u_E(Y)\le u_E(K)$ も従う。□

## 4　作用素環で同じ測度を用いると何を測っているか

単位的 $C^*$ 環 $A$ に $\Gamma$ が $\alpha$ で作用し、不変な空でないコンパクト凸集合 $K\subset T(A)$ を指定する。Gardella・Geffen・Kranz・Naryshkin・Vaccaro (2024, Definition 2.2) の一様トレース半ノルムの上限を $K$ に制限する。具体的には、有限列 $\xi\in C_c(\Gamma,A)$ の内積を $\langle\xi,\eta\rangle=\sum_h\xi(h)^*\eta(h)$、半ノルムを $\|\xi\|_{2,K}=\sup_{\tau\in K}\tau(\langle\xi,\xi\rangle)^{1/2}$、$A$ 上では $\|a\|_{2,K}=\sup_{\tau\in K}\tau(a^*a)^{1/2}$ とする。$\widetilde\alpha_s\xi(h)=\alpha_s(\xi(s^{-1}h))$ とおく。有限個の $a\in A,\ s\in\Gamma$ と任意の許容誤差に対し、$\|\langle\xi,\xi\rangle\|\le1$ のもとで
$$
 \|\xi a-a\xi\|_{2,K},\qquad
 \|1-\langle\xi,\xi\rangle\|_{2,K},\qquad
 \|\widetilde\alpha_s\xi-\xi\|_{2,K}
$$
を同時に許容誤差未満にできることを考える。原論文の Theorem 2.5, (1) $\Leftrightarrow$ (6) は、単位的可分 $A$、$T(A)\ne\varnothing$ に対し、**全**トレースでのこの条件と $T(A)$ 上の位相的従順性が同値だと示している。[Gardella・Geffen・Kranz・Naryshkin・Vaccaro (2024), §2](https://link.springer.com/article/10.1007/s00208-024-02833-9)

**可換の場合。** $A=C(X)$、$K\subset T(C(X))=\operatorname{Prob}(X)$ とする。上の制限した条件は、全 $E$ で $d_E(X,K)=0$ であることと同値である。確率場 $m$ から座標ごとの $\xi=\sqrt m$ を取ると
$$
 \|\sqrt p-\sqrt q\|_2^2\le\|p-q\|_1
$$
より従う。各点で長さは 1、可換性により交換子は零である。逆に $\xi$ に対し $r(x)=1-\|\xi(x)\|_2^2\ge0$ とおき、$m(x)=|\xi(x)|^2+r(x)\delta_e$ とする。$m$ は正規化された連続有限台の確率場で、
$$
 e_s(m,x)\le 2\|s_*\xi(x)-\xi(sx)\|_2+r(x)+r(sx).
$$
これは $\||v|^2-|w|^2\|_1\le(\|v\|_2+\|w\|_2)\|v-w\|_2$ による。$\mu\in K$ で積分し Cauchy–Schwarz を使う。$s_*\mu\in K$ なので $r(sx)$ を同じ半ノルムで抑えられ、同様に $x$ と $sx$ の変数変換で上の場の差は $\widetilde\alpha_s$ の半ノルムに一致する（$K$ 上の上限を取った後）。これで逆向きも従う。□

**一般のトレース集合で成り立つ向き。** $A$ が非可換でも、制限した近似条件から $K$ 上の位相的従順性が従う。列 $\xi$ に対し、各 $\tau\in K$ で $v_\xi(\tau)(h)=\tau(\xi(h)^*\xi(h))$ とし、不足質量 $1-\|v_\xi(\tau)\|_1$ を単位元へ置いた確率を $p_\xi(\tau)$ とする。これは連続な共通有限台の場である。$s\tau=\tau\circ\alpha_{s^{-1}}$ に対して $v_{\widetilde\alpha_s\xi}(s\tau)=s_*v_\xi(\tau)$。各座標の GNS ベクトルにノルム平方の差の評価を使い、和に Cauchy–Schwarz を施すと、ノルム 1 以下の列について $\|v_\xi(\tau)-v_\eta(\tau)\|_1\le 2\|\xi-\eta\|_{2,\tau}$ となる。不足質量は $\|1-\langle\xi,\xi\rangle\|_{2,K}$ 以下。従って $e_s(p_\xi,\tau)\le2\|\widetilde\alpha_s\xi-\xi\|_{2,K}+2\|1-\langle\xi,\xi\rangle\|_{2,K}$。この向きには面の仮定を使わない。□

**一般の商での移送。** $q:A\twoheadrightarrow B$ は同変な単位的全射、$T(B)\ne\varnothing$、$K=q^*T(B)$ とする。このとき $A$ で $K$ に制限した条件は **$B$ の通常のトレース従順性と同値**。$K$ は $\ker q$ 上で消えるトレース全体であり、正元で試せば閉じた不変面である。$A$ が可分なら前記 Theorem 2.5 により $K$ 上の作用の位相的従順性とも同値になる。

**証明。** $q$ は列の内積、交換子、群作用を保ち、上の三つの半ノルムの値を商の値に正確に移す。商の有限個のテスト元は $A$ に持ち上がる。逆向きで注意を要するのは列の通常ノルムの上界である。商の有限台の証人 $\eta$ を座標ごとに $z_h$ に持ち上げ、台の外を零とする。$H=\sum_hz_h^*z_h$、$f(t)=1/\sqrt{\max(1,t)}$ と置き、$\xi(h)=z_hf(H)$ とする。$q(H)=\langle\eta,\eta\rangle\le1$ より $q(f(H))=1$。また $f(H)Hf(H)\le1$ なので、$\xi$ はノルム 1 以下の正確な列の持ち上げである。各誤差は $K$ に関しては商の誤差そのものとなる。□

可換の場合は各閉面が $C(X)\to C(Y)$ という商に対応する。一般の $C^*$ 環で同じ形の商から得られる面に限ったことが、非可換の命題の仮定である。

## 5　同じ凸集合への作用が二つの判定を与える例

$\Gamma=F_2=\langle a,b\rangle$、$Y=\partial F_2$ を右 Cayley 木の端、$Z=\Gamma\cup\{\infty\}$ を離散群の一点コンパクト化とし、$X=Y\sqcup Z$ とする。左移動は $Y,Z$ に連続に作用し、$\infty$ を固定する。有限 $E$ について群自身の誤差を
$$
 c_E=\inf_{p\in\operatorname{Prob}_f(\Gamma)}\sum_{s\in E}\|s_*p-p\|_1
$$
と書く。

$Y$ 上では、端 $\xi$ に至る単位元からの半直線の最初の $n$ 頂点（単位元を含む）の一様分布 $m_n(\xi)$ を取る。これは有限語の接頭辞のみに依存し、全体で有限台かつ連続。生成元 $s$ に対して、$s$ と単位元から同じ端 $s\xi$ に向かう二本の半直線は隣り合う点から始まるため、一方がもう一方の一頂点後から続く。よって $e_s(m_n,\xi)=2/n$。語長について繰り返せば $e_s(m_n,\xi)\le 2|s|/n$。これが $Y$ の位相的従順性を直接証明する。

$0\le t<1$ に対して
$$
 K_t=\{(1-t)\nu+t\delta_\infty:\nu\in\operatorname{Prob}(Y)\}\ \subset\operatorname{Prob}(X).
$$
$\nu\mapsto(1-t)\nu+t\delta_\infty$ は $\operatorname{Prob}(Y)$ から $K_t$ への同変なアフィン同相。$Y$ の証人を $\nu$ に関して積分すれば $\operatorname{Prob}(Y)$ への作用も位相的従順。ところが任意の有限 $E$ について
$$
 \boxed{u_E(K_t)=0,\qquad d_E(X,K_t)=t\,c_E.} \tag{3}
$$
下界は各測度が固定点に与える質量 $t$ から出る。固定点でのあらゆる場の誤差は $c_E$ 以上である。上界には $Y$ 上で $m_n$、開かつ閉じた成分 $Z$ 全体で $c_E$ を任意の精度で達成する定数場を貼る。$n$ を大きくしてから群の側の許容誤差を零にすれば (3) を得る。

正の障害も直接確認できる。$S=\{a,a^{-1},b,b^{-1}\}$。有限集合 $L\subset\Gamma$ の左 Cayley 木での無向辺境界は少なくとも $2|L|$ 本ある。実際、有限森の内部辺数は $|L|$ 以下で、各頂点の次数は 4。各境界辺を両方向に数えると $\sum_{s\in S}\|s_*1_L-1_L\|_1=2|\partial L|\ge4|L|$。非負の有限台確率 $p$ の上位集合 $\{p>r\}$ に適用し $r$ で積分すると $c_S\ge4>0$。従って $K_0$ と $K_t$（$0<t<1$）は抽象的には同じコンパクト凸作用をもち、前者だけが指定したトレースでの条件を満たす。後者は面ではない。例えば $(1-t)\delta_\xi+t\delta_\infty$ の二つの端点は $K_t$ に入らない。2024 年の全トレースに関する同値の両辺を、同じ任意の不変閉凸部分集合へ制限する拡張は、すでに可換かつ単位的な例で失敗する。

**一つずつ測る場合の検算。** 同じ $X$ で端 $\xi\in Y$ を固定し、互いに異なる $g_j\in\Gamma$ に対し $\mu_j=(1-t)\delta_\xi+t\delta_{g_j}$ とする。各 $\rho_{\mu_j}$ では測度論的に従順である。$Y$ では上の半直線平均を用い、$\Gamma$ 上では $h\mapsto\delta_h$ が厳密に同変な Borel 場を与える。$\infty$ の質量は零なのでそこで任意の値を割り当てられる。一方 $\mu_j\to(1-t)\delta_\xi+t\delta_\infty$ なので、連続な $D_E(m,\cdot)$ を測度族全体で試すと下界 $tc_E$ が現れる。(3) と同じ貼り合わせが上界を与え、$d_E(X,\{\mu_j:j\ge1\})=tc_E$。無限遠での集中によって、一つの近似を選ぶ問題が変わった。

## 6　群・測度・幾何への特殊化

- $X$ が一点なら、同じ確率ベクトルを群の有限集合の移動で試す通常の Reiter 条件となる。弱 $^*$ 集積点は $\ell^\infty(\Gamma)$ の左不変平均で、逆も Reiter の定理による。これはコンパクト凸集合へのすべての連続アフィン作用の固定点性に等しい。[Reiter (1965)](https://doi.org/10.1016/S1385-7258(65)50072-X) ／ [Day (1961)](https://doi.org/10.1215/ijm/1255631582)
- コンパクト作用で全 Dirac 測度を指定すると、積分の上限は点ごとの上限であり、作用 groupoid の位相的従順性になる。非特異な確率作用で一つの測度を指定すれば §2 の測度論的条件になる。任意の標準 Borel 空間上の可算群の Borel 作用も、Borel 単射 $b$ を Cantor 空間に取り $x\mapsto(b(g^{-1}x))_{g\in\Gamma}$ とすることで、コンパクト距離化可能なシフトの Borel 部分集合に同変に実現できる。像に押し出した確率測度を用いればよい。[Zimmer (1978), エルゴード作用](https://doi.org/10.1016/0022-1236(78)90013-7) ／ [Adams・Elliott・Giordano (1994)](https://doi.org/10.1090/S0002-9947-1994-1250814-5)
- 幾何では有限生成群の語距離 $d(u,v)=|u^{-1}v|$ を取る。性質 A の確率場 $a_n(u)$ は台が $uB_{R_n}$ にあり、各固定距離以内での $\|a_n(u)-a_n(v)\|_1$ は一様に 0 に向かう。$m_n(x)=x_*a_n(x^{-1})$ と置くと台は $B_{R_n}$、$e_s(m_n,x)=\|a_n(x^{-1})-a_n(x^{-1}s^{-1})\|_1$ である。この $m_n$ の座標、各点の指示関数、それらの全左移動は可算族である。これらの関数による評価写像の像を可算積 $[0,1]^{\mathbb N}$ 内で閉じると、左作用が延長するコンパクト距離化可能なコンパクト化を得る。各 $m_n$ と有限台・近似不変性の評価も稠密性により延長する。逆に、このような位相的に従順なコンパクト化から $a_n(u)=u_*m_n(u^{-1})$ と戻せば性質 A が従う。Higson・Roe の Stone–Čech コンパクト化での定理の、可算個の証人に必要な部分である。[Higson・Roe (2000)](https://doi.org/10.1515/crll.2000.009)

## 7　結果の位置づけと再検算

指定した族を入力として保持し、(1)、(2)、閉じた面での等号、商から来るトレースでの移送、(3) の反例を一続きに証明した。両端の既知の同値、ミニマックス、トレース従順性の定義はそれぞれ上記の一次資料に依る。面と非面の比較はこのノートの直接の導出であり、文献上の優先権は未確認である。任意の非可換 $A$ の閉じた不変トレース面については、[別ノート](closed-trace-face-reiter.md)で二乗 Hellinger 誤差による比較を扱う。一般の groupoid でどの測度族を Morita 同値に沿って移すべきかも、この結果の範囲外である。

§5 の左右の移動規約を再検算する最小コード。正負の整数は互いに逆の生成元、語は既約語。有限チェックが対象とするのは半直線平均の支持であり、(1)–(3) の証明は上に記した。

~~~python
from itertools import product

generators = (1, -1, 2, -2)

def left(s, word):
    if word and word[0] == -s:
        return word[1:]
    return (s,) + word

for n in range(1, 6):
    cases = 0
    for word in product(generators, repeat=n):
        if any(a == -b for a, b in zip(word, word[1:])):
            continue
        prefixes = {word[:k] for k in range(n)}
        for s in generators:
            moved = {left(s, prefix) for prefix in prefixes}
            new_word = left(s, word)
            target = {new_word[:k] for k in range(n)}
            assert len(moved) == len(target) == n
            assert len(moved ^ target) == 2
            cases += 1
    print(n, cases)
~~~

出力は順に $(1,16),(2,48),(3,144),(4,432),(5,1296)$。有限計 1936 通り。
