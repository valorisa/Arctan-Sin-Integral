# Une intégrale trigonométrique avec arctangente : méthode par symétrie

> Source : vidéo YouTube « The trig integral of your dreams (or nightmare) », chaîne @maths_505 — https://youtu.be/8Bd46Jq1qOY

## Version rendue et contenu du dépôt

- **Ce fichier (`README.md`)** : la démonstration complète, rendue directement par GitHub.
- **[Version HTML autonome](https://valorisa.github.io/Arctan-Sin-Integral/integrale-arctan-sin-statique.html)** (GitHub Pages) : même texte, avec les formules pré-rendues en SVG. Elle ne dépend d'aucun script ni d'aucune police, et l'aspect est identique sur tous les appareils.
- **`integrale-arctan-sin-statique.html`** : le fichier source de cette version. Téléchargé et ouvert dans un navigateur, il s'affiche correctement, même hors ligne.

## Résultat

```math
I=\int_0^{\pi/2}\frac{\arctan(\sin\theta)}{\sqrt{\sin\theta}}\,d\theta=\frac{\sqrt{2\pi}}{32}\,\Gamma\left(\frac14\right)^2\approx1{,}029679594.
```

## Plan de la démonstration

1. Première substitution : $u=\sin\theta$.
2. Pourquoi essayer $u=\dfrac{1-z}{1+z}$ ?
3. Transformer le dénominateur et le différentiel.
4. Changer les bornes.
5. Transformer l’arctangente.
6. Le moment décisif : retrouver $I$.
7. Mettre l’intégrale restante sous la forme bêta.
8. Écrire le résultat avec la fonction gamma.

---

Oui. Reprenons depuis le début, en expliquant chaque changement de variable et surtout l’idée qui fait fonctionner la méthode.

Nous voulons calculer :

```math
\boxed{I=\int_0^{\pi/2}\frac{\arctan(\sin\theta)}{\sqrt{\sin\theta}}\,d\theta.}
```

Ici, $\arctan$ désigne la fonction réciproque de la tangente, et non $1/\tan$.

L’idée centrale est une **symétrie** : transformer l’intégrale pour retrouver le même dénominateur, mais remplacer l’arctangente par « $\frac{\pi}{4}$ moins cette arctangente ». Nous pourrons alors éliminer l’arctangente.

## 1. Première substitution : $u=\sin\theta$

Posons :

```math
u=\sin\theta.
```

En dérivant :

```math
du=\cos\theta\,d\theta,
```

donc :

```math
d\theta=\frac{du}{\cos\theta}.
```

Pour exprimer aussi le cosinus avec $u$, utilisons :

```math
\cos^2\theta=1-\sin^2\theta=1-u^2.
```

Comme $\theta$ appartient à $[0,\pi/2]$, le cosinus est positif ou nul :

```math
\cos\theta=\sqrt{1-u^2}.
```

Ainsi, à l’intérieur de l’intervalle :

```math
d\theta=\frac{du}{\sqrt{1-u^2}}.
```

Les bornes deviennent :

```math
\theta=0\Rightarrow u=0,\qquad\theta=\frac{\pi}{2}\Rightarrow u=1.
```

En remplaçant chaque élément :

```math
I=\int_0^1\frac{\arctan u}{\sqrt u\,\sqrt{1-u^2}}\,du.
```

Autrement dit :

```math
\boxed{I=\int_0^1\frac{\arctan u}{\sqrt{u(1-u^2)}}\,du.}
```

Les expressions qui deviennent infinies aux bornes se traitent par passage à la limite ; les intégrales rencontrées ici convergent.

## 2. Pourquoi essayer $u=\dfrac{1-z}{1+z}$ ?

Regardons le dénominateur :

```math
u(1-u^2)=u(1-u)(1+u).
```

Il contient trois facteurs :

```math
u,\qquad 1-u,\qquad 1+u.
```

La substitution

```math
\boxed{u=\frac{1-z}{1+z}}
```

est intéressante parce qu’elle transforme ces trois facteurs en expressions qui se simplifient entre elles.

Elle est aussi adaptée à l’arctangente, car :

```math
\tan\left(\frac{\pi}{4}-\alpha\right)=\frac{1-\tan\alpha}{1+\tan\alpha}.
```

Nous allons voir ces deux avantages séparément.

## 3. Transformer le dénominateur et le différentiel

Avec :

```math
u=\frac{1-z}{1+z},
```

calculons d’abord $1-u$ :

```math
1-u=1-\frac{1-z}{1+z}=\frac{1+z-(1-z)}{1+z}=\frac{2z}{1+z}.
```

Puis $1+u$ :

```math
1+u=1+\frac{1-z}{1+z}=\frac{1+z+(1-z)}{1+z}=\frac{2}{1+z}.
```

Donc :

```math
u(1-u)(1+u)=\frac{1-z}{1+z}\cdot\frac{2z}{1+z}\cdot\frac{2}{1+z}=\frac{4z(1-z)}{(1+z)^3}.
```

En prenant la racine :

```math
\sqrt{u(1-u^2)}=\frac{2\sqrt{z(1-z)}}{(1+z)^{3/2}}.
```

Calculons maintenant $du$, avec la dérivée d’un quotient :

```math
\frac{du}{dz}=\frac{(-1)(1+z)-(1-z)(1)}{(1+z)^2}=-\frac{2}{(1+z)^2}.
```

Ainsi :

```math
du=-\frac{2}{(1+z)^2}\,dz.
```

En combinant le différentiel et le dénominateur :

```math
\frac{du}{\sqrt{u(1-u^2)}}=-\frac{2}{(1+z)^2}\frac{(1+z)^{3/2}}{2\sqrt{z(1-z)}}\,dz.
```

Les facteurs $2$ s’annulent, et :

```math
\frac{(1+z)^{3/2}}{(1+z)^2}=\frac1{\sqrt{1+z}}.
```

Il reste :

```math
\frac{du}{\sqrt{u(1-u^2)}}=-\frac{dz}{\sqrt z\,\sqrt{1-z}\,\sqrt{1+z}}.
```

Puisque $(1-z)(1+z)=1-z^2$ :

```math
\boxed{\frac{du}{\sqrt{u(1-u^2)}}=-\frac{dz}{\sqrt{z(1-z^2)}}.}
```

C’est le premier succès : nous retrouvons le même dénominateur, avec $z$ à la place de $u$.

## 4. Changer les bornes

La relation peut aussi s’écrire :

```math
z=\frac{1-u}{1+u}.
```

Donc :

```math
u=0\Rightarrow z=1,\qquad u=1\Rightarrow z=0.
```

L’intégrale devient :

```math
I=-\int_1^0\frac{\arctan\left(\frac{1-z}{1+z}\right)}{\sqrt{z(1-z^2)}}\,dz.
```

Inverser les bornes fait disparaître le signe moins :

```math
\boxed{I=\int_0^1\frac{\arctan\left(\frac{1-z}{1+z}\right)}{\sqrt{z(1-z^2)}}\,dz.}
```

## 5. Transformer l’arctangente

La formule de la tangente d’une différence donne :

```math
\tan(A-B)=\frac{\tan A-\tan B}{1+\tan A\tan B}.
```

Prenons :

```math
A=\frac{\pi}{4},\qquad B=\arctan z.
```

Comme :

```math
\tan\frac{\pi}{4}=1,\qquad\tan(\arctan z)=z,
```

nous obtenons :

```math
\tan\left(\frac{\pi}{4}-\arctan z\right)=\frac{1-z}{1+z}.
```

Pour $z\in[0,1]$, l’angle $\frac{\pi}{4}-\arctan z$ est compris entre $0$ et $\frac{\pi}{4}$. Nous pouvons donc appliquer l’arctangente et écrire :

```math
\boxed{\arctan\left(\frac{1-z}{1+z}\right)=\frac{\pi}{4}-\arctan z.}
```

Ainsi :

```math
I=\int_0^1\frac{\frac{\pi}{4}-\arctan z}{\sqrt{z(1-z^2)}}\,dz.
```

## 6. Le moment décisif : retrouver $I$

Séparons les deux termes du numérateur :

```math
I=\frac{\pi}{4}\int_0^1\frac{dz}{\sqrt{z(1-z^2)}}-\int_0^1\frac{\arctan z}{\sqrt{z(1-z^2)}}\,dz.
```

La dernière intégrale est exactement $I$ !

En effet :

```math
I=\int_0^1\frac{\arctan u}{\sqrt{u(1-u^2)}}\,du,
```

et remplacer le nom de la variable $u$ par $z$ ne change rien à sa valeur.

Nous avons donc :

```math
I=\frac{\pi}{4}\int_0^1\frac{dz}{\sqrt{z(1-z^2)}}-I.
```

Ajoutons $I$ aux deux membres :

```math
2I=\frac{\pi}{4}\int_0^1\frac{dz}{\sqrt{z(1-z^2)}}.
```

Puis divisons par $2$ :

```math
\boxed{I=\frac{\pi}{8}\int_0^1\frac{dz}{\sqrt{z(1-z^2)}}.}
```

C’est le cœur de la méthode : nous avons fait disparaître l’arctangente.

## 7. Mettre l’intégrale restante sous la forme bêta

Il reste à calculer :

```math
J=\int_0^1\frac{dz}{\sqrt{z(1-z^2)}}.
```

Pour remplacer $1-z^2$ par $1-t$, posons :

```math
t=z^2.
```

Donc :

```math
z=\sqrt t,\qquad dz=\frac{dt}{2\sqrt t}.
```

Au dénominateur :

```math
\sqrt{z(1-z^2)}=\sqrt{\sqrt t(1-t)}=t^{1/4}(1-t)^{1/2}.
```

Les bornes restent $0$ et $1$. Nous obtenons :

```math
J=\int_0^1\frac{1}{t^{1/4}(1-t)^{1/2}}\frac{dt}{2t^{1/2}}.
```

En regroupant les puissances de $t$ :

```math
J=\frac12\int_0^1t^{-3/4}(1-t)^{-1/2}\,dt.
```

C’est ici que la fonction bêta intervient. Par définition :

```math
B(a,b)=\int_0^1t^{a-1}(1-t)^{b-1}\,dt.
```

Pour identifier les paramètres, nous comparons les exposants :

| Facteur de notre intégrale | Exposant dans la définition | Paramètre |
|---|---|---|
| $t^{-3/4}$ | $a-1=-3/4$ | $a=1/4$ |
| $(1-t)^{-1/2}$ | $b-1=-1/2$ | $b=1/2$ |

Par conséquent :

```math
J=\frac12B\left(\frac14,\frac12\right).
```

Comme $I=\frac{\pi}{8}J$ :

```math
\boxed{I=\frac{\pi}{16}B\left(\frac14,\frac12\right).}
```

C’est déjà une valeur exacte de l’intégrale.

## 8. Écrire le résultat avec la fonction gamma

La relation entre bêta et gamma est :

```math
B(a,b)=\frac{\Gamma(a)\Gamma(b)}{\Gamma(a+b)}.
```

Elle donne ici :

```math
B\left(\frac14,\frac12\right)=\frac{\Gamma\left(\frac14\right)\Gamma\left(\frac12\right)}{\Gamma\left(\frac34\right)}.
```

En utilisant $\Gamma(\frac12)=\sqrt\pi$ :

```math
\boxed{I=\frac{\pi\sqrt\pi}{16}\frac{\Gamma\left(\frac14\right)}{\Gamma\left(\frac34\right)}.}
```

Pour obtenir exactement la forme finale donnée dans la vidéo source, on utilise la formule de réflexion :

```math
\Gamma(x)\Gamma(1-x)=\frac{\pi}{\sin(\pi x)}.
```

Avec $x=\frac14$ :

```math
\Gamma\left(\frac14\right)\Gamma\left(\frac34\right)=\frac{\pi}{\sin(\pi/4)}=\pi\sqrt2.
```

Donc :

```math
\frac1{\Gamma\left(\frac34\right)}=\frac{\Gamma\left(\frac14\right)}{\pi\sqrt2}.
```

En remplaçant :

```math
I=\frac{\pi\sqrt\pi}{16}\frac{\Gamma\left(\frac14\right)^2}{\pi\sqrt2}=\frac{\sqrt\pi}{16\sqrt2}\Gamma\left(\frac14\right)^2.
```

Enfin, en multipliant le numérateur et le dénominateur du coefficient par $\sqrt2$ :

```math
\boxed{\displaystyle I=\frac{\sqrt{2\pi}}{32}\,\Gamma\left(\frac14\right)^2\approx1{,}029679594.}
```

La partie inventive est le changement de variable $u=(1-z)/(1+z)$. Bêta et gamma servent ensuite à exprimer proprement la valeur de l’intégrale restante.
