---
layout: note 
date: "2026-06-30" 
title: "Auto-generating \\mathcal, \\mathsf, and \\mathbb commands in the LaTeX preamble"
status: published
category: latex
---

When writing in LaTeX, I have gotten into the habit of using `\Acal` as short for `\mathcal{A}`, `\Bcal` as short for `\mathcal{B}`, etc., and similarly for `\mathsf{}`. 

It can be tedious to write out `\newcommand{\Xcal}{\mathcal{X}}` for each letter and then copy this from project to project. Instead, one can place the following in their preamble:


```LaTeX

%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%%% All the \mathcals %%%%
%%%%%%%%%%%%%%%%%%%%%%%%%%%
\def\ddefloop#1{
  \ifx
    \ddefloop#1
  \else\ddef{#1}
    \expandafter
    \ddefloop
  \fi}
\def\ddef#1{\expandafter\def\csname #1cal\endcsname{\ensuremath{\mathcal{#1}}}}

\ddefloop
ABCDEFGHIJKLMNOPQRSTUVWXYZ
\ddefloop
```
To obtain the same for `\mathsf{X}`, one need only replace `#1cal` with `#1sf` and `\mathcal{#1}` with `\mathsf{#1}`. Similarly, I tend to use `\RR` in place of `\mathbb{R}`, `\NN` in place of `\mathbb{N}`, and so on. The analogous command would look something like the following.


```LaTeX

%%%%%%%%%%%%%%%%%%%%%%%%%%
%%%% All the \mathbbs %%%%
%%%%%%%%%%%%%%%%%%%%%%%%%%
\def\ddefloop#1{
  \ifx
    \ddefloop#1
  \else\ddef{#1}
    \expandafter
    \ddefloop
  \fi}
\def\ddef#1{\expandafter\def\csname #1#1\endcsname{\ensuremath{\mathbb{#1}}}}

\ddefloop
ABCDEFGHIJKLMNOPQRSTUVWXYZ
\ddefloop
```
