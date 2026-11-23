# 閉トレース面での Reiter 誤差とアフィン作用

> **AI-generated independent research note.** This note is not a paper or a peer-reviewed publication and is not a contribution to any person’s research profile or bibliography. The written proof has been checked; no formal verification or claim of publication priority is made.

**結果。** 可算離散群が単位的 $C^*$ 環 $A$ に作用し、$K\subset T(A)$ が空でない不変弱 $^*$ 閉面であるとする。正確に単位質量をもつ有限列のトレース 2-ノルムによる二乗誤差は、$K$ 自身への作用を確率ベクトルの平方根で測った最小誤差と、群の各有限集合ごとに一致する。任意の有限個の近似可換性テストを加えても同じ値になる。$K$ が商の全トレースから来るという仮定、Bauer 性、可分性はいずれも証明に必要ない。

証明の要所は、有限 von Neumann 環の中心値トレースを、中心の各指標で評価したときに得られるトレースが $K$ に残ることである。これは面の性質そのものに対応する。中心のスペクトルから $K$ へ写す向きなので、極端トレースへの分解を連続に選ぶ必要がない。

## 1　比較する三つの下限

$\alpha:\Gamma\curvearrowright A$ とし、$s\tau=\tau\circ\alpha_{s^{-1}}$。$E\subset\Gamma$、$F\subset A_1$ は有限集合（$A_1$ は閉単位球）。$A$ 値の有限台の列 $\xi$ に対して
$$
 Q(\xi)=\sum_h\xi_h^*\xi_h,\qquad
 (\widetilde\alpha_s\xi)_h=\alpha_s(\xi_{s^{-1}h}),\qquad
 \|\xi\|_{2,\tau}^2=\tau(Q(\xi)).
$$
$a\xi-\xi a$ は各座標での交換子。今回の規約は、すべての誤差を同じトレースで足してから上限を取るものである。
$$
 f_\xi(\tau)=\sum_{s\in E}\|\widetilde\alpha_s\xi-\xi\|_{2,\tau}^2+
             \sum_{a\in F}\|a\xi-\xi a\|_{2,\tau}^2,\qquad
 R_{E,F}(A,K)=\inf_{\xi\in C_c(\Gamma,A),\,Q(\xi)=1_A}\sup_{\tau\in K} f_\xi(\tau).
 \tag{1}
$$
平方根の距離は $h(p,q)^2=\sum_j(\sqrt{p_j}-\sqrt{q_j})^2$ とする（係数 $1/2$ は入れない）。$p:K\to\operatorname{Prob}(\Gamma)$ は $\ell^1$ ノルム連続、各 $p$ ごとに全 $\tau$ に共通する有限台を持つ。左移動を $s_*$ とする。
$$
 d_E(p)=\sup_{\tau\in K}\sum_{s\in E} h\bigl(p(\tau),s_*p(s^{-1}\tau)\bigr)^2,\qquad
 H_E(K)=\inf_p d_E(p).
 \tag{2}
$$
確率の各座標が $\tau$ の連続アフィン関数である $p$ に限った下限を $H_E^{\rm aff}(K)$ とする。平方根の座標がアフィンであることは要求しない。従来の $\ell^1$ 誤差 $L_E(K)$ は (2) の $h^2$ を $\|p-q\|_1$ に置き換えて定める。群の作用はすべて着点 $\tau$ で比較した。始点で書く規約では $E$ を $E^{-1}$ にすれば同じ式になる。

**比較定理。** 上記の閉面 $K$ について
$$
 \boxed{R_{E,F}(A,K)=H_E^{\rm aff}(K)=H_E(K)},\qquad
 H_E(K)\le L_E(K)\le 2\sqrt{|E|H_E(K)}. \tag{3}
$$
二つの不等式は $h^2\le\|p-q\|_1\le 2h$ と Cauchy–Schwarz から従う。したがって通常の位相的 Reiter 条件との関係は消滅の同値である。支持をあらかじめ一つの有限集合に固定する版は (3) の対象外である。

## 2　面を特徴付ける中心切断

ここだけ $K$ を一般の空でない弱 $^*$ コンパクト凸集合として始める。$K$ に属するトレースの GNS 表現を足し合わせ
$$
 N_K=\pi(A)'',\qquad \pi=\bigoplus_{\tau\in K}\pi_\tau
