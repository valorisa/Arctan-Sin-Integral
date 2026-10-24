# Correction complète — Exercice 16(c)

On considère la sphère de centre $O$ et de rayon $1$. Si $A$ et $B$ sont deux points de cette sphère tels que $\mathbf a=\overrightarrow{OA}$ et $\mathbf b=\overrightarrow{OB}$ sont perpendiculaires, le cercle de centre $O$ passant par $A$ et $B$ a pour équation vectorielle

$$
\mathbf v(\theta)=\cos\theta\,\mathbf a+\sin\theta\,\mathbf b,\qquad 0\le\theta<2\pi .
$$

Cette formule est admise par l'énoncé. Elle s'applique à deux vecteurs **unitaires et perpendiculaires** : c'est l'idée directrice des trois questions.

## (i) Montrer que $\|\mathbf v(\theta)\|^2=1$

$A$ et $B$ sont sur la sphère unité, donc $\|\mathbf a\|=\|\mathbf b\|=1$. Comme $\mathbf a\perp\mathbf b$, on a $\mathbf a\cdot\mathbf b=0$.

Le carré de la norme est le produit scalaire du vecteur par lui-même :

$$
\begin{aligned}
\|\mathbf v(\theta)\|^2
&=(\cos\theta\,\mathbf a+\sin\theta\,\mathbf b)\cdot(\cos\theta\,\mathbf a+\sin\theta\,\mathbf b)\\
&=\cos^2\theta\,(\mathbf a\cdot\mathbf a)+2\cos\theta\sin\theta\,(\mathbf a\cdot\mathbf b)+\sin^2\theta\,(\mathbf b\cdot\mathbf b)
\end{aligned}
$$

