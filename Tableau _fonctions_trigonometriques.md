Produis un fichier readme.md à partir de ces différents tableaux (en un unique code bloc).

```markdown
# Trigonométrie : fonctions, réciproques et identités

Ce document récapitule les fonctions trigonométriques circulaires, leurs inverses multiplicatifs, leurs fonctions réciproques, ainsi que les identités fondamentales et les fonctions hyperboliques associées.

> **Attention à la notation :** \(\sin^{-1}x\) désigne généralement \(\arcsin x\), la fonction réciproque du sinus. Ce n’est **pas** \(1/\sin x\), qui s’écrit \(\csc x\).

## Fonctions trigonométriques circulaires

| Fonction | Notation | Définition en \(\sin,\cos\) | Inverse multiplicatif | Domaine usuel |
|---|---|---|---|---|
| Sinus | \(\sin\theta\) | \(y\) sur le cercle unité | \(\csc\theta=\frac{1}{\sin\theta}\) | \(\mathbb{R}\) |
| Cosinus | \(\cos\theta\) | \(x\) sur le cercle unité | \(\sec\theta=\frac{1}{\cos\theta}\) | \(\mathbb{R}\) |
| Tangente | \(\tan\theta\) | \(\frac{\sin\theta}{\cos\theta}\) | \(\cot\theta=\frac{1}{\tan\theta}\) | \(\cos\theta\neq0\) |
| Cotangente | \(\cot\theta\) | \(\frac{\cos\theta}{\sin\theta}\) | \(\tan\theta=\frac{1}{\cot\theta}\) | \(\sin\theta\neq0\) |
| Sécante | \(\sec\theta\) | \(\frac{1}{\cos\theta}\) | \(\cos\theta=\frac{1}{\sec\theta}\) | \(\cos\theta\neq0\) |
| Cosécante | \(\csc\theta\) | \(\frac{1}{\sin\theta}\) | \(\sin\theta=\frac{1}{\csc\theta}\) | \(\sin\theta\neq0\) |

## Fonctions réciproques

Les fonctions réciproques renvoient un **angle**, contrairement à \(\sec\), \(\csc\) et \(\cot\), qui sont des inverses multiplicatifs.

| Fonction réciproque | Notations | Définition | Domaine | Image principale |
|---|---|---|---|---|
| Arc sinus | \(\arcsin x\), \(\sin^{-1}x\) | \(y=\arcsin x \iff x=\sin y\) | \([-1,1]\) | \(\left[-\frac{\pi}{2},\frac{\pi}{2}\right]\) |
| Arc cosinus | \(\arccos x\), \(\cos^{-1}x\) | \(y=\arccos x \iff x=\cos y\) | \([-1,1]\) | \([0,\pi]\) |
| Arc tangente | \(\arctan x\), \(\tan^{-1}x\) | \(y=\arctan x \iff x=\tan y\) | \(\mathbb{R}\) | \(\left(-\frac{\pi}{2},\frac{\pi}{2}\right)\) |
| Arc cotangente | \(\operatorname{arccot}x\), \(\cot^{-1}x\) | \(y=\operatorname{arccot}x \iff x=\cot y\) | \(\mathbb{R}\) | Dépend de la convention, souvent \((0,\pi)\) |
| Arc sécante | \(\operatorname{arcsec}x\), \(\sec^{-1}x\) | \(y=\operatorname{arcsec}x \iff x=\sec y\) | \((-\infty,-1]\cup[1,\infty)\) | Dépend de la convention |
| Arc cosécante | \(\operatorname{arccsc}x\), \(\csc^{-1}x\) | \(y=\operatorname{arccsc}x \iff x=\csc y\) | \((-\infty,-1]\cup[1,\infty)\) | Dépend de la convention |

## Identités fondamentales

| Famille | Identités |
|---|---|
| Pythagore | \(\sin^2\theta+\cos^2\theta=1\) |
| Pythagore | \(1+\tan^2\theta=\sec^2\theta\) |
| Pythagore | \(1+\cot^2\theta=\csc^2\theta\) |
| Quotients | \(\tan\theta=\frac{\sin\theta}{\cos\theta}\), \(\cot\theta=\frac{\cos\theta}{\sin\theta}\) |
| Réciproques | \(\csc\theta=\frac{1}{\sin\theta}\), \(\sec\theta=\frac{1}{\cos\theta}\), \(\cot\theta=\frac{1}{\tan\theta}\) |
| Parité | \(\sin(-\theta)=-\sin\theta\), \(\cos(-\theta)=\cos\theta\), \(\tan(-\theta)=-\tan\theta\) |
| Périodicité | \(\sin(\theta+2\pi)=\sin\theta\), \(\cos(\theta+2\pi)=\cos\theta\), \(\tan(\theta+\pi)=\tan\theta\) |
| Addition | \(\sin(a\pm b)=\sin a\cos b\pm\cos a\sin b\) |
| Addition | \(\cos(a\pm b)=\cos a\cos b\mp\sin a\sin b\) |
| Addition | \(\tan(a\pm b)=\frac{\tan a\pm\tan b}{1\mp\tan a\tan b}\) |
| Double angle | \(\sin(2\theta)=2\sin\theta\cos\theta\), \(\cos(2\theta)=\cos^2\theta-\sin^2\theta\) |

## Exemple : relation entre \(\sec^2\) et \(\frac{1}{\cos^2}\)

Par définition :

\[
\sec\theta=\frac{1}{\cos\theta}
\]

Donc :

\[
\sec^2\theta=\left(\frac{1}{\cos\theta}\right)^2=\frac{1}{\cos^2\theta}
\]

Cette égalité est valable uniquement si \(\cos\theta\neq0\).

## Fonctions hyperboliques

Les fonctions hyperboliques sont les analogues des fonctions trigonométriques circulaires, mais définies à partir de l’exponentielle.

| Fonction | Notation | Définition | Inverse multiplicatif |
|---|---|---|---|
| Sinus hyperbolique | \(\sinh x\) | \(\frac{e^x-e^{-x}}{2}\) | \(\operatorname{csch}x=\frac{1}{\sinh x}\) |
| Cosinus hyperbolique | \(\cosh x\) | \(\frac{e^x+e^{-x}}{2}\) | \(\operatorname{sech}x=\frac{1}{\cosh x}\) |
| Tangente hyperbolique | \(\tanh x\) | \(\frac{\sinh x}{\cosh x}\) | \(\coth x=\frac{1}{\tanh x}\) |
| Cotangente hyperbolique | \(\coth x\) | \(\frac{\cosh x}{\sinh x}\) | \(\tanh x=\frac{1}{\coth x}\) |
| Sécante hyperbolique | \(\operatorname{sech}x\) | \(\frac{1}{\cosh x}\) | \(\cosh x=\frac{1}{\operatorname{sech}x}\) |
| Cosécante hyperbolique | \(\operatorname{csch}x\) | \(\frac{1}{\sinh x}\) | \(\sinh x=\frac{1}{\operatorname{csch}x}\) |

## Fonctions réciproques hyperboliques

| Fonction | Notations usuelles | Définition |
|---|---|---|
| Argument sinus hyperbolique | \(\operatorname{arsinh}x\), \(\operatorname{asinh}x\), \(\sinh^{-1}x\) | \(y=\operatorname{arsinh}x \iff x=\sinh y\) |
| Argument cosinus hyperbolique | \(\operatorname{arcosh}x\), \(\operatorname{acosh}x\), \(\cosh^{-1}x\) | \(y=\operatorname{arcosh}x \iff x=\cosh y\), avec \(x\ge1\) |
| Argument tangente hyperbolique | \(\operatorname{artanh}x\), \(\operatorname{atanh}x\), \(\tanh^{-1}x\) | \(y=\operatorname{artanh}x \iff x=\tanh y\), avec \(-1<x<1\) |
| Argument cotangente hyperbolique | \(\operatorname{arcoth}x\), \(\operatorname{acoth}x\), \(\coth^{-1}x\) | \(y=\operatorname{arcoth}x \iff x=\coth y\), avec \(\lvert x\rvert>1\) |
| Argument sécante hyperbolique | \(\operatorname{arsech}x\), \(\operatorname{asech}x\), \(\operatorname{sech}^{-1}x\) | \(y=\operatorname{arsech}x \iff x=\operatorname{sech}y\), avec \(0<x\le1\) |
| Argument cosécante hyperbolique | \(\operatorname{arcsch}x\), \(\operatorname{acsch}x\), \(\operatorname{csch}^{-1}x\) | \(y=\operatorname{arcsch}x \iff x=\operatorname{csch}y\), avec \(x\neq0\) |

## Pièges fréquents

- \(\sec\theta\) est l’inverse multiplicatif du cosinus : \(\sec\theta=\frac{1}{\cos\theta}\).
- \(\csc\theta\) est l’inverse multiplicatif du sinus : \(\csc\theta=\frac{1}{\sin\theta}\).
- \(\cot\theta\) est l’inverse multiplicatif de la tangente : \(\cot\theta=\frac{1}{\tan\theta}\).
- \(\arccos x\) est la réciproque du cosinus restreint à \([0,\pi]\) : elle renvoie un angle.
- \(\cos^{-1}x\) signifie habituellement \(\arccos x\), et non \(\frac{1}{\cos x}\).
- Les identités ne sont valables que lorsque les dénominateurs concernés sont non nuls.
```