$$
とする。各 $\tau$ は $N_K$ の正規トレースに延び、この族は正元を分離する。各 $\pi_\tau(A)''$ の GNS トレースが忠実であることから従う。従って $N_K$ は有限 von Neumann 環である。その正規中心値トレースを $C:N_K\to Z(N_K)$、中心の Gelfand スペクトルを $Y$ とおく。正規トレースは $C$ を通じて因子化する。中心値トレースをトレース単体に適用する基本的な事実については Blackadar・Rørdam を参照。[Blackadar・Rørdam (2024年プレプリント、2026年刊)](https://arxiv.org/abs/2409.09644)

$$
 j:Y\longrightarrow T(A),\qquad j(y)(a)=y(C(\pi(a))).
 \tag{4}
$$
これは弱 $^*$ 連続であり、$K$ が不変なら同変である。作用は GNS 表現の直和を並べ替えることで $N_K$ の正規自己同型に延び、$C$ の一意性から $C$ と可換である。

**中心切断補題。** 次の条件は同値である。

1. $K$ は $T(A)$ の面である。
2. $j(Y)\subset K$。
3. $N_K$ のあらゆる正規トレース状態を $A$ に引き戻すと $K$ に属する。

**証明。** (1) から (2) を示す。$a=a^*\in A$ に対して $c=\max_{\tau\in K}\tau(a)$。もし $C(\pi(a))\le c1$ が破れれば、ある $\varepsilon>0$ で中心スペクトル射影 $q=1_{(c+\varepsilon,\infty)}(C(\pi(a)))\ne0$。一つの $\tau\in K$ が $\tilde\tau(q)>0$ を満たす。$\tilde\tau$ は正規延長である。切断 $\rho(a')=\tilde\tau(q\pi(a'))/\tilde\tau(q)$ は $A$ のトレース状態で、$\tau$ の凸分解の成分なので面 $K$ に属する。質量が 1 の場合は $\rho=\tau$。中心値トレースの両側加群性から $\rho(a)\ge c+\varepsilon$ となり矛盾する。従って $j(y)(a)\le c$。すべての自己共役 $a$ でのこの半空間条件は、弱 $^*$ コンパクト凸集合 $K$ への所属を特徴付ける。

(2) から (3) は、中心上の状態が $Y$ 上の確率測度であり、正規トレース $\psi$ に対して $\psi=\psi|_Z\circ C$ となることから従う。$\psi\circ\pi$ は $j(Y)$ の重心である。(3) から (1) について、$\tau=t\sigma+(1-t)\rho\in K$、$0<t<1$ とする。$A^{**}$ 上の正規延長でも $t\tilde\sigma\le\tilde\tau$、$(1-t)\tilde\rho\le\tilde\tau$。従って両者の台は $\tilde\tau$ の台以下で、両者とも $N_K$ の正規トレースを定める。(3) より $\sigma,\rho\in K$。□

この最後の議論を明示すると、トレースの正規延長の台 $s(\tilde\tau)$ は中心射影であり、$z_K=\bigvee_{\tau\in K}s(\tilde\tau)$ とすれば $N_K\simeq z_K A^{**}$（直和表現の正規延長の核が $(1-z_K)A^{**}$）。面の場合
$$
 K=\{\sigma\in T(A):s(\tilde\sigma)\le z_K\}. \tag{5}
$$
$A$ 自身のイデアル $\ker\pi_\tau$ と $A^{**}$ の中心台にはこの点で異なる情報がある。$q$ は $A$ 内の射影である必要がない。

## 3　有限集合ごとの等式の証明

**列からアフィン場へ。** $Q(\xi)=1_A$ に対し $p_\xi(\tau)(h)=\tau(\xi_h^*\xi_h)$ とする。これは有限単体値の連続アフィン場で、各 GNS 空間の逆三角不等式から
$$
 h\bigl(p_\xi(\tau),s_*p_\xi(s^{-1}\tau)\bigr)^2
 \le\sum_h\|\xi_h-(\widetilde\alpha_s\xi)_h\|_{2,\tau}^2 .
$$
従って $H_E(K)\le H_E^{\rm aff}(K)\le R_{E,F}(A,K)$。この向きには面の仮定を使わない。

**中心での証人。** 逆向きには任意の連続場 $p$ を固定する。§2 により $j:Y\to K$ なので $b_h(y)=\sqrt{p(j(y))(h)}$ は $Z(N_K)=C(Y)$ の元である。有限個しか非零でなく、$Q(b)=1_{N_K}$。同変性と (2) から、$N_K$ の順序で
$$
 \sum_{s\in E}Q(\widetilde\alpha_s b-b)\le d_E(p)\,1_{N_K},
 \qquad [b_h,\pi(a)]=0\quad(a\in A).
 \tag{6}