(le produit scalaire est commutatif, d'où le facteur $2$). Avec $\mathbf a\cdot\mathbf a=\mathbf b\cdot\mathbf b=1$ et $\mathbf a\cdot\mathbf b=0$ :

$$
\|\mathbf v(\theta)\|^2=\cos^2\theta+\sin^2\theta=1 .
$$

Tous les points du cercle sont donc bien sur la sphère unité. $\blacksquare$

## (ii) Points d'intersection de $C_1$ et $C_2$

$$
C_1:\ \mathbf v_1(\alpha)=\frac{\cos\alpha}{\sqrt5}\begin{pmatrix}1\\2\\0\end{pmatrix}+\sin\alpha\begin{pmatrix}0\\0\\-1\end{pmatrix},\qquad 0\le\alpha<2\pi
$$

$$
C_2:\ \mathbf v_2(\beta)=\frac{\cos\beta}{\sqrt2}\begin{pmatrix}0\\1\\1\end{pmatrix}+\sin\beta\begin{pmatrix}1\\0\\0\end{pmatrix},\qquad 0\le\beta<2\pi
$$

*Notation.* L'énoncé note $\theta$ le paramètre de $C_2$. On le note ici $\beta$ pour distinguer les deux paramètres : un point commun peut correspondre à des valeurs différentes sur chaque cercle.

### Méthode 1 : égalité des coordonnées

Un point est commun aux deux cercles si $\mathbf v_1(\alpha)=\mathbf v_2(\beta)$, c'est-à-dire :

$$
\begin{cases}
\dfrac{\cos\alpha}{\sqrt5}=\sin\beta &(1)\\[6pt]
\dfrac{2\cos\alpha}{\sqrt5}=\dfrac{\cos\beta}{\sqrt2} &(2)\\[6pt]
-\sin\alpha=\dfrac{\cos\beta}{\sqrt2} &(3)
\end{cases}
$$

**Étape 1.** Les seconds membres de (2) et (3) sont égaux, donc

$$
\frac{2\cos\alpha}{\sqrt5}=-\sin\alpha,\qquad\text{soit}\qquad \sin\alpha=-\frac{2}{\sqrt5}\cos\alpha .
$$

**Étape 2.** Avec $\cos^2\alpha+\sin^2\alpha=1$ :

$$
\cos^2\alpha\left(1+\frac45\right)=1\ \Longrightarrow\ \cos^2\alpha=\frac59\ \Longrightarrow\ \cos\alpha=\pm\frac{\sqrt5}{3}.
$$

La relation de l'étape 1 impose des signes opposés :

$$
(\cos\alpha,\sin\alpha)=\left(\frac{\sqrt5}{3},-\frac23\right)\quad\text{ou}\quad\left(-\frac{\sqrt5}{3},\frac23\right).
$$

(Cela correspond à $\tan\alpha=-\dfrac{2}{\sqrt5}$, négative dans les quadrants 2 et 4.)

**Étape 3.** Points correspondants. Pour $\cos\alpha=\frac{\sqrt5}{3}$ et $\sin\alpha=-\frac23$ :

$$
\mathbf v_1(\alpha)=\frac13\begin{pmatrix}1\\2\\0\end{pmatrix}-\frac23\begin{pmatrix}0\\0\\-1\end{pmatrix}
=\begin{pmatrix}\frac13\\[2pt]\frac23\\[2pt]\frac23\end{pmatrix}.
$$

Le couple opposé donne le point opposé $\left(-\frac13,-\frac23,-\frac23\right)$.

**Étape 4.** Ces points sont-ils sur $C_2$ ? Pour le premier, (1) donne $\sin\beta=\frac13$ et (2) donne $\cos\beta=\frac{2\sqrt2}{3}$. Un tel $\beta$ existe car

$$
\left(\tfrac13\right)^2+\left(\tfrac{2\sqrt2}{3}\right)^2=\tfrac19+\tfrac89=1,
$$

et (3) est vérifiée : $-\sin\alpha=\frac23=\frac{\cos\beta}{\sqrt2}$. La vérification de (1) est indispensable : (2) et (3) seules ne contrôlent pas la première coordonnée. Pour le point opposé, on prend $\sin\beta=-\frac13$ et $\cos\beta=-\frac{2\sqrt2}{3}$.

### Méthode 2 : lecture géométrique (plus courte)

Les vecteurs $\frac1{\sqrt5}(1,2,0)$ et $(0,0,-1)$ sont unitaires et orthogonaux : $C_1$ est le grand cercle de la sphère unité situé dans le plan qu'ils engendrent, d'équation $y=2x$. De même, $C_2$ est le grand cercle situé dans le plan $z=y$.

Les points communs appartiennent aux deux plans, donc à leur droite d'intersection $(x,y,z)=(t,2t,2t)$. Ils sont aussi sur la sphère :

$$
t^2+4t^2+4t^2=1\ \Longrightarrow\ t=\pm\frac13 .
$$

Réciproquement, tout point de cette droite situé sur la sphère est sur chacun des deux plans et sur la sphère, donc sur $C_1$ et sur $C_2$.

### Conclusion

$$
C_1\cap C_2=\left\{\left(\tfrac13,\tfrac23,\tfrac23\right),\ \left(-\tfrac13,-\tfrac23,-\tfrac23\right)\right\}.
$$

## (iii) Cercle de centre $O$ passant par $A(0,1,0)$ et $P\left(\frac{\sqrt3}{2},\frac1{\sqrt6},-\frac1{2\sqrt3}\right)$

On pose $\mathbf a=\overrightarrow{OA}=(0,1,0)$ et $\mathbf p=\overrightarrow{OP}$.

### 1. Pourquoi il faut construire un second vecteur

$\mathbf a$ est unitaire. $\mathbf p$ l'est aussi :

$$
\|\mathbf p\|^2=\frac34+\frac16+\frac1{12}=\frac{9+2+1}{12}=1 .
$$

Mais $\mathbf a\cdot\mathbf p=\frac1{\sqrt6}\neq0$ : $\mathbf a$ et $\mathbf p$ ne sont pas perpendiculaires, on ne peut donc pas les utiliser directement dans la formule. On garde $\mathbf a$ et on construit un vecteur unitaire perpendiculaire à $\mathbf a$ dans le plan $OAP$.

### 2. Projection de $\overrightarrow{OP}$ sur $\overrightarrow{OA}$

Soit $H$ le projeté orthogonal de $P$ sur la droite $(OA)$. Comme $\|\mathbf a\|=1$ :

$$
\overrightarrow{OH}=\frac{\mathbf p\cdot\mathbf a}{\|\mathbf a\|^2}\,\mathbf a=\frac1{\sqrt6}\,\mathbf a=\left(0,\frac1{\sqrt6},0\right).
$$

### 3. Composante perpendiculaire à $\overrightarrow{OA}$

$$
\overrightarrow{HP}=\overrightarrow{OP}-\overrightarrow{OH}
=\left(\frac{\sqrt3}{2},\,0,\,-\frac1{2\sqrt3}\right)
=\frac1{2\sqrt3}\,(3,\,0,\,-1).
$$

On vérifie $\overrightarrow{HP}\cdot\mathbf a=0$ : ce vecteur est perpendiculaire à $\mathbf a$ et dirigé dans le plan $OAP$.

### 4. Normalisation

$\|(3,0,-1)\|=\sqrt{10}$, donc

$$
\mathbf b=\frac1{\sqrt{10}}\begin{pmatrix}3\\0\\-1\end{pmatrix}.
$$

(Équivalent : $\mathbf b=\overrightarrow{HP}/\|\overrightarrow{HP}\|$ avec $\|\overrightarrow{HP}\|=\sqrt{\frac34+\frac1{12}}=\sqrt{\frac56}$.) On a bien $\|\mathbf a\|=\|\mathbf b\|=1$ et $\mathbf a\cdot\mathbf b=0$.

### 5. Équation du cercle

$$
\boxed{\mathbf v(\theta)=\cos\theta\begin{pmatrix}0\\1\\0\end{pmatrix}+\frac{\sin\theta}{\sqrt{10}}\begin{pmatrix}3\\0\\-1\end{pmatrix},\qquad 0\le\theta<2\pi}
$$

Soit, en coordonnées :

$$
x=\frac{3}{\sqrt{10}}\sin\theta,\qquad y=\cos\theta,\qquad z=-\frac{1}{\sqrt{10}}\sin\theta .
$$

### 6. Vérification : le cercle passe par $A$ et $P$

- $\theta=0$ : $\mathbf v(0)=(0,1,0)=\overrightarrow{OA}$.
- Pour $P$, on prend $\cos\theta=\frac1{\sqrt6}$ et $\sin\theta=\sqrt{\frac56}$ (possible car $\frac16+\frac56=1$). Alors

$$
x=\frac{3}{\sqrt{10}}\sqrt{\frac56}=\frac{3}{\sqrt{12}}=\frac{\sqrt3}{2},\qquad
y=\frac1{\sqrt6},\qquad
z=-\frac1{\sqrt{10}}\sqrt{\frac56}=-\frac1{\sqrt{12}}=-\frac1{2\sqrt3},
$$

ce qui est bien $\overrightarrow{OP}$.

## Remarque : non-unicité

L'énoncé demande *une* équation vectorielle, il y en a plusieurs. Le cercle (donc le plan $OAP$) est unique, mais on peut échanger les rôles de $\mathbf a$ et $\mathbf b$, remplacer $\mathbf b$ par $-\mathbf b$, ou partir d'un autre couple de vecteurs unitaires orthogonaux du plan $OAP$. Toutes ces écritures décrivent le même cercle ; la forme ci-dessus a l'avantage de faire correspondre $\theta=0$ au point $A$.
