---
layout: note 
date: "2024-03-18" 
title: "Toggling verbosity in LaTeX derivations (old)"
status: archived
category: academic
---

<center><em>(An updated version of this post can be found <a href="/blogposts/toggling-verbosity-latex">here</a>. This one is only kept for posterity.)</em></center>

$$
\newcommand{\Fcal}{\mathcal{F}}
\newcommand{\RR}{\mathbb{R}}
\newcommand{\EE}{\mathbb{E}}
$$

I find it helpful to write proofs so that they can optionally be made more verbose (e.g. to fill in certain details in a derivation). There's a very simple trick you can use to accomplish this and it's already built in to LaTeX --- no additional packages needed. This idea was taken from [this reddit comment](https://old.reddit.com/r/LaTeX/comments/p321rh/is_there_a_way_to_have_two_versions_of_a_document/h8ojktk/).

Put the following in your preamble:

```LaTeX
% Verbose LaTeX doc.
\newif\ifverbose % Define a new Boolean value "verbose".
% Initially it is false.
\verbosefalse % set verbose to true/false here.
```

Any content you would like to restrict to the "verbose" version of your paper should then be wrapped in `\ifverbose <content> \if`.

# Demo

For the sake of example, consider the following short proof of the <a href="https://proofwiki.org/wiki/Second_Borel-Cantelli_Lemma" target="_blank">second Borel-Cantelli lemma</a> (the proof details do not matter for the purposes of this post).

<div class='theorem'>

<b>Claim:</b> If \((E_k)_{k=1}^\infty\) are independent events and \(\sum_{k=1}^\infty \Pr(E_k) = \infty\), then

\[ \Pr \left ( \limsup_{n \to \infty} E_n \right ) = 1. \]
  

<em>Proof.</em>
Writing out the probability of \(\limsup_{n} E_n\), we have

$$\begin{align}
  &\quad \Pr \left ( \limsup_{n \to \infty} E_n \right )\\
  &\equiv \Pr \left ( \bigcap_{m=1}^\infty \bigcup_{k = m}^\infty E_k \right ) \\
                                                 &{\color{lightgray}{= \lim_{m \to \infty}\Pr \left ( \bigcup_{k = m}^\infty E_k \right )}} \\
                                                 & \color{lightgray}{=1- \lim_{m \to \infty}\Pr \left ( \bigcap_{k = m}^\infty E_k^c \right ) }\\
                                                 & =1- \lim_{m \to \infty} \lim_{K \to \infty}  \Pr \left ( \bigcap_{k = m}^K E_k^c \right ) \\
                                                 &= 1- \lim_{m \to \infty} \lim_{K \to \infty} \prod_{k=m}^K \left [1-\Pr \left ( E_k \right ) \right ]\\
                                                 &\geq 1- \lim_{m \to \infty} \lim_{K \to \infty} \exp \left \{ -\sum_{k=m}^K \Pr(E_k) \right \}\\
                                                 & \color{lightgray}{= 1- \lim_{m \to \infty} \exp \left \{ -\sum_{k=m}^\infty \Pr(E_k) \right \}}\\
                                                 & \color{lightgray}{= 1- \lim_{m \to \infty} 0}\\
                                                 &= 1,
\end{align}$$

which completes the proof. \(\square\)
</div>
<br/>

If the above derivations are written with the following TeX, then toggling between `\verbosefalse` and `verbosetrue` in your preamble will remove/include the lines in gray above, respectively.


```LaTeX
\begin{align}
  \Pr \left ( \limsup_{n \to \infty} E_n \right )
  &\equiv \Pr \left ( \bigcap_{m=1}^\infty \bigcup_{k = m}^\infty E_k \right ) \\
  \ifverbose %BEGIN VERBOSE
  &= \lim_{m \to \infty}\Pr \left ( \bigcup_{k = m}^\infty E_k \right ) \\
  & =1- \lim_{m \to \infty}\Pr \left ( \bigcap_{k = m}^\infty E_k^c \right ) \\
  \fi %END VERBOSE
  & =1- \lim_{m \to \infty} \lim_{K \to \infty}  \Pr \left ( \bigcap_{k = m}^K E_k^c \right ) \\
  &= 1- \lim_{m \to \infty} \lim_{K \to \infty} \prod_{k=m}^K \left [1-\Pr \left ( E_k \right ) \right ]\\
  &\geq 1- \lim_{m \to \infty} \lim_{K \to \infty} \exp \left \{ -\sum_{k=m}^K \Pr(E_k) \right \}\\
  \ifverbose %BEGIN VERBOSE
  &= 1- \lim_{m \to \infty} \exp \left \{ -\sum_{k=m}^\infty \Pr(E_k) \right \}\\
  &= 1- \lim_{m \to \infty} 0\\
  \fi %END VERBOSE
  &= 1,
\end{align}
```

That's all there is to it.

---

*Bonus: if you use [yasnippet](https://github.com/joaotavora/yasnippet) in emacs or similar tools in neovim etc., it is very handy to have a snippet that creates the following.*
```LaTeX
\ifverbose %BEGIN VERBOSE
  %<content goes here>
\fi %END VERBOSE
```