$$
ここで使う連続性は中心のスペクトル $Y$ 上のもので、$K$ 上で連続な境界分解は使わない。

**正確な単位質量での局所近似。** 有限群では $\xi_h=|\Gamma|^{-1/2}1_A$ と定数一様分布により各下限が 0。以下 $\Gamma$ は無限とする。$L=\operatorname{supp}b$ とおく。有限列に対する Kaplansky 密度により、台が $L$ に入る列 $v_i\in C_c(\Gamma,A)$ で $Q(v_i)\le1_A$、$\pi(v_i)\to b$ を有界集合の $\sigma$-strong* 位相で満たすネットを取れる。具体的には $b$ を $M_{|L|+1}(N_K)$ の非対角な一列とし、行列環の単位球から strong* 近似して同じ角を切り出す。元の $A$ でのノルム上界は $N_K\simeq z_K A^{**}$ の元を他の直和成分で 0 にして $M_{|L|+1}(A^{**})$ に入れ、そこで $M_{|L|+1}(A)$ の単位球を使えば得られる。

$k\notin L$ に残差 $(1_A-Q(v_i))^{1/2}$ を一座標として加え、$\xi_i$ とする。$Q(\xi_i)=1_A$ が厳密に成立する。この新しい座標の像は $N_K$ で strong* に 0 に向かう。有界集合では積、随伴、正縮小元の平方根、正規自己同型はいずれもこの収束を保つ。各正規トレースで評価すると、(6) により
$$
 \forall\,\tau\in K,\qquad \inf_{Q(\xi)=1_A} f_\xi(\tau)\le d_E(p). \tag{7}
$$
ここでは初めから $K$ で一様な strong* 近似を仮定していない。

**一つの列への一様化。** $\mathscr D=\{f_\xi:Q(\xi)=1_A,\ \xi\in C_c(\Gamma,A)\}\subset C(K,\mathbb R)$ は凸である。実際、列 $\xi^j$ の台を $L_j$ とし、有限個の $(E\cup\{e\})L_jr_j$ が互いに素になるよう $r_j\in\Gamma$ を順に選ぶ。禁止される $r_j$ は各回有限個である。右移動 $R_{r_j}\xi(h)=\xi(hr_j^{-1})$ は $\widetilde\alpha_s$ と可換。非負の $t_j$ で $\sum_j t_j=1$ とすると $\xi=\sum_j\sqrt{t_j}R_{r_j}\xi^j$ は正確に単位質量を保ち、台の交差がないため $f_\xi=\sum_jt_j f_{\xi^j}$ となる。近似可換性の項にも同じことが成り立つ。

$f\in\mathscr D$ の各々は $\tau$ の連続アフィン関数。コンパクト凸集合 $K$ と凸集合 $\mathscr D$ の評価対 $(\tau,f)\mapsto f(\tau)$ に Sion の定理を適用すると
$$
 R_{E,F}(A,K)=\max_{\tau\in K}\inf_{Q(\xi)=1_A} f_\xi(\tau)\le d_E(p).
$$
最大値の存在は右辺の下限関数の上半連続性による。$p$ に関する下限で (3) を得る。□　右移動による列の凸化は Gardella ほかの証明にも現れる。同論文の全トレースでの消滅の議論から借りた部分である。[Sion (1958), pp. 173–174](https://msp.org/pjm/1958/8-1/pjm-v8-n1-p14-s.pdf) ／ [Gardella・Geffen・Kranz・Naryshkin・Vaccaro (2024), Theorem 2.5 の (8) から (1)](https://link.springer.com/article/10.1007/s00208-024-02833-9)

**近似単位質量との整合。** $Q(\eta)\le1_A$、$\|1_A-Q(\eta)\|_{2,K}\le\delta$ とし、$\|c\|_{2,K}=\sup_{\tau\in K}\tau(c^*c)^{1/2}$ と書く。新しい座標に $r^{1/2}=(1_A-Q(\eta))^{1/2}$ を加えれば、$\sup_{\tau\in K}\|r^{1/2}\|_{2,\tau}\le\sqrt{\delta}$。$K$ の不変性とトレース性から、各移動テストと各単位球の交換子テストの 2-ノルムの増分は $2\sqrt{\delta}$ 以下。従って、すべての有限テストでの消滅は近似単位質量版とも同値である。非単位的 $A$ の内部では有限和 $Q(\xi)\in A$ が乗数環の単位元に等しくなることはない。(1) は単位的な設定での定理である。

## 4　Bauer 性、同じ台、連続アフィン化の境界

距離化可能な閉面では $\partial_eK=K\cap\partial_eT(A)$ であり、各極端トレースの GNS 閉包は有限因子である。Choquet 分解の一意性により $\tau\in K$ の境界測度 $\mu_\tau$ は $\partial_eK$ に集中する。Bauer の場合は重心写像 $\operatorname{Prob}(\partial_eK)\to K$ がアフィン同相。確率場の境界値を $\mu_\tau$ で積分し直すと連続アフィン場になる。$h^2$ の同時凸性（各座標で Cauchy–Schwarz）と $\mu_{s\tau}=s_*\mu_\tau$ により誤差は増えず、元の有限台も保つ。非 Bauer のときはこの操作が不連続になりうる。(3) の同じ下限という主張では、場の取り替えと有限台の拡大を許している。

**商から来ない閉面での反例。** 積位相を入れた明示的単体
$$
 S=\{(x,d)\in[0,1]^{\mathbb N}\times[-1,1]:\ \sum_n x_n+|d|\le1\}
$$
を考える。有限部分和の条件の共通部分なのでコンパクト。$e_n=(\delta_n,0),\,u=(0,1),\,v=(0,-1)$ とすると、任意の点の境界測度は $e_n$ に質量 $x_n$、$u,v$ にそれぞれ $(1-\sum_nx_n\pm d)/2$ を与える。これが唯一の表示で、これらの点がちょうど極端点である。また $e_n\to o=(u+v)/2$。$K=\{x_1=0\}$ は真の閉面であり、それ自身が非 Bauer である。

Blackadar の実現定理により $T(A)\simeq S$ を持つ単純単位的 AF 環 $A$ がある。例えば自明作用を取れば $K$ は不変。すべてのトレースが $A$ 上忠実であり、この真の面を商の全トレースの引き戻しとして得ることはできない。$u,v$ は同じ零核をもつが、異なる有限因子トレースで正規延長の中心台は直交する。実際、それぞれの中心台が切り出す直和成分は因子で、もし台が等しければその因子の唯一の正規トレース状態として $u=v$ になってしまう。一方、$0<t<1$ の異なる $tu+(1-t)v$ は相互に異なるトレースであり、正規延長の中心台もすべて同じ $s(\tilde u)+s(\tilde v)$ である。(5) は面への所属を判定し、個々のトレースにはさらに中心上の重みが残る。[Blackadar (1980)](https://doi.org/10.1016/0022-1236(80)90062-2)

連続関数 $f(x,d)=d^2$ を $K$ 上で取る。極端トレース上の値をそのまま使い $Bf(\tau)=\int f\,d\mu_\tau$ とすると
$$
 Bf(e_n)=0\quad(n\ge2),\qquad Bf(o)=1,\qquad f(o)=0.
$$
従って、この境界値をもつ連続アフィン拡張は存在しない。二座標の確率場 $(f,1-f)$ に対しても同じ問題が起きる。

さらに $z=f\circ j\in Z(N_K)$ は $K$ に関する一様トレース完備化 $\overline{\pi(A)}^{\,u,K}$ に属さない。極端トレース $\lambda$ の正規延長は中心では一つの指標 $y_\lambda$ となり $j(y_\lambda)=\lambda$。よって $\tilde e_n(z)=0$、$\tilde o(z)=(\tilde u(z)+\tilde v(z))/2=1$。一様 2-ノルムで $A$ の有界な元により近似できる元なら、$|\tau(a)|\le\|a\|_{2,\tau}$ によりトレース評価は連続アフィン関数の一様極限になり、これは起こりえない。§3 が中心元の一様な持ち上げを要求すると破綻する箇所を、この例で確かめられる。

## 5　一次資料と到達点

- Ozawa (2013), Theorem 3 は初めから距離化可能な閉トレース面を取り、その極端境界上の有界 Borel 関数を $Z(N_K)$ に表し、一様トレース完備化に属する中心元をアフィン関数系の中心で特徴付けている。距離化可能な場合、その写像を $C(K)$ の境界への制限と合成すると (4) の引き戻しと一致する。実際、両者は各評価関数 $\widehat a(\tau)=\tau(a)$ を $C(\pi(a))$ に送り、これらの自己共役評価関数が $C(K)$ を生成する。今回の中心切断の証明では境界測度を経由せず、非距離化可能な $K$ にも同じ比較が通る。[Ozawa (2013), Theorem 3](https://arxiv.org/pdf/1304.3523)
- Gardella・Geffen・Kranz・Naryshkin・Vaccaro (2024), Definition 2.2, Theorem 2.5 の (1) と (6) は、単位的可分 $A$ の**全**トレースでのトレース従順性と $T(A)$ 自身への作用の位相的従順性を特徴付ける。少なくとも距離化可能な面での消滅の同値は、Ozawa の閉面定理と原論文の局所近似・凸化を組み合わせて導ける。今回明示した比較は、正確な単位質量、各有限 $E,F$ での下限の一致、連続場と連続アフィン確率場の下限の一致まで含む。[Gardella・Geffen・Kranz・Naryshkin・Vaccaro (2024)](https://link.springer.com/article/10.1007/s00208-024-02833-9)
- Carrión・Castillejos・Evington・Gabe・Schafhauser・Tikuisis・White (2023年初版、2026年改訂) の Definition 3.13, Proposition 3.14 は、トレース完備化の枠組みで、面の仮定と極端トレースの因子性の関係を明記する。同論文の §3.6 では Bauer 単体に関する $W^*$-bundle 構造を扱う。(3) で用いたのは有限 von Neumann 包絡環と、個々のトレースでの近似から誤差を一様化する手順である。ファイバーの同型性や bundle の自明化を仮定していない。[Carrión ほか (2023/2026)](https://arxiv.org/html/2310.20594v6)

**本ノートで証明したこと。** (3)–(5)、近似質量版との消滅の同値、非 Bauer の単純 AF 例での連続アフィン拡張および一様完備化への所属の失敗。**追加仮定で成り立つこと。** Bauer 面では、各連続場の境界値を保ち、台を増やさずにアフィン化できる。**未確認。** 非 Bauer 面で有限台を固定した最適化の一般的な等式、通常の $\ell^1$ 誤差との数値的な一致については主張しない。有限テストの等式の文献上の優先性は判定していない。

## 再検算

下の標準 Python コードは、§3 の台の移動を非可換な $2\times2$ 行列で検査する。$\Gamma=\mathbb Z$ が行列の二つの座標を入れ替える自己同型の冪で作用する。等式はトレースを取る前の行列として検査する。二つの列の係数 $3/5,4/5$ の分母を払った。無限次元の近似とミニマックスは上の証明で正当化した。

~~~python
# A = M_2(C), real test matrices, Gamma = Z. Matrices are row-major.
Z = (0, 0, 0, 0)
I = (1, 0, 0, 1)
P = (1, 0, 0, 0)
Q = (0, 0, 0, 1)
U = (0, 1, 1, 0)
T = (0, 1, 0, 0)

def add(a, b):
    return tuple(x + y for x, y in zip(a, b))

def scale(n, a):
    return tuple(n * x for x in a)

def sub(a, b):
    return add(a, scale(-1, b))

def adj(a):
    return (a[0], a[2], a[1], a[3])

def mul(a, b):
    return tuple(sum(a[2*i+k]*b[2*k+j] for k in range(2))
                 for i in range(2) for j in range(2))

def square_sum(values):
    total = Z
    for a in values:
        total = add(total, mul(adj(a), a))
    return total

def energy(column):
    total = Z
    for s in (-1, 1, 2):
        moved = {h+s: mul(mul(U, v), U) if s % 2 else v
                 for h, v in column.items()}
        total = add(total, square_sum(sub(moved.get(h, Z), column.get(h, Z))
                    for h in moved.keys() | column.keys()))
    for a in (T, P, U):
        total = add(total, square_sum(sub(mul(a, v), mul(v, a))
                                      for v in column.values()))
    return total

x = {0: P, 1: Q}
y = {0: T, 2: adj(T)}
assert square_sum(x.values()) == square_sum(y.values()) == I
for shift in (7, 13):
    w = {h: scale(3, v) for h, v in x.items()}
    w.update({h+shift: scale(4, v) for h, v in y.items()})
    assert square_sum(w.values()) == scale(25, I)
    assert energy(w) == add(scale(9, energy(x)), scale(16, energy(y)))
print("two exact matrix energy identities verified")
~~~
